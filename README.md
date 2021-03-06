# Arrays

Los arrays son un tipo de variable especial que puede contener más de un valor a la vez.

Ya hemos visto cómo asignar un solo valor a una variable determinada. Puede ser un ```number```, un ```string```... Los arrays, en cambio, pueden tener varios valores. Por ejemplo, un array puede contener 5 ```string```, 34 ```number```, 125 ```objects```, etc. No hay límite para la cantidad de items que puedes meter dentro de un array.

Hablando metafóricamente, un ```array``` es una caja donde puedes meter otras cajas en un orden determinado, y puedes ir solicitando estas cajas dependiendo del orden en el que estén colocadas.

La sintaxis de un ```array``` es el siguiente:

```javascript
let thingsToBuy = ['Naranjas', 'Manzanas', 'Leche', 'Cereales'];
```
Los ```array``` se escriben entre ```[ ]``` y se separan los items que hay dentro con una ```,```. Este array se puede a su vez asignar a un nombre de una variable ```var```, ```let```, o ```const```. En el ejemplo de arriba, hemos creado un ```array``` con 4 items (```string```) dentro, y lo hemos asignado en la variable ```thingsToBuy```. Ahora podemos tener acceso a él desde esta variable.

En este caso, todos los items del ```array``` son ```string```, pero podrían ser de cualquier tipo. También pueden ser variables, e incluso más ```array``` dentro del mismo.

Veamos un ejemplo:
```javascript
let coding = true;
let dogs = ['Jordi', 'Maya'] 
let myArray = ['water', 25, coding, dogs]

console.log(myArray) // ['water', 25, true, ['Jordi', 'Maya']];
```

## Cómo acceder al contenido del ```array```

Para acceder a un item determinado de un ```array``` es necesario llamarlo por su posición dentro del mismo.

Cojamos como ejemplo la variable ```thingsToBuy``` que hemos declarado anteriormente en el ejercicio. Para llamar a cada uno de los items que están dentro de este ```array``` se hace de la siguiente forma:
```javascript
thingsToBuy[0] // 'Naranjas'
thingsToBuy[1] // 'Manzanas'
thingsToBuy[2] // 'Leche'
thingsToBuy[3] // 'Cereales'
```

:warning: Es importante tener en cuenta que, en los ```array```, el primer item está ocupando el puesto número ```0```.

Como podemos ver en el ejemplo, cuando corro el código de ```myArray[0]``` obtenemos el primer item de nuestro ```array```: ```'Naranjas'```.

Si corremos el siguiente código: ```thingsToBuy[1]```, obtendremos el item que ocupa el segundo lugar de la lista, es decir, ```'Manzanas'```, y así sucesivamente.

## Como cambiar, añadir o eliminar items de un ```array```

### Cambiar un item determinado

Imaginemos que, tomando nuevamente nuestra variable ```thingsToBuy```, hemos cambiado de opinión con respecto a los items que tenemos dentro y queremos cambiar ```'Manzanas'``` por ```'Peras'```. Esto se haría de la siguiente forma:

```javascript
console.log(thingsToBuy) // ['Naranjas', 'Manzanas', 'Leche', 'Cereales']
thingsToBuy[1] = 'Peras';
console.log(thingsToBuy) // ['Naranjas', 'Peras', 'Leche', 'Cereales']
```

En este ejemplo, hemos re-asignado directamente el item que ocupa el segundo puesto en la lista (```thingsToBuy[1]```) y le hemos dado un nuevo valor ```'Peras'```. Esta es una de las formas, probablemente la más sencilla, de cambiar un item de un ```array``` cuando sabes exactamente la posición que quieres cambiar.

### Añadir un item al final del ```array```

Existe un método que te permite añadir un item y que ocupe el último puesto de tu ```array```. Este método se llama ```push()```. 

Se aplica de la siguiente forma:

```javascript
let myLuckyNumbers = [4, 13, 45, 78];
myLuckyNumbers.push(99)
console.log(myLuckyNumbers) // [4, 13, 45, 78, 99]
```

Antes del ```.push()``` hay que poner el ```array``` al que queremos añadirle un item al final. Y, entre los paréntesis, hay que poner el elemento que queremos introducir. 

### Añadir un item al principio del ```array```

De forma similar, existe un método que te permite añadir un item y que ocupe el primer puesto del ```array```. Este método se llama ```unshift()```. 

Se aplica de la siguiente forma:

```javascript
let carBrands = ["Toyota", "Ferrari", "Seat"];
carBrands.unshift("Volvo")
console.log(carBrands) // ["Volvo", "Toyota", "Ferrari", "Seat"]
```

Antes del ```.unshift()``` hay que poner el ```array``` al que queremos añadirle un item al principio. Y, entre los paréntesis, hay que poner el elemento que queremos introducir. 

### Eliminar el primer item de un ```array```

Para eliminar el primer item de un ```array```, es decir, el item en la posición ```0```, existe un método que se llama ```shift()```.

Se aplica de la siguiente forma:

```javascript
let countries = ["Spain", "France", "Germany", "Mexico"];
countries.shift()
console.log(countries) // ["France", "Germany", "Mexico"]
```

Antes del ```.shift()``` hay que poner el ```array``` al que queremos eliminarle el primer item. Entre los paréntesis no hay que poner nada.

### Eliminar el último item de un ```array```

Para eliminar el último item de un ```array``` existe un método que se llama ```pop()```.

Se aplica de la siguiente forma:

```javascript
let footballTeams = ["Real Madrid", "Villarreal", "Betis", "Granada"];
footballTeams.pop()
console.log(footballTeams) // ["Real Madrid", "Villarreal", "Betis"]
```

Antes del ```.pop()``` hay que poner el ```array``` al que queremos eliminarle el último item. Entre los paréntesis no hay que poner nada.


## Otros métodos y propiedades

Existen muchas propiedades y métodos de mucha utilidad que podemos utilizar sobre cualquier ```array``` para realizar acciones sobre éste u obtener información determinada sobre él.

Algunos de los más comunes y útiles son:

### .includes( )

Este método determina si un existe un elemento determinado dentro de un ```array``` o ```string```. El resultado será ```true``` si el elemento está y ```false``` si no lo está. Este método se aplica directamente a un ```array``` o ```string``` y entre paréntesis hay que poner el elemento que estamos buscando.

Ejemplos:

```javascript
let someArray = ['potato', 'fruits', 'cheese'];
someArray.includes('potato') // true
someArray.includes('apple') // false

let someWord = 'Wild Code School'
someWord.includes('e') // true
someWord.includes('w') // false
```
:warning: Hay que tener en cuenta que ```.includes()``` es 'case sensitive', es decir, que diferencia entre las letras mayúsculas y minúsculas; las considera como letras diferentes.

### .reverse( )

Este método cambia de orden los elementos dentro de un ```array```. No recibe argumentos.

Ejemplo:

```javascript
let someArray = ['potato', 'fruits', 'cheese'];
someArray.reverse() // ['cheese', 'fruits', 'potato']
```

### .length

Esta propiedad devuelve el valor de la longitud de un determinado ```array``` o ```string```.

Ejemplos:

```javascript
let someArray = ['potato', 'fruits', 'cheese'];
someArray.length // 3

let someWord = 'Wild Code School'
someWord.length // 16
```
:warning: Hay que tener en cuenta que en los ```string```, los espacios son considerados como un caracter. Por lo tanto, cuando calculemos ```.length``` de un string, también nos va a contar los espacios en blanco.

### .indexOf( )

Este método devuelve la posición dentro de un ```array``` o ```string``` del primer elemento específico que encuentra de izquierda a derecha. En el caso de que el elemento buscado no exista dentro del ```array```, ```indexOf()``` devolverá el valor ```-1```. Se aplica a un ```array``` o ```string```, y se pasa como argumento el elemento del que queremos obtener el ```index```.

Ejemplos:

```javascript
let someArray = ['potato', 'fruits', 'cheese'];
someArray.indexOf('potato') // 0
someArray.indexOf('manzana') // -1

let someWord = 'Wild Code School'
someWord.indexOf(' ') // 4
```

### .splice( )

Este método elimina elementos de un ```array``` desde una determinada posición dentro de este. También puede añadir elementos desde el ```index``` seleccionado. Devuelve los elementos eliminados.

Puede recibir muchos argumentos: 
- El primero indica el ```index``` desde donde vamos a empezar a eliminar items (este mismo incluido).
- El segundo indica la cantidad de items que quieres eliminar.
- Del tercero en adelante se indica el contenido que quieres introducir sustituyendo los elementos que has eliminado.

Ejemplos:

```javascript
let someArray = ['potato', 'fruits', 'cheese'];
someArray.splice(0,1) // someArray = ['fruits', 'cheese']

let anotherArray = [45, 23, 97]
anotherArray.splice(1, 2, 2, 5, 4) // anotherArray = [45, 2, 5, 4]

```

### .every( )

Este método revisa si todos los elementos dentro de un array pasan una condición determinada. Recibe una función como argumento, y ésta devolverá los valores que cumplan la condición anteriormente nombrada. Esta funcion, la que pasamos como argumento dentro de ```every()```, a su vez recibe un argumento que será igual a cada item del array.

```.every()``` te devuelve un valor ```true```, si todos los items cumplen la condición, o ```false```. 



Ejemplos:

```javascript
let numbersArray = [3, -5, 14, 95];

numbersArray.every((number)=>{
  return number > 0;
}) // false

numbersArray.every((number)=>{
  return number !== 5;
}) // true
```

Faltan:

- map()
- filter()
- reduce()
- find()
- some()
