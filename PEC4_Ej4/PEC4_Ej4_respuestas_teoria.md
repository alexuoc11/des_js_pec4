# PEC4
## PEC4 Ejercicio 4

### Apartado 1

NgFor : 

En general a la hora de aplicar estas variables, la mejor opción es cambiar el nombre de la clase de nuestro elemento. Por ejemplo:

``` *ngFor="let item of lista;let impar = odd;let par = even;" [ngClass]="{azul:par,verde:impar}" ```

- index : Este sera el numero del indice, es decir si repetimos un elemento 5 veces, el primer elemento tendrá el indice 0 y el último 4. Esta variable nos ayudará a poder diferenciar facilmente cada uno de los elementos que hemos repetido.
- even : Con esta variable podremos diferenciar facilmente los elementos pares de todos los que creamos. Esta variable la podremos utilizar para hacer distinciones entre par e impar, como por ejemplo un estilo diferente.
- odd : Con esta variable podremos diferenciar facilmente los elementos impares de todos los que creamos. Esta variable la podremos utilizar para hacer distinciones entre par e impar, como por ejemplo un estilo diferente.
- first : Podremos distinguir el primer elemento de todos los creados, de tal manera que podremos tratarlo diferente. Algunas de las practicas más comunes són cambiar el estilo del fondo.
- last : Podremos distinguir el último elemento de todos los creados, de tal manera que podremos tratarlo diferente. Algunas de las practicas más comunes són cambiar el estilo del fondo.

### Apartado 2

trackBy : Esta función ayuda a que el navegador no tenga que volver a construir todo el documento, sino que solamente hará los cambios que le indiquemos con la variable trackBy. Esta variable tendrá asignada una función que le especificará todo lo necesario.

### Apartado 3

Conocemos las 3 directivas estructurales más utilizadas NgIf, NgFor y NgSwitch. Las dos primeras no pueden ser utilizadas con otras directivas, por ejemplo un elemento no puede tener las directivas NgIf y NgFor a la vez, pero si cualquiera de ellas por separado.
Este codigo sería correcto:
``` <p *ngIf="variable">Este es un párrafo</d> ```
Mientras que este es inválido:
``` <p *ngIf="variable" *ngFor="let elemento of miArray">Este es un párrafo</p> ```

En cambio la tercera directiva estructural 'NgSwitch', depende de otras para funcionar correctamente. Ya que para funcionar necesitara que incluyamos los valores: ngSwitchCase y ngSwitchDefault. Por ejemplo:

<code> 
    <div [ngSwitch]="estado">
        <p *ngSwitchCase="1">El estado es 1</p>
        <p *ngSwitchCase="2">El estado es 2</p>
        <p *ngSwitchDefault>No es ningún estado conocido</p>
    </div>
</code>