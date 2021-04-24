---
description: >-
  Son muchas las guías y técnicas que podemos implementar para hacer una buena
  arquitectura en nuestra aplicación y no existe una única regla.
---

# Recomendaciones Generales

Como mencione antes no existe una única regla para crear una buena arquitectura para nuestra aplicación, es bueno seguir la guía de estilos en Angular y con el equipo de trabajo, si se tiene o de forma individual, si tu solo estas liderando o ejecutando un proyecto, es bueno crear un mapa o hacer una planeación, sobre que vas a implementar en tu aplicación. Esto sirve para que otros desarrolladores que se vayan uniendo al equipo, sepan que usaste y porque, ademas de dejar una mínima documentación de tu proyecto. 

Adicional a las consideraciones ya mencionadas es bueno también considerar lo siguiente en tu aplicación:

**Accesibilidad**. Es importante hacer accesible nuestra aplicación a todos y esto  nos ayuda a considerar más aspectos.

**i18n**. La internacionalización es un aspecto que puede afectar enormemente tu aplicación, porque es bueno considerar si se desea que este en varios lenguajes y esto implica analizar qué herramientas vamos a usar y cómo estructurar el proyecto. 

**Ambientes o Environments**. Vamos a mover nuestra aplicación en diferentes ambientes.

**CI/CD \(Continues Integration / Continues Deployment\)**.  

**CDN, contenedor, servidor**. Como realizaremos el despliegue de nuestra aplicación, usaremos Docker o un contenedor. Esta parte no afecta tal vez mucho nuestro código, pero sí es bueno saber que otras herramientas usaremos para que nuestro producto sea usado.

**Unit testing o pruebas unitarias**. Qué herramientas vamos a usar, vamos a usar karma. 

**End-to-End testing**. ****Se va a usar Cypress. Esto podría afectar un poco el código en cuanto a que se deben tomar algunas decisiones como si se van a usar Ids o las etiquetas, para hacer las pruebas.

**API**. En este punto se tiene en cuenta el punto de vista de backend, para definir algunos verbos que se van a usar, la seguridad.

Se pueden considerar más aspectos, los que requieras o tu equipo. 

Crear una plantilla, de los puntos claves a definir en cada proyecto, nos ayuda a ahorrar tiempo para no tener que volver a pensar en cuáles son los principales aspectos que debemos considerar a la hora de iniciar la arquitectura.







