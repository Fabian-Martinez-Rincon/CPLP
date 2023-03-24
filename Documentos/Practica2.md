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
    - `N:` conjunto de símbolos no terminales, que en este caso son `<numero_entero>` y `<digito>`.
    - `T:` conjunto de símbolos terminales, que son los dígitos del 0 al 9.
    - `S:` símbolo inicial, que es `<numero_entero>`.
    - `P:` conjunto de producciones, que definen cómo se generan las cadenas válidas en el lenguaje. En este caso, hay dos producciones para `<numero_entero>` y una para `<digito>`. Las producciones indican que un `<numero_entero>` puede ser generado concatenando un `<digito>` y otro `<numero_entero>`, o bien concatenando un `<numero_entero>` y un `<digito>`, o bien siendo simplemente un `<digito>`. La producción para `<digito>` indica que un `<digito>` puede ser cualquiera de los dígitos del 0 al 9.
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
N = {<numero_entero>, <digito>, <resto_numero>}
T = {0, 1, 2, 3, 4, 5, 6, 7, 8, 9}
S = <numero_entero>
P = {
    <numero_entero> ::= <digito> <resto_numero>
    <resto_numero> ::= <digito> <resto_numero> | " "
    <digito> ::= "0" | "1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9"
}
```

[Compilado](https://bnfplayground.pauliankline.com/?bnf=%3Cnumero_entero%3E%20%3A%3A%3D%20%3Cdigito%3E%20%3Cresto_numero%3E%0A%3Cresto_numero%3E%20%3A%3A%3D%20%3Cdigito%3E%20%3Cresto_numero%3E%20%7C%20%22%20%22%0A%3Cdigito%3E%20%3A%3A%3D%20%220%22%20%7C%20%221%22%20%7C%20%222%22%20%7C%20%223%22%20%7C%20%224%22%20%7C%20%225%22%20%7C%20%226%22%20%7C%20%227%22%20%7C%20%228%22%20%7C%20%229%22&name=Resto)

```ebnf
<numero_entero> ::= <digito> <resto_numero>
<resto_numero> ::= <digito> <resto_numero> | " "
<digito> ::= "0" | "1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9"
```

La principal diferencia es que se ha introducido un nuevo símbolo no terminal <resto_numero>, que se encargará de generar los dígitos restantes después del primer dígito. Además, se ha modificado la producción de <numero_entero> para que sea la concatenación de un \<digito> y un <resto_numero>, y se ha añadido una nueva producción para <resto_numero> que indica que puede ser la concatenación de un \<digito> y otro <resto_numero>, o bien ser la cadena vacía ε.

Con esta modificación, la gramática ya no es ambigua, ya que cada cadena generada solo tiene un árbol de derivación posible.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 6**

Defina en BNF (Gramática de contexto libre desarrollada por Backus- Naur) la gramática para la definición de una palabra cualquiera.

```ebnf
<text> ::= <character> <text> | <character>
<character> ::= <letter> | <digit>
<letter> ::= "A" | "B" | "C" | "D" | "E" | "F" | "G" | "H" | "I" | "J" | "K" | "L" | "M" | "N" | "O" | "P" | "Q" | "R" | "S" | "T" | "U" | "V" | "W" | "X" | "Y" | "Z" | "a" | "b" | "c" | "d" | "e" | "f" | "g" | "h" | "i" | "j" | "k" | "l" | "m" | "n" | "o" | "p" | "q" | "r" | "s" | "t" | "u" | "v" | "w" | "x" | "y" | "z"
<digit> ::= "0" | "1" | "2" | "3" | "4" | "5" | "6" | "7" | "8" | "9"
```

O tambien

```ebnf
<texto> ::= <letra> <texto> | <caracter>
<letra> ::= [A-Z] | [a-z]
```

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 7**

Defina en EBNF la gramática para la definición de números reales. Inténtelo
desarrollar para BNF y explique las diferencias con la utilización de la gramática EBNF.

```ebnf
<real> ::= ([0-9] [0-9]*) ("." [0-9]+ )?
```

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 8**

Utilizando la gramática que desarrolló en los puntos 6 y 7, escriba el árbol sintáctico
de:

#### `a)` Conceptos

#### `b)` Programación

#### `c)` 1255869
```
                        <real>
                            |
                    +------+------+
                    |             |
                [0-9]+       ("." [0-9]+)?
                    |                |
                    1              null
                    |                 
                +--+--+
                |     |
                [0-9]+  |
                |     |
                2    +--+--+
                    |     |
                    [0-9]+  |
                    |     |
                    5    +--+--+
                            |     |
                        [0-9]+  |
                            |     |
                            5     |
                                |
                                +--+--+
                                |     |
                            [0-9]+  |
                                |     |
                                8     |
                                    |
                                    +--+--+
                                    |     |
                                [0-9]+  |
                                    |     |
                                    6     |
                                        |
                                        +--+--+
                                        |     |
                                    [0-9]+  |
                                        |     |
                                        9     |
```

En este árbol, cada nodo interno representa una regla de la gramática, y los nodos hoja representan los valores reales. Aquí, el valor real es 1255869, que se compone de seis dígitos enteros. Entonces, la regla `<real>` se satisface simplemente tomando `[0-9]+` como la primera parte de la regla, y la segunda parte opcional `(("." [0-9]+)?)` se omite por completo.

#### `d)` 854,26
```ebnf
                            <real>
                                |
                        +------+------+
                        |             |
                    [0-9]+       ("." [0-9]+)?
                        |                |
                        8           +--+--+
                        |           |     |
                    +--+--+     [0-9]+  |
                    |     |        |     |
                    [0-9]+  |        2     |
                    |     |              |
                    5    +--+--+
                        |     |
                        [0-9]+  |
                        |     |
                        4    +--+--+
                                |     |
                            [0-9]+  |
                                |     |
                                2     |
```

#### `e)` Conceptos de lenguajes


<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 9**

Defina utilizando diagramas sintácticos la gramática para la definición de un
identificador de un lenguaje de programación. Tenga presente como regla que un identificador no puede comenzar con números.

```ebnf
<real> ::= <letra> ( (([0-9]) | <letra> )*)
<letra> ::= ([A-Z] | [a-z])
```

Arbol de definición
```
             identificador
                    |
                +---+----+
                |        |
               letra  letra/digito/_
                |
             +--+---+
             |      |
          letra  letra/digito/_
```

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 10**

- `a)` Defina con EBNF la gramática para una expresión numérica, dónde intervienen variables y números. Considerar los operadores +, -, * y / sin orden de prioridad. No considerar el uso de paréntesis. <br><br>
    ```ebnf
    <operacion> ::= <numero> <signo> <numero>
    <numero> ::= [0-9]+
    <signo> ::= "+" | "-" | "*" | "/"
    ```
- `b)` A la gramática definida en el ejercicio anterior agregarle prioridad de operadores.
- `c)` Describa con sus palabras los pasos y decisiones que tomó para agregarle prioridad de operadores al ejercicio anterior.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### **Ejercicio 11**

La siguiente gramática intenta describir sintácticamente la sentencia for de ADA, indique cuál/cuáles son los errores justificando la respuesta

```ebnf
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

