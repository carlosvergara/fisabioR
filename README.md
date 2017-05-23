
`fisabior`
==========

Acerca de este proyecto
-----------------------

`fisabior` es un paquete de R cuyo único propósito es estructurar y organizar el entorno de trabajo, facilitando el trabajo en equipo.

El proyecto generado con su función principal (`init_proj()`) se estructura en 3 directorios, lo que permite seguir un criterio unificado a la hora de trabajar en equipo o, sencillamente, retomar un trabajo individual que se aparcase hace algún tiempo. El contenido de cada uno de estos directorios es:

-   configuracion: en este directorio se almacena todo archivo de configuración común al equipo de trabajo. Un ejemplo lo tienes en el archivo `configuracion/config.R`, el cual se ejecuta al inicio de cada sesión de RStudio para cargar tanto funciones comunes como paquetes de uso continuado.
-   datos: donde se almacenan los bancos de datos necesarios para el análisis. Se estructura en tres subdirectorios:
    -   brutos: datos TAL CUAL se reciben, sin importar su formato.
    -   procesados: datos procesados listos para cargar durante el análisis. Preferentemente se utilizará un formato de valores separados por comas, empleando el punto como separador decimal y dándole la extensión apropiada al archivo (`*.csv`), aunque también es posible emplear el formato nativo de R (`*.RData`) o una base de datos SQL.
    -   cartografia: directorio para guardar archivos de cartografía asociados al proyecto. Preferentemente se utilizará el formato Shapefile (.shp) y, en caso de emplear una proyección de los datos, se aconseja emplear la EPSG 4326 (datum WGS84).
-   r: directorio principal, el cual contiene todos los scripts de código R necesarios para la ejecución del proyecto. Solo contiene archivos con extensión `*.R`.

A su vez, la función `init_proj()` permite crear directorios extra para el seguimiento de un artículo y para almacenar código foráneo:

-   articulo: aquí se alberga todo el contenido relacionado con la publicación del proyecto, estructurándose, a su vez, en tres subdirectorios.
    -   enviado: documentos tal cual se enviaron para su publicación,
    -   revision: documentos que han sido revisados por pares y requieren modificaciones,
    -   proof: versión de imprenta de las publicaciones aceptadas.
-   src: directorio de código secundario, donde se guardan los archivos con código no-R, eligiendo para ello el subdirectorio más apropiado:
    -   bugs: modelos escritos con código en lenguaje BUGS,
    -   cpp: código en C++,
    -   jags: modelos escritos con código en lenguaje JAGS (aunque es similar a BUGS, tiene sus peculiaridades),
    -   stan: modelos escritos con código en lenguaje Stan.

Gracias al conjunto de funciones `informe_*()` y `presentacion_*()`, se pueden generar informes y presentaciones en varios formatos, todos ellos dentro del directorio `informes`, el cual a su vez contiene un directorio por formato, albergando también las imágenes y datos de caché:
-   informes:
    -   docx: documentos MS Office Word producidos por rmarkdown-knitr,
    -   odt: documentos LibreOffice Writer producidos rmarkdown-knitr,
    -   pdf: documentos PDF producidos por rmarkdown-knitr-LaTeX,
    -   latex: documentos TeX y PDF producidos por knitr-LaTeX,
    -   beamer: presentaciones TeX y PDF producidos por rmarkdown-knitr-LaTeX,
    -   html: documentos HTML producidos por rmarkdown-knitr.
        -   cache: conjuntos de datos `*.Rdata` generados durante el análisis, los cuales se guardan de manera temporal como copia de respaldo que evita tener que ejecutar una y otra vez todos los datos. También alberga aquellos datos procedentes de informes elaborados con `knitr` para los que se establezca como opción `cache = TRUE` los cuales, dependiendo del programa empleado para generarlos, se almacenaran en subdirectorios creados junto con el informe.
        -   figuras: gráficos en diversos formatos generados tanto en el análisis como en la redacción de informes.

Instalación
-----------

Puedes instalar este paquete empleando la función `install_github()` del paquete `devtools`, para lo cual debes ejecutar el siguiente código:

```
install.packages("devtools")
devtools::install_github("fisabio/fisabior")
```


Acerca de `fisabior`
--------------------

`fisabior` es el nombre que nos hemos dado como grupo de usuarios de R dentro de la Fundación para el Fomento de la Investigación Sanitaria y Biomédica de la Comunidad Valenciana (FISABIO). A febrero de 2017, el grupo está compuesto por:

-   Miguel Ángel Martínez-Beneito (<martinez_mig@gva.es>),
-   Gonzalo García-Donato (<garcia_gon@gva.es>),
-   Paloma Botella-Rocamora (<botella_pal@gva.es>),
-   Jordi Pérez-Panadés (<perez_jorpan@gva.es>),
-   Francisca Corpas-Burgos (<corpas_fra@gva.es>),
-   Hèctor Perpiñán-Fabuel (<perpinan_hec@gva.es>),
-   Carlos Vergara-Hernández (<carlos.vergara@uv.es>).

Si al igual que nosotros te encanta la estadística en R, o si tuvieras alguna duda acerca del grupo o su actividad, puedes contactarnos sin problema.
