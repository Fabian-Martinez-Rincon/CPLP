## MT1 Resumen

#### Verdadero o Falso

Marque con una cruz las respuestas Faltas
- [ ] El R-Valor de un puntero es el L-Valor del objeto que quiere representar
- [ ] Un error de Tipo Sintáctico siempre provoca un error de tipo semántico
- [ ] Los errores de semántica estática se detectan cuando el programa pasa a ejecución

#### Pregunta

Lea el siguiente fragmento de texto sacado de un libro de un lenguaje de programación XX y diga qué caracteristica del mismo le hace pensar en alguno de los criterios de evaluación de lenguajes. Justifique la respuesta. Qué otro concepto podría tenerse en cuenta para evaluar este criterio?

```python
while True:
  try:
    x = int(input("Please enter a number: "))
    break
  except ValueError:
    print("Oops!  That was no valid number.  Try again...")
```

La sentencia **try** funciona de la siguiente manera.
- Primero, se ejecuta la cláusula **try** (el código entre las palabras reservadas **try** y **except**).
- Si no ocurre ninguna excepción, el bloque **except** se salta el resto de la cláusula. Luego termina la ejecución de la sentencia **try**.
- Si ocurre una excepción durante la ejecución de la clausula **try**, el resto de la cláusula se salta. Luego, si su tipo coincide con la excepción nombrada luego de la palabra reservada **except**, se ejecuta la cláusula **except**, y la ejecución continúa luego de la sentencia **try**.
- Si ocurre una excepción que no coincide con la excepción nombrada en la cláusula **except**, esta se pasa a la sentencia **try** más afuera; si no se encuentra nada que la maneje, es una excepción no manejada, y la ejecución se frena con un mensaje como los mostrados arriba.

#### Pregunta

<table><td>

```pascal
program ideaone;
...
var while:integer;
...
begin
...
  cad:="hola";
  while:=20/2;
  writeln(while,cad);
end.
```
</td><td>
En el proceso de compilación del siguiente programa escrito en Pascal, que tipo de error podría llegar a detectar el compilador, en la sentencia (whileL:=20/2)?. Especifique el error que podría detectarse y en qué proceso del compilador se detectaria. Justifique la respuesta
</td></table>

#### Rta

El compilador de Pascal podría detectar un error de sintaxis en la sentencia while:=20/2. El compilador se encarga de analizar y traducir el código fuente del programa en Pascal a un código ejecutable. Durante este proceso, el compilador sigue una serie de reglas gramaticales y sintácticas para asegurarse de que el código esté correctamente escrito.

En la sentencia mencionada, hay un error de sintaxis debido al uso de la palabra reservada while como identificador de una variable. En Pascal, while es una palabra clave que se utiliza para definir una estructura de control de bucle, no puede ser utilizado como nombre de una variable.

Por lo tanto, el compilador detectaría un error de sintaxis en esa línea y generaría un mensaje de error indicando que se encontró un identificador inválido. El mensaje de error podría ser similar a "Error: Identificador inválido 'while'".

Este tipo de error se detectaría durante la fase de análisis sintáctico del compilador, también conocida como análisis gramatical. Durante esta fase, el compilador verifica que el código fuente cumpla con las reglas gramaticales definidas por el lenguaje Pascal. En caso de que se encuentre una violación de estas reglas, se genera un error de sintaxis y el compilador no puede continuar con la compilación hasta que se corrija el error.

#### Pregunta

Sea el siguiente ejemplo escrito en dos lenguajes distintos, indique las diferencias en cuanto a la sintaxis concreta y pragmática y determina si la sintaxis abstracta es coincidente o no lo es.

<table><tr><td>Pascal</td><td>Python</td></tr>
<tr><td>

```pascal
while a<n do
  begin
    a := b-1;
    b := a+1;
  end;
```
</td><td>

```python
while a<n do
  a = b-1;
  b = a+1;
```
</td></tr></table>

#### Rta

Las diferencias entre los dos ejemplos en cuanto a la sintaxis concreta y pragmática son las siguientes:

1. Delimitadores de bloque:
   - En Pascal, se utilizan las palabras clave **begin** y **end** para delimitar un bloque de código dentro de un bucle o una estructura condicional. Es obligatorio usarlos y el código dentro del bloque debe estar indentado.
   - En Python, se utiliza la indentación para delimitar un bloque de código. No se utilizan palabras clave como **begin** y **end**. La indentación debe ser consistente en todo el código y generalmente se utiliza una tabulación o un número específico de espacios.

2. Asignaciones:
   - En Pascal, se utiliza el operador **:=** para realizar una asignación. Por ejemplo, **a := b-1** asigna el valor de **b-1** a la variable **a**.
   - En Python, se utiliza el operador **=** para realizar una asignación. Por ejemplo, **a = b-1** asigna el valor de **b-1** a la variable **a**.

En cuanto a la sintaxis abstracta, ambos ejemplos son coincidentes. Ambos utilizan la estructura de control de bucle **while** para repetir un bloque de código mientras se cumpla una condición específica. La condición **a < n** se evalúa en ambos casos para determinar si el bucle debe continuar ejecutándose. Dentro del bucle, se realizan asignaciones a las variables **a** y **b** utilizando operadores aritméticos.

Aunque hay diferencias en la sintaxis concreta y pragmática, la sintaxis abstracta, que se refiere a la estructura y el propósito general del código, es la misma en ambos casos.

> La sintaxis concreta se refiere a las reglas gramaticales y estructurales específicas del lenguaje, mientras que la sintaxis pragmática abarca consideraciones prácticas y convenciones de estilo en la escritura del código. 

## MT2 Resumen

#### Verdadero o Falso

Marque con una cruz (X) la respuesta verdadera

- [ ] El tipo de dato de una variable es un atributo que indica solamente el conjunto de valores y operaciones posibles que la misma puede tener
- [ ] Una variable es semiestática en cuanto a su L-Valor si se aloca en memoria en el mismo momento que la unidad que la contiene y se desaloca cuando la unidad termina su ejecución
- [ ] El punto de retorno de una unidad de programa dentro del registro de activación de un lenguaje basado en pila define cual es la unidad de programa que la invocó

#### Pregunta

<table><td>

```pascal
program ideaone;
var a,b:integer;
procedure x((tipo), y);
begin
  write(a);
  y:=y-5;
  write(y);
  write(a);
end;
begin
  a:=3;
  x(a);
  writeln(a);
end.
```
</td><td>

Sea el siguiente código, analice y justifique con qué tipos (tipo) de parámetro el resultado de la impresión en pantalla será idéntico accediento al entorno de la unidad llamante durante la ejecución de la unidad. Indique y justifique si existen casos en que pueden representarse errores con los tipos que ha contestado. Escriba los resultados de la ejecución en cada caso (Ej Imprime 1,2,3,4) Respuesta.


</td>
</table>
