- [A) Escriba fragmentos de código de mínimo 5 y máximo 10 líneas de extensión](#a)
- [B) Cite ejemplos de código (mínimo 5, máximo 15 líneas) en ambos lenguajes](#b)
- [C) Cite un ejemplo de código (5 líneas mínimo, 10 líneas máximo) para cada](#c)
- [D) Defina un ejemplo de código (5 líneas mínimo,15 líneas máximo) en cada](#d)

---

## `Ejercicio A)` 
Escriba fragmentos de código de mínimo 5 y máximo 10 líneas de extensión que permitan ejemplificar al menos tres criterios de evaluación en los lenguajes asignados. Puede citar un ejemplo para cada criterio elegido y compararlo entre los lenguajes, colocando una breve descripción textual para cada uno.

---

### Simplicidad y legibilidad

Es la forma en la que el lenguaje está diseñado para ser fácil de leer/entender.
- Los lenguajes de programación deberían
    - Poder producir programas fáciles de escribir y de leer.
    - Resultar fáciles a la hora de aprenderlo o enseñarlo

Los siguientes código muestran cómo calcular la media de una lista de números en los lenguajes elegidos utilizando una función.

<table><td>

`Python`
```python
def calcular_media(lista):
    suma = 0
    for num in lista:
        suma += num
    media = suma / len(lista)
    return media

numeros = [2, 4, 6, 8, 10]
media = calcular_media(numeros)
print("La media es:", media)
```

</td>
<td>

`JavaScript`
```javascript
function calcularMedia(lista) {
  let suma = 0;
  for (let i = 0; i < lista.length; i++) {
    suma += lista[i];
  }
  let media = suma / lista.length;
  return media;
}
let numeros = [2, 4, 6, 8, 10];
let media = calcularMedia(numeros);
console.log("La media es:", media);
```

</td></table>

La unica diferencia clara es el uso de llaves para determinar los bloques, el uso del `let` que especifica que sea una variable dinamica y el uso obligatorio

---

### Confiabilidad

Podemos ilustrar la confiabilidad de estos lenguajes con su manejo de excepciones

<table> <tr> <td>Python</td><td> JavaScript</td></tr>

<tr><td>

```python 
try:
    resultado = 10 / x
except Exception as error:
    print("Se ha producido un error")
finally:
    x = 0
```


</td><td>


```javascript
try {
    let resultado = 10 / x
}
catch (error) {
    console.log("Se ha producido un error")
} finally {
    x = 0;
}
```
</td>
</tr> </table>


#### `Comparación Python y Javascript en confiabilidad`

En ambos lenguajes, se puede usar try-catch (JavaScript) o try-except (Python) para manejar excepciones y ejecutar un bloque de código en caso de que ocurra una excepción. Ambos lenguajes también admiten manejar múltiples excepciones y ejecutar un código según el tipo de excepción capturada. Tambien permiten el uso de la cláusula finally para definir un bloque de código que siempre se ejecutará.

---

### ORTOGONALIDAD

La ortogonalidad en Python y JavaScript se refiere a la independencia y coherencia de los distintos conceptos y elementos que conforman estos lenguajes, lo cual permite una gran flexibilidad y facilidad de uso.


<table> <tr> <td>Python</td><td> JavaScript</td></tr>

<tr><td>

```python
a = 5
b = 2
c = a + b
d = a * b
e = a / b
f = a % b
g = "Hola, "
h = "mundo!"
i = g + h
```

Un ejemplo de ortogonalidad en Python es el uso de operadores, ya que estos pueden ser utilizados con distintos tipos de datos sin restricciones.

</td><td>

```javascript
let a = 5;
let b = 2;
let c = a + b;
let d = a * b;
let e = a / b
let f = a % b
let g = "Hola, ";
let h = "mundo!";
let i = g + h;
```

Un ejemplo de ortogonalidad en JavaScript es el uso de operadores y funciones en diferentes tipos de datos, lo que permite una mayor flexibilidad en el código.
</td>
</tr> </table>

Ofrecen una alta ortogonalidad, pero existen diferencias en su implementación, especialmente en lo que respecta a su tipado, manejo de excepciones y enfoque de orientación a objetos.

## `Ejercicio B)`
Cite ejemplos de código (mínimo 5, máximo 15 líneas) en ambos lenguajes asignados que permitan analizar A NIVEL SINTÁCTICO 4 estructuras de control de manera comparada entre los lenguajes asignados. Coloque una breve descripción a cada ejemplo.

#### IF
<table><tr><td>Python</td><td>JavaScript</td></tr>
<tr><td>

```python
a = 10
if a > 0:
    print("a es positivo")
elif a < 0:
    print("a es negativo")
else:
    print("a es cero")
```
</td><td>

```javascript
let a = 10;
if (a > 0) {
    console.log("a es positivo");
}
else if (a < 0) {
    console.log("a es negativo");
} else {
    console.log("a es cero");
}
```
</td></tr>
</table>

La sintaxis es similar: se utiliza la palabra clave if seguida de una expresión booleana entre paréntesis. Si la expresión es verdadera, se ejecuta el código dentro del bloque if, de lo contrario, busca la proxima clausula `else if/elif`, si ninguna de las anteriores es verdadera se ejecuta el código dentro del bloque else.

#### FOR EACH
<table><tr><td>Python</td><td>JavaScript</td></tr>
<tr><td>

```python
lista = [1, 2, 3, 4, 5]
suma = 0
for elemento in lista:
    suma += elemento
print(suma)
```
</td><td>

```javascript
let lista = [1, 2, 3, 4, 5];
let suma = 0;
for (let elemento of lista) {
  suma += elemento;
}
console.log(suma)
```
</td></tr>
</table>

En Python, se utiliza la sintaxis **for variable in iterable**, donde variable es la variable de iteración y iterable es el objeto a recorrer. En JavaScript, se utiliza la sintaxis **for (variable of iterable**), donde inicialización es el valor inicial de la variable de iteración, condición es la expresión booleana que determina cuándo detener el bucle, e incremento es la operación que se realiza en cada iteración.

#### While
<table><tr><td>Python</td><td>JavaScript</td></tr>
<tr><td>

```python
lista = [1, 2, 3, 4, 5]
suma = 0
i = 0
while i < len(lista):
    suma += lista[i]
    i+=1
print(suma)
```
</td><td>

```javascript
let lista = [1, 2, 3, 4, 5];
let suma = 0;
let i = 0;
while (i < lista.length) {
  suma += lista[i];
  i++;
}
console.log(suma);
```
</td></tr>
</table>

En ambos lenguajes, se utiliza la palabra clave while seguida de una expresión booleana entre paréntesis. El código dentro del bloque while se ejecuta mientras la expresión booleana sea verdadera.

#### Case/Switch
<table><tr><td>Python</td><td>JavaScript</td></tr>
<tr><td>

```python
finDeSemana = 2
match finDeSemana: 
    case 1: print("Sabado")
    case 2: print("Domingo")
    case _: print("Día de semana")
```
</td><td>

```javascript
let finDeSemana = 2;
switch (finDeSemana) {
    case 1:
        console.log("Sábado");
        break;
    case 2:
        console.log("Domingo");
        break;
    default:
        console.log("Día de semana");
        break;
}
```
</td></tr>
</table>

Tanto la estructura switch...case de JavaScript como la estructura match de Python permiten realizar selecciones, condicionales de código en función del valor de una expresión, pero existen algunas diferencias importantes entre ambas. La sintaxis de match es más concisa que la de switch, y match es más poderoso ya que permite realizar comparaciones más complejas y evitar errores comunes. En general, match es más seguro y explícito que switch.

---

## `Ejercicio C)`
Cite un ejemplo de código (5 líneas mínimo, 10 líneas máximo) para cada lenguaje asignado donde pueda distinguirse con claridad chequeos de semántica estática y dinámica a la hora de ejecutar/interpretar código. Debe poder entenderse con claridad, más allá de la naturaleza del lenguaje, distintos tipos de errores que se controlan y el momento en que dichos chequeos se realizan hasta poder ejecutar propiamente el programa.

#### Error de Semantica dinamica
<table><tr><td>Python</td><td>Javascript</td></tr><tr><td>

```python
def division(a, b):
    resultado = a / b
    return resultado

resultado_division = division(3, 0)
print(resultado_division)
```

Error
```
ZeroDivisionError: division by zero
```
</td><td>

```javascript
function division(a, b) {
    return a / b;
}

let x = 5;
let y = 0;
let resultado = division(x, y);
```
Error
```
NaN
```

</td>
</tr></table>

#### Error de Semantica Estatica

Python y JavaScript son lenguajes de programación de tipado dinámico, lo que significa que los tipos de datos se determinan en tiempo de ejecución. Como resultado, no tienen una semántica estática incorporada que detecte errores de tipo en tiempo de compilación. Sin embargo, existen herramientas y bibliotecas de verificación de tipos estáticos que pueden ser utilizadas para detectar errores de tipo antes de la ejecución del código.

## `Ejercicio D)`
Defina un ejemplo de código (5 líneas mínimo,15 líneas máximo) en cada lenguaje seleccionado donde se visualicen los distintos tipos de variables que soporta el lenguaje en cuanto al tiempo de vida, y realice una tabla donde se sitúen todos los identificadores junto con los valores de sus atributos tal como se vió en la práctica correspondiente.

<table> <td>

```javascript
1.let x = 10
2.function miFuncion() {
3.    const y = 5;
4.    const x = 11;
5.    console.log(`valor de x local: ${x}, valor de y local: ${y}`);
6.}
7.function miFuncion2() {
8.    x = x + 5;
9.}
10.console.log(`valor de x inicial: ${x}`);
11.miFuncion();
12.miFuncion2();
13.console.log(`valor de x final: ${x}`);
```

| Identificado | Lvalo | RValo | Alcance | T. vida |
| --- | --- | --- | --- | --- |
| x |  dinamica | 10, 15 | 1-4, 7-13 -> | <- 1-13 -> | 
| miFuncion | dinamica |  | 2-13 | 2-6 |
| y | dinamica | 5 | 3-6 | 2-6 |
| x (local) | dinamica | 11 | 4-6 | 2-6 |
| miFuncion2 | dinamica |  | 7-13 | 7-9 |
</td><td>

```python
1.x = 10
2.def mi_funcion():
3.    y = 5
4.    x = 11
5.    print(f"valor de x local: {x}, valor de y local: {y}")
6.def mi_funcion2():
7.    global x;
8.    x = x + 5
9.print(f"valor de x inicial: {x}")
10.mi_funcion()
11.mi_funcion2()
12.print(f"valor de x final: {x}")
```

| Identificado | Lvalo | RValo | Alcance | T. vida |
| --- | --- | --- | --- | --- |
| x |  dinamica | 10, 15 | 1-4, 6-12-> | <- 1-12 -> | 
| mi_funcion | dinamica |  | 2-12 | 2-5 |
| y | dinamica | 5 | 3-5 | 2-5 |
| x (local) | dinamica | 11 | 4-5 | 2-5 |
| mi_funcion2 | dinamica |  | 6-13 | 6-9 |
</td> </table>





