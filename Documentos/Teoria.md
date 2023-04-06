<h1 align="center"> Teoria </h1>


- [Objetivos de Diseño]()
    - [Simplicidad y Legibilidad]()
    - [Claridad en los bindings]()
    - [Confiabilidad]()
    - [Soporte]()
    - [Abstracción]()
    - [Ortogonalidad]()
    - [Eficiencia]()



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

**`El mismo concepto semántico - distinta sintaxis`** un ejemplo de esto sería el uso de la palabra clave "function" en JavaScript y la palabra clave "def" en Python, que se utilizan para definir funciones en ambos lenguajes, pero tienen una sintaxis diferente. Esto puede resultar confuso para los programadores que conocen un lenguaje y están aprendiendo otro.

**`Distintos conceptos semánticos - la misma notación sintáctica`** un ejemplo de esto sería el uso del operador "+" en Python para concatenar cadenas y para sumar números. Esto puede resultar confuso para los programadores que no conocen las reglas semánticas detrás del operador.

**`Abuso de operadores sobrecargados`** un ejemplo de esto sería el lenguaje C++, que permite a los programadores sobrecargar los operadores para que realicen acciones personalizadas. Si se abusa de esta característica, puede resultar difícil para los programadores comprender el significado de una expresión sin conocer la implementación subyacente del operador sobrecargado.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Claridad en los bindings

Los elementos de los lenguajes de programación pueden ligarse a sus atributos o propiedades en diferentes momentos.

- [Definición del lenguaje]()
- [Implementación del lenguaje]()
- [En escritura del programa]()
- [Compilación]()
- [Cargado del programa]()
- [En ejecución]()

La ligadura en cualquier caso debe ser clara

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Confiabilidad

La confiabilidad está relacionada con la 
seguridad
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

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ortogonalidad

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Eficiencia


<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">