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

- includes()
- pop()
- push()
- unshift()
- reverse()
- shift()
- length

- indexOf()
- splice()

- map()
- filter()
- reduce()

Para despues:
- find()
- some()
- every()
- reduce()
- splice()
