
fisabioR
========

Acerca de este proyecto
-----------------------

fisabioR es un paquete de R cuyo único propósito es estructurar y organizar el entorno de trabajo, facilitando el trabajo en equipo.

El proyecto generado con su única función `init_proj()` se estructura en 8 directorios lo que permite seguir un criterio unificado a la hora de trabajar en equipo o, sencillamente, retomar un trabajo individual que se aparcase hace algún tiempo. El contenido de cada uno de estos directorios es:

-   articulo: aquí se alberga todo el contenido relacionado con la publicación del proyecto, estructurándose, a su vez, en tres subdirectorios.
    -   enviado: documentos tal cual se enviaron para su publicación,
    -   revision: documentos que han sido revisados por pares y requieren modificaciones,
    -   proof: versión de imprenta de las publicaciones aceptadas.
-   cache: conjuntos de datos `*.Rdata` generados durante el análisis, los cuales se guardan de manera temporal como copia de respaldo que evita tener que ejecutar una y otra vez todos los datos. También alberga aquellos datos procedentes de informes elaborados con `knitr` para los que se establezca como opción `cache = TRUE`.
-   configuracion: en este directorio se almacena todo archivo de configuración común al equipo de trabajo. Un ejemplo lo tienes en el archivo `configuracion/config.R`, el cual se ejecuta al inicio de cada sesión de RStudio para cargar tanto funciones comunes como paquetes de uso continuado.
-   datos: donde se almacenan los bancos de datos necesarios para el análisis. Se estructura en dos subdirectorios:
    -   brutos: datos TAL CUAL se reciben, sin importar su formato.
    -   procesados: datos procesados listos para cargar durante el análisis. Preferentemente se utilizará un formato de valores separados por comas, empleando el punto como separador decimal y dándole la extensión apropiada al archivo (`*.csv`), aunque también es posible emplear el formato nativo de R (`*.RData`) o una base de datos SQL.
-   figuras: gráficos en diversos formatos generados tanto en el análisis como en la redacción de informes.
-   informes:
    -   docx: documentos MS Office Word producidos por rmarkdown-knitr,
    -   odt: documentos LibreOffice Writer producidos rmarkdown-knitr,
    -   markdown: documentos markdown y html producidos por rmarkdown-knitr,
    -   latex: documentos TeX y PDF producidos por knitr-LaTeX.
-   r: directorio principal, el cual contiene todos los scripts de código R necesarios para la ejecución del proyecto. Solo contiene archivos con extensión `*.R`.
-   src: directorio de código secundario, donde se guardan los archivos con código no-R, eligiendo para ello el subdirectorio más apropiado:
    -   bugs: modelos escritos con código en lenguaje BUGS,
    -   cpp: código en C++,
    -   jags: modelos escritos con código en lenguaje JAGS (aunque es similar a BUGS, tiene sus peculiaridades),
    -   stan: modelos escritos con código en lenguaje Stan.

Acerca de fisabioR
------------------

fisabioR es el nombre que nos hemos dado como grupo de usuarios de R dentro de la Fundación para el Fomento de la Investigación Sanitaria y Biomédica de la Comunidad Valenciana (FISABIO). A enero de 2017, el grupo está compuesto por:

-   Miguel Ángel Martínez-Beneito (<martinez_mig@gva.es>),
-   Gonzalo García-Donato (<garcia_gon@gva.es>),
-   Paloma Botella-Rocamora (<botella_pal@gva.es>),
-   Jordi Pérez-Panadés (<perez_jorpan@gva.es>),
-   David Martín-Baena (<martin_dav@gva.es>),
-   Francisca Corpas-Burgos (<corpas_fra@gva.es>),
-   Héctor Perpiñán-Fabuel (<perpinan_hec@gva.es>),
-   Carlos Vergara-Hernández (<carlos.vergara@uv.es>).

Si, al igual que nosotros, te encanta la estadística en R, o si tuvieras alguna duda en el futuro acerca del grupo o su actividad, puedes contactarnos sin problema.
