# MarkDownPatrones

##ADAPTER

1. **Funcionalidad**

      Busca una manera estandarizada de adaptar un objeto a otro. Se utiliza para transformar una interfaz en otra, de tal modo que una clase que no pudiera utilizar la primera, haga uso de ella a través de la segunda.
Es conocido como Wrapper (al patrón Decorator también se lo llama Wrapper, con lo cual es nombre Wrapper muchas veces se presta a confusión). 

2. **Diagrama**

      ![Diagrama de el patron Adapter][imagenAdapter]

3. **Motivo de Eleccion**

       Se quiere utilizar una clase que llame a un método a través de una interface, pero se busca utilizarlo con una clase que no implementa ese interface.
       Se busca determinar dinámicamente que métodos de otros objetos llama un objeto.
       No se quiere que el objeto llamado tenga conocimientos de la otra clase de objetos.
       Este patrón convierte la interfaz de una clase en otra interfaz que el cliente espera. Esto permite a las clases trabajar juntas,        lo que de otra manera no podrían hacerlo debido a sus interfaces incompatibles.


##BUILDER

1. **Funcionalidad**

       Este patrón permite que un objeto sea creado a partir de varias partes de este que individualmente contribuyen a la construcción. Debido a esto 
       permite que un mismo proceso de construcción de cabida a varias representaciones. 

2. **Diagrama**

      ![Diagrama de el patron Builder][imagenbuilder]

3. **Motivo de Eleccion**

       El patrón builder es útil en muchos casos ya que en ocasiones un objeto es tan complejo y  tiene muchas maneras de representarse que resulta 
       complicando de cierta manera el código al crear varios objetos complejos. Caso en el cual *Builder* es muy útil pues nos evita crear más de un 
       objeto complejo, y en vez de esto, crear un objeto a partir de sus partes que son unidas por un constructor que se encuentra en el *Director*. 
       Las partes que recibe son especificadas por el cliente y son traídas de los *Builder Concretos* que tendrían las diferentes representaciones que 
       se pueden hacer del objeto. El patrón ahorra creaciones innecesarias y a su vez organiza el código de manera que sea más entendible y sencillo de 
       manejar.



##PROTOTYPE

1. **Funcionalidad**

      El patrón prototype tiene como finalidad crear objetos **clonando** instancias ya existentes, clonara la información necesaria que tenga el 
      prototipo y de ahí en adelante este clon será independiente del prototipo y de otros clones. 

2. **Diagrama**

      ![Diagrama de el patron Prototype][imagenprototype]


3. **Motivo de Eleccion**

      Usar este patrón evita la creación de varios objetos “caros”, es decir que consumen tanto memoria como tiempo en la ejecución del programa. Además 
      de esto permite que las clonaciones se generen a medida que el programa lo va requiriendo. Otra de las cosas que hace a prototype un patrón de 
      diseño “amigable” es que da la posibilidad de hacer *Deep copy* o *Shallow copy*, que varian en la informacion que se clona del prototipo, esto 
      enfatizando en las necesidades que surgen en la ejecución del programa, si se necesita un clon idéntico al prototipo se hará un *Deep copy*, en 
      cambio si lo que se requiere es un clon que tenga lo fundamental del prototipo pero que sus atributos puedan variar será un *Shallow copy*.


##DECORATOR

1. **Funcionalidad**

     El patrón Decorator permite añadir responsabilidades a objetos concretos de forma dinámica, evitando usar la herencia ya que esta no es flexible, 
     en vez de esta crea un objeto que se encargue de añadir la nueva responsabilidad.


2. **Diagrama**

      ![Diagrama de el patron Decorator][imagendecorator]


3. **Motivo de Eleccion**

     Este patrón es muy útil al momento de necesitar que una funcionalidad de un objeto se pueda quitar o agregar dinámicamente. Como la descripción del 
     patrón lo dice, evita crear una relación de *herencia* innecesaria creando un objeto *Decorator*, que es el que toma las funcionalidades *Decorator 
     Concreto* que se le quieren añadir o modificar al objeto inicial *Componente* durante el proceso del programa. Este *Decorator* nos facilita el 
     planteamiento que se hace al momento de crear por ejemplo un juego en el que un personaje puede tener muchas fases en el transcurso del juego, no 
     hace falta tener cuatro personajes diferentes e instanciarlos cuando los necesitamos, sino que podemos hacer uso de los *Decoradores Concretos* 
     para dar funcionalidades especificas al objeto Concreto en el momento que el programa lo requiera.


##BRIDGE

1. **Funcionalidad**

       Este patrón elimina la inconveniencia del caso cuando un objeto tiene ciertas posibles implementaciones,el uso habitual es mediante la herencia. 
       muchas veces la herencia puede presentar problemas como el acoplar el codigo con una cierta implementacion.


2. **Diagrama**

      ![Diagrama de el patron Bridge][imagenBridge]

3. **Motivo de Eleccion**
      
       Este patron es util cuando la implementacion de una abtraccion debe ser cambiada en tiempo de ejecución, es decir que cuando la implementacion de una abstraccion deba cambiar no debe repercutir en el código.
       Elimina el enlace permanente. tambien permite que las implementaciones sean extensibles por medio de subclases.
       La aplicación de este patron permite reducir o simplificar jerarquias muy pobladas.
 

##FACADE

1. **Funcionalidad**

       Este patrón simplifica el sistema permitiendo el uso de una interfaz simplificada para tratar con los subsistemas pertinentes haciendo así al sisema mas fácil de usar.
       Este patrón reduce la dependencia entre subsistemas. Es llamado fachada pues a vista del cliente se genera un entorno mas sencillo y lo que hace el cliente es ingresar a un subsistema que estructura un entorno de programacion mas sencillo.
 

2. **Diagrama**

      ![Diagrama de el patron Facade][imagenFacade]

3. **Motivo de Eleccion**
      
       Este patron debe usarse para proporcionar una interfaz mas sencilla cuando el sistema es complejo tambien para desacoplar un subsistema de otros haciéndolo mas independiente, nos permite dividir el sistema en niveles pudiendo usar la fachada como el nivel de aplicacion y nos simplifica el tratar con cada subsistema haciendo que solo deleguemos las peticiones que se puedan hacer desde este nivel.


##SINGLETON

1. **Funcionalidad**

       Porque es re singleton
       El uso de este patrón es limitar el numero de instancias de una clase. pareciera ser la manera de crear una variable global de manera correcta , podríamos verlo como una instancia a la que se le proporciona un punto de acceso global.
 

2. **Diagrama**

      ![Diagrama de el patron Singleton][imagenSingleton]

3. **Motivo de Eleccion**

      Este patron permite la representacion de objetos unívoco durante el ciclo de vida del sistema puede llegar a ser muy útil en casos donde es estrictamente necesario tratar con una y solo una instancia de dicho objeto por ejemplo un servidor teniendo como exepcion los casos donde a un objeto sean necesarias multiples instancias 

##FACTORY METHOD

1. **Funcionalidad**

       Este patrón permite abstraer la forma en la que se crean los objetos, permitiendo tratar las clases a crear de forma genérica dejando para más tarde la decisión de qué clases crear o cómo crearlas.
       
2. **Diagrama**

      ![Diagrama de el patron factoy method][imagenfactorymethod]

3. **Motivo de Eleccion**

      Factory method es para aplicaciones que pueden presentar múltiples documentos a los usuarios. Las principales abstracciones en este Framework son las clases Application y Document, ambas clases son abstractas y los clientes tienen que dejar a las subclases sus implementaciones específicas de la aplicación.
      
##ABSTRACT FACTORY

1. **Funcionalidad**

       Este patrón permite proporciona una interfaz de familias de objetos o que depenen entre si, sin especificar sus clases concretas.
       
2. **Diagrama**

      ![Diagrama de el patron abstract factoy][imagenabstractfactory]

3. **Motivo de Eleccion**

      Este patron tiene aplicabilidad cuando el usuario tiene distintas interfaces con distintos comportamientos que requieren ser restructurados o reformados, presentar una categoria abstracta que permita derivar la creacion y comportamiento de distintos tipos de objetos. 
      
##FLYWEIGHT

1. **Funcionalidad**

      Busca eliminar o reducir la redundancia cuando tenemos gran cantidad de objetos que contienen información idéntica, además de           lograr un equilibrio entre flexibilidad y rendimiento (uso de recursos).


2. **Diagrama**

      
![Diagrama de el patron Flyweight][imagenflyweight]



3. **Motivo de Eleccion**

     Este patrón quiere evitar el hecho de crear un gran número estados de objeto para representar a un sistema. Permite compartir            estados para soportar un gran número de objetos pequeños aumentando la eficiencia en espacio. Este patrón quiere evitar el hecho de      crear un gran número estados de objeto para representar a un sistema. Es muy util al momento de eliminar o reducri la redundancia        cuando se tiene a gran cantidad de objetos que continen la misma informacion.
      
      ##PROXY

1. **Funcionalidad**

      Proxy se utiliza como intermediario para acceder a un objeto, permitiendo controlar el acceso a el. Para ello obliga que las llamadas a un objeto ocurran indirectamente a través de un objeto proxy, que actúa como un sustituto del objeto original, delegando luego las llamadas a los métodos de los objetos respectivos.



2. **Diagrama**

      
![Diagrama de el patron proxy][imagenproxy]



3. **Motivo de Eleccion**

Puede ser utilizado en infinitas ocasiones y se le puede otorgar varios usos. Tiene una gran ventaja y es que no obliga al desarrollador a crear demasiada estructura para realizar este patrón, sino que es una forma estándar de acceder a una clase que potencialmente puede ser conflictiva. Por otro lado, no ayuda al desarrollador a crear un algoritmo, sino que el desarrollador tiene que hacer toda la lógica.


   ##COMPOSITE

1. **Funcionalidad**

      Composite sirve para construir algoritmos u objetos complejos a partir de otros más simples y similares entre sí, gracias a la composición recursiva y a una estructura en forma de árbol. Dicho de otra forma, permite construir objetos complejos componiendo de forma recursiva objetos similares en una estructura de árbol.


2. **Diagrama**

      
![Diagrama de el patron composite][imagencomposite]



3. **Motivo de Eleccion**

Este patrón busca representar una jerarquía de objetos conocida como “parte-todo”, donde se sigue la teoría de que las "partes" forman el "todo", siempre teniendo en cuenta que cada "parte" puede tener otras "parte" dentro. 

##TEMPLATE METHOD

1. **Funcionalidad**

    
  
Define una estructura algorítmica cuya lógica quedará a cargo de las subclases. Para ello, escribe una clase abstracta que contiene parte de la lógica necesaria para realizar su finalidad. En ella se define una estructura de herencia que sirve de plantilla ("Template" significa plantilla) de los métodos en las subclases. 



2. **Diagrama**

      

![Diagrama de el patron Template Method][imagenTemplate] 



3. **Motivo de Eleccion**

      

Este patron permite que ciertos pasos de un algoritmo en una operacion de una superclase sean redefinidos en las subclases sin necesidad de tener que sobreescribir la operacion entera.

##OBSERVER

1. **Funcionalidad**

Este patrón de diseño permite reaccionar a ciertas clases llamadas observadores sobre un evento determinado.
Es usado en programación para monitorear el estado de un objeto en un programa. Está relacionado con el principio de invocación implícita. La motivación principal de este patrón es su utilización como un sistema de detección de eventos en tiempo de ejecución. 

2. **Diagrama**

![Diagrama de el patron Observer][imagenObserver]
3. **Motivo de eleccion**

Define una relacion uno a muchos entre objetos, asi cuando un objeto cambia el estado, todos los que son dependientes se notifican y se actualiza automaticamente.

##STATE

1. **Funcionalidad**

Permite que un objeto modifique su comportamiento cada vez que cambie su estado interno. Busca que un objeto pueda reaccionar según su estado interno. Si bien muchas veces esto se puede solucionar con un boolean o utilizando constantes, esto suele terminar con una gran cantidad de if-else, código ilegible y dificultad en el mantenimiento. La intención del State es desacoplar el estado de la clase en cuestión.

2. **Diagrama**

![Diagrama de el patron State][imagenState]

3. **Motivo de eleccion**

Permite a un objeto alterar su comportamiento cuando se trata de cambios en el estado interno. El objeto aparecera para cambiar su clase.

##VISITOR

1. **Funcionalidad**

Busca separar un algoritmo de la estructura de un objeto. La operación se implementa de forma que no se modifique el código de las clases sobre las que opera.
Si un objeto es el responsable de mantener un cierto tipo de información, entonces es lógico asignarle también la responsabilidad de realizar todas las operaciones necesarias sobre esa información.

2. **Diagrama**

![Diagrama de el patron Visitor][imagenVisitor]

3. **Motivo de eleccion**

Representa una operacion que debe ser llevada a cabo basada en los elementos de la estructura de un objeto. Visitor permite definir una nueva operacion sin cambiar las clases de los elementos en los que opera.


[imagenAdapter]:https://danielggarcia.files.wordpress.com/2014/02/021914_0036_patronesest1.png?w=620
[imagenBridge]:https://danielggarcia.files.wordpress.com/2014/03/031614_2328_patronesest1.png?w=620
[imagenFacade]:https://danielggarcia.files.wordpress.com/2014/02/022014_2335_patronesest1.png?w=620
[imagenSingleton]:https://danielggarcia.files.wordpress.com/2014/02/021714_0053_patronesdec1.png?w=620
[imagenbuilder]: https://danielggarcia.files.wordpress.com/2014/02/builder.png
[imagenprototype]: https://danielggarcia.files.wordpress.com/2014/02/021614_1902_patronesdec1.png?w=620
[imagendecorator]:https://danielggarcia.files.wordpress.com/2014/03/030914_2321_patronesest1.png?w=620
[imagenfactorymethod]:https://danielggarcia.files.wordpress.com/2014/03/031614_2328_patronesest1.png?w=620
[imagenabstractfactory]:https://danielggarcia.files.wordpress.com/2014/03/031614_2328_patronesest1.png?w=620
[imagenflyweight]:https://danielggarcia.files.wordpress.com/2014/03/032414_2059_patronesest1.png?w=620
[imagenproxy]:https://danielggarcia.files.wordpress.com/2014/04/040614_2034_patronesest1.png?w=620
[imagencomposite]: https://danielggarcia.files.wordpress.com/2014/03/033014_1801_patronesest1.png?w=620
[imagenObserver]: https://danielggarcia.files.wordpress.com/2014/06/060214_0019_patronesdec1.png?w=620
[imagenTemplate]: https://danielggarcia.files.wordpress.com/2014/05/050414_1810_patronesdec1.png?w=620
[imagenState]: https://danielggarcia.files.wordpress.com/2014/05/052014_0541_patronesdec1.png?w=620
[imagenVisitor]: http://www.juntadeandalucia.es/servicios/madeja/sites/default/files/imagecache/wysiwyg_imageupload_lightbox_preset/wysiwyg_imageupload/10/PatronVisitor.jpg


