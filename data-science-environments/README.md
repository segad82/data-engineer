La forma de trabajar en ciencia de datos inicialmente era estática mediante la programación con archivos de texto plano (scripts) hasta que se definieron los notebooks.
Basados en el conceptop REPL (Read -> Evaluate -> Print -> Loop), generaron los jupyter notebooks.
Estos permiten generar documentos de texto enriquecido mediante Markdown, incluyendo imágenes, gif's, ecuaciones y código de programación ejecutable. (Python, R, Julia o Matlab)
De tal forma que ahora es más sencillo prototipar análisis de datos.

¿Donde se puede trabajar con jupyter notebooks?
Existen herramientas en la nube como Google Colb y Deepnote que incorporan un entorno completo para ciencia de datos.
También se puede trabajar de manera local mediante Visual Studio Code, instalando extensiones como Python, MagicPython, Material Icon Theme y Jupyter.

Normalmente se suele trabajar en más de un proyecto durante periodos de tiempo, por lo tanto, manejar las dependencias se vuelve un problema.
Es por esto que existen los ambientes virtuales y Conda es una herramienta que nos permite administrarlos independientemente del lenguaje de programación con el que estés trabajando.
Conda es una heramienta multiplataforma y para poder usarla, es necesario instalar Miniconda o Anaconda.
Miniconda es la versión mínima para que funcione Conda y dentro de sus dependencia, se encuentra Python.
Anaconda es una colección de paquetes incluyendo Miniconda, diseñado para el trabajo diario en ciendia de datos.

¿Cómo instalar Anaconda?
Ingresar a la página oficial, copiar el link de descarga y desde la línea de comandos, escribir lo siguiente:
> wget -O <file name>.sh <link>

Para instalar Anaconda, escribir los siguiente desde la línea de comandos:
> sh <file name>.sh
Responder "yes" a todas las opciones.

Para levantar servidor de notebooks con Anaconda, escribir lo siguiente en la línea de comandos:
> jupyter-notebook
Esto abrirá una página en el navegador que permite trabajar con notebooks.

Al instalar Anaconda, automáticamente crea un ambiente llamado "base".

Para ver información del ambiente, escribir lo siguiente:
> conda info

Para crear un nuevo ambiente, escribir lo siguiente en la línea de comandos:
> conda create --name <env name>

Para activar un ambiente, escribir los siguiente:
> conda activate <ambiente>

Para desactivar un ambiente, escribir:
> conda deactivate

Para listar los ambientes, escribir:
> conda env list

Para instalar paquetes en un ambiente, escribir:
> conda install <paquete>=<version> <n>=<n> ...

Para instalar la última version de un paquete, escrbir:
> conda install <paquete> <n> ...

Para actualizar un pquete, escribir:
> conda update <paquete> <n> ...

Para listar los paquetes de un ambiente, escribir:
> conda list
> conda list <paquete>

Para eliminar un pquete instalado, escribir:
> conda remove <paquete>

Para clonar un ambiente, escribir:
> conda create --name <nuevo ambiente> --copy --clone <viejo ambiente>

Para eliminar un ambiente, escribir:
> conda env remove --name <ambiente>
