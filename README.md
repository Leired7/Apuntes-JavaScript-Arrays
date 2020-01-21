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

### Añadir un item al final de la lista

Existe un método que 
