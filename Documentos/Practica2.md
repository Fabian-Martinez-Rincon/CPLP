<h1 align="center"> 📓 Practica 2
</h1>

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

<div align="center">

[Siguiente](/Documentos/Practica3.md)<br>
[Anterior](/Documentos/Practica1.md)

</div>

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

Objetivo: conocer como se define léxicamente un lenguaje de programación y cuales son las
herramientas necesarias para hacerlo

- [Ejercicio 1 Complete el siguiente cuadro](#ejercicio-1)
- [Ejercicio 2 ¿Cuál es la importancia de la sintaxis para un lenguaje?](#ejercicio-2)
- [Ejercicio 3 ¿Explique a qué se denomina regla lexicográfica y regla sintáctica?](#ejercicio-3)
- [Ejercicio 4 ¿En la definición de un lenguaje, a qué se llama palabra reservadas?](#ejercicio-4)
- [Ejercicio 5 Dada la siguiente gramática escrita en BNF](#ejercicio-5)
- [Ejercicio 6 Defina en BNF](#ejercicio-6)
- [Ejercicio 7 Defina en EBNF la gramática para la definición de números reales](#ejercicio-7)
- [Ejercicio 8 Utilizando la gramática que desarrolló en los puntos 6 y 7](#ejercicio-8)
- [Ejercicio 9 Defina utilizando diagramas sintácticos la gramática para la definición](#ejercicio-9)
- [Ejercicio 10 ](#ejercicio-10)
- [Ejercicio 11 : La siguiente gramática intenta describir sintácticamente la sentencia for de ADA](#ejercicio-11)
- [Ejercicio 12 Realice en EBNF la gramática para la definición un tag div en html 5](#ejercicio-12)
- [Ejercicio 13 Defina en EBNF una gramática para la construcción de números primos](#ejercicio-13)
- [Ejercicio 14 Sobre un lenguaje de su preferencia escriba en EBNF la gramática para la definición](#ejercicio-14)

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 1**
Aca va el cuadro de la fotocopia

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 2**

¿Cuál es la importancia de la sintaxis para un lenguaje? ¿Cuáles son sus elementos?

La sintaxis es fundamental en cualquier lenguaje de programación ya que es la que permite definir las reglas y estructuras para escribir el código fuente de manera clara, concisa y coherente. La sintaxis es esencial para que el programa pueda ser interpretado y ejecutado correctamente por la máquina, ya que esta solo entiende un conjunto específico de instrucciones bien definidas. La sintaxis también ayuda a que el código sea más fácil de leer y entender por otros programadores.

#### Los elementos de la sintaxis en un lenguaje de programación incluyen:

- **`Palabras reservadas:`** <br> son las palabras que tienen un significado especial en el lenguaje y que no pueden ser utilizadas como nombres de variables o funciones. Por ejemplo, en JavaScript, las palabras reservadas son if, else, for, while, function, etc.
- **`Identificadores:`** <br> son los nombres de variables, funciones, objetos, clases, etc. Los identificadores deben seguir ciertas reglas de nomenclatura, como no contener espacios, comenzar con una letra o un guión bajo, etc.
- **`Operadores:`** <br> son los símbolos que representan operaciones matemáticas, lógicas, de comparación, etc. Por ejemplo, en JavaScript, los operadores incluyen +, -, *, /, &&, ||, >, <, etc.
- **`Delimitadores:`** <br> son los símbolos que se utilizan para separar o agrupar elementos en el código. Por ejemplo, en JavaScript, los delimitadores incluyen (), {}, [], ;, etc.
- Literales: son los valores constantes que aparecen directamente en el código fuente. Por ejemplo, en JavaScript, los literales pueden ser números, cadenas de texto, booleanos, objetos, etc.
- **`Comentarios:`** <br> son los textos que se utilizan para explicar el código o hacer anotaciones para otros programadores. Los comentarios no son interpretados por la máquina y no afectan el funcionamiento del programa.

En resumen, la sintaxis es crucial para cualquier lenguaje de programación, ya que define las reglas y estructuras para escribir código legible y coherente. Sin una sintaxis bien definida, el código sería difícil de interpretar y ejecutar por la máquina, y sería difícil de entender para otros programadores.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 3**

¿Explique a qué se denomina regla lexicográfica y regla sintáctica?

Las reglas lexicográficas y sintácticas son fundamentales en la definición y construcción de lenguajes formales, incluyendo los lenguajes de programación. Las reglas lexicográficas definen cómo se deben estructurar y utilizar los elementos léxicos de un lenguaje, mientras que las reglas sintácticas definen cómo se deben estructurar y utilizar los elementos sintácticos del lenguaje. Ambas reglas son esenciales para garantizar que los programas escritos en un lenguaje formal sean interpretados y ejecutados correctamente.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 4**

¿En la definición de un lenguaje, a qué se llama palabra reservadas? ¿A qué son
equivalentes en la definición de una gramática? De un ejemplo de palabra reservada en el lenguaje que más conoce. (Ada,C,Ruby,Python,..)

En la definición de un lenguaje, se llama palabras reservadas a aquellas palabras que tienen un significado especial y están reservadas para su uso por parte del lenguaje en sí mismo. Estas palabras no pueden ser utilizadas como identificadores o nombres de variables en el código del programa.

En la definición de una gramática, las palabras reservadas son equivalentes a los símbolos no terminales o las producciones que representan las estructuras sintácticas especiales del lenguaje.

En el lenguaje de programación Python, algunas palabras reservadas incluyen:

- **`if:`** se utiliza para declarar una condición que debe cumplirse para que se ejecute un bloque de código.
- **`else:`** se utiliza para declarar un bloque de código que se ejecutará si la condición del if no se cumple.
- **`while:`** se utiliza para declarar un bucle que se ejecutará mientras se cumpla una condición.
- **`for:`** se utiliza para declarar un bucle que se ejecutará un número determinado de veces.
- **`def:`** se utiliza para declarar una función en Python.
- **`class:`** se utiliza para declarar una clase en Python.

Estas palabras reservadas tienen un significado especial en Python y no pueden ser utilizadas como nombres de variables o funciones en el código.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 5**

Dada la siguiente gramática escrita en BNF:

```BNF
G= ( N, T, S, P)
N = {<numero_entero>, <digito> }
T = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9}
S = <numero_entero>
P = {
<numero_entero>::=<digito><numero_entero> | <numero_entero><digito> | <digito>
<digito> ::= 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9
}
```

- `a)` Identifique las componentes de la misma
- `b)` Indique porqué es ambigua y corríjala


<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 6**

Defina en BNF (Gramática de contexto libre desarrollada por Backus- Naur) la
gramática para la definición de una palabra cualquiera.


<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 7**

Defina en EBNF la gramática para la definición de números reales. Inténtelo
desarrollar para BNF y explique las diferencias con la utilización de la gramática EBNF.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 8**

Utilizando la gramática que desarrolló en los puntos 6 y 7, escriba el árbol sintáctico
de:

- `a)` Conceptos
- `b)` Programación
- `c)` 1255869
- `d)` 854,26
- `e)` Conceptos de lenguajes


<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 9**

Defina utilizando diagramas sintácticos la gramática para la definición de un
identificador de un lenguaje de programación. Tenga presente como regla que un identificador no puede comenzar con números.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 10**

- `a)` Defina con EBNF la gramática para una expresión numérica, dónde intervienen variables y números. Considerar los operadores +, -, * y / sin orden de prioridad. No considerar el uso de paréntesis.
- `b)` A la gramática definida en el ejercicio anterior agregarle prioridad de operadores.
- `c)` Describa con sus palabras los pasos y decisiones que tomó para agregarle prioridad de operadores al ejercicio anterior.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 11**

La siguiente gramática intenta describir sintácticamente la sentencia for de ADA, indique cuál/cuáles son los errores justificando la respuesta

```BNF
N= {<sentencia_for>,  <bloque>, <variable>, <letra>, <cadena>, <digito>, <otro>, <operacion>,
<llamada_a_funcion>, <numero>,  <sentencia> }
P= { <sentencia_for>::= for (i= IN 1..10) loop <bloque> end loop;
<variable>::= <letra> | <cadena>
<cadena>::= { ( <letra> | <digito> | <otro> ) }+
<letra>::=( a | .. | z | A | .. | Z )
<digito>::= ( 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 0 )
<bloque>::=  <sentencia> | <sentencia> <bloque> | <bloque> <sentencia> ;
<sentencia>::= <sentencia_asignacion> | <llamada_a_funcion> | <sentencia_if> |
<sentencia_for> |  <sentencia_while> | <sentencia_switch> }
```


<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">


### **Ejercicio 12**

Realice en EBNF la gramática para la definición un tag div en html 5. (Puede
ayudarse con el siguiente enlace (https://developer.mozilla.org/es/docs/Web/HTML/Elemento/div)

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 13**

Defina en EBNF una gramática para la construcción de números primos.¿Qué
debería agregar a la gramática para completar el ejercicio?

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 14**

Sobre un lenguaje de su preferencia escriba en EBNF la gramática para la definición de funciones o métodos o procedimientos (considere los parámetros en caso de ser necesario)


<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">



























