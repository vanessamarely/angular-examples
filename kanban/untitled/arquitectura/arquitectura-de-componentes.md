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

Estos componentes son los Smart on inteligentes

* Layout components o componentes de diseño



