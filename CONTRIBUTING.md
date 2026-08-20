# Contribuyendo

[HSF training][hsf-training] es un proyecto de código abierto,
y damos la bienvenida a contribuciones de todo tipo:
nuevas lecciones,
correcciones de material existente,
informes de errores,
y revisiones de los cambios propuestos, todos son bienvenidos.

## Acuerdo de Contribución

Al contribuir,
aceptas que podemos redistribuir tu trabajo bajo [nuestra licencia](LICENSE.md).
A cambio,
abordaremos tus problemas y/o evaluaremos tu propuesta de cambio lo más pronto posible,
y te ayudaremos a convertirte en miembro de nuestra comunidad.
Todos los involucrados en [HSF training][hsf-training]
aceptan cumplir con nuestro [código de conducta](CODE_OF_CONDUCT.md).

## Cómo Contribuir

La forma más sencilla de empezar es abrir un "issue"
para informarnos sobre un error,
una redacción incómoda,
o un error factual.
Esta es una buena manera de presentarte
y conocer a algunos de los miembros de nuestra comunidad.

1. Si no tienes una cuenta en [GitHub][github],
   puedes escribir a los coordinadores en la [lista de correo de HSF training][email].
   Sin embargo,
   podremos responder más rápidamente si utilizas uno de los métodos descritos a continuación.

2. Si tienes una cuenta en [GitHub][github],
   o estás dispuesto/a a [crear una][github-join],
   pero no sabes cómo usar Git,
   puedes reportar problemas o sugerir mejoras [creando un issue][issues].
   Esto nos permite asignar el elemento a alguien
   y responder a él en una discusión encadenada.

3. Si te sientes cómodo/a con Git,
   y te gustaría agregar o cambiar material,
   puedes enviar un "pull request" (PR).
   Las instrucciones para hacerlo están [incluidas a continuación](#usando-github).

## Qué Contribuir

Hay muchas formas de contribuir,
desde escribir nuevos ejercicios y mejorar los existentes,
hasta actualizar o completar la documentación
y enviar [informes de errores][issues]
sobre cosas que no funcionan, no están claras o están ausentes.
Si buscas ideas, consulta la pestaña 'Issues' para ver
una lista de problemas asociados a este repositorio,
o también puedes revisar todos los problemas en [hsf-training][hsf-training-issues].

También hay [una lista][hsf-training-gfis] de todos los problemas que son particularmente fáciles y adecuados
para las primeras contribuciones.

Los comentarios sobre issues y las revisiones de pull requests son igualmente bienvenidos:
somos más inteligentes juntos que por separado.
Las revisiones de principiantes y recién llegados son especialmente valiosas:
es fácil para quienes han estado utilizando estas lecciones durante un tiempo
olvidar lo impenetrable que puede ser parte de este material,
por lo que siempre se agradecen ojos nuevos.

## Usando GitHub

Si decides contribuir a través de GitHub, es posible que desees consultar
[Cómo Contribuir a un Proyecto de Código Abierto en GitHub][how-contribute].
Para gestionar cambios, seguimos [el flujo de GitHub][github-flow].
Cada lección tiene mantenedores que revisan issues y pull requests o animan a otros a hacerlo.
Los mantenedores son voluntarios de la comunidad y tienen la última palabra sobre lo que se fusiona en la lección.
Para usar la interfaz web para contribuir a una lección:

1. Haz un fork del repositorio original a tu perfil de GitHub.
2. Dentro de tu versión del repositorio bifurcado, muévete a la rama `main` y
   crea una nueva rama para cada cambio significativo que se realice.
3. Navega a los archivos que deseas cambiar dentro de las nuevas ramas y realiza las revisiones necesarias.
4. Confirma todos los archivos cambiados dentro de las ramas correspondientes.
5. Crea pull requests individuales desde cada una de tus ramas modificadas
   a la rama `main` dentro del repositorio original.
6. Si recibes comentarios, realiza cambios utilizando tus ramas específicas del problema del repositorio bifurcado y
   los pull requests se actualizarán automáticamente.
7. Repite según sea necesario hasta que se haya abordado todo el feedback.

Al comenzar a trabajar, asegúrate de que tu clon de la rama `main` original esté actualizado
antes de crear tus propias ramas específicas de revisión a partir de allí.
Además, por favor, trabaja solo desde tus ramas recién creadas y *no*
desde tu clon de la rama `main` original.
El sitio se construye y se publica automáticamente desde `main` mediante el
[workflow de despliegue](.github/workflows/deploy.yml); no hay ninguna rama para editar directamente la copia publicada.

# Generando el sitio localmente

Este sitio se construye con Jupyter Book 2. Al momento de escribir esto, la versión 2 todavía es una pre-release, así que hay que instalarla con `pip install --pre "jupyter-book==2.*"`. Una vez que haya una versión estable disponible, se podrá instalar con `pip install jupyter-book` o `conda install -c conda-forge "jupyter-book>=2"`.

Se puede servir localmente una versión en vivo del sitio ejecutando el siguiente comando en la raíz del repositorio:

```
jupyter book start
```

Puedes hacer cambios en los archivos fuente y se verán reflejados en la versión en vivo del sitio.

Una vez que estés conforme, puedes comprobar que todo se construye correctamente desde cero borrando el directorio `_build` y ejecutando la construcción completa.

```
rm -rf _build
jupyter book build --execute --strict --html
```

## Sobre la traducción

Este repositorio es la traducción al español de
[hsf-training-scikit-hep-webpage](https://github.com/hsf-training/hsf-training-scikit-hep-webpage).
Si encuentras un problema que también existe en la versión en inglés,
por favor repórtalo (o corrígelo) también en el repositorio original,
para que ambas versiones se mantengan sincronizadas.

## Otros Recursos

Más información sobre cómo contribuir o cómo contactarnos: [Inicio de HSF training][hsf-training]

[hsf-training-issues]: https://github.com/issues?q=user%3Ahsf-training+is%3Aopen
[hsf-training]: https://hepsoftwarefoundation.org/activities/training.html
[email]: https://groups.google.com/g/hsf-training-wg
[github]: https://github.com
[github-flow]: https://guides.github.com/introduction/flow/
[github-join]: https://github.com/join
[how-contribute]: https://docs.github.com/en/get-started/quickstart/contributing-to-projects
[issues]: https://guides.github.com/features/issues/
[hsf-training-gfis]: https://github.com/issues?q=is%3Aissue+is%3Aopen+archived%3Afalse+sort%3Aupdated-desc+label%3A%22good+first+issue%22+org%3Ahsf-training
