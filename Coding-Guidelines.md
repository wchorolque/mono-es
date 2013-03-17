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
    
<a name="git"/>
##Cambios en el flujo de trabajo en Git

<a name="codigo_fuente"/>
##Control de código fuente

<a name="buenas_practicas"/>
##Buenas prácticas




