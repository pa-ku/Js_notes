# JSNotes

Una pequeña recopilacion de metodos de javascript, con ejemplos y descripciones

| **Método** | **Descripción** |
| --- | --- |
| `at` | Permite acceder a elementos del array usando índices positivos y negativos. |
| `find` | Regresa el elemento encontrado. |
| `findIndex` | Regresa el índice del primer elemento que cumpla la condición. |
| `indexOf` | Regresa el índice del elemento encontrado, sino regresa `-1`. |
| `some` | Si un elemento cumple la condición, regresa `true`, sino `false` y no sigue iterando. |
| `every` | Si todos los elementos cumplen la condición, retorna `true`, sino `false`. |
| `includes` | Determina si existe el elemento especificado, regresa `true` o `false`. |
| `filter` | Crea un nuevo array con todos los elementos que pasen la prueba implementada por la función dada. |
| `reduce` | Aplica una función a un acumulador y a cada elemento del array (de izquierda a derecha) para reducirlo a un solo valor. |
| `sort` | Ordena los elementos de un array en su lugar y devuelve el array. El orden es según la posición del valor Unicode de cada carácter. |
| `toSorted` | No modifica el array original como sort |
| `reverse` | Invierte el orden de los elementos de un array en su lugar y devuelve el array. |
| `concat` | Se utiliza para unir dos o más arrays. Este método no cambia los arrays existentes, sino que devuelve un nuevo array. |
| `slice` | Devuelve una copia de una parte del array dentro de un nuevo array desde el inicio hasta el fin (sin incluirlo). |
| `splice` | Cambia el contenido de un array eliminando elementos existentes y/o agregando nuevos elementos. |
| `flat` | Crea un nuevo array con todos los elementos de sub-array concatenados recursivamente hasta la profundidad especificada. |
| `fill` | Cambia todos los elementos en un array por un valor estático, desde el índice de inicio hasta el índice final. |
| `join` | Une todos los elementos de un array (o un array-like object) en una cadena y la devuelve. |
| `copyWithin` | Copia una parte del array a otra ubicación en el mismo array y devuelve el array, sin modificar su longitud. |
| `Math.max(...array)` | Regresa el valor más alto del array |
| `Math.min(...array)` | Regresa el valor más pequeño del array |

&nbsp;

| Método | Acceso al índice | Break | Retorno | Descripción |
| --- | --- | --- | --- | --- |
| `for` | Sí  | Sí  | `undefined` | Iterar sobre elementos |
| `while` | Sí  | Sí  | `undefined` | Iterar hasta que una condición sea falsa |
| `forEach` | Sí  | No  | `undefined` | Ejecutar una función para cada elemento |
| `for...of` | No (1) | Sí  | `undefined` | Iterar sobre elementos de objetos iterables |
| `map` | No  | No  | Nuevo array | Crear un nuevo array transformado |

**Nota:**

1.  Con `for...of`, puedes acceder al índice usando el método `entries()`, como se muestra a continuación:

```javascript
const array = ['a', 'b', 'c'];
for (const [index, element] of array.entries()) {
  console.log(index, element); //0 'a' 1 'b' 2 'c'
}
```

## GroupBy

Agrupa los elementos que cumplan la condición del callback, el primer valor es el array  de objetos, el segundo es cada elemento, accediendo al key type se agrupan en esa categoria, tambien puede recibir un condicional de precio y especificar en que categoria se juntaran los que cumplan esa condicion

```javascript
const result = Object.groupBy(bikes, bike => bike.type)

 mtb: [{ name: 'trek', type: 'mtb' },
       { name: 'venzo', type: 'mtb' }],
 road: [{ name: 'cannondale', type: 'road' },
       { name: 'cube', type: 'road' }]
  
const result = Object.groupBy(array, provedor => provedor.price > 100 ? 'caro' : 'barato')
 caro: [{ name: 'netflix', price: 200 }],
 barato: [{ name: 'youtube', price: 100 }]
```

## Splice

Elimina o agrega elementos a un array en el indice indicado

array.splice( startIndex,n°elementos agregados, elemento agregado )

```javascript
const animales= ['🐢','🐸','🐷']
animales.splice (1,0,'🦊') //🐢,🦊,🐸,🐷
```

## LocalStorage

```javascript
//Crear
localStorage.setItem("nombre", 'Pablo')
//Usar
localStorage.getItem("nombre") //Pablo
//Eliminar
localStorage.removeItem("nombre")
//Eliminar todos
localStorage.clear()
```

## Console

```javascript
//Contar las veces que se ejecuta
for (let i = 0; i < 3; i++) {
  console.count("count") //count: 1 count: 2 count: 3
}

//Error
console.error()

//Mensaje de alerta
console.warn()

//Calcular tiempo de una tarea
console.time()
console.timeEnd() //default: 0ms

//Crear tabla
console.table([{firstname:"Pablo", lastname:"Kuhn" , age:20}])

| (index) | firstname | lastname | age |
----------------------------------------
|    0    | 'Pablo'  | 'Kuhn' | 29  |

//Mensajes de consola colapsables
console.groupCollapsed()
//El resto de mensajes de consola que estaran ocultos, tablas listas etc
```

