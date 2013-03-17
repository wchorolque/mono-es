#Guías de Codificación

El nuevo código escrito para XWT debe seguir las
[guías de codificación genericas de Mono](http://www.mono-project.com/Coding_Guidelines),
con las siguientes excepciones:

* Usar CamelCase para nombres de campos.
* El código debe ser sangrado usando el tabulador, no usar espacios, el tabulador debe tener una longitud de 4 espacios.
* La llave de apertura { de una clase o espacio de nombres debe ser colocada en una nueva linea de igual forma en los
métodos.

Este documento contiene las guias de codificación para el Proyecto Mono. Esta guía contiene cuatro secciones importantes:

* [Estilo de codificación](#estilo), sobre cómo organizar tu código fuente.
* [Cambios en el flujo de trabajo en Git](#git) Discute como cambió nuestro flujo de trabajo a cambiado ahora que Mono
esta organizado en GitHub
* [Control de código fuente](#codigo_fuente) detalles acerca del uso del control de código fuente
* [Buenas prácticas](#buenas_practicas) usados en el proyecto

<a name="estilo"/>
##Estilo de codificación

Para mantener el código fuente consistente, por favor use las siguientes convenciones. De aquí en adelante `bueno` y
`malo` son atributos usados para indicar si el código coincide o no con el estilo de codificación. Esto no es una
llamada de atención a tus habilidades de escribir código si no una llamada de atención al estilo y apariencia. Por favor
trata de seguir las guías de codificación para asegurar la estetica.

Puede que también desees leer la documentación de
[.Net Framework Design Guidelines](http://msdn.microsoft.com/en-us/library/ms229042.aspx), sin embargo las guías de
codificación de Mono que se describen a continuación tienen preferencia si existe algún conflictos.

###Indentación

Usa una tabulacion equivalente a 8 espacios para escribir tu código (afortunadamente podemos mantener esto consistente).
Si estas modificando el código fuente de alguien mas trata de mantener el estilo de codificación parecido.

    for (i = 0; i < 10; i++) {
            if (something (i) ) {
                    do_more ();
            }
    }

Esto toma espacio valioso, mejor escribelo como esto:

    for (i = 0; i < 10; i++) {
            if (!something (i))
                    continue;
            do_more();
    }

Las sentencias `switch` tienen el `case` a la misma altura `switch`:

    switch (x) {
    case 'a':
            ...
    case 'b':
            ...
    }

###Rendimiento y Legibilidad

Es más importante ser correcto que ser veloz.

Es más importante ser mantenible que ser veloz.

Código rápido que sea complicado de mantener probablemente sea despreciado.

###Donde colocar los espacios

Use un espacio antes de abrir un parentesis cuando llame a funciones o haga uso de indices, como este:

    method (a);
    b [10];

No coloque un espacio después del paréntesis de apertura ni antes del parentesis de cierre, es decir:

_bueno_

    method (a);
    array [10];

_malo_

    method ( a );
    array[ 10 ];

No coloque un espacio entre los tipos genéricos, es decir:

_bueno_

    var list = new List<int> ();

_malo_

    var list = new List <int> ();

###Donde colocar las llaves

Dentro un bloque de código, coloque las llaves de apertura en la misma línea de la sentencia:

_bueno_

    if (a) {
            code();
            code();
    }

_malo_

    if (a)
    {
            code ();
            code ();
    }

Evite el uso innecesario de llaves de apertura y cierre, el espacio vertical se limita generalmente:

_bueno_

    if (a)
            code();

_malo_

    if (a) {
            code ();
    }


<a name="git"/>
##Cambios en el flujo de trabajo en Git

<a name="codigo_fuente"/>
##Control de código fuente

<a name="buenas_practicas"/>
##Buenas prácticas




