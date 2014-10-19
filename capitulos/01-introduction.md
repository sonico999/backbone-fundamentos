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

Si usted está escribiendo una aplicación donde la gran parte del trabajo pesado para la representación de vista y manipulación de datos estarán ocurriendo en el navegador, es posible encontrar un marco de JavaScript MV * útil. Ejemplos, las aplicaciones que entran en esta categoría son GMail, NewsBlur y la aplicación móvil de LinkedIn.

Este tipo de aplicaciones suelen descargar una sola carga útil que contiene todos los scripts, hojas de estilo, que muchos usuarios necesitan para tareas comunes y luego realizar una gran cantidad de comportamiento adicional en el fondo. Por ejemplo, es trivial para alternar entre la lectura de un correo electrónico o un documento escrito a uno sin necesidad de enviar una nueva petición al servidor.

Sin embargo, si usted está construyendo una aplicación que todavía se basa en el servidor para la mayor parte del trabajo pesado de la página/vista de renderizado y estás usando un poco de JavaScript o jQuery para hacerlas más interactivas, en un marco MV * pueden ser excesivos. Sin duda hay aplicaciones Web complejas donde la representación parcial de puntos de vista se pueden acoplar con una aplicación de una sola página con eficacia, pero para todo lo demás, puede que te encuentres mejor apegarse a una configuración más sencilla.

La madurez en software (marco) el desarrollo no es simplemente sobre cuánto tiempo un framework tiene alrededor. Es acerca de la solidez de la estructura y lo más importante es lo bien que ha evolucionado para llenar su papel. Se ha vuelto más eficaz en la solución de los problemas comunes? ¿Sigue mejorando a medida que los desarrolladores a crear aplicaciones más grandes y complejas con ella?


### ¿Por qué considerar Backbone.js?

Backbone ofrece un conjunto mínimo de estructuración de datos (modelos, colecciones) y la interfaz de usuario (Vistas, URL) primitivas que son útiles al crear aplicaciones dinámicas utilizando JavaScript. No es obstinado, lo que significa que tiene la libertad y flexibilidad para crear la mejor experiencia para su aplicación web cómo mejor le parezca. Usted puede utilizar la arquitectura prescrita que ofrece fuera de lo estabecido o ampliarla para satisfacer sus necesidades.

La biblioteca no se centra en los widgets o sustitución de la forma en que la estructura de los objetos - sólo le proporciona utilidades para la manipulación y consulta de datos en la aplicación. También no prescribe un motor de plantillas específicas -, mientras que usted es libre de utilizar el micro-plantillas que ofrece, Underscore.js (una de sus dependencias), puntos de vista se puede unir a HTML construido usando su solución de plantillas de su elección.

En cuanto a la gran cantidad de aplicaciones creadas con Backbone, es claro que funciona bien. Backbone también funciona bastante bien con otras bibliotecas, lo que significa que puede incrustar widgets de Backbone en una aplicación escrita con AngularJS, utilizarlo con TypeScript, o simplemente utilizar una clase individual (como modelos) como respaldo de datos para aplicaciones simples.

No hay problemas de rendimiento al utilizar una estructura básica para estructurar su aplicación. Evita los bucles de ejecucion, la unión de dos vías, y el sondeo constante de sus estructuras de datos para actualizaciones y trata de mantener las cosas simples como sea posible. Dicho esto, si usted desea ir contra la corriente, puede poner en práctica, por supuesto, este tipo de cosas en la parte superior de la misma. Backbone no te dejará.

Con una vibrante comunidad de autores de plugins y extensiones, hay una probabilidad de que si usted está buscando lograr algún  comportamiento que carece de Backbone, existe un proyecto complementario que trabaja bien con él. Esto es más simple por la documentación de Backbone alfabetizada de su código fuente, permitiendo que cualquier persona la oportunidad de entender fácilmente lo que está pasando detrás de las escenas.

Después de haber sido perfeccionado a lo largo de dos años y medio de desarrollo, Backbone es una biblioteca madura que continuará ofreciendo una solución minimalista para construir mejores aplicaciones web. Yo lo uso regularmente y espero que usted encuentre tan útil adición a su cinturón de herramientas como yo.


### Configuración de espectativas

El objetivo de este libro es crear un repositorio autentico y centralizada de información que puede ayudar a aquellos en desarrollo aplicaciones del mundo real con Backbone. Si te encuentras con una sección o tema que usted piensa que podría ser mejorado o ampliado en, no dude en presentar un problema (o mejor aún, un pull-petición) en [sitio GitHub] del libro (https://github.com / addyosmani / backbone-fundamentos). No pasará mucho tiempo y usted estará ayudando a otros desarrolladores a evitar los problemas que usted se encontró.

Los temas incluyen la teoría de MVC y cómo construir aplicaciones utilizando de Backbone Modelos, Vistas, Colecciones, y Routers. Yo además enseñare temas avanzados como el desarrollo modular con Backbone.js y AMD (vía RequireJS), soluciones a problemas comunes, como vistas anidadas, la forma de resolver los problemas de enrutamiento con Backbone y jQuery Mobile, y mucho más.

He aquí un vistazo de lo que aprenderá en cada capítulo:

<i>Capítulo 2, Fundamentos</i> traza la historia del patrón de diseño MVC e introduce la forma en que se implementa por Backbone.js y otros frameworks de JavaScript.

<i>Capítulo 3, Backbone Básico</i> cubre las principales características del núcleo de Backbone.js y las tecnologías, técnicas que se necesitan saber para poder aplicarlo.

<i>Capítulo 4, Ejercicio 1: Todos - tú primera aplicación Backbone.js</i> te lleva paso a paso a través del desarrollo de una aplicación simple de lista de tareas del lado del cliente.

<i>Capítulo 5, Ejercicio 2: Biblioteca de Libros - tú primera aplicaciín RESTfull Backbone.js</i> le guía a través del desarrollo de una aplicación de biblioteca de libros que persiste su modelo a un servidor utilizando una API REST.

<i>Capítulo 6, Extensiones Backbone</i> describe Backbone.Marionette y Thorax, dos extensiónes del frameworks de que añaden funciones a Backbone.js que son útiles para el desarrollo de aplicaciones a gran escala.

<i>Capítulo 7, Problemas comunes y soluciones</i> revisa problemas comunes que pueden surgir al utilizar Backbone.js y formas de abordarlos.

<i>Capítulo 8, Desarrollo modular</i> examina cómo los módulos y RequireJS AMD se pueden utilizar para modularizar su código.

<i>Capítulo 9, Ejercicio 3: Todos - Tu Primera aplicación Backbone Modular + RequireJS </i> te lleva a través de la reescritura de la aplicación creada en el ejercicio 1 para ser más modular, con la ayuda de RequireJS.

<i>Capítulo 10, Paginación de Peticiones y Colecciones Backbone</i> paseos a través de la forma de utilizar el plugin Backbone.Paginator para paginar datos para sus colecciones.

<i>Capítulo 11, Backbone Boilerplate y Grunt BBB</i> introduce poderosas herramientas que puede utilizar para iniciar una nueva aplicación Backbone.js con código repetitivo.

<i>Capítulo 12, Aplicaciones móviles</i> aborda los problemas que surgen cuando se utiliza Backbone con jQuery Mobile.

<i>Capítulo 13, Jasmine</i> cubre cómo prueba de unidad  de código Backbone utilizando el framework de pruebas Jasmine.

<i>Capítulo 14, QUnit</i> discute cómo utilizar QUnit para las pruebas unitarias.

<i>Capítulo 15, SinonJS</i> discute cómo utilizar SinonJS para la unidad de pruebas de sus aplicaciones de Backbone.

<i>Capítulo 16, Recursos</i> proporciona referencias a los recursos relacionados con Backbone-adicionales.

<i>Capítulo 17, Conclusiones</i> envuelve nuestro recorrido por el mundo del desarrollo Backbone.js.

<i>Capítulo 18, Apéndice</i> vuelve a nuestro patrón de diseño MVC discusión por contraste con el patrón Model-View-Presenter (MVP) y examina cómo Backbone.js refiere a ambos. Un tutorial de escribir una biblioteca-Backbone a partir de cero y otros temas también están cubiertos.
