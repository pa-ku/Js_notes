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
| `reverse`     | Invierte el orden de los elementos de un array en su lugar y devuelve el array.                 |
| `concat`      | Se utiliza para unir dos o más arrays. Este método no cambia los arrays existentes, sino que devuelve un nuevo array. |
| `slice`       | Devuelve una copia de una parte del array dentro de un nuevo array desde el inicio hasta el fin (sin incluirlo). |
| `splice`      | Cambia el contenido de un array eliminando elementos existentes y/o agregando nuevos elementos.  |
| `flat`        | Crea un nuevo array con todos los elementos de sub-array concatenados recursivamente hasta la profundidad especificada. |
| `fill`        | Cambia todos los elementos en un array por un valor estático, desde el índice de inicio hasta el índice final. |
| `join`        | Une todos los elementos de un array (o un array-like object) en una cadena y la devuelve.        |
| `copyWithin`  | Copia una parte del array a otra ubicación en el mismo array y devuelve el array, sin modificar su longitud. |


| Método    | Acceso al índice | Break | Mutabilidad | Paralelismo | Retorno        | Compatibilidad | Propósito Principal                       |
|-----------|------------------|-------|-------------|-------------|----------------|----------------|-------------------------------------------|
| `for`     | Sí               | Sí    | No          | No          | `undefined`    | ES1            | Iterar sobre elementos                    |
| `while`   | Sí               | Sí    | No          | No          | `undefined`    | ES1            | Iterar hasta que una condición sea falsa  |
| `forEach` | Sí               | No    | No          | No          | `undefined`    | ES5            | Ejecutar una función para cada elemento   |
| `for...of`| No (1)           | Sí    | No          | No          | `undefined`    | ES6            | Iterar sobre elementos de objetos iterables |
| `map`     | No               | No    | No          | No          | Nuevo array    | ES5            | Crear un nuevo array transformado         |
| `filter`  | No               | No    | No          | No          | Nuevo array    | ES5            | Crear un nuevo array con elementos que pasan una prueba |
| `reduce`  | No               | No    | No          | No          | Valor único    | ES5            | Reducir array a un solo valor             |
| `find`    | No               | No    | No          | No          | Elemento       | ES6            | Encontrar el primer elemento que cumple una condición |

**Nota:** 
1. Con `for...of`, puedes acceder al índice usando el método `entries()`, como se muestra a continuación:
```javascript
const array = ['a', 'b', 'c'];
for (const [index, element] of array.entries()) {
  console.log(index, element);
}
````


## MathMax
Regresa el valor más alto 
```javascript
const numbers = [1,2,3,6000,5,5000,7,8,3000] 
Math.max(...numbers)
output: 6000
```

## Splice
Elimina o agrega elementos a un array en el indice indicado

array.splice( startIndex,n°elementos agregados, elemento agregado )

 ```javascript
const animales= ['🐢','🐸','🐷']
animales.splice (1,0,'🦊')
Output:🐢,🦊,🐸,🐷
```






