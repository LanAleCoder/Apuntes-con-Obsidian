# Iniciando con JavaScript
### ¿Que son los tipos?
Son reglas que definen de que tipo es un objeto, si es tipo numero, tipo texto, etc...
Existen los siguientes
| Tipo | Descripción |  
| ----------- | ----------- |  
| Number | Es un dato de tipo número que generalmente se utiliza para hacer operaciones con números(no utilizar number en ocasiones que no se van a utilizar, por ejemplo, número de telefono, número de teléfono no es un number ya que no se va hacer operaciones con eso, como por ejemplo sumarlo, restarlo o dividirlo) |  
| String | Utilizado para escribir texto, aquí si estaría bien utilizarlo para guardar numeros de telefono, ya que con los strings no se hacen operaciones como sumar o restar |
| Boolean |  Indica si es verdadero o falso
| undefined | Indica que el valor no esta definido, la variable si existe, pero no tiene ningun valor |
| null | Indica que realmente existe, pero no tiene tipo ni valor |
 **Todos estos son tipos primitivos, indica que son inmutables**  

### .toUpperCase():
  pasar un string a mayusculas, ejemplo: var text = "texto"
 
 ``` toUpperCase metodo
 var textoMayus = text.toUpperCase()
 console.log(textoMayus) 
```
 
### .push():
el metodo push permite agregar un elemento al final de un array, ejemplo:
``` push
const lista = [];
lista.push(1)
console.log(lista)

CONSOLE
[1]
```

### Acceder a las posiciones de un array:
``` posicion-de-un-array
const lista = [1, 2, 3 ,4 ,5]
console.log(lista[0])

CONSOLE
1
```

Al utilizar [[#push]] mutamos la variable directamente pero para evitar que mutemos la variable y en este caso es un array, podemos utilizar concat y crear una nueva variable, ya que al mutar un array creamos un desorden y termina siendo dificil de manejar en algunas ocasiones, ejemplo:
``` Como-no-mutar-un-array
❌❌❌❌
const lista = [];
lista.push(1);
console.log(lista);
// Aquí realmente lo estamos mutando directamente
CONSOLE
[1]
❌❌❌❌

✅✅✅✅✅✅✅
const lista = [];
const nuevaLista = lista.concat(1,2,3,4,5,6);

console.log(nuevaLista)
// Aquí lo que hicimos fue crear una nueva variable con un nuevo valor.

CONSOLE
(6)[1,2,3,4,5,6]
{
	0: 1
	1: 2
	2: 3
	3: 4
	4: 5
	5: 6
}
✅✅✅✅✅✅✅
Esto solo es una de las diferentes formas que existen.
```

### Un objeto:
Al crear un objeto, podemos decir que es un diccionario, ya que nos permite tener una llave y valor, ejemplo:
``` Objeto
const persona = {
	nombre: "Yo",
	yutu: "No",
	minecraft: "Si",
}
```
### ¿Como acceder a un objeto?
```Acceder-a-un-objeto
const persona = {
	nombre: "Yo",
	yutu: "No",
	minecraft: "Si",
}
// Vamos a acceder al nombre
console.log(persona.nombre)

CONSOLE
Yo
```
### ¿Como accedo dinamicamente?
``` Acceder-dinamicamente-a-un-objeto
const persona = {
	nombre: "Yo",
	yutu: "No",
	minecraft: "Si",
}
// Accedemos por medio de parametros
const parametro = "nombre"
console.log(persona[parametro])

CONSOLE
Yo
```

### Crear una función
Una constante esta formada por una constante, a la cual se le asigna como valor, una función, primero le ponemos los parentesis, lo cual va iniciar la firma de una funcion y en los parentesis se le asigna los parametros de la función, luego con una flecha le indicamos el cuerpo de la función, lo cual va ser lo que va operar, ejemplo:

``` Crear-una-function-expression
Creamos la constante: const sumar

Le asignamos a la constante una función e inicializamos la firma de la función con los parantesis:

> const sumar = ()

En los parentesis asignamos el nombre de los parametros que va recibir la función:

> const sumar = (numero1, numero2)

Después con => indicamos cuando terminan los parametros de la función y tambien indicamos lo que va ejecutar, o sea el cuerpo de la función, que vendria siendo las llaves {}, aqui va ir todo nuestro código:

> const sumar = (numero1, numero2) => {
> return numero1 + numero2
> }

Para ejecutar la función basta con escribir el nombre de la función y parentesis:

sumar(1,2)

Dentro de los parentesis escribimos los parametros que tiene que recibir, en este caso van a ser dos numeros, 1 y 2, que lo que haria seria sumar los dos numeros.

Una versión más resumida para este caso sería utilizar lo siguiente

const sumar = (numero1, numero2) => numero1 + numero2;
									^
				Justo aquí automaticamente se toma como return	

```


Palabras:
> Multiparadigma: 