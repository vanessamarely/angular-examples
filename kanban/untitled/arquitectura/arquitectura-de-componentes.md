---
description: >-
  Nuestras aplicaciones esta llenas de componentes y ayuda mucho pensar en como
  queremos estructurarlos para pensar en la arquitectura de ellos.
---

# Arquitectura de Componentes

La mayoría de aplicaciones que construimos no son paginas estáticas, hay un estado y hay diferentes tipos de componentes donde el estado podría vivir. 

### Tipos de Componentes

* Presentational componentes o Componentes de presentación

Muy conocidos como Dumb o componentes tontos. Son stateless o sin estado y usan Inputs/Outputs para su comunicación. Enviamos un valor, renderizamos los valores, emite un evento cuando esta listo y algún otro componente administra el estado y hace las actualizaciones respectivas del estado. 

Con estos componentes nos probamos a nosotros mismos en cuanto a la separación de la complejidad en la lógica que podemos llegar hacer, en estos componentes no hay necesidad de crear servicios mockeados, o hacer alguna petición solo pasamos los inputs, se verifica alguna información de ser necesaria y se emite un output

* Container components o Componentes contenedores

Estos componentes son los Smart o inteligentes. Se encargan de conector los "dumb" al estado de la aplicación. Maneja los eventos emitidos, el de presentación emite un evento, y este  responde a ese evento y se hace los llamados al servidor y actualiza lo necesario para ver los cambios necesarios en la UI o interfaz de usuario. El contenedor es el que controla todo.

* Layout components o componentes de diseño

Para estos no se maneja data, por lo que no es necesario una actualización cuando hay un cambio. Lo podemos ver como una página que tiene una estructura definida, o una plantilla que nos servirá para luego organizar otros componentes.

### Flujo de datos

cuando estamos creando nuestra aplicación podemos ubicar los tres tipos de componentes de la siguiente forma:

Container \(Contenedor\)     -&gt;        Layout \(Diseño\)      -&gt;     Presentational \(Presentación\)

Entre el contenedor y el componente de presentación una forma de compartir la data es mediante Input y Outputs.

![](../../../.gitbook/assets/screen-shot-2021-02-23-at-9.47.05-pm.png)

 La data viene de una petición como por el HttpClient, una Store \(NgrX\), o una ruta y todo va al contenedor, esas diferentes fuentes van al contenedor y este hace lo que requiere el estado y lo pasa al componente presentacional, para renderizar lo que se necesita. 

![](../../../.gitbook/assets/screen-shot-2021-02-23-at-10.02.21-pm.png)

Son dos componentes los importantes uno en mostrar el contenido y el otro de manejar la data.

###  Porqué necesitamos un estado?

Se tiene un servidor que tiene un valor,  se puede tener las rutas que trae data que se comparte entre ellas, y se muestra esa data en la página. Necesitamos la data proveniente de algún lugar para mostrarla en otro; y el estado es quién se encarga de ayudarnos en la comunicación de esas dos necesidades, se puede decir que es la interface entre los datos y los componentes. Ademas nos ayuda a tener los datos consistentes entre componentes y a mantener la comunicación entre ellos.

###  Tipos de Estados

* Estado del servidor

El estado del servidor es la data en el Backend. Hacemos peticiones de la data  al servidor, mediante puede ser un HttpCliente o una url y hacemos la petición de la data. 

* Estado de la aplicación

El estado de la aplicación es lo que nos ayuda a persistir la data a través de toda la aplicación

* Estado de la página

El estado de la página es lo que solo es necesario en la página.

En este punto llega un gran interrogante, como saber cual debemos usar o como debemos poner la data?

Y debemos hacer una análisis del diseño de nuestra aplicación en este punto nos preguntamos, debo compartir la data en toda la aplicación?, la necesito en ciertas páginas?, cuanto debe durar la persistencia de la data? la comparto en una sesión o debe ser en multiples? 

Tenemos varias opciones para responder a nuestras preguntas anteriores.

* Servicios. usando el patrón singleton, podemos crear un subject, exponemos un observable, donde se pueden subscribir a él, puedo obtener lo que necesito y si necesito hacer un update llamo a un set para que se encargue de la actualización. Todos los que se hayan subscrito obtendrán el estado correspondiente, este método ayuda a mantener una consistencia.
* Librerías para manejar el estado  \(NGRX, NGXS\)
* Router o Enrutamiento. Almacena la persistencia de la data, permitiendo que exista en una sesión y también permite compartir paginas o rutas. En el enrutamiento podemos compartir parámetros que usaremos a través de la aplicación.
* Estado del componente. Smart component se encarga de manejar todo el estado.

### Cómo definimos la arquitectura de nuestra aplicación?

* Analiza los requerimientos. Necesitamos hacer un análisis de lo que se desea hacer, es posible que nuestra aplicación crezca y se deba reestructurar, pero de los requerimientos actuales se debe pensar en crear código, que no posea mucha complejidad, que se pueda escalar y que los nuevos integrantes del equipo puedan entender, para que sean participes activos de la aplicación.
* Fácil de mantener. Es este punto ayuda mucho el anterior, es bueno pensar en componentes aislados en su lógica, pero aveces de la prisa lo olvidamos, es bueno siempre recordar que la aplicación va a crecer y se debe hacer un alto a tiempo en el código y pensar en una solución que sea entendible y fácil de mantener para todos.
* Desarrollar funciones o características que  nos ayuden a estructurar la aplicación, donde algunas ayudan al mantenimiento del estado de la aplicación.
* Se debe definir el alcance del estado, no todos los estados deben ser visibles en toda la aplicación, es bueno aprender a ubicar de acuerdo al tipo de estado su lugar correcto
* Separar el contenedor de la presentación, se debe definir que componente es solo para mostrar información que no tendrá lógica compleja y cual se encargara de manejar la lógica a mostrar en el presentacional.













