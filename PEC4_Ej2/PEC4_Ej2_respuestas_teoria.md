# PEC4
## PEC4 Ejercicio 2

### Apartado 1

El comando que hemos utilizado para crear nuestro proyecto es:

` ng new vinoteca `

- Ficheros de configuración en la raíz del proyecto. 
  - tsconfing.app.json : Este fichero contiene la configuración de Typescript, también contiene las opciones de compilación de Angular.
  - angular.json : Este fichero contiene la configuración de nuestro proyecto Angular. Entre ellos projectType, architect, scripts, styles, outputPath, sourceMap.
  - package.json : Este fichero JSON contiene la configuración de nuestra aplicación web, entre esta información encontramos el nombre, la versión, la descripción, el autor, ...
  - .editorconfig : Este será un fichero oculto nos ayudará con nuestro editor de texto, si trabajamos en una equipo de más de una persona este fichero ayudará a que el formato sea el mismo para todos.
  - .gitignore : Este fichero le indica a GitHub que ficheros o carpetas tiene que ignorar.
- Directorio node_modules : Este sera una carpeta en la que se instalan las dependencias y los paquetes mediante npm. Es un fichero que ocupa mucho espacio y por lo tanto se tiene que borrar a la hora de subirlo a github. Para ver todas las dependencias  
- Directorio src: En este directorio se encontrarán todos los ficheros con codigo ya sea css, html, js o ts.
  - index.html : Es el html que se ejecutará primero a la hora de acceder a la pagina. Este sera un html muy sencillo que solo contendra el elemento de la app.
  - main.ts : Este sera el fichero Typescript principal, será el punto de entrada de nuestra aplicación. Este importará todos los modulos que són necesarios.
  - styles.css : Este será el fichero de estilo principal de nuestro proyecto, que se encargará de la parte visual de nuestra pagina. Después cada componente tendrá el suyo propio.
  - test.ts : Este fichero Typescript contendrá todos los test que tenemos para nuestro programa. Se pueden especificar en el archivo de configuración.
  - polyfills.ts : Con este fichero conseguiremos que nuestra aplicación sea compatible con varios buscadores.
  - Directorio environments : Con este directorio podremos configurar si estamos en el entorno de producción o en el de desarrollo.
  - Directori assets : Aqui se encontrarán todos los ficheros 'non-post' como pueden ser imagenes, css, js, ... Que no se encuentran en la carpeta src.
  - Directori app : Aqui se encontrarán todos los componentes creados y también las clases, interfaces o modelos que creemos.
    - Ficheros app.component.* : Estos serán todos los ficheros que conforman un nuevo componente. Los componentes tienen un fichero de estilo (css), un fichero html y un fichero ts que nos indica toda la información del componente.
    - Fichero app.module.ts : 

### Apartado 2

- app.module.ts - @NgModule (declarations, imports, providers, bootstrap).

  - declarations : Los compoentes, directivas y pipes que pertenecen a este NgModule. 
  - imports : Modulos en los que se exportan clases que se necesitan en algun componente que este en este NgModule.
  - providers : El provider es cualquier cosa que puede crear o devolver un servicio.


- app.component.ts - @Component (selector, templateUrl, styleUrls).

  - selector : El selector nos muestra la etiqueta que tendrá nuestro componente para poder utilizarlo en el html.
  - templateUrl : La direccion del modulo-relativo de este componente html.
  - styleUrls : Dirección del archivo de estilo de este componente. 
