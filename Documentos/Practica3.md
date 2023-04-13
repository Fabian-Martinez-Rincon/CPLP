<h1 align="center"> 📒 Practica 3</h1>

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

<div align="center">

[Siguiente](/Documentos/Practica4.md)<br>
[Anterior](/Documentos/Practica2.md)

</div>

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">


Objetivo: Interpretar el concepto de semántica de los lenguajes de programación.

- [Ejercicio 1](#ejercicio-1)
- [Ejercicio 2](#ejercicio-2)
- [Ejercicio 3](#ejercicio-3)
- [Ejercicio 4](#ejercicio-4)
- [Ejercicio 5](#ejercicio-5)
- [Ejercicio 6](#ejercicio-6)
- [Ejercicio 7](#ejercicio-7)
- [Ejercicio 8](#ejercicio-8)

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

## Ejercicio 1
¿Qué define la semántica?

La semántica describe el significado de los símbolos, palabras y frases de un lenguaje ya sea lenguaje natural o lenguaje informático que es sintácticamente válido

Para luego poder darle significado a una construcción del lenguaje

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

## Ejercicio 2

- `a)` ¿Qué significa compilar un programa?
- `b)` Describa brevemente cada uno de los pasos necesarios para compilar un programa.
- `c)` ¿En qué paso interviene la semántica y cual es su importancia dentro de la compilación?

- a) Compilar un programa significa convertir el código fuente escrito en un lenguaje de programación de alto nivel en un lenguaje de bajo nivel que pueda ser entendido por la computadora y ejecutado por el procesador.
- b) Los pasos necesarios para compilar un programa son los siguientes:
    - Análisis léxico: En esta etapa, el compilador lee el código fuente y lo divide en tokens o palabras clave del lenguaje de programación, como identificadores, constantes, operadores y símbolos.
    - Análisis sintáctico: El compilador utiliza una gramática formal para comprobar si los tokens se combinan de acuerdo con las reglas sintácticas del lenguaje de programación. Si se detecta un error, el compilador emite un mensaje de error.
    - Análisis semántico: En esta etapa, el compilador verifica que el programa tenga sentido semántico, es decir, que las operaciones y las funciones se estén utilizando correctamente y que el tipo de datos sea coherente.
    - Generación de código intermedio: El compilador crea un código intermedio que es más fácil de traducir al código de máquina. Este código intermedio es a menudo un lenguaje ensamblador de bajo nivel, pero puede ser una representación en un lenguaje de alto nivel, como C.
    - Optimización de código: El compilador intenta mejorar el código intermedio para que se ejecute más rápido o utilice menos memoria.
    - Generación de código de máquina: El compilador convierte el código intermedio en código de máquina que la computadora puede entender y ejecutar.
    - Enlazado: El compilador vincula el código generado con las bibliotecas y los archivos necesarios para producir un programa ejecutable.
- c) La etapa de análisis semántico es donde se evalúa la corrección semántica del programa. Esta etapa es importante porque garantiza que el programa se comporte como se espera y evita errores comunes como divisiones por cero o intentos de acceso a memoria no asignada. Si un error semántico se pasa por alto, puede ser difícil de detectar y puede causar problemas en el programa en tiempo de ejecución.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

## Ejercicio 3

Con respecto al punto anterior ¿es lo mismo compilar un programa que interpretarlo? Justifique su respuesta mostrando las diferencias básicas, ventajas y desventajas de cada uno.

No, compilar un programa y interpretarlo son dos enfoques diferentes para ejecutar un código fuente.

Compilar un programa implica traducir todo el código fuente a lenguaje de máquina de bajo nivel antes de ejecutarlo. El código compilado se almacena en un archivo ejecutable, que se puede ejecutar directamente en el sistema operativo de la computadora. Una vez que se ha creado el archivo ejecutable, no es necesario compilar el código fuente cada vez que se desea ejecutar el programa.

Por otro lado, interpretar un programa implica leer y ejecutar el código fuente línea por línea, sin la necesidad de compilar previamente el código a un archivo ejecutable. Un intérprete es un programa que lee y ejecuta el código fuente en tiempo real. Cada vez que se ejecuta el programa, el intérprete vuelve a leer el código fuente y lo ejecuta línea por línea.

A continuación, se presentan algunas diferencias básicas, ventajas y desventajas entre compilar y interpretar un programa:

#### **`Diferencias básicas`**

- La compilación convierte todo el código fuente en un archivo ejecutable, mientras que la interpretación lee y ejecuta el código fuente en tiempo real.
- El archivo ejecutable resultante de la compilación se puede ejecutar varias veces sin la necesidad de volver a compilar, mientras que el código interpretado debe leerse y ejecutarse cada vez que se ejecuta el programa.
- La compilación requiere un proceso de construcción adicional antes de la ejecución del programa, mientras que la interpretación no requiere ese proceso.

#### **`Ventajas de la compilación`**

- La ejecución de programas compilados suele ser más rápida que la interpretación, ya que no se requiere leer y analizar el código fuente cada vez que se ejecuta el programa.
- El archivo ejecutable resultante se puede distribuir fácilmente a otros usuarios y ejecutarse en diferentes sistemas operativos sin tener que instalar el compilador en cada uno de ellos.
- La compilación puede realizar optimizaciones de código que mejoran el rendimiento y la eficiencia del programa.

#### **`Desventajas de la compilación`**

- La compilación puede ser un proceso más lento y complicado que la interpretación, ya que implica varios pasos, incluyendo el análisis semántico y la optimización de código.
- Los errores en el código fuente pueden no detectarse hasta después de la compilación, lo que puede retrasar la corrección de los errores y la depuración del programa.
- Los programas compilados suelen ser más grandes en tamaño que los programas interpretados, lo que puede ser un problema en sistemas con poco espacio en disco.

#### **`Ventajas de la interpretación`**

- La interpretación es más fácil de depurar y corregir errores, ya que el código fuente se lee y ejecuta en tiempo real.
- Los programas interpretados suelen ser más portables, ya que el código fuente se puede ejecutar en cualquier sistema que tenga el intérprete adecuado instalado.
- La interpretación es útil para tareas de desarrollo y pruebas de prototipos, ya que permite una iteración rápida del código fuente.


#### **`Desventajas de la interpretación`**

- La interpretación puede ser más lenta que la compilación, ya que el código fuente debe leerse y analizarse cada vez que se ejecuta el programa.
- La interpretación puede ser menos eficiente en el uso de los recursos de la computadora, ya que el intérprete debe estar en ejecución durante toda la duración del programa.
- La interpretación puede ser más difícil de proteger contra ingeniería inversa, ya que el código fuente se encuentra disponible en su forma original.
- Los programas interpretados pueden ser más susceptibles a errores de sintaxis y errores en tiempo de ejecución, ya que el código fuente no se verifica completamente hasta que se ejecuta cada línea

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

## Ejercicio 4

Explique claramente la diferencia entre un error sintáctico y uno semántico. Ejemplifique cada caso.

Un error sintáctico se produce cuando el código fuente no cumple con las reglas de sintaxis del lenguaje de programación en el que está escrito. En otras palabras, un error sintáctico ocurre cuando se comete un error de gramática en el código fuente que impide que el compilador o el intérprete entienda el significado del código.

Por ejemplo, en el lenguaje de programación Python, si se escribe:

```python
if a == 5
    print("a es igual a 5")
```

Se producirá un error sintáctico porque falta el dos puntos (:) después de la condición del if.

Por otro lado, un error semántico se produce cuando el código fuente cumple con las reglas de sintaxis del lenguaje de programación, pero su significado no es el que se pretendía. Es decir, el código puede compilarse o interpretarse sin errores, pero su resultado es incorrecto porque hay un error en la lógica o en la comprensión del problema que se está resolviendo.

Por ejemplo, supongamos que se escribe un código en Python para calcular el promedio de tres números:

```python
a = 5
b = 6
c = 7
promedio = a + b + c / 3
print("El promedio es:", promedio)
```

En este caso, el código se compilará y se ejecutará sin errores, pero el resultado será incorrecto, ya que el operador de división (/) se evalúa antes que la suma. Para obtener el resultado correcto, la expresión debe ser escrita de la siguiente manera:

```python
a = 5
b = 6
c = 7
promedio = (a + b + c) / 3
print("El promedio es:", promedio)
```

En resumen, la principal diferencia entre un error sintáctico y uno semántico es que el primero se produce cuando el código fuente no cumple con las reglas de sintaxis del lenguaje, mientras que el segundo ocurre cuando el código fuente tiene un significado incorrecto o no deseado debido a un error en la lógica o en la comprensión del problema que se está resolviendo.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

## Ejercicio 5

Sean los siguientes ejemplos de programas. Analice y diga qué tipo de error se produce (Semántico o Sintáctico) y en qué momento se detectan dichos errores (Compilación o Ejecución).
Aclaración: Los valores de la ayuda pueden ser mayores.

---

#### a) Pascal

```pas
Program P
var 
    5: integer;
var 
    a:char;
Begin
    for i:=5 to 10 do begin
        write(a);
        a=a+1;
    end;
End.
```

Ayuda: Sintáctico 2, Semántico 3

Sintacticos
- **`En la línea 3`**, se está declarando una variable con un nombre inválido (un número no puede ser un identificador válido en Pascal).
- **`En la línea 7`**, se usa el operador "=" en lugar del operador ":=" para asignar un valor a la variable.

Semanticos
- **`En la línea 4`**, hay una declaración de variable innecesaria y redundante.
- **`En la línea 6`**, se usa una variable que no ha sido declarada previamente.
- **`En la línea 8`**, se usa el operador "+" para concatenar caracteres en lugar del operador "succ()" para obtener el siguiente carácter en la tabla ASCII.

---

#### b) Java:

```java
public String tabla(int numero, arrayList<Boolean> listado)
{
    String result = null;
    for(i = 1; i < 11; i--) {
        result += numero + "x" + i + "=" + (i*numero) + "\n";
        listado.get(listado.size()-1)=(BOOLEAN) numero>i;
    }
    return true;
}
```

Ayuda: Sintácticos 4, Semánticos 3, Lógico 1

---

#### c) C

```c
# include <stdio.h>
int suma; /* Esta es una variable global */
int main()
{  int indice;
    encabezado;
    for (indice = 1 ; indice <= 7 ; indice ++)
    cuadrado (indice);
    final(); Llama a la función final */
    return 0;
}
cuadrado (numero)
int numero;
{   int numero_cuadrado;
    numero_cuadrado == numero * numero;
    suma += numero_cuadrado;
    printf("El cuadrado de %d es %d\n",
    numero, numero_cuadrado);
}
```

Ayuda: Sintácticos 2, Semánticos 6

---

#### d)Python

```py
#!/usr/bin/python
print "\nDEFINICION DE NUMEROS PRIMOS"
r = 1
while r = True:
    N = input("\nDame el numero a analizar: ")
    i = 3
    fact = 0
    if (N mod 2 == 0) and (N != 2):
        print "\nEl numero %d NO es primo\n" % N
    else:
        while i <= (N^0.5):
            if (N % i) == 0:
                mensaje="\nEl numero ingresado NO es primo\n" % N
                msg = mensaje[4:6]
                print msg
                fact = 1
        i+=2
        if fact == 0:
            print "\nEl numero %d SI es primo\n" % N
r = input("Consultar otro número? SI (1) o NO (0)--->> ")
```

Ayuda: Sintácticos 2, Semánticos 3

---

#### e) Ruby
```ruby
def ej1
    Puts 'Hola, ¿Cuál es tu nombre?'
    nom = gets.chomp
    puts 'Mi nombre es ', + nom
    puts 'Mi sobrenombre es 'Juan''
    puts 'Tengo 10 años'
    meses = edad*12
    dias = 'meses' *30
    hs= 'dias * 24'
    puts 'Eso es: meses + ' meses o ' + dias + ' días o ' + hs + ' horas'
    puts 'vos cuántos años tenés'
    edad2 = gets.chomp
    edad = edad + edad2.to_i
    puts 'entre ambos tenemos ' + edad + ' años'
    puts '¿Sabes que hay ' + name.length.to_s + ' caracteres en tu nombre, ' + name + '?'
end
```

Ayuda: Semánticos +4

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

## Ejercicio 6
Dado el siguiente código escrito en pascal. Transcriba la misma funcionalidad de acuerdo al lenguaje que haya cursado en años anteriores. Defina brevemente la sintaxis (sin hacer la gramática) y semántica para la utilización de arreglos y estructuras de control del ejemplo.

```pas
Procedure ordenar_arreglo(var arreglo: arreglo_de_caracteres;cont:integer);
var
    i:integer; ordenado:boolean;
    aux:char;
begin
    repeat
        ordenado:=true;
        for i:=1 to cont-1 do
            if ord(arreglo[i])>ord(arreglo[i+1]) then begin
                aux:=arreglo[i];
                arreglo[i]:=arreglo[i+1];
                arreglo[i+1]:=aux; ordenado:=false
            end;
    until ordenado;
end;
```



Observación: Aquí sólo se debe definir la instrucción y qué es lo que hace cada una; detallando alguna particularidad del lenguaje respecto de ella. Por ejemplo el for de java necesita definir una variable entera, una condición y un incremento para dicha variable.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

## Ejercicio 6

Explique cuál es la semántica para las variables predefinidas en lenguaje Ruby self y nil. ¿Qué valor toman; cómo son usadas por el lenguaje?

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

## Ejercicio 7

Determine la semántica de null y undefined para valores en javascript.¿Qué diferencia hay entre ellos?

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

## Ejercicio 8

Determine la semántica de la sentencia break en C, PHP, javascript y Ruby. Cite las características más importantes de esta sentencia para cada lenguaje

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

## Ejercicio 9

Defina el concepto de ligadura y su importancia respecto de la semántica de un programa. ¿Qué diferencias hay entre ligadura estática y dinámica? Cite ejemplos (proponer casos sencillos)

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">