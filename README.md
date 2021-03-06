![Autos](https://images.pexels.com/photos/1280560/pexels-photo-1280560.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940)
# **Arrays**

El objeto Array de JavaScript es un objeto global que es usado en la construcción de arrays, que son objetos tipo lista de alto nivel.

## Tabla de contenidos
1. [Crear un Array](#crear-un-array)
2. [Acceder a un elemento de Array mediante su índice](#acceder-a-un-elemento-de-array-mediante-su-índice)
3. [Recorrer un Array](#recorrer-un-array)
    * [Recorrer un Array (forEach)](#recorrer-un-array (forEach))
    * [Recorrer un Array (map)](#recorrer-un-array-(map))
4. [Añadir un elemento al final de un Array](#añadir-un-elemento-al-final-de-un-array)
5. [Eliminar el ultimo elemento de un Array](#eliminar-el-ultimo-elemento-de-un-array)
6. [Añadir un elemento al principio de un Array](#añadir-un-elemento-al-principio-de-un-array)
7. [Eliminar el primer elemento de un Array](#eliminar-el-primer-elemento-de-un-array)
8. [Encontrar el índice de un elemento del Array](#encontrar-el-índice-de-un-elemento-del-array)
9. [Eliminar un único elemento mediante su posición](#eliminar-un-único-elemento-mediante-su-posición)
10. [Eliminar varios elementos a partir de una posición](#eliminar-varios-elementos-a-partir-de-una-posición)
11. [Copiar un Array](#copiar-un-array)
12. [Longitud de un Array](#longitud-de-un-array)
13. [Filter](#filter)


## **Descripción**

Los arrays son objetos similares a una lista cuyo prototipo proporciona métodos para efectuar operaciones de recorrido y de mutación. Tanto la longitud como el tipo de los elementos de un array son variables. Dado que la longitud de un array puede cambiar en cualquier momento, y los datos se pueden almacenar en ubicaciones no contiguas, no hay garantía de que los arrays de JavaScript sean densos; esto depende de cómo el programador elija usarlos. En general estas características son cómodas, pero si, en su caso particular, no resultan deseables, puede considerar el uso de arrays con tipo.

## **Operaciones básicas habituales**

### **Crear un Array**

```javascript
var nombres = ["Eddy","David"]
```

### **Acceder a un elemento de Array mediante su índice**

```javascript
console.log(nombres[0])
// Eddy
```

### **Recorrer un Array**
---
#### **1. Recorrer un Array (forEach)**
> *__nota:__ El método forEach() ejecuta la función indicada una vez por cada elemento del array.*

```javascript
nombres.forEach((elemento,indice) => {
    console.log(indice, elemento)
})
```

#### **2. Recorrer un Array (map)**
>*__Nota:__ El método map() crea un nuevo array con los resultados de la llamada a la función indicada aplicados a cada uno de sus elementos.*

```javascript
var numeros = [1,2,3,4,5,6,7,8,9,10,11,12]
var tablaDelCinco = numeros.map(element => element * 5)
console.log(tablaDelCinco)
```

### **Añadir un elemento al final de un Array**
---
```javascript
nombres.push("Jose") // Añade "Jose" al final del array.
console.log(nombres)
```

### **Eliminar el ultimo elemento de un Array**
---
```javascript
nombres.pop() // Elimina el ultimo elemento del array, en este caso "Jose"
console.log(nombres)
```

### **Añadir un elemento al principio de un Array**
---
```javascript
nombres.unshift("Leandro") //Agrega "Leandro" al principio del arreglo.
console.log(nombres)
```

### **Eliminar el primer elemento de un Array**
---
```javascript
nombres.shift()
console.log(nombres)
```

### **Encontrar el índice de un elemento del Array**
---

```javascript
var posicion = nombres.indexOf("Eddy"); //Esto retorna un numero, que es la posicion del elemento en el array.
console.log(posicion)
```

### **Eliminar un único elemento mediante su posición**
---
Este metodo utiliza dos parametros, la posición del primer elemento que se elimina y el número de elementos que queremos eliminar.

```javascript
nombres.splice(0,1) // De esta manera estas eliminando el elemento "Eddy" del array 'nombres'.
console.log(nombres)
```
### **Eliminar varios elementos a partir de una posición** 
---

 *Nota: Con .splice() no solo se puede eliminar elementos del array, si no que también podemos extraerlos guardándolo en un nuevo array.* 

 >¡Ojo! que al hacer esto estaríamos modificando el array de origen.

```javascript
var vegetales = ['Repollo', 'Nabo', 'Rábano', 'Zanahoria']
console.log(vegetales)
var elementosEliminados = vegetales.splice(1,2)
console.log(`Elementos eliminados del array: ${elementosEliminados}`)
console.log(`Elementos actuales en el array: ${vegetales}`)
```
### **Copiar un Array**
---
```javascript
nombres.push('Eddy','Jose','Ruperta')
var copiaArray = nombres.slice()
console.log(copiaArray)
```
### **Longitud de un Array**
---
```javascript
var longitud = nombres.length
console.log(longitud) // 4
console.log(nombres[0].length)
```

### **Filter**
---
*El método filter() crea un nuevo array con todos los elementos que cumplan la condición implementada por la función dada.*
```javascript
console.log(numeros)
var menores = numeros.filter(x=>x<5)
console.log(menores,)
```

***Fuentes:***

[![imagen](https://static001.infoq.cn/resource/image/25/fe/2509a9d41e00061cfc6fdb781632dcfe.png)](https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Global_Objects/Array)