# JSNotes
Una pequeña recopilacion de metodos de javascript, con ejemplos y descripciones

| **Método**    | **Descripción**                                                                                 | 
|---------------|-------------------------------------------------------------------------------------------------| 
| `at`| Permite acceder a elementos del array usando índices positivos y negativos. |
| `find`        | Regresa el elemento encontrado.                                                                 |
| `findIndex`   | Regresa el índice del primer elemento que cumpla la condición.                                  |
| `indexOf`     | Regresa el índice del elemento encontrado, sino regresa `-1`.                                   |
| `some`        | Si un elemento cumple la condición, regresa `true`, sino `false` y no sigue iterando.           |
| `every`       | Si todos los elementos cumplen la condición, retorna `true`, sino `false`.                      |
| `includes`    | Determina si existe el elemento especificado, regresa `true` o `false`.                         |
| `filter`      | Crea un nuevo array con todos los elementos que pasen la prueba implementada por la función dada.|
| `reduce`      | Aplica una función a un acumulador y a cada elemento del array (de izquierda a derecha) para reducirlo a un solo valor. |
| `sort`        | Ordena los elementos de un array en su lugar y devuelve el array. El orden es según la posición del valor Unicode de cada carácter. | 
| `toSorted`    | No modifica el array original como sort | 
| `reverse`     | Invierte el orden de los elementos de un array en su lugar y devuelve el array.                 |
| `concat`      | Se utiliza para unir dos o más arrays. Este método no cambia los arrays existentes, sino que devuelve un nuevo array. |
| `slice`       | Devuelve una copia de una parte del array dentro de un nuevo array desde el inicio hasta el fin (sin incluirlo). |
| `splice`      | Cambia el contenido de un array eliminando elementos existentes y/o agregando nuevos elementos.  |
| `flat`        | Crea un nuevo array con todos los elementos de sub-array concatenados recursivamente hasta la profundidad especificada. |
| `fill`        | Cambia todos los elementos en un array por un valor estático, desde el índice de inicio hasta el índice final. |
| `join`        | Une todos los elementos de un array (o un array-like object) en una cadena y la devuelve.        |
| `copyWithin`  | Copia una parte del array a otra ubicación en el mismo array y devuelve el array, sin modificar su longitud. |


| Método    | Acceso al índice | Break | Retorno        | Descripción                      |
|-----------|------------------|-------|-------------------|-------------------------------------------|
| `for`     | Sí               | Sí    | `undefined`    | Iterar sobre elementos                    |
| `while`   | Sí               | Sí    | `undefined`    | Iterar hasta que una condición sea falsa  |
| `forEach` | Sí               | No    | `undefined`    | Ejecutar una función para cada elemento   |
| `for...of`| No (1)           | Sí    | `undefined`    | Iterar sobre elementos de objetos iterables |
| `map`     | No               | No    | Nuevo array    | Crear un nuevo array transformado         |


**Nota:** 
1. Con `for...of`, puedes acceder al índice usando el método `entries()`, como se muestra a continuación:
```javascript
const array = ['a', 'b', 'c'];
for (const [index, element] of array.entries()) {
  console.log(index, element); //0 'a' 1 'b' 2 'c'
}
````


## MathMax
Regresa el valor más alto 
```javascript
const numbers = [1,2,3,6000,5,5000,7,8,3000] 
Math.max(...numbers) //6000
```

## Splice
Elimina o agrega elementos a un array en el indice indicado

array.splice( startIndex,n°elementos agregados, elemento agregado )

 ```javascript
const animales= ['🐢','🐸','🐷']
animales.splice (1,0,'🦊') //🐢,🦊,🐸,🐷
```

## LocalStorage
````javascript
//Crear
localStorage.setItem("nombre", 'Pablo')
//Usar
localStorage.getItem("nombre") //Pablo
//Eliminar
localStorage.removeItem("nombre")
//Eliminar todos
localStorage.clear()
````

## Console
````javascript
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
````


# Algoritmos
Un conjunto de instrucciones paso a paso que se siguen para resolver un problema o completar una tarea.

| Algoritmo          | Uso                                              |
|--------------------|--------------------------------------------------|
| Búsqueda Binaria   | Encontrar un elemento en una lista ordenada      |
| Quicksort          | Ordenar listas de manera eficiente               |
| Merge Sort         | Ordenar listas, especialmente útil en listas grandes |
| Dijkstra           | Encontrar el camino más corto en un grafo        |
| A* (A-star)        | Búsqueda del camino más corto, usado en IA de videojuegos |
| Algoritmo de KMP   | Búsqueda de patrones en textos                    |
| Algoritmo de Euclides | Calcular el máximo común divisor (MCD)         |
| Árbol AVL          | Estructura de datos de árbol balanceado          |
| Floyd-Warshall     | Encontrar caminos más cortos entre todos los pares de nodos en un grafo |
| Algoritmo de PageRank | Clasificar páginas web según relevancia, usado por Google |
| BFS (Breadth-First Search) | Búsqueda en amplitud en grafos           |
| DFS (Depth-First Search) | Búsqueda en profundidad en grafos          |

### Recursividad 
La recursividad es una técnica donde una función se llama a sí misma para resolver un problema. Se utiliza mucho para problemas que pueden dividirse en subproblemas más pequeños del mismo tipo. Es como si tuvieras que bajar una escalera y para cada escalón decides volver a llamar a tu cerebro para que te diga cómo bajar el siguiente.

## Paradigmas de diseño

### Divide y Venceras
  1. Tomar el problema original
  2. Dividirlo en partes mas pequeñas hasta ser tan pequeñas que sea más facil solucionarlos
  4. Tomar las pequeñas soluciones y unirlas hasta generar el resultado del problema



## Busqueda Binaria
Sirve para ncontrar un elemento en una lista ordenada. Funciona dividiendo repetidamente la lista a la mitad y comparando el elemento buscado con el elemento del medio.
__Es muy eficiente, con una complejidad de tiempo de `O(log n)`, lo que la hace mucho más rápida que una búsqueda lineal para listas grandes.__

#### 1. _Inicio_: Con un array ordenado empezás con dos índices, uno al principio (inicio) y otro al final (fin) de la lista.
#### 2. _Calcular el indice medio_: Calculás el índice del medio de la lista y comparás el elemento del medio con el que estás buscando.
#### 3. _Comprobar resultados_:
  - Si el elemento del medio es igual al que buscás, ¡bingo! Lo encontraste.
  - Si el elemento del medio es menor al buscado, se sumara +1 al indice y se probara nuevamente el elemento siguiente ej: 4,5,6,7
  - Si el elemento del medio es mayor al buscado, se restara -1 al indice y se probara nuevamente el elemento anterior ej: 3,2,1,0
#### 4. _Repetir_: Repetís el proceso con la mitad restante de la lista hasta que encontrés el elemento o la lista no tenga más elementos para dividir regresando -1.

`````javascript
const numbers = [100, 300, 50, 20,600, 200, 250, 130 ,70,20, 5]
numbers.sort( (a,b ) => a - b ) //Ordenar el array

function busquedaBinaria (array,objetivo) {
let inicio = 0
let final = array.length -1

while(inicio <= final){
  const medio = Math.floor( (inicio + final) / 2 ) //se obtiene el indice medio del array
//math floor para redondear, ya que si el indice es 11 la mitad no daria un numero decimal
  
  if(array[medio] === objetivo){
    return `index: ${medio} value: ${objetivo}`  //index: 8 value: 200
  }
  else if( array[medio] < objetivo){
    inicio = medio + 1
  }
  else {
    final = medio -1
  }
}
  return -1 //si no se encuentra retorna -1
}
  
  busquedaBinaria(numbers, 200)
``````
