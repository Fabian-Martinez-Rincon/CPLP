<h1 align="center"> 📝 Practica 7 Sistemas y tipos de Datos</h1>

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

<div align="center">

[Siguiente](/Documentos/Practica6.md)<br>
[Anterior](/Documentos/Practica8.md)

</div>

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

**`Objetivo`** Comprender las nociones fundamentales sobre las diversas propiedades de los sistemas de tipos y los tipos de datos

- [Ejercicio 1 Sistemas de tipos](#ejercicio-1)
- [Ejercicio 2 Tipos de datos](#ejercicio-2)
- [Ejercicio 3 Tipos compuestos](#ejercicio-3)
- [Ejercicio 4 Mutabilidad/Inmutabilidad](#ejercicio-4)
- [Ejercicio 5 Manejo de punteros](#ejercicio-5)
- [Ejercicio 6 TAD](#ejercicio-6)

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 1 Sistemas de tipos

#### ¿Qué es un sistema de tipos y cuál es su principal función?

---

#### b) Definir y contrastar las definiciones de un sistema de tipos fuerte y débil (probablemente en la bibliografía se encuentren dos definiciones posibles. Volcar ambas en l respuesta). Ejemplificar con al menos 2 lenguajes para cada uno de ellos y justificar.

---

#### a) Además de la clasificación anterior, también es posible caracterizar el tipado como estático o dinámico. ¿Qué significa esto? Ejemplificar con al menos 2 lenguajes para cada uno de ellos y justificar.


<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 2: Tipos de datos

#### a) Dar una definición de tipo de dato.

---

#### b) ¿Qué es un tipo predefinido elemental? Dar ejemplos.

---

#### c) ¿Qué es un tipo definido por el usuario? Dar ejemplos.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

#### 1. Dar una breve definición de: producto cartesiano (en la bibliografía puede aparecer también como product type), correspondencia finita, uniones (en la bibliografía puede aparecer también como sum type) y tipos recursivos.


#### 2. Identificar a qué clase de tipo de datos pertenecen los siguientes extractos de código. En algunos casos puede corresponder más de una

<table>
<tr><td>Java</td><td>C</td> <td>C</td></tr>
<tr><td>

```java
class Persona {
  String nombre;
  String apellido;
  int edad;
}
```
</td><td>

```C
typedef struct _nodoLista {
  void *dato;
  struct _nodoLista *siguiente
} nodoLista;
typedef struct _lista {
  int cantidad;
  nodoLista *primero
} Lista;
```
</td> <td>

```C
union codigo {
  int numero;
  char id;
};
```
</td></tr>
<tr><td>Ruby</td><td>PHP</td> <td>Python</td></tr>
<tr><td>

```Ruby
hash = {
  uno: 1,
  dos: 2,
  tres: 3,
  cuatro: 4
}
```
</td><td>

```php
function doble($x) {
  return 2 * $x;
}
```
</td> <td>

```python
tuple = (
  'physics',
  'chemistry', 
  1997, 2000
  )
```
</td></tr>
<tr><td>Hashell</td><td>Hashell</td> <td></td></tr>
<tr><td>

```Haskell
data ArbolBinarioInt =
Nil |
Nodo int
(ArbolBinarioInt dato)
(ArbolBinarioInt dato)
```

Ayuda para interpretar:
‘ArbolBinarioInt’ es un
tipo de dato que puede ser
Nil (“vacío”) o un Nodo con
un dato número entero (int)
junto a un árbol como hijo
izquierdo y otro árbol como
hijo derech

</td><td>Hashell</td> <td></td></tr>
</table>