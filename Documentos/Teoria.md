<h1 align="center"> Teoria </h1>


- Objetivos de Diseño
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
- [Semantica](#semántica)


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
- **`Reglas léxicas`** Conjunto de reglas para formar las “word”, a partir de los caracteres del alfabeto
- **`Reglas sintácticas`** Conjunto de reglas que definen como formar las “expresiones” y “sentencias”

---

### Tipos de Sintáxis

**ABSTRACTA** Se refiere básicamente a la estructura

```pas
while (x!= y)   while x<>y do
{ begin
  ----------- --------
};
```

**CONCRETA** Se refiere básicamente a la parte léxica

**PRAGMÁTICA** Se refiere básicamente al uso práctico

---

## Semántica

Conjunto de reglas para dar significado a los programas sintácticamente válidos.