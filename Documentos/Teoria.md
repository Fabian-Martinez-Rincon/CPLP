<h1 align="center"> Teoria </h1>


- Objetivos de Diseño (Clase 1)
    - [Simplicidad y Legibilidad](#simplicidad-y-legibilidad)
    - [Claridad en los bindings](#claridad-en-los-bindings)
    - [Confiabilidad](#confiabilidad)
    - [Soporte](#soporte)
    - [Abstracción](#abstracción)
    - [Ortogonalidad](#ortogonalidad)
    - [Eficiencia](#eficiencia)
- [Sintáxis](#sintáxis)
    - [Caracteristicas](#características-de-la-sintáxis)
    - [Elementos](#elementos-de-la-sintáxis)
    - [Estructura](#estructura-sintáctica)
    - [Como definir la sintáxis](#cómo-definir-la-sintáxis)
    - [BNF](#bnf)
    - [Gramática](#gramática)
    - [Arboles Sintacticos](#arboles-sintacticos)
    - [Arboles de Derivación](#arboles-de-derivación)
    - [Producciones recursivas](#producciones-recursivas)
    - [Gramaticas ambiguas](#gramaticas-ambiguas)
    - [Subgramáticas](#subgramáticas)
    - [EBNF](#ebnf)
    - [CONWAY](#conway)
---
- [Semantica (Clase 2)](#semántica)
  - [Estatica](#semantica-estática)
    - [Gramática de atributos](#gramatica-de-atributos)
  - [Dinamica](#semantica-dinamica)
    - [Axiomática](#semantica-axiomática)
    - [Denotacional](#semantica-denotacional)
    - [Operacional](#semantica-operacional)
      - [Variable]()
      - [Concepto]()
      - [Nombre]()
      - [Alcance]()
      - [Tipo]()
      - [L-Value]()
      - [R-Value]()
- [Interpretación](#interpretación)
- [Compilación](#compilación)
- [Interpretación vs Compilación](#interpretación-vs-compilación)
  - [Por como se ejecuta](#por-como-se-ejecuta)
  - [Por orden de ejecución](#por-orden-de-ejecución)
  - [Por el tiempo consumido de ejecución](#por-el-tiempo-consumido-de-ejecución)
  - [Por la eficiencia posterior](#por-la-eficiencia-posterior)
  - [Por el espacio ocupado](#por-el-espacio-ocupado)
  - [Por la detección de errores](#por-la-detección-de-errores)
  - [Combinación de tecnicas](#combinación-de-tecnicas)
- [Compiladores](#compiladores)
  - [Etapa de Análisis](#1-etapa-de-análisis)
    - [Análisis léxico](#análisis-léxico-scanner)
    - [Análisis sintáctico](#análisis-sintáctico-parser)
    - [Análisis semántico](#análisis-semántico-semántica-estática)
  - [Etapa de Síntesis](#2-etapa-de-síntesis)
    - [Optimización del código](#optimización)
    - [Generación del código](#generación-de-código-intermedio)

---

- [Concepto de ligadura (Binding) Clase 3]()

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Simplicidad y Legibilidad

Los lenguajes de programación deberían

- Poder producir programas fáciles de escribir y de leer.
- Resultar fáciles a la hora de aprenderlo o enseñarlo

Ejemplo de cuestiones que atentan contra esto

---

**`Muchas componentes elementales`** un ejemplo de esto sería el lenguaje Assembly, que tiene una gran cantidad de instrucciones elementales que se deben conocer y utilizar para escribir programas. Esto puede resultar difícil para los programadores novatos que necesitan recordar una gran cantidad de instrucciones para poder escribir un programa simple.

Ejemplo

```Assembly
MOV AX, 5 ; mueve el valor 5 al registro AX
MOV BX, 10 ; mueve el valor 10 al registro BX
ADD AX, BX ; suma los valores de AX y BX y almacena el resultado en AX
```

En este ejemplo de código Assembly, se pueden ver múltiples instrucciones elementales que deben conocerse y utilizar para escribir un programa simple.

---

**`Conocer subconjuntos de componentes`** un ejemplo de esto sería el lenguaje C++, que tiene múltiples subconjuntos de componentes que se utilizan en diferentes contextos. Por ejemplo, hay diferentes formas de definir una función en C++ y el programador necesita conocer las diferencias entre ellas y cuál subconjunto debe utilizarse en una situación particular.

```c++
#include <iostream>

using namespace std;

void suma(int a, int b) {
  cout << a + b << endl;
}

int main() {
  suma(5, 10);
  return 0;
}
```

En este ejemplo de código C++, se pueden ver dos subconjuntos de componentes que se utilizan para definir una función y para imprimir un valor en la consola. Los programadores necesitan conocer las diferencias entre ellos y cuál subconjunto debe utilizarse en una situación particular.

---

**`El mismo concepto semántico - distinta sintaxis`** un ejemplo de esto sería el uso de la palabra clave "function" en JavaScript y la palabra clave "def" en Python, que se utilizan para definir funciones en ambos lenguajes, pero tienen una sintaxis diferente. Esto puede resultar confuso para los programadores que conocen un lenguaje y están aprendiendo otro.

```javascript
function suma(a, b) {
  return a + b;
}
```

```py
def suma(a, b):
  return a + b
```

En estos ejemplos de código JavaScript y Python, se puede ver que se utilizan diferentes palabras clave ("function" y "def") para definir una función en cada lenguaje, lo que puede resultar confuso para los programadores que conocen un lenguaje y están aprendiendo otro.

---

**`Distintos conceptos semánticos - la misma notación sintáctica`** un ejemplo de esto sería el uso del operador "+" en Python para concatenar cadenas y para sumar números. Esto puede resultar confuso para los programadores que no conocen las reglas semánticas detrás del operador.

```python
cadena1 = "Hola "
cadena2 = "mundo"
print(cadena1 + cadena2) #concatenación de cadenas
print(2 + 3) #suma de números
```

En este ejemplo de código Python, se utiliza el mismo operador "+" para concatenar cadenas y para sumar números. Esto puede resultar confuso para los programadores que no conocen las reglas semánticas detrás del operador.

---

**`Abuso de operadores sobrecargados`** un ejemplo de esto sería el lenguaje C++, que permite a los programadores sobrecargar los operadores para que realicen acciones personalizadas. Si se abusa de esta característica, puede resultar difícil para los programadores comprender el significado de una expresión sin conocer la implementación subyacente del operador sobrecargado.

```c++
class NumeroComplejo {
public:
  NumeroComplejo(double r = 0.0, double i = 0.0) : real(r), imag(i) {}

  NumeroComplejo operator+(const NumeroComplejo& otro) {
    return NumeroComplejo(real + otro.real, imag + otro.imag);
  }

private:
  double real;
  double imag;
};

int main() {
  NumeroComplejo a(1.0, 2.0);
  NumeroComplejo b(3.0, 4.0);
  NumeroComplejo c = a + b;
  return 0;
}
```

En este ejemplo de código C++, se sobrecarga el operador "+" para sumar números complejos. Si se abusa de esta característica, puede resultar difícil para los programadores comprender el significado de una expresión sin conocer la implementación subyacente del operador sobrecargado.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Claridad en los bindings

La claridad en los bindings es fundamental para garantizar la correcta ejecución del programa. Los bindings son los enlaces entre los elementos de un lenguaje de programación y sus atributos o propiedades. Si estos enlaces no están claros, pueden producirse errores o comportamientos inesperados en el programa.

- **`Definición del lenguaje`** En la definición del lenguaje, se establecen las reglas sintácticas y semánticas que deben seguir los programas escritos en ese lenguaje. Por ejemplo, en el lenguaje C++, el símbolo "->" se utiliza para acceder a las propiedades de un objeto a través de un puntero.
- **`Implementación del lenguaje`** En la implementación del lenguaje, se define cómo se ejecutarán las instrucciones y cómo se realizarán las operaciones en el programa. Por ejemplo, en el lenguaje Python, el operador "+" se sobrecarga para permitir la concatenación de cadenas y la suma de números.
- **`Escritura del programa`** En la escritura del programa, los programadores deben entender cómo se relacionan las variables y los valores en el programa. Por ejemplo, en el lenguaje Java, se utiliza la palabra clave "new" para crear una instancia de un objeto y asignarla a una variable.
- **`Compilación`** En la compilación, el código fuente se convierte en código ejecutable que puede ser entendido por el sistema operativo o la máquina virtual. Durante este proceso, se deben establecer correctamente los bindings entre las funciones, los objetos y los valores en el programa.
- **`Cargado del programa`** En el momento de cargar el programa, se deben establecer los bindings entre el código ejecutable y los recursos del sistema, como la memoria y los archivos. Si estos enlaces no se establecen correctamente, el programa puede fallar al ejecutarse.
- **`En ejecución`** Durante la ejecución del programa, los bindings se utilizan para acceder a las propiedades de los objetos, pasar valores entre funciones y realizar operaciones en el programa. Si estos enlaces no están claros, pueden producirse errores en tiempo de ejecución.

La ligadura en cualquier caso debe ser clara.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Confiabilidad

La confiabilidad está relacionada con la seguridad
- **`Chequeo de tipos`** Cuanto antes se encuentren errores menos costoso resulta realizar los arreglos que se requieran.
- **`Manejo de excepciones`** La habilidad para interceptar errores en tiempo de ejecución, tomar medidas correctivasy continuar.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Soporte

- Debería ser accesible para cualquiera que quiera usarlo o instalarlo (Lo ideal sería que su compilador o intérprete sea de dominio público)
- Debería poder ser implementado en diferentes plataformas
- Deberían existir diferentes medios para poder familiarizarse con el lenguaje: tutoriales, cursos textos, etc.


<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Abstracción

Capacidad de definir y usar estructuras u operaciones complicadas de manera que sea posible ignorar muchos de los detalles. (Abstracción de procesos y de datos)

Por ejemplo, en un lenguaje de programación orientado a objetos como Java, la abstracción se logra mediante la definición de clases, que encapsulan datos y comportamientos relacionados en una unidad cohesiva. Una clase define la estructura y el comportamiento de un objeto en términos de propiedades y métodos abstractos, sin entrar en detalles de implementación. Esto permite a los programadores crear y manipular objetos de manera más intuitiva y eficiente.

En un lenguaje de programación funcional como Haskell, la abstracción se logra mediante la definición de funciones puras, que toman uno o más argumentos y producen un resultado sin tener efectos secundarios. Al definir funciones en términos de entradas y salidas abstractas, en lugar de su implementación detallada, los programadores pueden crear programas más concisos y comprensibles.

En general, la abstracción se utiliza en el diseño de lenguajes de programación para simplificar la complejidad de los programas y permitir a los programadores pensar en términos más abstractos y de más alto nivel. Al proporcionar mecanismos para definir conceptos complejos en términos más simples y abstractos, los lenguajes de programación pueden mejorar la legibilidad, la reutilización y la mantenibilidad del código.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ortogonalidad

La ortogonalidad en el diseño de lenguajes de programación se refiere a la independencia y coherencia de las características del lenguaje. En un lenguaje ortogonal, cada característica se puede combinar con cualquier otra característica sin restricciones, y las reglas del lenguaje se aplican de manera consistente.

**Un ejemplo** de un lenguaje que no cumple con la ortogonalidad sería un lenguaje en el que ciertas combinaciones de características no están permitidas o dan lugar a resultados inesperados. Por ejemplo, si en un lenguaje de programación no se permite combinar la herencia de clases con la sobrecarga de operadores, esto sería una violación de la ortogonalidad.

Otro ejemplo podría ser un lenguaje en el que la sintaxis de una característica cambia dependiendo del contexto en el que se utiliza. Por ejemplo, en algunos lenguajes de programación, el operador de asignación puede tener diferentes formas dependiendo de si se utiliza en una declaración de variable o en una expresión. Esto puede hacer que el lenguaje sea más difícil de entender y utilizar de manera correcta.

En resumen, un lenguaje que no cumple con la ortogonalidad puede limitar la expresividad y la flexibilidad de los programadores al restringir las combinaciones de características que pueden utilizar, o al hacer que las reglas del lenguaje sean inconsistentes o difíciles de entender.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Eficiencia

- Tiempo y Espacio
- Esfuerzo humano
- Optimizable

La eficiencia en un lenguaje de programación se refiere a su capacidad para ejecutar programas de manera rápida y con un uso eficiente de los recursos del sistema, como la memoria y la CPU. Los lenguajes de programación más eficientes son aquellos que pueden realizar tareas complejas en el menor tiempo posible y con el menor consumo de recursos.

La eficiencia de un lenguaje puede estar influenciada por varios factores, como el diseño del lenguaje, la implementación del compilador o intérprete, y la arquitectura del sistema en el que se ejecuta el programa.

En general, los lenguajes de programación que se consideran más eficientes son aquellos que están diseñados para ser compilados en código de máquina, ya que el código generado por un compilador puede ejecutarse más rápido que el código interpretado por un intérprete. Además, los lenguajes que permiten al programador tener un mayor control sobre la gestión de la memoria, como el lenguaje C, también suelen ser más eficientes que los lenguajes que gestionan la memoria de manera automática, como el lenguaje Python.

Sin embargo, la eficiencia de un lenguaje también puede verse afectada por la complejidad del algoritmo utilizado en el programa, y no solo por el lenguaje en sí mismo. En muchos casos, es posible escribir programas más eficientes utilizando técnicas de optimización, independientemente del lenguaje de programación utilizado.

En resumen, la eficiencia es un aspecto importante a considerar en la elección de un lenguaje de programación, especialmente si se espera que el programa resultante deba ejecutarse en dispositivos con recursos limitados o en entornos de alta demanda de recursos.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

## Sintáxis

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

---

### Estructura Sintáctica

- **`Vocabulario o words`** Conjunto de caracteres y palabras necesarias para construir  expresiones, sentencias y programas. Ej: identificadores, operadores, palabras claves, etc. Las words no son elementales se construyen a partir del alfabeto 
- **`Expresiones`**
  - Son funciones que a partir de un conjunto de datos devuelven un resultado.
  - Son bloques sintácticos básicos a partir de los cuales se construyen las sentencias y programas
- **`Sentencias`**
  - Componente sintáctico más importante.
  - Tiene un fuerte impacto en la facilidad de escritura y legibilidad
  - Hay sentencias simples, estructuradas y anidadas.

---

### Reglas léxicas y sintácticas.

**`Reglas léxicas`** Conjunto de reglas para formar las “word”, a partir de los caracteres del alfabeto

Un ejemplo:

- Diferencias entre mayúsculas y minúsculas
- Símbolo de distinto. 
  - En C `!=`
  - En Pascal `<>`

**`Reglas sintácticas`** Conjunto de reglas que definen como formar las “expresiones” y “sentencias”

Un ejemplo

El `if` en C no lleva `then`, en Pascal si

La diferencia entre léxico y sintáctico es arbitrario, dan la apariencia externa del lenguaje.

---

### Tipos de Sintáxis

**ABSTRACTA** Se refiere básicamente a la estructura

**CONCRETA** Se refiere a la parte léxica

**PRAGMÁTICA** Se refiere al uso práctico

Un poco mas explicado

- **`Sintaxis abstracta`** En Python, la estructura abstracta de una función es la siguiente: `def nombreDeLaFuncion(parametro1, parametro2):`. Esto es lo que se conoce como una declaración de función, y se utiliza para definir una función en Python. La estructura abstracta de la declaración de función incluye el nombre de la función, los parámetros que recibe (en este caso, `parametro1` y `parametro2`), y dos puntos (`:`) al final de la línea. El código de la función en sí se escribe en líneas siguientes, con una indentación de cuatro espacios.
- **`Sintaxis concreta`** En Python, la sintaxis concreta para definir una lista es la siguiente: `miLista = [1, 2, 3, 4, 5]`. Una lista en Python es una colección ordenada de elementos, y se puede definir utilizando corchetes (`[` y `]`). En este ejemplo, estamos definiendo una lista llamada miLista con cinco elementos: los números del 1 al 5.
- **`Sintaxis pragmática`** En Python, la sintaxis pragmática para imprimir un mensaje en la consola es la siguiente: `print("Hola, mundo!")`. La función `print()` se utiliza para imprimir un mensaje en la consola o en la salida estándar. En este ejemplo, estamos imprimiendo el mensaje "Hola, mundo!".

### Cómo definir la sintáxis

- Se necesita una descripción finita para definir
un conjunto infinito (conjunto de todos los programas bien escritos)
- Formas para definir la sintaxis:
  - `Lenguaje natural`. Ej.: Fortran
  - Utilizando la gramática libre de contexto, definida por Backus y Naun: `BNF`. Ej: Algol
  - `Diagramas sintácticos` son equivalentes a BNF pero mucho mas intuitivos

---

### BNF

- Es una notación formal para describir la sintaxis
- Es un metalenguaje. Significa que esta por encima de un lenguaje, ya que podemos definir un lenguaje
- Utiliza metasímbolos **< > ::= |**
- **Terminal** Un terminal es cuando ya no tengo posibilidad de finirlo
- Define las reglas por medio de “producciones”. Nos permiten definir las reglas de nuestra sintaxis
  - Ejemplo:
  - < digito > ::= 0|1|2|3|4|5|6|7|8|9
  - `< digito >` No terminal
  - `::=` Metasimbolo
  - `0|1|2|3|4|5|6|7|8|9` Terminales

---

### Gramática

- Conjunto de reglas finita que define un conjunto infinito de posibles sentencias válidas en el lenguaje.
- Una gramática esta formada por una 4-tupla
- **G = ( N, T, S, P)**
  - `N` Conjunto de Símbolos no terminales
  - `T` Conjunto de Símbolos terminales
  - `S` Símbolo distinguido de la gramática que pertenece a N
  - `P` Conjunto de producciones

---

### Arboles Sintacticos

Los árboles sintácticos son una herramienta utilizada en los lenguajes de programación para representar la estructura sintáctica de un programa. En esencia, un árbol sintáctico es una representación visual de cómo se relacionan los diferentes elementos del programa según las reglas sintácticas del lenguaje.

En un árbol sintáctico, cada nodo representa un elemento del programa, como una palabra clave, un identificador, un operador, etc. Los nodos están conectados entre sí por medio de aristas que indican cómo se relacionan entre sí. El nodo raíz del árbol representa el programa completo, mientras que los nodos hoja representan los elementos más pequeños del programa.

Los árboles sintácticos son particularmente útiles para entender cómo un programa es parseado (analizado) por un compilador o un intérprete. Además, pueden ser utilizados como herramientas para detectar errores sintácticos en el código fuente, ya que un programa que no cumple con las reglas sintácticas del lenguaje no podrá ser representado mediante un árbol sintáctico válido.

Aquí te dejo un ejemplo simple de un árbol sintáctico para la expresión matemática `2 + 3 * 4`

```markdown
       +
      / \
     2   *
        / \
       3   4
```

En este árbol, el nodo raíz es el operador `+`, y tiene dos nodos hijos: uno que representa el número `2` y otro que representa la operación `3 * 4`. El nodo hijo de la operación de multiplicación a su vez tiene dos nodos hijos, que representan los números `3` y `4`, respectivamente.

Este árbol sintáctico muestra la estructura jerárquica de la expresión matemática, y es útil para entender cómo se evalúa esta expresión.


---

### Arboles de Derivación

Los árboles de derivación (también conocidos como árboles de análisis) son otra herramienta utilizada en los lenguajes de programación para representar la estructura sintáctica de un programa. A diferencia de los árboles sintácticos, que muestran la estructura jerárquica de un programa, los árboles de derivación representan la derivación (o reducción) de una regla gramatical en un programa.

En un árbol de derivación, cada nodo representa una regla gramatical del lenguaje, y los nodos hoja representan los elementos del programa, como identificadores, números, operadores, etc. El proceso de construcción de un árbol de derivación implica la aplicación de las reglas gramaticales del lenguaje de manera recursiva para derivar el programa.

Aquí te dejo un ejemplo simple de un árbol de derivación para la expresión matemática `2 + 3 * 4` utilizando la notación de Backus-Naur (BNF):

```ebnf
<expr> ::= <term> | <expr> "+" <term>
<term> ::= <factor> | <term> "*" <factor>
<factor> ::= <number> | "(" <expr> ")"

<expr>
 |
 +-- <term>
     |
     +-- <factor>
         |
         +-- <number> (2)
     |
     +-- "*" 
     |
     +-- <factor>
         |
         +-- <expr>
             |
             +-- <term>
                 |
                 +-- <factor>
                     |
                     +-- <number> (3)
                 |
                 +-- "*" 
                 |
                 +-- <factor>
                     |
                     +-- <number> (4)
```

En este árbol de derivación, cada nodo interior representa una regla gramatical, mientras que los nodos hoja representan los elementos terminales del programa. El nodo raíz del árbol representa la regla gramatical `<expr>`, que se deriva recursivamente aplicando las reglas `<term>` y `<factor>` según las operaciones `+` y `*` en la expresión original.

Los árboles de derivación son útiles para entender cómo se analiza sintácticamente un programa, y pueden ser utilizados como herramientas para detectar errores sintácticos en el código fuente. Sin embargo, a diferencia de los árboles sintácticos, los árboles de derivación no muestran la estructura jerárquica del programa, y pueden ser más difíciles de interpretar visualmente.

---

### Producciones recursivas


- Son las que hacen que el conjunto de sentencias descripto sea infinito
- Ejemplo de producciones recursivas:
  ```ebnf
  <natural> ::= <digito> | <digito><digito> | ....... |
  <digito>..............<digito>
  ```
- Si lo planteamos recursivamente
  ```ebnf
  GN = ( N, T, S, P)
  N = { <natural>, <digito> } T = { 0, 1, 2, 3, 4, 5, 6, 7, 8, 9 }
  S = <natural>
  P = {
    <natural> ::= <digito> | <digito> <natural>,
    <digito> ::= 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9
  }
  ```
- Cualquier gramática que tiene una producción recursiva describe un lenguaje infinito.
- Regla recursiva por la izquierda
  - La asociatividad es por la izquierda
  - El símbolo no terminal de la parte izquierda de una regla de producción aparece al comienzo de la parte derecha
- Regla recursiva por la derecha
  - La asociatividad es por la derecha
  - El símbolo no terminal de la parte izquierda de una regla de producción aparece al final de la parte derecha

---

### Gramaticas ambiguas

- Una gramática es ambigua si una sentencia puede derivarse de mas de una forma
```ebnf
G= ( N, T, S, P)
N = { <id>, <exp>, <asig>}
T = { A, B, C, +, *, -, /, :=}
S = <asig>
P1 = {
  <asig> ::= <id> := <exp>
  <exp> ::= 
    <exp>+<exp>|
    <exp>*<exp>|
    <exp>-<exp>|
    <exp>/<exp>|
    <id>
  <id> ::= A | B | C
}
```

En estos casos a la hora de generar el arbol de derivación, podemos entrar por cualquier opción, y esto genera arboles distintos para una misma expresión.


---

### Subgramáticas

Sea la gramática para identificadores 
```ebnf
GI = ( N, T, S, P)
N = { <id>, <letra>, <digito>, <otro> }
T = { A, ................, Z, 0, ........, 1}
S = <id>
P = { 
  <id> ::= <letra> | <letra><otro>,
  <otro> ::= 
    <letra> |
    <digito> | 
    <letra><otro> |
    <digito><otro>,
  <letra> ::= A | B | C | .............| Z
  <digito> ::= 0 | 1 | 2 | | 9 
}
```

Una vez que definimos subconjuntos y sabemos que estan bien, no hace falta que los volvamos a tratar de implementar, ya que al ser reglas, estas mismas se pueden reutilizar.

"La filosofía de composición es la forma en que trabajan los compiladores"

---

### EBNF

- Esta gramática es la **BNF extendida**
- Los metasimbolos que incorporados son:
- **`[ ]`** elemento optativo puede o no estar
- **`(|)`** selección de una alternativa
- **`{}`** repetición
- **`*`** 0 o mas veces 
- **`+`** una o mas veces
- **`?`** cero o una vez

Ejemplo Definición de nros Enteros

<table>
<tr>
  <td>BNF</td><td>EBNF</td>
</tr>
<tr>

<td>

```ebnf
<enterosig> ::= +<entero> | -<entero> | <entero>
<entero> ::= <digito> | <entero><digito>
```

</td>
<td>

```ebnf
<enterosig>::= [(+|-)]<digito>{<digito>}*
```

Tambien podria ser:

```ebnf
<enterosig>::= [-]{<digito>}+
```


</td>

</tr>
</table>

---

### CONWAY

- Es un grafo sintáctico o carta sintáctica
- Cada diagrama tiene una entrada y una salida, y el camino determina el análisis.
- Cada diagrama representa una regla o producción
- Para que una sentencia sea válida, debe haber una camino desde la entrada hasta la salida que la describa.
- Se visualiza y entiende mejor que BNF o EBNF

![conwayInvertido](https://user-images.githubusercontent.com/55964635/230680253-acf2eef4-44b7-4f24-a94e-0fee7992cbaf.png)

---

## Semántica

Conjunto de reglas para dar significado a los programas sintácticamente válidos.

Con otras palabras:

La semántica describe el significado de los símbolos, palabras y frases de un lenguaje ya sea lenguaje natural o lenguaje informático que es sintácticamente válido

Para luego poder darle significado a una construcción del lenguaje

***Ejemplos Practicos***

  <table>
  <tr>
  <td> La variable `x` no fue declarada </td> <td> En una expresión se combinan diferentes tipos de datos y no hay reglas que lo permitan o la resuelvan </td><td> Se declararon 2 variables con el mismo nombre en un mismo entorno </td>
  </tr>
  <tr>
  <td>
  
  ```c
  #include <stdio.h>
  int main(){
    int a, result;
    char cadena;

    cadena = "h";
    result = a + x;
    printf(resul);
    return 0;
  }
  ```
  </td>
  <td>
  
  ```c
  #include <stdio.h>
  int main(){
    int a, result;
    char cadena;

    cadena = "h";
    result = a + cadena;
    printf(resul);
    return 0;
  }
  ```
  
  </td>
  <td>
  
  ```c
  #include <stdio.h>
  int main(){
    int a;
    int a, b;

    b = a * 2;
    printf(resul);
    return 0;
  }
  ```

  </td>
  </tr>
 
</table>

---

## Semantica Estática

- No está relacionada con el significado de la ejecución del programa, está más relacionado con las formas válidas.
- El análisis está ubicado entre el análisis sintáctico y el análisis de semántica dinámica, pero más cercano a la sintaxis.
- Se las llama así porque el análisis para el chequeo se hace en compilación (antes de la ejecución).
- BNF/EBNF no sirve para esto. Estas son gramáticas libres de contexto no se meten con el significado si con las formas

La semántica estática en un lenguaje de programación se refiere a la evaluación de los programas en tiempo de compilación. En este sentido, los errores de compatibilidad de tipos, errores de declaración de variables duplicadas y errores de variables no declaradas antes de referenciarlas, son ejemplos de errores de semántica estática que se pueden detectar en tiempo de compilación.

Para responder a cada pregunta específica:

- **¿Cómo detectar errores de compatibilidad de tipos (ej. C)?** <br>
En C, los errores de compatibilidad de tipos se pueden detectar en tiempo de compilación. El compilador verificará que los tipos de datos utilizados en las operaciones sean compatibles entre sí. Si el compilador encuentra una operación con tipos de datos incompatibles, generará un error de compilación. Por ejemplo, si se intenta sumar un entero y un carácter en C, el compilador generará un error porque los tipos de datos son incompatibles.
- **¿Cómo detectar errores de declaración de variables duplicadas (ej. C)?** <br>
En C, los errores de declaración de variables duplicadas también se pueden detectar en tiempo de compilación. Si se intenta declarar dos variables con el mismo nombre en el mismo ámbito, el compilador generará un error. Por ejemplo, si se intenta declarar dos variables con el nombre "contador" dentro de la misma función en C, el compilador generará un error.
- **¿Cómo detectar errores de variables no declaradas antes de referenciarlas (ej. Python)?**<br>
En Python, los errores de variables no declaradas antes de referenciarlas se pueden detectar en tiempo de compilación mediante el uso de linters y herramientas de análisis estático de código. Estas herramientas escanean el código fuente en busca de referencias a variables que no han sido declaradas previamente y generan una advertencia o un error. Por ejemplo, si se intenta utilizar una variable "edad" antes de declararla en Python, una herramienta de análisis estático de código generará una advertencia.

---

### Gramatica de Atributos

- Para describir la sintaxis y la semántica estática formalmente sirven las denominadas gramáticas de atributos, inventadas por Knuth en 1968.
- Son **gramáticas sensibles al contexto** (GSC). Generalmente resuelven los aspectos de la semántica estática.
- La usan los compiladores
- A las construcciones del lenguaje se les asocia información a través de **`atributos`** asociados a los símbolos (terminales o no terminales) de la gramática
- Un atributo puede ser el valor de una variable, el tipo de una variable o expresión, lugar que ocupa una variable en la memoria, dígitos significativos de un número, etc.
- Los valores de los atributos se obtienen mediante las llamadas “**ecuaciones o reglas semánticas**” asociadas a las producciones gramaticales.
- Las reglas sintácticas (producciones) son similares a BNF.
- Las ecuaciones (reglas semánticas) permiten detectar errores y obtener valores de atributos.
- Los atributos están directamente relacionados a los símbolos gramaticales (terminales y no terminales)
- Las GA se suelen expresar en forma tabular para obtener el valor del atributo

Como funciona la gramática de atributos:

- Usa la tabla y machea si encuentra la producción/regla y del otro lado la ecuación que me permite llegar a los atributos.
- Mira las Reglas (símil BNF/EBNF) y busca atributos para terminales y no terminales.
- Si encuentra el atributo debe llegar a obtener su valor.
- Para obtenerlo genera ecuaciones.

De la ejecución de las ecuaciones:
- se ingresan símbolos a la tabla de símbolos,
- Detectar y dar mensajes de error
- detecta dos variables iguales,
- controla tipo y variables de igual tipo,
- ciertas combinaciones no permitidas (reglas específicas del lenguaje)
- otras cosas no permitidas por el lenguaje
- Es decir, el chequeo de semántica estática
- Generar un código para el siguiente paso

En definitiva, se debe tratar de representar todo lo que necesitemos que salte antes de la ejecución y no seadetectado sintácticamente

Otra explicacion un poco más concisa.

---

La gramática de atributos es una técnica utilizada en la teoría de compiladores para calcular valores o propiedades para cada símbolo no terminal de una gramática. Los atributos se pueden utilizar para representar información semántica sobre un programa, como el tipo de una expresión o la dirección de memoria asignada a una variable.

Aquí hay un ejemplo simple de una gramática de atributos para un lenguaje de expresiones aritméticas:

```r
E -> E1 + T {E.val = E1.val + T.val}
E -> T {E.val = T.val}
T -> T1 * F {T.val = T1.val * F.val}
T -> F {T.val = F.val}
F -> ( E ) {F.val = E.val}
F -> num {F.val = num.valor}
```

En esta gramática, cada regla de producción está asociada con un conjunto de atributos. Por ejemplo, en la regla de producción `E -> E1 + T`, se define el atributo `val` para el símbolo no terminal `E` como la suma de los atributos `val` para los símbolos no terminales `E1` y `T`.

Para calcular los valores de los atributos, se utiliza un algoritmo de evaluación de atributos que recorre el árbol de análisis sintáctico generado por la gramática. Por ejemplo, para evaluar la expresión `2 + 3 * 4`, el algoritmo de evaluación de atributos calcularía primero el valor de `3 * 4` y luego sumaría `2` al resultado.

Otro ejemplo de gramática de atributos podría ser el siguiente para un lenguaje de programación simple que permita declarar variables:

```r
programa -> declaraciones sentencias {programa.tabla = declaraciones.tabla}
declaraciones -> declaracion declaraciones {declaraciones.tabla = agregarVariable(declaracion.tabla, declaraciones.tabla)}
declaraciones -> vacio {declaraciones.tabla = tablaDeSimbolosVacia()}
declaracion -> tipo identificador {declaracion.tabla = agregarVariable(identificador.valor, tipo.tipo, declaracion.tabla)}
sentencias -> sentencia sentencias {sentencias.tabla = sentencia.tabla}
sentencias -> vacio {sentencias.tabla = tablaDeSimbolosVacia()}
sentencia -> identificador = expresion {sentencia.tabla = verificarTipo(identificador, expresion, sentencia.tabla)}
sentencia -> imprimir ( expresion ) {sentencia.tabla = verificarTipoExpresion(expresion, sentencia.tabla)}
expresion -> expresion1 + expresion2 {expresion.tipo = verificarTipo(expresion1.tipo, expresion2.tipo)}
expresion -> expresion1 - expresion2 {expresion.tipo = verificarTipo(expresion1.tipo, expresion2.tipo)}
expresion -> identificador {expresion.tipo = buscarTipo(identificador.valor, expresion.tabla)}
expresion -> entero {expresion.tipo = int}
```

Esta gramática describe un lenguaje de programación simple que permite declarar variables, asignarles valores y mostrar valores por pantalla.

Las reglas de producción que comienzan con "programa" y "declaraciones" se utilizan para definir la tabla de símbolos del programa, que se utiliza para almacenar información sobre las variables declaradas en el programa.

- `programa -> declaraciones sentencias` indica que la tabla de símbolos del programa es la misma que la tabla de símbolos de las declaraciones.
- `declaraciones -> declaracion declaraciones` indica que se pueden declarar varias variables en una lista, y que cada variable se agrega a la tabla de símbolos del programa utilizando la función `agregarVariable`. Esta función toma como argumentos la tabla de símbolos actual y la información de la variable a agregar.
- `declaraciones -> vacio` indica que la tabla de símbolos del programa está vacía si no se declaran variables.
- `declaracion -> tipo identificador` indica que cada declaración de variable debe incluir un tipo y un identificador, y que la información de la variable se agrega a la tabla de símbolos utilizando la función `agregarVariable`.
- `sentencias` se utilizan para procesar las sentencias del programa, que pueden ser asignaciones de variables o impresiones de valores por pantalla. 
- `sentencias -> sentencia sentencias` indica que se pueden tener varias sentencias en una lista, y que la tabla de símbolos de la lista de sentencias es la misma que la tabla de símbolos de la sentencia.
- `sentencias -> vacio` indica que la tabla de símbolos de la lista de sentencias está vacía si no hay sentencias.
- `sentencia` procesan las diferentes tipos de sentencias.
- `sentencia -> identificador = expresion` indica que la sentencia es una asignación de valor a una variable. La regla utiliza la función "`verificarTipo`" para asegurarse de que el tipo de la expresión sea compatible con el tipo de la variable a la que se le asigna el valor. La función "`verificarTipo`" toma como argumentos el identificador de la variable, la expresión y la tabla de símbolos actual.
- `sentencia -> imprimir ( expresion )` indica que la sentencia es una instrucción para imprimir un valor por pantalla. La regla utiliza la función `verificarTipoExpresion` para asegurarse de que el tipo de la expresión sea compatible con el tipo de valor que se quiere imprimir. La función `verificarTipoExpresion` toma como argumentos la expresión y la tabla de símbolos actual.
- `expresion` se utilizan para procesar las expresiones matemáticas del programa. 
- `expresion -> expresion1 + expresion2` indica que la expresión es una suma de dos valores, y utiliza la función "`verificarTipo`" para asegurarse de que los tipos de las dos expresiones sean compatibles. La función "`verificarTipo`" toma como argumentos los tipos de las dos expresiones.
- `expresion -> expresion1 - expresion2` indica que la expresión es una resta de dos valores, y utiliza la función "`verificarTipo`" para asegurarse de que los tipos de las dos expresiones sean compatibles.
- `expresion -> identificador` indica que la expresión es una referencia a una variable, y utiliza la función `buscarTipo` para obtener el tipo de la variable a partir de su identificador. La función `buscarTipo` toma como argumentos el identificador de la variable y la tabla de símbolos actual.
- `expresion -> entero` indica que la expresión es un valor entero, y su tipo se establece como "int".

En resumen, esta gramática de atributos utiliza funciones semánticas para agregar información a la tabla de símbolos del programa y para verificar la compatibilidad de tipos en las diferentes partes del código. Estas funciones se llaman "atributos" y se utilizan para procesar los nodos del árbol de análisis sintáctico generado a partir del código fuente del programa.

---

## Semantica Dinamica

- Es la que describe el significado de ejecutar las diferentes construcciones del lenguaje de programación.
- Su efecto se ve durante la ejecución del programa.
- Influirá la interacción con el usuario y errores de la programación
- `Recordemos` Los programas sólo se pueden ejecutar si son correctos en la sintáxis y la semántica estática.

#### ¿Cómo se describe la semántica dinámica?

- No es fácil escribirla
- No existen herramientas estándar (fáciles y claras) como en el caso de la sintáxis (diagramas sintácticos y BNF)
- Es complejo describir relación entre entrada y salida del programa
- Es complejo describir cómo se ejecutará en cierta plataforma.
- Etc.

#### Soluciones más utilizadas

- Formales y complejas:
  - Semántica axiomática
  - Semántica denotacional
- No formal:
  - Semántica operacional
  - Sirven para comprobar la ejecución, la exactitud de un lenguaje, comparar funcionalidades de distintos programas.
  - Se pueden usar combinados, no sirven todos para todos los tipos de lenguajes de programación

Veremos una descripción general para conocerlos

---

## Semantica Axiomática

- Considera al programa como “una máquina de estados” donde cada instrucción provoca un cambio de estado.
- Se parte de un axioma (verdad) que sirve para verificar "estados y condiciones" a probar
- Los constructores de un lenguaje de programación se formalizan describiendo como su ejecución provoca un cambio de estado (cada vez que se ejecuta).
- Se desarrolló para probar la corrección de los programas.
- La notación empleada es el “cálculo de predicados”
- Un estado se describe con un predicado
- El predicado describe los valores de las variables en ese estado
- Existe un estado anterior y un estado posterior a la ejecución del constructor.
- Cada sentencia se precede y se continúa con una expresión lógica que describe las restricciones y relaciones entre los datos.

La semántica axiomatica es una rama de la lógica matemática que se enfoca en describir la semántica de un lenguaje formal a través de la definición de un conjunto de axiomas y reglas de inferencia.

Un ejemplo práctico de la semántica axiomatica puede ser la especificación formal de un lenguaje de programación. En este caso, los axiomas y reglas de inferencia describen la semántica del lenguaje, es decir, cómo se comportan los programas en términos de su significado.

Por ejemplo, supongamos que queremos especificar la semántica de un lenguaje de programación muy simple que solo permite la definición de variables y la asignación de valores a esas variables. Podríamos definir los siguientes axiomas y reglas de inferencia:

- `1)` Axioma de definición de variables: Toda variable debe ser declarada antes de ser usada.
- `2)` Axioma de asignación de valores: Se puede asignar un valor a una variable declarada previamente.
- `3)` Regla de inferencia de igualdad: Si dos expresiones son iguales, entonces pueden ser reemplazadas una por la otra sin afectar el resultado del programa.

A partir de estos axiomas y reglas de inferencia, podemos definir la semántica de nuestro lenguaje de programación. Por ejemplo, si tenemos el siguiente programa:

```
x = 5
y = x + 3
```

Podemos inferir que la variable `x` debe ser declarada antes de ser usada (por el axioma 1), que se puede asignar un valor a `x` (por el axioma 2), que se puede sumar `x` y `3` para obtener el valor de y (por la regla de igualdad), y que finalmente `y` tendrá el valor `8`. De esta manera, podemos especificar la semántica de nuestro lenguaje de programación de manera rigurosa y formal, lo que permite verificar la corrección de los programas escritos en ese lenguaje.

---

## Semantica Denotacional

- Se basa en la teoría de funciones recursivas y modelos matemáticos
- Se diferencia de la axiomática por la forma que describe los estados:
- **`Axiomática`** lo describe a través de los PREDICADOS (con variables de estado)
- **`Denotacional`** lo describe a través de FUNCIONES (funciones recursivas)
- Define una correspondencia entre los constructores sintácticos y sus significados
- Describe la dependencia funcional entre el resultado de la ejecución y sus datos iniciales

Producción definir binarios: 
```ebnf
<Nbin>::=0|1|<Nbin> 0 | <Nbin> 1
FNbin(0) = 0 FNbin(<Nbin> 0) = 2 * FNbin(<Nbin>)
FNbin(1) = 1 FNbin(<Nbin> 1) = 2 * FNbin(<Nbin>) + 1

110 El resultado es un 6
FNbin(<Nbin>0)
2* FNbin(<Nbin>1)
2*[2*FNbin(1)+1]
2*[2*1+1]
2*[3]
6 
```

---

## Semantica Operacional

- El significado de un programa se describe mediante otro lenguaje de bajo nivel implementado sobre una máquina abstracta
- Los cambios que se producen en el estado de la máquina abstracta, cuando se ejecuta una sentencia del lenguaje de programación, definen su significado
- Es un método informal porque se basa en otro lenguaje de bajo nivel y puede llevar a errores
- Es el más utilizado en los libros de texto para explicar el significado (PL/1 fue el primero)

Ejemplo con codigo

<table>
<tr>
 <td>Lenguaje</td><td>Maquina abstracta</td>
</tr>
<tr>

<td>

```pas
for i:=pri to ult do
begin
  ...................
end
```

</td>
<td>

```pas
i:= pri (inicializo i)
lazo if i > ult goto sal
  .....
  i:=i+1
  goto lazo
sal
```

</td>

</tr>
</table>


## Variable 

#### Abstracción

- **`Variable`** -> Celda de Memoria
- **`Nombre`** -> Dirección
- **`Sentencia de Asignación`** -> Modificación destructiva del valor

#### Concepto

`x = 8`

¿Qué me dispara esa sentencia? ¿Me da alguna información? ¿Cuál?
- **`Nombre`** string de caracteres que se usa para referenciar a la variable. (identificador)
- **`Alcance`** es el rango de instrucciones en el que se conoce el nombre
- **`Tipo`** valores y operaciones
- **`L-value`** es el lugar de memoria asociado con la variable (tiempo de vida)
- **`R-value`** es el valor codificado almacenado en la ubicación de la variable

---

## Interpretación

- Hay un Programa escrito en lenguaje de programación interpretado
- Ej: Lisp, Smalltalk, Basic, Python, Ruby, PHP, Perl, etc.
- Hay un Programa llamado Intérprete que realiza la traducción de ese lenguaje interpretado en el momento de ejecución
 El proceso que realiza cuando se ejecuta sobre cada una de las sentencias del programa es:
  - Leer
  - Analizar
  - Decodificar
  - Ejecutar
  - Una a una las sentencias de programa
- Sólo pasa por ciertas instrucciones no por todas, según sea la ejecución (ventajas y desventajas)
- El Intérprete cuenta con una serie de herramientas para la traducción a lenguaje de máquina
- Por cada posible acción hay un subprograma en lenguaje de máquina que ejecuta esa acción.
- La interpretación se realiza llamando a estos subprogramas en la secuencia adecuada hasta generar el resultado de la ejecución.
- Un intérprete ejecuta repetidamente la siguiente secuencia de acciones:
  - **`Obtiene`** la próxima sentencia
  - **`Determina`** la acción a ejecutar
  - **`Ejecuta`** la acción

---

## Compilación

- Elegimos un lenguaje de alto nivel de este tipo.
- Ej.: Ada, C ++, Fortran, Pascal,.....
- Tenemos nuestro programa escrito
- Usamos un programa llamado Compilador que realiza la traducción a un lenguaje de máquina
- Se traduce/compila antes de ser ejecutado.
- Pasa por todas las instrucciones antes de la ejecución (ventajas y desventajas)
- El código que se genera se guarda y se puede reusar ya compilado.
- La compilación implica varias etapas, que analizaremos luego......
- El compilador toma todo el programa escrito en un lenguaje de alto nivel que llamamos lenguaje fuente antes de su ejecución.
- Luego de la compilación va a generar un lenguaje objeto que es generalmente el ejecutable (escrito en lenguaje de máquina) o un lenguaje de nivel intermedio (o lenguaje ensamblador).

---

## Interpretación vs Compilación

### Por como se ejecuta

- **`Intérprete`**
  - Ejecuta el programa de entrada directamente línea a línea
  - Dependerá de la acción del usuario o de la entrada de datos y de alguna decisión del programa
  - Siempre se debe tener el Programa Interprete
  - El programa fuente será público (necesito ambos)
- **`Compilador`**
  - Se utiliza el compilador antes de la ejecución
  - Produce un programa equivalente en lenguaje objeto
  - El programa fuente no será publico

---

### Por orden de ejecución

- **`Intérprete`**
  - Sigue el orden lógico de ejecución (no necesariamente recorre todo el código)
- **`Compilador`**
  - Sigue el orden físico de las sentencias (recorre todo)

---

### Por el tiempo consumido de ejecución

- **`Intérprete`**
  - Por cada sentencia que pasa realiza el proceso de decodificación (lee, analiza y ejecuta) para determinar las operaciones y sus operandos. Es repetitivo
  - Si la sentencia está en un proceso iterativo (ej.: for/while), se realizará la tarea de decodificación tantas veces como sea requerido
  - La velocidad de proceso se puede ver afectada
- **`Compilador`**
  - Pasa por todas las sentencias.
  - No repite lazos
  - Traduce todo de una sola vez.
  - Genera código objeto ya compilado.
  - La velocidad de compilar dependerá del tamaño del código

---

### Por la eficiencia posterior

- **`Intérprete`**
  - Más lento en ejecución. Se repite el proceso cada vez que se ejecuta el programa
  - Para ser ejecutado en otra máquina se necesita tener si o si el intérprete instalado
  - El programa fuente será publico
- **`Compilador`**
  - Más rápido ejecutar desde el punto de vista del hardware porque ya está en un lenguaje de más bajo nivel.
  - Detectó más errores al pasar por todas las sentencias
  - Está listo para ser ejecutado. Ya compilado es más eficiente.
  - Por ahí tardó más en compilar porque se verifica todo previamente
  - El programa fuente no será publico


---

### Por el espacio ocupado

- **`Intérprete`**
  - No pasa por todas las sentencias entonces ocupa menos espacio de memoria.
  - Cada sentencia se deja en la forma original y las instrucciones interpretadas necesarias para ejecutarlas se almacenan en los subprogramas del interprete en memoria
  - Cosas cómo tablas de símbolos, variables y otros se generan cuando se usan en forma más dinámica
- **`Compilador`**
  - Si pasa por todas las sentencias
  - Una sentencia puede ocupar decenas o centenas de sentencias de máquina al pasar a código objeto
  - Cosas cómo tablas de símbolos, variables, etc. se generan siempre se usen o no
  - Entonces el compilador hace ocupar más espacio

---

### Por la detección de errores

- **`Intérprete`**
  - Las sentencias del código fuente pueden ser relacionadas directamente con la sentencia en ejecución entonces se puede ubicar el error.
  - Es más fácil detectarlos por donde pasa la ejecución
  - Es más fácil corregirlos
- **`Compilador`**
  - Se pierde la referencia entre el código fuente y el código objeto.
  - Es casi imposible ubicar el error, pobres en significado para el programador.
  - Se deben usar otras técnicas (ej. Semántica Dinámica)

---

### Combinación de tecnicas

- Interpretación pura y Compilación pura son dos extremos
- En la práctica muchos lenguajes combinan ambas técnicas para sacar provecho a cada una
- Los compiladores y los intérpretes se diferencian en como reportan los errores de ejecución,
- También, hay otras diferencias que vimos anteriormente en la Comparación
- Ciertos entornos de programación contienen las dos versiones: interpretación y compilación

#### 1 - Primero Interpreto y luego Compilo

- Se utiliza el intérprete en la etapa de desarrollo para facilitar el diagnóstico de errores.
- Con el programa validado se compila para generar un código objeto más eficiente.

#### 2 - Primero Compilo y luego Interpreto

- Se hace traducción a un código intermedio a bajo nivel que luego se interpretará
- Sirve para generar código portable, es decir, código fácil de transferir a diferentes máquinas y con diferentes arquitecturas.
- Ejemplos:
- Compilador Java genera código intermedio llamado “bytecodes”. Luego es interpretado por JavaScript en la máquina cliente.
- C# (Cii Sharp) de Microsoft .NET
- VB.NET (Visual Basic . NET de Microsoft)
- PHYTON, etc.


---

## Compiladores

- Traducen todo el programa
- Pueden generar un "código ejecutable" (.exe) o un "código intermedio" (.obj)
- Ej. de programas que se compilan:
  - C, Ada, Pascal, etc.
- La compilación puede ejecutarse en 1 o 2 etapas

En ambos casos se cumplen varias sub-etapas, las principales son:

Como funcionan?

![eeeee](https://user-images.githubusercontent.com/55964635/230736134-42033360-5e6f-4070-b5fe-73abf164e6fc.png)

---

### 1) Etapa de Análisis

- Análisis léxico (Programa Scanner)
- Análisis sintáctico (Programa Parser)
- Análisis semántico (P. Semántica estática)

---

#### Análisis léxico (Scanner)

- Es el que lleva más tiempo
- Hace el análisis a nivel de palabra (LEXEMA)
- Divide el programa en sus elementos: identificadores, delimitadores, símbolos especiales, números, palabras clave, palabras reservadas, comentarios, etc.
- Analiza el tipo de cada TOKEN para ver si son válidos
- Filtra comentarios y separadores como: espacios en blanco, tabulaciones, etc.
- Genera errores si la entrada no coincide con ninguna categoría léxica
- Convierte a representación interna los números en punto fijo o punto flotante
- Pone los identificadores en la tabla de símbolos
- Reemplaza cada símbolo por su entrada en la tabla de símbolos
- El resultado de este paso será el descubrimiento de los items léxicos o tokens. 

Ejemplo de token, lexema y regla

| ID | Componente Léxico | Lexema | Patrón |
| --- | --- | --- | --- |
| 201 | IF | if | if |
| 202 | OP_RELACIONAL | <, >, != , == |  |
| 203 | IDENTIFICADOR | var, s1, suma, prom | letra (letra | digito | gb)* |
| 204 | ENTERO | 2, 23, 5124 | (digito)+ |

---

#### Análisis sintáctico (Parser)

- El análisis se realiza a nivel de sentencia.
- Se identifican las estructuras; sentencias, declaraciones, expresiones, etc. ayudándose con los tokens.
- El analizador sintáctico se alterna con el análisis lexico y semántico. Usualmente se utilizan técnicas basadas en gramáticas formales.
- Se usa una gramática para construir el "árbol sintáctico" del programa.
- Toma una sentencia y se compara con el "árbol derivación" para ver si lo que entra es correcto

---

#### Análisis semántico (semántica estática)

- Fase medular, una de las más importantes
- Las estructuras sintácticas reconocidas por el analizador sintáctico son procesadas y la estructura del código ejecutable continúa tomando forma.
- Se agrega otro tipo de información implícita (como variables no declaradas)
- Se realiza la comprobación de tipos (aplica gramática de atributos)
- Se agrega a la tabla de símbolos los descriptores de tipos
- Se realizan comprobaciones de duplicados, problema de tipos, etc.
- Se realizan comprobaciones de nombres. (ej: toda variable debe estar declarada en su entorno)
- Es el nexo entre etapas inicial y final del compilador (Análisis y Síntesis)

#### Generación de código intermedio

- Transformación del código fuente en una representación de código intermedio para una máquina abstracta.
- A esta representación intermedia, que se parece al código objeto pero que sigue siendo independiente de la máquina, se le llama código intermedio.
- El código objeto es dependiente de la máquina
- Debe ser fácil de producir
- Debe ser fácil de traducir al programa objeto
- Hay varias técnicas
- El código intermedio más habitual es el código de 3-direcciones.
- Pasa todo el código a secuencia de proposiciones de la forma x := y op z

#### Ejemplo de generación de código intermedio

- Código de 3-direcciones Forma: A:= B op C,
- `A`, `B`, `C` son operandos/variables
- `op` es un operador binario
- Se permiten condicionales simples
- Se permiten saltos.
- Cada sentencia se traduce en N líneas

Codigo

```pascal
while (a >0) and (b<(a*4-5)) do 
  a:=b*a-10;
```

Codigo Traducido

```asembly
L1: if (a>0) goto L2 
  goto L3 
L2: t1:=a*4 
  t2:=t1-5 
  if (b < t2) goto L4 
  goto L3

L4: t1:=b*a
  t2:=t1-10
  a:=t2
  goto L1
L3: …….
```


---

### 2) Etapa de Síntesis

- Optimización del código
- Generación del código
- **`1)`** más vinculado al código fuente
- **`2)`** más vinculado a características del código objeto y del hradware y arquitectura

**Etapa de Síntesis:**

- Construye el programa ejecutable y genera el código necesario
- Interviene el Linkeditor (Programa). Si hay traducción separada de módulos se enlazan los distintos módulos objeto del programa (módulos, unidades, librerías, procedimientos, funciones, subrutinas, macros, etc.)
- Se genera el módulo de carga. Programa objeto completo
- Se realiza el proceso de optimización. (Optativo)
- El cargador Loader (Programa) lo carga en memoria

---

#### Optimización

- No se hace siempre y no lo hacen todos los compiladores.
- Es Optativo
- Los optimizadores de código (programas) pueden ser herramientas independientes, o estar incluidas en los compiladores e invocarse por medio de opciones de compilación.
- Hay diversas formas y cosas a optimizar:
- elegir entre velocidad de ejecución y tamaño del código ejecutable.
- generar código para un microprocesador específico dentro de una familia de microprocesadores,
- eliminar la comprobación de rangos o desbordamientos de pila
- evaluación para expresiones booleanas,
- eliminación de código muerto o no utilizado,
- eliminación de funciones no utilizadas
- Etc...

`Ejemplo` Posibles optimizaciones locales:

Cuando hay 2 saltos seguidos se puede quedar 1 solo

<table>
<tr>
  <td>Ejemplo anterior</td>
  <td>Luego optimización
</td>
</tr>
<tr>
<td>

```Assembly
L1: if (a>0) goto L2
  goto L3
L2: t1:=a*4
  t2:=t1-5
  if (b < t2) goto L4
  goto L3
L4: t1:=b*a
  t2:=t1-10
  a:=t2
  goto L1
L3: …….
```

</td>

<td>

```Assembly
L1: if (a<=0) goto L3
  t1:=a*4
  t2:=t1-5
  if (b >= t2) goto L3
  t1:=b*a
  t2:=t1-10
  a:=t2
  goto L1
L3: …….
```

</td>

</tr>
</table>

---

## Concepto de ligadura

#### Semantica

<table>
<tr><td>ENTIDAD</td><td>ATRIBUTO</td></tr><tr><td>

- Variable 
- Rutina 
- Sentencia

</td><td>

- nombre, tipo, área de memoria, etc 
- nombre, parámetros formales, parámetros  reales, etc 
- acción asociada

</td>
</tr>
</table>

DESCRIPTOR: lugar donde se almacenan los 
atributos

---

#### Binding

- `1)` Los programas trabajan con entidades
- `2)` Las entidades tienen atributos
- `3)` Estos atributos tienen que establecerse antes de poder usar la entidad
- `4)` LIGADURA: es la asociación entre la entidad y el atributo

---

#### Ligadura
Diferencias entre los lenguajes de programación

- El número de entidades
- El número de atributos que se les pueden ligar
- El momento en que se hacen las ligaduras (binding time).
- La estabilidad de la ligadura: una vez establecida se puede modificar?

---

#### Momento de Ligadura

- Estatico
  - Definición del lenguaje
  - Implementación del lenguaje
  - Compilación (procesamiento)
- Dinamico
  - Ejecución

---

#### Momento y Estabilidad

- Una ligadura es estática si se establece antes de la ejecución y no se puede cambiar. El termino estático referencia al momento del binding y a su estabilidad.
- Una ligadura es dinámica si se establece en el momento de la ejecución y puede cambiarse de acuerdo a alguna regla especifica del lenguaje

Excepción: constantes

#### Ejemplos

<table><tr><td> En Definición </td><td>En Implementación</td><td>En Compilación</td><td>En Ejecución</td></tr>

<tr><td>

- Forma de las sentencias
- Estructura del programa
- Nombres de los tipos predefinidos

**En lenguaje C**

- **int**
- Para denominar a los enteros

</td><td>

Representación de los números y sus operaciones

**En lenguaje C**

- **int**
- Representación
- Operaciones que pueden realizarse sobre ellos

</td><td>

Asignación del tipo a las variables

**En Lenguaje C**

- **int a**
- Se liga tipo a la variable

</td>
<td>

- Variables con sus valores
- Variables con su lugar de almacenamiento

**En lenguaje C**

- **int a**
- el valor de una variable entera se liga en ejecución y puede cambiarse muchas veces.

</td>
</tr>

</table>