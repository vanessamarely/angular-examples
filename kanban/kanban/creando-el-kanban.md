---
description: "Ahora vamos a iniciar con nuestro Kanban, así que manos a la obra \U0001F44D"
---

# Creando el kanban

## Prerrequisitos 

Los prerrequisitos serán de un nivel de conocimientos técnicos y de una instalación mínima requerida en tu máquina.  


En conocimientos técnicos es importante que conozcas lo básico de Angular, como son los componentes, directivas, módulos, servicios, routing y formularios.   


### En la instalación mínima requerida, te preguntarás que debo tener instalado? 

Es importante tener instalado [**node.js**](https://nodejs.org/en/) y [**npm**](https://www.npmjs.com/) para que podamos instalar Angular.  


Necesitamos un  Editor de texto o IDE, puede ser [**visual studio code**](https://code.visualstudio.com/)  o el IDE o el editor de texto de tu preferencia.

{% hint style="info" %}
**Qué es un IDE?** 

Es un entorno de desarrollo integrado o interactivo, que te permite hacer más funcionalidades, puedes instalar extensiones en el para ayudarte a ser más productivo en tu trabajo. Incluso hay extensiones para editar el tema de nuestro entorno de desarrollo.  
{% endhint %}

Por último necesitamos el [CLI-Angular](https://cli.angular.io/), que nos facilita la creación, generación, ejecución, testing, deploy, en el caso de no tener aún este último instalado, solo necesitas ejecutar en tu terminal, este comando: 

```bash
npm install -g @angular/cli
```

Un Kanban es como un tablero. Sabemos que hemos estado en una situación social de pandemia, que nos ha afectado un poco a nivel productivo, este proyecto te ayudará a organizar un poco tus tareas del día a día, de una forma ágil y efectiva. 

Dirás que este tablero, es parecido a una aplicación de las que encuentras por ahí para descargarla en tu máquina, para qué este proyecto?. Te cuento que con este proyecto podrás ver un poco que tanto tiene esa aplicación que descargas, lo harás tú mismo y podrás personalizarlo de acuerdo a tus necesidades e integrarlo con las herramientas que desees, puedes ir gradualmente aumentandole la complejidad. 

En este tablero podremos ir creando nuestras tareas, tendremos 3 listas, una de tareas:  ¿qué hacer?, otra de tareas en progreso, y una de está hecho, en estas listas iremos colocando las tareas que vayan pasando por cada una de esas etapas.  


Tendremos un home, en él podremos ver una lista de nuestras tareas de acuerdo a la prioridad, estas tareas se crearán en la sección tablero donde crearemos nuestras tareas, las podremos mover por nuestras listas y una vez creadas, podemos, en el home revisarlas por categorías.  


Usaremos un poco de componentes CDK, así que repasaremos un poco estos conceptos.

  


