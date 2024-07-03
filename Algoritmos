# Algoritmos

Un conjunto de instrucciones paso a paso que se siguen para resolver un problema o completar una tarea.

| Algoritmo | Uso |
| --- | --- |
| Búsqueda Binaria | Encontrar un elemento en una lista ordenada |
| Quicksort | Ordenar listas de manera eficiente |
| Merge Sort | Ordenar listas, especialmente útil en listas grandes |
| Dijkstra | Encontrar el camino más corto en un grafo |
| A* (A-star) | Búsqueda del camino más corto, usado en IA de videojuegos |
| Algoritmo de KMP | Búsqueda de patrones en textos |
| Algoritmo de Euclides | Calcular el máximo común divisor (MCD) |
| Árbol AVL | Estructura de datos de árbol balanceado |
| Floyd-Warshall | Encontrar caminos más cortos entre todos los pares de nodos en un grafo |
| Algoritmo de PageRank | Clasificar páginas web según relevancia, usado por Google |
| BFS (Breadth-First Search) | Búsqueda en amplitud en grafos |
| DFS (Depth-First Search) | Búsqueda en profundidad en grafos |

### Recursividad

La recursividad es una técnica donde una función se llama a sí misma para resolver un problema. Se utiliza mucho para problemas que pueden dividirse en subproblemas más pequeños del mismo tipo. Es como si tuvieras que bajar una escalera y para cada escalón decides volver a llamar a tu cerebro para que te diga cómo bajar el siguiente.

### Metodo Sort

El método `sort((a, b) => a - b)` de JavaScript utiliza un algoritmo de ordenamiento cuya implementación puede variar según el motor de JavaScript del navegador. Sin embargo, en la mayoría de los motores modernos, como V8 (usado en Google Chrome y Node.js), se utiliza una combinación de dos algoritmos: Timsort y QuickSort.

## Paradigmas de diseño

### Divide y Venceras

1.  Tomar el problema original
2.  Dividirlo en partes mas pequeñas hasta ser tan pequeñas que sea más facil solucionarlos
3.  Tomar las pequeñas soluciones y unirlas hasta generar el resultado del problema

## Calcular complejidad

**Temporal:** Mide cuánto tiempo toma ejecutar un algoritmo en función del tamaño de la entrada.

**Espacial:** mide cuánta memoria utiliza el algoritmo.

**O(1) - Constante**

- El tiempo de ejecución no cambia con el tamaño de la entrada.

**O(n) - Lineal**

- El tiempo de ejecución crece linealmente con el tamaño de la entrada.

**O(n^2) - Cuadrática**

- El tiempo de ejecución crece cuadráticamente con el tamaño de la entrada.
- ```javascript
    function printPairs(arr) {
      for (let i = 0; i < arr.length; i++) {
        for (let j = 0; j < arr.length; j++) {
          console.log(arr[i], arr[j]);
        }
      }
    }
    ```
    

**O(log n) - Logarítmica**

- El tiempo de ejecución crece logarítmicamente con el tamaño de la entrada

```javascript
function busquedaBinaria(arr, target) {
  let left = 0;
  let right = arr.length - 1;
  while (left <= right) {
    let mid = Math.floor((left + right) / 2);
    if (arr[mid] === target) return mid;
    if (arr[mid] < target) left = mid + 1;
    else right = mid - 1;
  }
  return -1;
}
```

## Busqueda Binaria

Sirve para ncontrar un elemento en una lista ordenada. Funciona dividiendo repetidamente la lista a la mitad y comparando el elemento buscado con el elemento del medio.  
**Es muy eficiente, con una complejidad de tiempo de `O(log n)`, lo que la hace mucho más rápida que una búsqueda lineal para listas grandes.**

#### 1. *Inicio*: Con un array ordenado empezás con dos índices, uno al principio (inicio) y otro al final (fin) de la lista.

#### 2. *Calcular el indice medio*: Calculás el índice del medio de la lista y comparás el elemento del medio con el que estás buscando.

#### 3. *Comprobar resultados*:

- Si el elemento del medio es igual al que buscás, ¡bingo! Lo encontraste.
- Si el elemento del medio es menor al buscado, se sumara +1 al indice y se probara nuevamente el elemento siguiente ej: 4,5,6,7
- Si el elemento del medio es mayor al buscado, se restara -1 al indice y se probara nuevamente el elemento anterior ej: 3,2,1,0

#### 4. *Repetir*: Repetís el proceso con la mitad restante de la lista hasta que encontrés el elemento o la lista no tenga más elementos para dividir regresando -1.

```javascript
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
```

&nbsp;

## Tabla Comparativa

| Algoritmo | Complejidad Promedio | Complejidad Peor Caso | Estabilidad | Uso de Memoria | Optimizado para datos reales |
| --- | --- | --- | --- | --- | --- |
| Timsort | O(n log n) | O(n log n) | Sí  | Moderado | Sí  |
| QuickSort | O(n log n) | O(n²) | No  | Bajo | No  |
| Merge Sort | O(n log n) | O(n log n) | Sí  | Alto | No  |
| Heap Sort | O(n log n) | O(n log n) | No  | Moderado | No  |
| Bubble Sort | O(n²) | O(n²) | Sí  | Bajo | No  |
| Insertion Sort | O(n²) | O(n²) | Sí  | Bajo | Sí (en listas pequeñas) |
| Selection Sort | O(n²) | O(n²) | No  | Bajo | No  |
