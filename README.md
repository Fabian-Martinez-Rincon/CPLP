<div align="center">

[![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/Nomadiix/CPLP)
[![GitHub stars](https://img.shields.io/github/stars/Nomadiix/CPLP)](https://github.com/FabianMartinez1234567/CPLP/stargazers/)
[![GitHub repo size in bytes](https://img.shields.io/github/repo-size/Nomadiix/CPLP)](https://github.com/Nomadiix/CPLP)
 </div>

<h1 align="center"> 🧠 CPLP</h1>
<div align="center">
<img src="https://media.giphy.com/media/3oz8xNkfjM07d7dK0w/giphy.gif"/>
</div>

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

- [TP Integrador](/Documentos/tpIntegrador.md)
- [EBNF](/Documentos/EBNF.md)
- [Teoria](/Documentos/Teoria.md)
- [Practica 1 Teoria](/Documentos/Practica1.md)
- [Practica 2 BNF/EBNF](/Documentos/Practica2.md)
- [Practica 3 Semantica Estatica/Dinamica](/Documentos/Practica3.md)
- [Practica 4 Variables](/Documentos/Practica4.md)
- [Practica 5 Pilas de ejecución (Esta la hice full en papel)](/Documentos/Practica5.md)
- [Practica 6 Parametros](/Documentos/Practica6.md)
- [Practica 7 Sistemas y tipos de Datos](/Documentos/Practica7.md)
- [Practica 8 Excepciones](/Documentos/Practica8.md)
- [Practica 9 Estructuras de control y sentencias](/Documentos/Practica9.md)
- [Resumen Final](/Final%20CPLP/finalResumen.md)

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

# Parcial de Promoción Resumen

---

## Teoria 1 Introducción y Evaluación de Lenguajes

- Simplicidad y Legibilidad
- Claridad en los bindings
- Confiabilidad
- Soporte
- Abstración
- Ortogonalidad
- Eficiencia
- Sintaxis
  - **Abstracta** Se refiere a la estructura
  - **Concreta** Se refiere a la parte léxica
  - **Pragmática** Se refiere al uso práctico
  - BNF, EBNF Y CONWAY
- Semántica

---

## Teoria 2 Semántica

- Semantica Estatica - Gramatica de Atributos
- Semantica Dinamica
  - Formales y Complejas
    - Semantica Axiomatica
    - Semantica denotacional
  - No Formal
    - Semantica Operacional
- Procesamiento de un Programa (Programas Traductores)
  - Interpretación
  - Compilación
  - Interpretación y Compilación

---

## Teoria 3 Semantica Operacional

- Ligadura Estatica
- Ligadura Dinamica
- Variable (Nombre, Alcance, Tipo, L-Valor, R-Valor)
- Sobrecarga

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

# 💻 Resumen Practica 6 Párametros

Ateriormente hicimos la practica de pila estatica y dinamica, ahora le vamos a agregar parametros, que son los siguientes:


<table>
<tr><td>Parametro</td><td>Descripción</td><td>Ejemplo</td></tr>
<tr><td>Valor</td><td>

Trabajamos con una copia del valor recibido 
- x = 3

</td><td>

```ada
procedura rutina(x:integer);
begin
  x = x + 1
end;

a = 3;
rutina(a);
```

</td></tr>
<tr><td>Referencia</td><td>

Trabajamos siempre modificando el valor original
- a <--- x

</td><td>

```ada
procedura rutina(io x:integer);
begin
  x = x + 1
end;

a = 3;
rutina(a);
```

</td></tr>
<tr><td>Nombre</td><td>
Tomamos el contexto completo, y trabajamos con las variables originales al contexto (Hay te estar atentos si las variables se modifican por referencia o si son globales)

- x ↑ r1 [ y + r2 [y] ]

</td><td>

```ada
Procedure main;
y: integer;
r1:array[1..6] of integer;
r2:array[1..5] of integer;

procedura rutina(nombre x:integer);
begin
  x = x + 1
end;

rutina(r1[ y + r2 [y]]);
```

</td></tr>
<tr><td>Valor-Resultado</td><td>

Es igual al pasaje por valor solo que este trabaja con la copia y al final del proceso, retorna el valor modificado a la variable original. (El valor esta en el)
- x(a) = 3 

</td><td>

```ada
procedura rutina(valor-resultado x:integer);
begin
  x = x + 1
end;
a = 3;
rutina(a); //VR = 4
```

</td></tr>
</table>

### Datos a tener en cuenta

- El arbol de anidamiento simplemente para saber que función esta contenida en otra, no es necesario para la practica.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">


# 👾 Resumen Practica 7 Tipos de Datos

### Tipos de datos compuestos

<details > <summary> <b> Producto cartesiano </b> </summary> 

Es un **conjunto cuyos elementos están ordenados n-tupla**, es decir, es una construcción en teoría de conjuntos y programación que combina dos conjuntos o tipos de datos para formar un nuevo conjunto o tipo cuyos elementos contienen una combinación de elementos de ambos conjuntos. En programación, esto puede representarse mediante una estructura de datos que contiene múltiples campos o propiedades**.** Por ejemplo, los registros. Es una relación 1 a muchos

#### Producto Cartesiano

<table> <td>

```python
tuple = (
  'physics',
  'chemistry', 
  1997, 2000
  )
```
</td><td>

```java
class Persona {
  String nombre;
  String apellido;
  int edad;
}
```
</td></table>



#### Producta Cartesiano y Recursión


<table> <td>

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
</td><td>

```Haskell
data ArbolBinarioInt =
Nil |
Nodo int
(ArbolBinarioInt dato)
(ArbolBinarioInt dato)
```
</td></table>

</details>
<details> <summary> <b> Correspondencia Finita </b> </summary>

La correspondencia finita se refiere a una relación uno a uno entre los elementos de dos conjuntos finitos. Para cada elemento en el primer conjunto, hay exactamente un elemento correspondiente en el segundo conjunto, y viceversa. Esta correspondencia puede ser representada mediante una función que asigna cada elemento del primer conjunto a un único elemento del segundo conjunto. El tipo de dato serían los arreglos.

<table> <td>

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
</td></table>


</details>
<details> <summary> <b> Uniones </b> </summary>

Las uniones, también conocidas como sum type o tipo suma, son una construcción en programación que permite combinar varios tipos de datos en uno solo. En una unión, un valor puede pertenecer a uno de los tipos dentro de la unión. Esto se puede utilizar para representar alternativas o opciones donde un valor puede ser de diferentes tipos.



<table> <td>

```C
union codigo {
  int numero;
  char id;
};
```
</td><td>

```Haskell
data Color =
  Rojo |
  Verde |
  Azul
```

</td></table>





</details>
<details> <summary> <b> Tipos Recursivos </b> </summary> 

Los tipos recursivos son aquellos que se definen en términos de sí mismos. Esto significa que un tipo puede contener instancias de sí mismo como parte de su estructura. Los tipos recursivos son útiles para modelar estructuras de datos que contienen referencias a sí mismas, como árboles o listas enlazadas. Esta recursividad permite
la construcción de estructuras de datos complejas y anidadas.

#### Producto Cartesiano y Recursión

<table> <td>

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
</td><td>

```Haskell
data ArbolBinarioInt =
Nil |
Nodo int
(ArbolBinarioInt dato)
(ArbolBinarioInt dato)
```

</td></table>

</details>

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">


# 🤖 Resumen Practica 8 Excepciones

En pascal y en PL1 no tenemos un manejo de excepciones muy complejo. En cuanto a la estuctura, es parecido a pascal.

#### Diferencias entre un lenguaje y otro

| Pascal | PL/1 |
| ------ | ---- |
| var x:int | DCL x Integer; |
| procedure | Proc |
| procedure Manejador1 begin x:=x + 1; end; | ON CONDITION Manejador1 BEGIN x = x + 1; END; |


<details> <summary> <b> Ejemplo Completo </b> </summary> 

<table><tr><td>Pascal</td><td>PL/1</td></tr>
<tr><td>

```pascal
Program Principal;
var x:int; b1,b2:boolean;

Procedure P (b1:boolean);
  var x:int;
  Procedure Manejador1
  begin
    x:=x + 1;
  end;
begin
  x:=1;
  if b1=true then Manejador1;
  x:=x+4;
end;

Procedure Manejador2;
begin
  x:=x * 100;
end;

Begin
  x:=4;
  b2:=true;
  b1:=false;
  if b1=false then Manejador2;
  P(b);
  write (x);
End
```
</td><td>

```PL/1
Prog Principal;
  DCL x Integer;
  DCL b1,b2 Boolean;
PROC P (b1 Boolean);
  DCL x Integer;
BEGIN
  ON CONDITION Manejador1 BEGIN x = x + 1; END;
  X = 1;
  IF b1=true THEN SIGNAL CONDITION Manejador1
  x = x + 4;
END;
BEGIN
  ON CONDITION Manejador2 BEGIN x = x * 100; END;
  X = 4;
  b2 = true;
  b1 = false;
  IF b1=false THEN SIGNAL CONDITION Manejador2
  P(b1);
  WRITE (x);
END.
```

</td></tr></table>

</details>

### Parcial de [@Guadev](https://github.com/guadaevequoz)

![2](https://github.com/Fabian-Martinez-Rincon/Fabian-Martinez-Rincon/assets/55964635/fbd524bf-d6b7-41c5-9d78-31534791b5aa)
![3](https://github.com/Fabian-Martinez-Rincon/Fabian-Martinez-Rincon/assets/55964635/acea487b-d0a4-41fb-8637-674a62d07055)

### Ejercicio 3a)

En el main se entra a la primera iteración del for dentro del try siendo **i=1**, entra al if, imprime **`1`** y llama al metodo **`rethrow`**. El método evalua en el try y entra al primer if, ya que se envio con el parametro **`primer`** y Lanza la excepción **`firstException`**. Termina el try y la excepción es manejada por el cath del primer try dele método y tira una excepción **`ThirdException`** y se imprime "tercerException" y termina el programa.

Por lo que la opción válida es la 

>1) Imprime "1", luego "Tercer Exception" y termina el programa.

### Ejercicio 3b)

Si se pusiera todo en el bloque try/cath dentro del for, los resultados serian diferentes, ya que el for podria continuar ejecutandose haya sido manejada una excepción o no dentro de su bloque. El resultado final de la impresion seria

> "1", "Tercera Excepción", "2", "Tercer Excepción", "3", "Tercer Excepción"

- Salta la excepción **first Exceptión** y se maneja dentro del **rethrow** en el segundo **cath** y en el **cath** del for donde imprime.
- Salta la excepción **second Exception** y se maneja dentro del **rethrow** en el primer **cath** y en el **cath** del for donde imprime.
- Salta la excepción **third Exception** y como no se puede manejar en **rethrow** es directamente manejada en el main, en el for.




