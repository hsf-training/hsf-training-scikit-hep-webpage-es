# Configuración

## Para el tutorial

Este tutorial utiliza una muestra de los paquetes del [proyecto Scikit-HEP](https://scikit-hep.org/) (Uproot, Awkward Array, hist, Vector, zfit, iminuit, Particle, fastjet), que son todos componentes que podrías o no usar en tu análisis, así como Python 3, NumPy y una variedad de otras librerías populares (Pandas, Matplotlib, JupyterLab).

En lugar de pedirte que los instales todos, ofrecemos dos formas diferentes de ejecutar todo en tu navegador: GitHub Codespaces y Binder.
Recomendamos que uses GitHub Codespaces (consulta las instrucciones a continuación). Si esta opción no es viable para ti, puedes usar Binder, aunque ten en cuenta que los recursos podrían ser muy limitados.

### GitHub Codespaces

<!--
<p align="center">
  <iframe width="427" height="251" src="https://www.youtube.com/embed/gcAuyqW4QRc" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</p>
-->

Para usar GitHub Codespaces, necesitas crear una cuenta en [GitHub](https://github.com) (¡es gratis! También puedes unirte a su programa educativo para obtener más beneficios gratuitos).

Haz clic en el siguiente botón (se abrirá una nueva página), luego vuelve a estas instrucciones:

<p align="center">
  <a href="https://codespaces.new/hsf-training/hsf-training-scikit-hep-webpage-es?quickstart=1" target="_blank">
    <img src="https://github.com/codespaces/badge.svg" alt="Iniciar GitHub Codespaces">
  </a>
</p>

Después de iniciar el codespace de GitHub, observa las líneas en la pestaña "Terminal" de abajo. Puede tomar un tiempo hasta que el entorno se configure por completo. Si ves líneas como estas:

```
Use Cmd/Ctrl + Shift + P -> View Creation Log to see full logs
✔ Finishing up...
⠦ Running updateContentCommand...
  › python3 -m pip install -r requirements.txt
```

la instalación sigue en curso. Esto tomará alrededor de 5 minutos, así que ten paciencia.

Una vez que haya terminado, deberías ver solamente una línea de comandos vacía como esta:

```
@klieret ➜ /workspaces/hsf-training-scikit-hep-webpage-es (main) $
```

Espera unos segundos para asegurarte de que no se ejecute nada más.

¡Estás listo/a para comenzar! 🎉

Puedes ver y ejecutar los notebooks desde la interfaz de VSCode. Sin embargo, si prefieres usar JupyterLab, puedes añadir `?editor=jupyter` a la URL en tu navegador, de modo que quede así: `https://<id-de-tu-codespace>.github.dev/?editor=jupyter`. Alternativamente, puedes ir a [tus codespaces](https://github.com/codespaces/), buscar el codespace que acabas de crear, hacer clic en los tres puntos del lado derecho y seleccionar "Open in JupyterLab".

### Binder

Simplemente haz clic en el siguiente botón:

<p align="center">
  <a href="https://mybinder.org/v2/gh/hsf-training/hsf-training-scikit-hep-webpage-es/main?urlpath=lab" target="_blank">
    <img src="https://mybinder.org/badge_logo.svg" alt="Iniciar Binder">
  </a>
</p>


## Después del tutorial

Si deseas instalar algunos de estos paquetes en tu propia computadora o en la de tu laboratorio, te recomendamos [Miniforge](https://github.com/conda-forge/miniforge) (o Anaconda/Miniconda con el [canal conda-forge](https://conda-forge.org/docs/user/introduction.html#how-can-i-install-packages-from-conda-forge)). Este método también proporciona una manera de [instalar ROOT en el mismo entorno](https://github.com/conda-forge/root-feedstock#readme). Para configurar el entorno, utiliza el archivo [environment.yml](https://github.com/hsf-training/hsf-training-scikit-hep-webpage-es/blob/main/environment.yml) que está en la [raíz](https://github.com/hsf-training/hsf-training-scikit-hep-webpage-es) de este repositorio, así:

```bash
conda env create -f environment.yml
```

o puedes instalar los paquetes individuales que necesites, por ejemplo,

```bash
conda install uproot awkward   # ... ¿otros?
```

Alternativamente, puedes instalar localmente todos los paquetes requeridos con pip usando

```bash
pip install -r requirements.txt
```

o individualmente, por ejemplo,

```bash
pip install uproot awkward   # ... ¿otros?
```

### Una nota sobre Windows

Todos los paquetes usados en este tutorial están disponibles para Windows excepto `xrootd`, que es el que permite a Uproot leer archivos a través de URLs `root://`. Aun así puedes seguir el tutorial completo: las lecciones que abren un archivo remoto con `root://` también dan una URL `https://` para el mismo archivo, así que descomenta esa línea en su lugar.

`pip install -r requirements.txt` omite `xrootd` automáticamente en Windows. El archivo `environment.yml` de conda no lo hace, porque los archivos de entorno de conda no pueden expresar dependencias específicas de cada plataforma, así que en Windows usa pip, o instala dentro de [WSL](https://learn.microsoft.com/windows/wsl/install), o usa GitHub Codespaces o Binder como se describió arriba.
