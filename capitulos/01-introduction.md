# Introducción

Frank Lloyd Wright dijo una vez “No se puede hacer un arquitecto. Sin embargo, puedes abrir las puertas y ventanas hacia las luz.” En este libro, Espero mostrarles algo de luz sobre la forma de mejorar la estructura de las aplicaciones web, abriendo las puertas a lo que esperamos sean aplicaciones mantenibles, legibles en el futuro.

El objetivo de toda la arquitectura es construir algo parecido; en nuestro caso, hasta un código que es duradero y encanta tanto a nosotros y a los desarrolladores que mantendrán nuestro código mucho despues que que nos hayamos ido.Todos queremos que nuestra arquitectura se simple pero hermosa.

Frameworks y bibliotecas modernas de javascript pueden traer estructura y organización a nuestros proyectos, estableciendo un fundamento mantenibles desde el principio. Se basan en ensayos y tribulaciones de los desarrolladores que han tenido que solucionar el caos de una retrollamada similar a la que se enfrentan o podrán en un futuro cercano.

Al desarrollar aplicaciones utilizando sólo jQuery, la pieza faltante es una manera de estructurar y organizar el código. Es muy fácil crear una aplicación JavaScript que termina en una maraña de selectores y callbacks de jQuery, tratando desesperadamente de mantener los datos sincronizados entre el código HTML para su interfaz de usuario, la lógica en JavaScript, y las llamadas a su API para los datos.

Sin nada para ayudar a domar el desorden, es probable encadenando un conjunto de plugins y librerías independientes para compensar la funcionalidad o construir todo usted mismo a partir de cero, teniendose que mantener por sí mismo. Backbone te resuelve este problema, proporcionando una forma de organizar limpiamente tu código, la separación de responsabilidades en partes identificables que son fáciles de mantener.

En "Desarrollo de aplicaciones Backbone.js," Yo y algunos autores experimentados te mostraré cómo mejorar tu estructura de aplicaciones web utilizando la biblioteca popular de JavaScript, Backbone.js

### Qué es MVC?

Una serie de marcos modernos de JavaScript proporciona a los desarrolladores un camino fácil para la organización de su código utilizando variaciones de un patrón conocido como MVC (Model-View-Controller). MVC separa la logica de una aplicación en tres partes:

* Los Modelos representan los datos de un modelo específico en una aplicación. Piense en esto como un "tipo" de datos que puede modelar -- como un usuario, fotos o una nota de Todo. Los modelos pueden notificar a los observadores cuando cambian de estado.
* Las Vistas normalmente constituyen la interfaz de usuario en una aplicación (por ejemplo, el marcado y plantillas), pero no son. Observan modelos, pero no se comunican directamente con ellos.
* Los Controladores manejan la entrada (por ejemplo, los clicks, las acciones del usuario) y actualizan los modelos.

Por lo tanto, en una aplicación MVC, la entrada del usuario recibe la acción de los controladores ¿Cual modelo se actualiza. Las Vistas observan a los modelos y actualizan la interfaz de usuario cuando se producen cambios.

Los Frameworks JavaScript MVC no siempre siguen estrictamente el patrón anterior. Algunas soluciones (incluyendo Backbone.js) fusionan la responsabilidad del controlador en la vista, mientras que otros enfoques añaden componentes adicionales conbinandolos.

Por esta razón nos referimos a los frameworks como partidarios del modelo MV *; es decir, es muy probable que tenga un modelo y de una vista, pero un controlador podría no estar presente y otros componentes pueden entrar en juego.

### Que es Backbone.js?

![](img/backbonejsorg.jpg)

Backbone.js es una biblioteca JavaScript ligera que añade estructura a su código de cliente. Hace que sea fácil de manejar y separan la logica en su aplicación, dejándole con un código que es más fácil de mantener en un largo plazo.

Los desarrolladores utilizan habitualmente las bibliotecas como Backbone.js para crear aplicaciones de una sola página (SPAs). SPAs Los desarrolladores utilizan habitualmente las bibliotecas como Backbone.js para crear aplicaciones de una sola página (ZEPA). ZEPA son aplicaciones web que se cargan en el navegador y luego reaccionan a los cambios de datos en el lado del cliente sin necesidad de actualizar la página completa desde el servidor.

Backbone es maduro, popular, y tiene una comunidad de desarrolladores entusiasmada, así como una gran cantidad de plugins y extensiones disponibles que se basan en ella. Se ha utilizado para crear aplicaciones no triviales por empresas como Disqus, Walmart, SoundCloud and LinkedIn.

Backbone se centra en darle métodos útiles para consultar y manipular los datos en lugar de reinventar el modelo de objetos de JavaScript. Es una biblioteca, en ves de un framework, que juega bien con los demás y funciona bien, a partir de widgets integrados a aplicaciones de gran escala.

Como es pequeño, también hay poco que descargar en conexiones móviles o lentas. El código entero de Backbone puede ser leído y comprendido en tan sólo unas horas.

### ¿Cuándo necesito un Framework MVC JavaScript?

Cuando la construcción de una aplicación de una sola página usando JavaScript, si se trata de una interfaz de usuario compleja o simplemente está tratando de reducir el número de peticiones HTTP requeridos para los nuevos Vistas, es probable que te tengas que inventar muchas de las piezas que conforman un marco MV * .

En primer lugar, no es terriblemente difícil de escribir su propio Framework de una aplicación, que ofrece una manera obstinada para evitar código espagueti; sin embargo, decir que es igual de trivial para escribir algo tan robusto como Backbone sería una suposición manifiestamente incorrecta.

Hay mucho más que entra en la estructuración de una aplicación que atando una biblioteca de manipulación de DOM, plantillas, y el enrutamiento. Frameworks Maduros MV * típicamente incluyen no sólo las piezas que tendrpias que escribir, pero también incluyen soluciones a los problemas que te encuentras en el camino. Esto es un ahorro de tiempo en que no hay que subestimar su valor.

Así que, ¿dónde probablemente necesitará un framework MV * y dónde no?

If you’re writing an application where much of the heavy lifting for view rendering and data manipulation will be occurring in the browser, you may find a JavaScript MV* framework useful. Examples of applications that fall into this category are GMail, NewsBlur and the LinkedIn mobile app.

These types of applications typically download a single payload containing all the scripts, stylesheets, and markup users need for common tasks and then perform a lot of additional behavior in the background. For instance, it’s trivial to switch between reading an email or document to writing one without sending a new page request to the server.

If, however, you’re building an application that still relies on the server for most of the heavy-lifting of page/view rendering and you’re just using a little JavaScript or jQuery to make things more interactive, an MV* framework may be overkill. There certainly are complex Web applications where the partial rendering of views can be coupled with a single-page application effectively, but for everything else, you may find yourself better sticking to a simpler setup.

Maturity in software (framework) development isn't simply about how long a framework has been around. It's about how solid the framework is and more importantly how well it's evolved to fill its role. Has it become more effective at solving common problems? Does it continue to improve as developers build larger and more complex applications with it?


### Why Consider Backbone.js?

Backbone provides a minimal set of data-structuring (Models, Collections) and user interface (Views, URLs) primitives that are helpful when building dynamic applications using JavaScript. It's not opinionated, meaning you have the freedom and flexibility to build the best experience for your web application how you see fit. You can either use the prescribed architecture it offers out of the box or extend it to meet your requirements.

The library doesn't focus on widgets or replacing the way you structure objects - it just supplies you with utilities for manipulating and querying data in your application. It also doesn't prescribe a specific template engine - while you are free to use the Micro-templating offered by Underscore.js (one of its dependencies), views can bind to HTML constructed using your templating solution of choice.

Looking at the [large](http://backbonejs.org/#examples) number of applications built with Backbone, it's clear that it scales well. Backbone also works quite well with other libraries, meaning you can embed Backbone widgets in an application written with AngularJS, use it with TypeScript, or just use an individual class (like Models) as a data backer for simpler apps.

There are no performance drawbacks to using Backbone to structure your application. It avoids run loops, two-way binding, and constant polling of your data structures for updates and tries to keep things simple where possible. That said, should you wish to go against the grain, you can of course implement such things on top of it. Backbone won't stop you.

With a vibrant community of plugin and extension authors, there's a likelihood that if you're looking to achieve some behavior Backbone is lacking, a complementary project exists that works well with it. This is made simpler by Backbone offering literate documentation of its source code, allowing anyone an opportunity to easily understand what is going on behind the scenes.

Having been refined over two and a half years of development, Backbone is a mature library that will continue to offer a minimalist solution for building better web applications. I regularly use it and hope that you find it as useful an addition to your toolbelt as I have.


### Setting Expectations

The goal of this book is to create an authoritative and centralized repository of information that can help those developing real-world apps with Backbone. If you come across a section or topic which you think could be improved or expanded on, please feel free to submit an issue (or better yet, a pull-request) on the book's [GitHub site](https://github.com/addyosmani/backbone-fundamentals). It won't take long and you'll be helping other developers avoid the problems you ran into.

Topics will include MVC theory and how to build applications using Backbone's Models, Views, Collections, and Routers. I'll also be taking you through advanced topics like modular development with Backbone.js and AMD (via RequireJS), solutions to common problems like nested views, how to solve routing problems with Backbone and jQuery Mobile, and much more.

Here is a peek at what you will be learning in each chapter:

<i>Chapter 2, Fundamentals</i> traces the history of the MVC design pattern and introduces how it is implemented by Backbone.js and other JavaScript frameworks.

<i>Chapter 3, Backbone Basics</i> covers the major features of the Backbone.js core and the technologies and techniques you will need to know in order to apply it.

<i>Chapter 4, Exercise 1: Todos - Your First Backbone.js App</i> takes you step-by-step through development of a simple client-side Todo List application.

<i>Chapter 5, Exercise 2: Book Library - Your First RESTful Backbone.js App</i> walks you through development of a Book Library application which persists its model to a server using a REST API.

<i>Chapter 6, Backbone Extensions</i> describes Backbone.Marionette and Thorax, two extension frameworks which add features to Backbone.js that are useful for developing large-scale applications.

<i>Chapter 7, Common Problems and Solutions</i> reviews common issues you may encounter when using Backbone.js and ways of addressing them.

<i>Chapter 8, Modular Development</i> looks at how AMD modules and RequireJS can be used to modularize your code.

<i>Chapter 9, Exercise 3: Todos - Your First Modular Backbone + RequireJS App</i> takes you through rewriting the app created in Exercise 1 to be more modular with the help of RequireJS.

<i>Chapter 10, Paginating Backbone Requests & Collections</i> walks through how to use the Backbone.Paginator plugin to paginate data for your Collections.

<i>Chapter 11, Backbone Boilerplate And Grunt BBB</i> introduces powerful tools you can use to bootstrap a new Backbone.js application with boilerplate code.

<i>Chapter 12, Mobile Applications</i> addresses the issues that arise when using Backbone with jQuery Mobile.

<i>Chapter 13, Jasmine</i> covers how to unit test Backbone code using the Jasmine test framework.

<i>Chapter 14, QUnit</i> discusses how to use QUnit for unit testing.

<i>Chapter 15, SinonJS</i> discusses how to use SinonJS for unit testing your Backbone apps.

<i>Chapter 16, Resources</i> provides references to additional Backbone-related resources.

<i>Chapter 17, Conclusions</i> wraps up our tour through the world of Backbone.js development.

<i>Chapter 18, Appendix</i> returns to our design pattern discussion by contrasting MVC with the Model-View-Presenter (MVP) pattern and examines how Backbone.js relates to both. A walkthrough of writing a Backbone-like library from scratch and other topics are also covered.
