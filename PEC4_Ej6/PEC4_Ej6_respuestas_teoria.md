# PEC4
## PEC4 Ejercicio 6

### Apartado 1

style encapsulation : el estilo de un componente se puede encapsular para que no afecte al resto de la aplicación. Hay tres modos de encapsulacion : Shadow DOM, Emulated y none. Esto nos ayuda a que esta parte de nuestro codigo no afecte o entre en conflicto con el resto del documento.

### Apartado 2

shadow DOM : Este nos permite insertar en nuestro documento un "documento" aparte. Habrán diferentes partes:

- Shadow host: El nodo regular del DOM al que es atado el shadow DOM.
- Shadow tree: El arbol DOM dentro del shadow DOM.
- Shadow boundary: El punto en el que el shadow DOM termina y el DOM regular comienza.
- Shadow root: El nodo raiz del arbol Shadow.

Podremos insertar nuestro shadow root en nuestro shadow host. 
En la siguiente imagen se puede ver facilmente:
(Insertaria una imagen pero nose como se hace en MarkDown asi que dejo el link : https://media.prod.mdn.mozit.cloud/attachments/2018/01/29/15788/9d23f749f26b93a00f5c2aa72f00e720/shadow-dom.png)

### Apartado 3

changeDetection : significa actualizar el DOM siempre que se modifiquen los datos. Angular puede detectar cuándo cambian los datos de los componentes y luego volver a renderizar automáticamente la vista para reflejar ese cambio. Existen diferentes modos, entre ellos: Default y OnPush.

### Apartado 4 

Diferencias entre Default y OnPush

Default : Por defecto, Angular tiene que ser conservador y verificar cada posible cambio, esto se denomina comprobación sucia o dirty checking. Se dispara con demasiada frecuencia, al menos en los siguientes casos:
- Eventos desde el browser
- Timers, intervals etc..
- Llamadas http
- Promesas y código asíncrono.
Por si fuera poco, además de dispararse mucho es muy costoso. Determinar que algo ha cambiado implica comparar dos estados: el actual y el anterior.

OnPush: Como se puede prever, la detección del cambio manual es lanzada por el programador. No siempre va a ser laborioso, pero será más consciente pues para que ocurra han de darse alguna de estas circunstancias:
- Explícitamente el programador solicita la detección llamando a `ChangeDetectorRef.detectChanges();
- Implícitamente al usar el pipe Async en la vista se llama a ese mismo método.
- Conscientemente el desarrollador obliga a un componente a repintarse si le cambia la referencia a un @Input().

### Apartado 5

Ciclo de vida de los componentes

Cada componente tiene un ciclo de vida, es decir tiene diversas etapas, en concreto pasara por 8 etapas que se llaman 'lifecycle hook' o 'evento de enlace de ciclo de vida'.
Se pueden separar en dos fases, una vinculada al componente en si y la otra centrada en los hijos del componente. Ahora veremos las etapas en especifico:
- ngOnChanges: Este evento se ejecuta cada vez que se cambia un valor de un input control dentro de un componente.
- ngOnInit: Se ejecuta una vez que Angular ha desplegado los data-bound properties(variables vinculadas a datos) o cuando el componente ha sido inicializado, una vez que ngOnChanges se haya ejecutado.
- ngDoCheck: Se activa cada vez que se verifican las propiedades de entrada de un componente. 
- ngAfterContentInit: Se ejecuta cuando Angular realiza cualquier muestra de contenido dentro de las vistas de componentes y justo después de ngDoCheck. 
- ngAfterContentChecked: Se ejecuta cada vez que el contenido del componente ha sido verificado por el mecanismo de detección de cambios de Angular; se llama después del método ngAfterContentInit.
- ngAfterViewInit: Se ejecuta cuando la vista del componente se ha inicializado por completo.
- ngAfterViewChecked: Se ejecuta después del método ngAfterViewInit y cada vez que la vista del componente verifique cambios.
- ngOnDestroy: Este método se ejecutará justo antes de que Angular destruya los componentes. Es muy útil para darse de baja de los observables y desconectar los event handlers para evitar memory leaks o fugas de memoria.