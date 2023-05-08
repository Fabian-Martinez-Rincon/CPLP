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

## BNF Para la Practica

- [Pagina para testear](https://bnfplayground.pauliankline.com/)
- [Pagina para EBNF](https://planetcalc.com/6385/)

En la gramática de Backus-Naur Form (BNF) se utilizan diferentes símbolos para representar elementos gramaticales y construcciones sintácticas. Aquí te presento los símbolos más comunes utilizados en la notación BNF:

- `::=` se utiliza para indicar la definición de una regla de producción.
- `|` se utiliza para separar opciones dentro de una misma regla de producción.
- `< >` se utilizan para indicar no terminales (símbolos no léxicos o variables).
- `" "` o `' '` se utilizan para indicar literales o símbolos terminales (símbolos léxicos o constantes).
- `[...]` se utiliza para indicar que un elemento es opcional.
- `{...}` se utiliza para indicar que un elemento se puede repetir cero o más veces.
- `(...)` se utiliza para agrupar elementos.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 1**
![Ejercicio1](https://user-images.githubusercontent.com/55964635/233866278-933fe5c8-8af3-4bb0-a21a-6c9208b3284e.jpg)

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 2**

¿Cuál es la importancia de la sintaxis para un lenguaje? ¿Cuáles son sus elementos?

Conjunto de reglas que definen como componer letras, dígitos y otros caracteres para formar los programas

Por ejemplo

<table>
<tr> <td>Ejemplo en pascal</td>
  <td>

```pas
v: array [1..10] of integer;
```

  </td>
</tr>
<tr><td>Ejemplo en C</td>
  <td>

```c
int v[10];
```

  </td>
</tr>
</table>

---

### Características de la sintáxis

- La sintáxis debe ayudar al programador a escribir programas correctos sintácticamente
- La sintáxis establecen reglas que sirven para que el programador se comunique con el procesador 
- La  sintáxis debe contemplar soluciones a caracterísitcas tales como:
  - Legibilidad
  - Verificabilidad
  - Traducción
  - Falta de ambigüedad

La sintáxis establece reglas que definen cómo deben combinarse las componentes básicas, llamadas **`“word”`**, para formar sentencias y programas.

---

### Elementos de la sintáxis

- Alfabeto o conjunto de caracteres
- Identificadores
- Operadores
- Palabra clave y palabra reservada
- Comentarios y uso de blancos

Detallados

- **`Identificadores`** Elección más ampliamente utilizada: Cadena de letras y dígitos, que deben comenzar con una letra. Si se restringe la longitud se pierde legibilidad
- **`Operadores`** Con los operadores de suma, resta, etc. la mayoría de los lenguajes utilizan +, -. En los otros operadores no hay tanta uniformidad (**|^)
- **`Comentarios`** Hacen los programas más legibles
- **`Palabra clave y palabra reservada`** Palabra clave o keywords, son palabras claves que tienen un significado dentro de un contexto. Palabra reservada, son palabras claves que además no pueden ser usadas por el programador como identificador de otra entidad.

**Ventajas de su uso:**

- Permiten al compilador y al programador expresarse claramente
- Hacen los programas más legibles y permiten una rápida traducción

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 3**

¿Explique a qué se denomina regla lexicográfica y regla sintáctica?

Las reglas léxicas y sintácticas le dan la apariencia externa al lenguaje, establecen reglas para la estructura de la sintaxis. La estructura de la sintaxis se compone de:

- `Words` Vocabulario o words es el conjunto de palabras y caracteres necesarios para construir expresiones, sentencias y programas. 
  - Por ejemplo: identificadores, operadores, palabras clave, etc. Las words no son elementales, se construyen a partir del alfabeto.
- `Expresiones` No son más que funciones a partir de un conjunto de datos que devuelven un valor, son bloques sintácticos.
- `Sentencias` Es el componente más importante. Tiene un fuerte impacto en la escritura y legibilidad. Hay sentencias simples, estructuradas y anidadas.
- Las reglas de la estructura son:
  - `Reglas léxicas`: Conjunto de reglas para formar las word, a partir de caracteres del alfabeto. Por ejemplo: diferencias entre mayúsculas y minúsculas, símbolos distintos, etc.
  - `Reglas sintácticas`: Conjunto de reglas que definen cómo formar las expresiones y sentencias. Por ejemplo: cuando se escriba la sentencia if se debe escribir la palabra if, luego la condición, luego el then, el begin, la sentencia, etc.

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

```ebnf
G = ( N, T, S, P)
N = {<numero_entero>, <digito> }
T = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9}
S = <numero_entero>
P = {
    <numero_entero>::=<digito><numero_entero> | <numero_entero><digito> | <digito>
    <digito> ::= 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9
}
```

[Compilado](https://bnfplayground.pauliankline.com/?bnf=%3Cnumero_entero%3E%20%20%20%20%3A%3A%3D%20%3Cdigito%3E%20%3Cnumero_entero%3E%20%7C%20%3Cdigito%3E%20%7C%20%3Cnumero_entero%3E%20%3Cdigito%3E%0A%3Cdigito%3E%20%20%20%20%20%3A%3A%3D%20%220%22%20%7C%20%221%22%20%7C%20%222%22%20%7C%20%223%22%20%7C%20%224%22%20%7C%20%225%22%20%7C%20%226%22%20%7C%20%227%22%20%7C%20%228%22%20%7C%20%229%22%0A&name=Ejercicio%20Fabo)

```ebnf
<numero_entero> ::= <digito> <numero_entero> | <digito> | <numero_entero> <digito>
<digito> ::= "0" | "1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9"
```

- `a)` Identifique las componentes de la misma
  - `G` Gramática, son reglas finitas que definen un conjunto infinito de posibles sentencias válidas en el lenguaje. Está formada por una 4-tupla.
  - `N` conjunto de símbolos no terminales, que en este caso son `<numero_entero>` y `<digito>`.
  - `T` conjunto de símbolos terminales, que son los dígitos del 0 al 9.
  - `S` símbolo inicial, que es `<numero_entero>`.
  - `P` conjunto de producciones, que definen cómo se generan las cadenas válidas en el lenguaje. En este caso, hay dos producciones para `<numero_entero>` y una para `<digito>`. Las producciones indican que un `<numero_entero>` puede ser generado concatenando un `<digito>` y otro `<numero_entero>`, o bien concatenando un `<numero_entero>` y un `<digito>`, o bien siendo simplemente un `<digito>`. La producción para `<digito>` indica que un `<digito>` puede ser cualquiera de los dígitos del 0 al 9.
- `b)` Indique porqué es ambigua y corríjala

La gramática es ambigua porque una misma cadena puede ser generada por más de un árbol de derivación. Por ejemplo, la cadena "123" puede ser generada de dos formas diferentes:

- **<numero_entero>** → 
    - \<digito> <numero_entero> → 
    - 1 <numero_entero> →
    - 1 \<digito> <numero_entero> → 
    - 1 2 <numero_entero> → 
    - 1 2 3
- **<numero_entero>** → 
    - <numero_entero> \<digito> 
    - → 12 \<digito> 
    - → 1 2 3

Para corregir la ambigüedad, se puede modificar la gramática de varias formas posibles. Aquí se presenta una opción:

```ebnf
G = (N, T, S, P)
N = {<numero_entero>, <digito>}
T = {0...9}
S = <numero_entero>
P = {
    <numero_entero> ::= <digito> <numero_entero>
    <digito> ::= 0 | ... | 9
}
```



La principal diferencia es que se ha introducido un nuevo símbolo no terminal \<resto_numero>, que se encargará de generar los dígitos restantes después del primer dígito. Además, se ha modificado la producción de \<numero_entero> para que sea la concatenación de un \<digito> y un \<resto_numero>, y se ha añadido una nueva producción para \<resto_numero> que indica que puede ser la concatenación de un \<digito> y otro \<resto_numero>, o bien ser la cadena vacía ε.

Con esta modificación, la gramática ya no es ambigua, ya que cada cadena generada solo tiene un árbol de derivación posible.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 6**

Defina en BNF (Gramática de contexto libre desarrollada por Backus- Naur) la gramática para la definición de una palabra cualquiera.

```ebnf
G = (N, T, S, P)
N = {
  <palabra>,
  <caracter>
}
T = {0...9, a...z, A...Z}
S = <palabra>
P = {
  <palabra> ::= <letra> | <letra><palabra>
  <letra> ::= a | ... | z | a | ... | Z | " "
}
```

![](2023-05-07-23-27-08.png)

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 7**

Defina en EBNF la gramática para la definición de números reales. Inténtelo
desarrollar para BNF y explique las diferencias con la utilización de la gramática EBNF.

<table><tr><td>EBNF 854</td><td>BNF 21.5</td></tr><tr><td>

```ebnf
G = (N, T, S, P)
N = {<real>, <numero>, <digito>}
T = {0...9, ., +, -}
S = <real>
P = {
  <real> ::= ["-"] <numero> ["." <numero>]
  <numero> ::= {<digito>}+
  <digito> ::= 0 | ... | 9
}
```
</td><td>

```ebnf
G = (N, T, S, P)
N = {<real>, <numero>, <digito>}
T = {0...9, ., -}
S = <real>
P = {
	<real> ::=
    <numero>                |
    <numero> "." <numero>   | 
    - <numero>              |
    - <numero> "." <numero> 
	<numero> ::=  <digito> | <digito><numero>
	<digito> ::= 0 | ... | 9
}
```
</td></tr><tr>
<td>

![image](https://user-images.githubusercontent.com/55964635/234172176-1244c2b6-3fab-41a1-aee2-425285c838ea.png)
</td>

<td>



![image](https://user-images.githubusercontent.com/55964635/234171988-5af1f557-927e-42fd-8f98-e99fe539d718.png)
</td></tr></table>


![](2023-05-07-23-28-01.png)

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 8**

Utilizando la gramática que desarrolló en los puntos 6 y 7, escriba el árbol sintáctico
de:

| Conceptos | Programación |
| --- | --- |
| ![Conceptos](https://user-images.githubusercontent.com/55964635/233899650-b270136e-87ae-499c-9729-8ae1b38ed11e.jpg) | ![Programacion](https://user-images.githubusercontent.com/55964635/233901701-d7b44a37-fda8-4ce9-8810-bed09383c114.jpg) |
| 1255869 | 854,26 Esta corregido arriba (en el 7) |
| ![image](https://user-images.githubusercontent.com/55964635/233906831-18fb1f5d-0dec-4e71-899b-98c5f1067728.png) | ![image](https://user-images.githubusercontent.com/55964635/233906881-9d617c98-d469-4e03-8b33-b1fdb24f0579.png) |

![](/Practica/Practica2/8.jpg)
![](/Practica/Practica2/82.jpg)

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 9**

Defina utilizando diagramas sintácticos la gramática para la definición de un identificador de un lenguaje de programación. Tenga presente como regla que un identificador no puede comenzar con números.

<table><td>



```ebnf
G = ( N, T, S, P)
N = {<real>, <letra>}
T = {0..9, A..Z, a..z}
S = <real>
P = {
    <identificador> ::= <letra> {<caracter>}*
    <caracter> ::= (<letra> | <digito>)
    <letra> ::= (a | ... | z | A | ... | Z)
    <digito> ::= (0 | ... | 9)
}
```
</td><td>

Cambia los cuadrados de los terminales por circulos

![6](https://user-images.githubusercontent.com/55964635/233878007-0360094b-d320-44d3-9d92-d43fdda52bb1.jpg)
</td>
</table>





<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 10**

<table><tr><td>

`a)` Defina con EBNF la gramática para una expresión numérica, dónde intervienen variables y números. Considerar los operadores +, -, * y / sin orden de prioridad. No considerar el uso de paréntesis.
</td><td>

`b)` A la gramática definida en el ejercicio anterior agregarle prioridad de operadores.
</td></tr>

<tr><td>


```ebnf
G = ( N, T, S, P)
N = {
  <elemento>, 
  <identificador>, 
  <caracter>, 
  <numero>, 
  <digito>, 
  <letra>, 
}
T = {0-9, a-Z, +, -, *, /}
S = <operacion>
P = {
  <expresion> ::= <elemento> {<termino>}+
  <termino> ::= {(* | / | + | -)<elemento>}


  <elemento> ::= (<identificador> | <numero>)
  <identificador> ::= <letra>{<caracter>}*
  <caracter> ::= <digito> | <letra>
  <numero> ::= {<digito>}+
  <digito> ::= 0 | ... | 9
  <letra> ::= a | ... | z | A | ... Z
}
```
</td><td>

```ebnf
G = ( N, T, S, P)
N = {
  <expresion>,
  <operacion>,
  <sumaResta>,
  <multiplicacionDivision>,
  <elemento>,
  <identificador>,
  <caracter>,
  <numero>,
  <digito>,
  <letra>
}
T = {0..9, a,z, A..Z, "+", "-", "*", "/"}
S = <operacion>
P = {
  <expresion> ::= <operacion> {<sumaResta>}*
  <operacion> ::= <elemento><multiplicacionDivision> | <elemento>
  <sumaResta> ::= ("+" | "-")<operacion>
  <multiplicacionDivision> ::= ("*" | "/")<elemento>


  <elemento> ::= (<identificador> | <numero>)
  <identificador> ::= <letra>{<caracter>}*
  <caracter> ::= <digito> | <letra>
  <numero> ::= {<digito>}+
  <digito> ::= 0 | ... | 9
  <letra> ::= a | ... | z | A | ... Z
}
```
</td></tr></table>


`c)` Describa con sus palabras los pasos y decisiones que tomó para agregarle prioridad de operadores al ejercicio anterior. 
Lo primero que hacemos es determinar las multiplicaciones y divisiones del programa y dejo las sumas para el final.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 11**

La siguiente gramática intenta describir sintácticamente la sentencia for de ADA, indique cuál/cuáles son los errores justificando la respuesta

```ebnf
N= {
    <sentencia_for>, 
    <bloque>, <variable>, 
    <letra>, 
    <cadena>, 
    <digito>, 
    <otro>, 
    <operacion>,
    <llamada_a_funcion>, 
    <numero>, 
     <sentencia> 
}

P= { 
    <sentencia_for>::= for (i= IN 1..10) loop <bloque> end loop;
    <variable>::= <letra> | <cadena>
    <cadena>::= { ( <letra> | <digito> | <otro> ) }+
    <letra>::=( a | .. | z | A | .. | Z )
    <digito>::= ( 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 0 )
    <bloque>::=  <sentencia> | <sentencia> <bloque> | <bloque> <sentencia> ;
    <sentencia>::= <sentencia_asignacion> | <llamada_a_funcion> | <sentencia_if> |
    <sentencia_for> |  <sentencia_while> | <sentencia_switch> 
}
```

Falta definir las siguientes
- <otro>
- <sentencia_asignacion>
- llamada_a_funcion

### **Ejercicio 12**

Realice en EBNF la gramática para la definición un tag div en html 5. (Puede
ayudarse con el siguiente enlace (https://developer.mozilla.org/es/docs/Web/HTML/Elemento/div)

```enbf
<div> ::= 
  "<div>" 
    <bloque> 
  "</div>"
<bloque> ::= [0-9]*
```

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 13**

Defina en EBNF una gramática para la construcción de números primos.¿Qué
debería agregar a la gramática para completar el ejercicio?

No se puede porque tiene nros infinitos

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 14**

Sobre un lenguaje de su preferencia escriba en EBNF la gramática para la definición de funciones o métodos o procedimientos (considere los parámetros en caso de ser necesario)

```ebnf
G = (N, T, S, P)
N = {<funcion>}
T = {a-z, A-Z, 0-9}
S = <funcion>
P = {
  <div> ::= "funcion " <espacio> <identificador> <espacio> "(" <espacio> <parametros>? <espacio> ")" <espacio> 
  <espacio> ::= "\s"*
  <letras> ::= ([a-z] | [A-Z])


  <tipoDato> ::= "int" | "real" | "string"
  <parametros> ::= <parametro> <parametros> | <parametro>
  <parametro> ::= <tipoDato> <espacio> <identificador> ","
  <identificador> ::= <letras> ( ([0-9] | <letras> )*)
}
```

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

