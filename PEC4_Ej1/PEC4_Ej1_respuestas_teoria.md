# PEC4
## PEC4 Ejercicio 1

- ng new : Con este comando vemos que se genera una estructura para nuestra aplicación con angular, durante este proceso se nos preguntará si utilizar rutas y que tipo de hojas de estilo tendremos (CSS, SASS/LESS,...). La estructura estará formado por un componente principal, un archivo index.html (muy sencillo), un modulo principal en ts y un archivo JSON con la configuración de nuestra aplicación (angular-cli.json).

- ng generate : Angular CLI tiene un comando 'generate' que nos ayuda a generar componentes, interfaces, services, modules,...
  - component : Si elegimos generar un componente, la aplicación generara diferentes archivos para el nuevo componente, entre ellos 'item.component.ts', 'item.component.html', 'item.component.css' y 'item.component.spec.ts'.
  - directive : Crea una nueva directiva, esta se representa como un atributo en una etiqueta HTML que se puede utilizar en un elemento del DOM y le dota de un comportamiento. Las más usadas y que se generan por defecto són : NgClass, NgStyle, NgIf y NgFor. A la hora de crearla solamente tendremos que indicar su nombre.
  - enum : Si utilizamos el 'comando ng generate enum' se nos creará el archivo 'nombre.enum.ts'. Y dentro de este podremos crear una estructura de prototipos, que podremos utilizar en Typescript. Por ejemplo si creamos la estructura:
  
    <pre><code>
    enum PropertyType {
        House = 'House',
        Apartment = 'Apartment',
        Flat = 'Flat',
        Studio = 'Studio'
    } 
    </code></pre>
      

    Despues podremos acceder al tipo 'PropertyType.Apartment'.
  - guard : Podremos generar tambien 'Guards', estos son la funcionalidad, logica y codigo que sera ejecutado antes de que la ruta sea cargada. Hay diferentes tipos de guards : CanActivate, CanActivateChild, CanDeactivate, Resolve y CanLoad.
  - interface : Con este comando podremos crear interfaces, una interfaz nos permite crear una estructura parecida a una clase, esta puede tener atributos y metodos:
  
    <pre><code>
    interface Cliente {
        nombre: String;
        cif: String;
        direccion: String;
        creado: Date;
    } 
    </code></pre>
  - pipe : Los pipes son una herramienta de Angular que nos permite transformar visualmente por ejemplo, cambiar un texto a mayúsculas o minúsculas, o darle formato de fecha y hora. Mediante el comando 'generate' podremos crear nuevas pipes, por defecto Angular incorpora algunas: Uppercase y lowercase, Slice, Decimal, Percent, Currency, Json, Async, Date, ...  
  - service : Con el comando 'generate' podremos crear Servicios, esto nos ayuda a la hora en la que dos o más componentes tengan que realizar una misma acción y tengamos que repetir codigo.
- ng serve : Si utilizamos el comando a 'serve' se iniciará un servidor local de desarrollo en el puerto 4200. Para acceder con el buscador tendremos que buscar la URL : http://localhost:4200 .
- ng test : Con este comando seremos capaces de iniciar todos los tests que hayamos marcado en la configuracion.
- ng version : Devuelve la version de Angular CLI que estamos utiliziando para este servidor local de desarrollo.
