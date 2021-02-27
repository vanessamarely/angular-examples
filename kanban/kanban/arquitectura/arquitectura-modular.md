# Arquitectura Modular

A la hora de organizar nuestro código deseamos que nuestra aplicación sea escalable y limpia, y en esa escalabilidad nos ayuda encontrar una estructura de carpetas adecuada para nuestro proyecto.

El tener una estructura bien definida nos ayuda a ubicar los diferentes elementos que vamos a ir creando, y nos da una mejor visibilidad.

Cada estructura varia, como cada proyecto o aplicación, antes de crear nuestros componentes, módulos, servicios, etc., tenemos que tener claro cual será la responsabilidad que este va a tener. En la guía de estilo menciona todas estas practicas en las que nos podemos basar para logras esto.

De acuerdo a nuestro proyecto podemos tener diferentes formas de organizar nuestros archivos, sea crear módulos por cada feature que vaya a tener nuestra aplicación, o incluso crear módulos, donde agruparemos ciertos elementos de acuerdo a su uso, si es común, o compartido.

Comúnmente se tienen los siguientes módulos en las aplicaciones:

* Core: El CoreModule, asume el rol de AppModule raíz, tendrá aquellos componentes universales y otras características donde solo hay una instancia por aplicación, servicios Singleton, entre otros.
* Share: El SharedModule es donde deben ir todos los componentes, pipes/filters y directivas compartidas en nuestra aplicación. El SharedModule se puede importar en cualquier otro módulo cuando esos elementos se reutilicen. El módulo compartido no debería depender del resto de la aplicación y, por lo tanto, no debería depender de ningún otro módulo.
* Feature: Para aquellos componentes que realizan una funcionalidad especifica en el proyecto.

En la documentación de Angular, podemos ver un ejemplo sencillo del uso de los modelos mencionados:

