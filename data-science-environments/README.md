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

Comando avanzados de conda.

Al tratar de instalar paquetes que no están disponibles en los canales de anaconda (ej. bolton), se debe buscar el canal en www.anaconda.org.
Una vez identificado el canal se debe instalar de la siguiente manera.

> conda install --channel <canal> <paquete>

Conda registra un histórico de revisiones y cada revisión hacer referencia a la instalación de uno o más paquetes.
Para listar las revisiones, se hace de la siguiente manera:
> conda list --revision

Para regresar a un punto de revisión, escribir:
> conda install --revision <número de revisión>

Otro de los grandes beneficios de trabajar con Conda es que se puede compartir con otros los entornos para asegurar la correcta ejecución de proyectos.
Para exportar un entorno con sus dependencias específicas, escribir:
> conda env export

Para exportar un entorno con el nombre y versión de sus dependencias, escribir:
> conda env export --no-builds

Para exportar un entorno con la lista de dependencias que se han instalado manualmente, escribir:
> conda env export --from-history

Para exportar un entorno a un archivo, escribir:
> conda env export --file enviroment.yml

Para importar un entorno, escribir:
> conda env create --file enviroment.yml

Al tratar de importar ambientes con muchas dependencias, esto puede tardar mucho tiempo, es por esto que existe una herramienta llamada Mamba la cual permite al igual que Conda, manimular ambientes distribuyendo los proceso en paralelo.
Cómo instalar Mamba?
> conda install --channel conda-forge mamba

Al importar nuevamente el ambiente pero con Mamba, lo hará en menos tiempo por la distribución de sus procesos en paralelo:
> mamba env create --file enviroment.yml

Una recomendación que podría evitar dolores de cabeza es crear 3 ambientes de trabajo por cada proyecto.

project/
    data/
    model/
    notebook/
    envs/
        external.yml
        model.yml
        comunication.yml
