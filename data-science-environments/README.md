La forma de trabajar en ciencia de datos inicialmente era estática mediante la programación con archivos de texto plano (scripts) hasta que se definieron los notebooks.
Basados en el conceptop REPL (Read -> Evaluate -> Print -> Loop), generaron los jupyter notebooks.
Estos permiten generar documentos de texto enriquecido mediante Markdown, incluyendo imágenes, gif's, ecuaciones y código de programación ejecutable. (Python, R, Julia o Matlab)
De tal forma que ahora es más sencillo prototipar análisis de datos.

¿Donde se puede trabajar con jupyter notebooks?
Existen herramientas en la nube como Google Colb y Deepnote que incorporan un entorno completo para ciencia de datos.
También se puede trabajar de manera local mediante Visual Studio Code, instalando extensiones como Python, MagicPython, Material Icon Theme y Jupyter.

¿Cómo instalar Anaconda?
Ingresar a la página oficial, copiar el link de descarga y desde la línea de comandos, escribir lo siguiente:
> wget -O <file name>.sh <link>

Para instalar Anaconda, escribir los siguiente desde la línea de comandos:
> sh <file name>.sh
Responder "yes" a todas las opciones.

Para levantar servidor de notebooks con Anaconda, escribir lo siguiente en la línea de comandos:
> conda jupyter-notebook
Esto abrirá una página en el navegador que permite trabajar con notebooks.

Al instalar Anaconda, automáticamente crea un ambiente llamado "base".
Para crear un nuevo ambiente, escribir los siguiente en la línea de comandos:
> conda create --name <env name>

Para cambiar al nuevo ambiente, escribir los siguiente:
> conda 
