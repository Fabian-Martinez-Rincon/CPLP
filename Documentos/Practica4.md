<h1 align="center"> 📝 Practica 4</h1>

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

<div align="center">

[Siguiente](/Documentos/Practica3.md)<br>
[Anterior](/Documentos/Practica5.md)

</div>

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">


**`Objetivo`**: Conocer el manejo de identificadores en memoria y como lo definen e implementan los diferentes lenguajes

- [Ejercicio 1 Tome una de las variables de la línea 3 del siguiente código](#ejercicio-1)
- [Ejercicio 2 Indique cuales son las diferentes formas de inicializar una variable](#ejercicio-2)
- [Ejercicio 3 Explique los siguientes conceptos asociados al atributo l-valor ](#ejercicio-3)
- [Ejercicio 4](#ejercicio-4)
- [Ejercicio 5](#ejercicio-5)
- [Ejercicio 6](#ejercicio-6)
- [Ejercicio 7](#ejercicio-7)
- [Ejercicio 8](#ejercicio-8)
- [Ejercicio 9](#ejercicio-9)
- [Ejercicio 10](#ejercicio-10)
- [Ejercicio 11](#ejercicio-11)
- [Ejercicio 12](#ejercicio-12)
- [Ejercicio 13](#ejercicio-13)
- [Ejercicio 14](#ejercicio-14)
- [Ejercicio 15](#ejercicio-15)

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

## Ejercicio 1

- `a)` Tome una de las variables de la línea 3 del siguiente código e indique y defina cuales son sus atributos:
- `b)` Compare los atributos de la variable del punto `a)` con los atributos de la variable de la línea 4. Que dato contiene esta variable?

<table> <td>

```pascal
1.Procedure Practica4();
2.var
3.  a,i:integer
4.  p:puntero
5.Begin
6.  a:=0;
7.  new(p);
8.  p:= ^i
9.  for i:=1 to 9 do
10.     a:=a+i;
11. end; //Este end esta mal
12. ... //Hagamos como que no existe
13. p:= ^a;
14. ...
15. dispose(p);
16.end;
```
</td><td>

| Identificador | L-VALOR       | R-VALOR   | ALCANCE | T.VIDA |
| ------------- | ------------- | --------- | ------- | ------ |
| Practica4     | -             | -         | 1-16    |  1-16  |
| a             | automatica    | 0         | 3-16    | 1-16   |
| i             | automatica    | undefined | 3-16    | 1-16   |
| p             | automatica    | ^i        | 4-16    | 7-15   |

</td>
</table>



<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 2

#### `a)` Indique cuales son las diferentes formas de inicializar una variable en el momento de la declaración de la misma.

Una variable puede inicializarse vacía o con un valor acorde al tipo de la variable. Internamente, si no le asigno un valor en memoria se guardará vacía hasta que la variable tome un valor

#### `b)` Analice en los lenguajes: Java, C, Phyton y Ruby las diferentes formas de inicialización de variables que poseen. Realice un cuadro comparativo de esta característica.

<table><td>

En los lenguajes Java y C, se pueden inicializar variables declarando y asignando un valor en la misma línea o declarando primero la variable y luego asignando un valor. Además, en Java es posible inicializar arreglos mediante la creación de una nueva instancia y especificando su tamaño. En Python y Ruby, las variables se pueden inicializar asignándoles un valor o dejándolas en estado nulo. En general, los cuatro lenguajes permiten la inicialización de variables de manera similar, aunque con algunas diferencias sintácticas. Python y Ruby tienen una sintaxis más simple, mientras que Java y C ofrecen más opciones y control en la inicialización de arreglos.
</td><td>

| Lenguaje | Sintaxis de inicialización de variables |
| -------- | --------------------------------------- |
| Java     | Tipo variable = valor;                  |
|          | Tipo variable;                          |
|          | variable = valor;                       |
|          | Tipo[] variable = new Tipo[tamaño];     |
| C        | Tipo variable = valor;                  |
|          | Tipo variable;                          |
|          | variable = valor;                       |
|          | Tipo variable[tamaño];                  |
| Python   | variable = valor                        |
|          | variable = None                         |
| Ruby     | variable = valor                        |
|          | variable = nil                          |
</td></table>





<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 3
- Explique los siguientes conceptos asociados al atributo l-valor de una:
- De al menos un ejemplo de cada uno.
- Investigue sobre que tipos de variables respecto de su l-valor hay en los lenguajes C y Ada.

El atributo l-valor se refiere a la capacidad de una variable para ser utilizada como una referencia a la ubicación de memoria donde se almacena su valor. Los diferentes tipos de variables pueden tener diferentes atributos l-valor según la forma en que se declaran y utilizan en el programa.

#### `a` Variable estática.

Se declara con la palabra clave "static" y se almacena en una ubicación fija en la memoria durante toda la vida del programa. 

```c
void myFunction() {
  static int x = 0; // variable estática
  x++; // incrementar valor de x
  printf("Valor de x: %d\n", x);
}
```

---

#### `b` Variable automática o semiestática.
Se declara dentro de una función o un bloque y se almacena en la pila durante la ejecución de la función o el bloque. 

```ada
procedure myProcedure is
  a : Integer := 10; -- variable automática
begin
  null;
end myProcedure;
```

---

#### `c` Variable dinámica.

Se crea y se destruye dinámicamente durante la ejecución del programa, y su ubicación en la memoria se determina en tiempo de ejecución. 

```python
my_list = [1, 2, 3] # variable dinámica
my_list.append(4)
print(my_list) # [1, 2, 3, 4]
```

---

#### `d` Variable semidinámica.
Se declara como una matriz en tiempo de compilación pero se inicializa y cambia de tamaño en tiempo de ejecución. 

```c
void myFunction() {
  int n;
  printf("Ingrese tamaño de la matriz: ");
  scanf("%d", &n);
  int arr[n]; // variable semidinámica
  for (int i = 0; i < n; i++) {
    arr[i] = i;
    printf("%d ", arr[i]);
  }
}
```


<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 4
- `a)` ¿A qué se denomina variable local y a qué se denomina variable global?
- `b)` ¿Una variable local puede ser estática respecto de su l-valor? En caso afirmativo dé un ejemplo
- `c)` Una variable global ¿siempre es estática? Justifique la respuesta.
- `d)` Indique qué diferencia hay entre una variable estática respecto de su l-valor y una constante

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 5
- `a)` En Ada hay dos tipos de constantes, las numéricas y las comunes. Indique a que se debe dicha clasificación.
- `b)` En base a lo respondido en el punto a), determine el momento de ligadura de las constantes del siguiente código:
- `H` constant Float:= 3,5;
- `I` constant:= 2;
- `K` constant float:= H*I;

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 6
Sea el siguiente archivo con funciones de C:

```ada
Archivo.c
{ 
    int x=1; (1)
    int func1();{
    int i;
    for (i:=0; i < 4; i++) 
        x=x+1;
    }
    int func2();{
    int i, j;
    /*sentencias que contienen declaraciones y
    sentencias que no contienen declaraciones*/
    ......
    for (i:=0; i < 3; i++)
        j=func1 + 1;
    }
}
```

Analice si llegaría a tener el mismo comportamiento en cuanto a alocación de memoria, sacar la declaración (1) y colocar dentro de func1() la declaración static int x =1;

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 7
Sea el siguiente segmento de código escrito en Java, indique para los identificadores si son globales o locales.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

<table>

<tr><td>

```java
Clase Persona {
public long id
public string nombreApellido
public Domicilio domicilio
private string dni;
public string fechaNac;
public static int cantTotalPersonas;
//Se tienen los getter y setter de cada una
de las variables
//Este método calcula la edad de la persona
a partir de la fecha de nacimiento
```

</td><td>

```java
public int getEdad(){
    public int edad=0;
    public string fN = this.getFechaNac();
        ...
        ...
    return edad;
}
}
Clase Domicilio {
    public long id;
    public static int nro
    public string calle
    public Localidad loc;
    //Se tienen los getter y setter de cada una de las variables
}
```

</td></tr>

</table>

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 8
Sea el siguiente ejercicio escrito en Pascal

```pas
1- Program Uno;
2- type tpuntero= ^integer;
3-      var mipuntero: tpuntero;
4-      var i:integer;
5-      var h:integer;
6- Begin
7-      i:=3;
8-      mipuntero:=nil;
9-      new(mipuntero);
10-     mipunterno^:=i;
11-     h:= mipuntero^+i;
12-     dispose(mipuntero);
13-     write(h);
14-     i:= h- mipuntero;
15- End.
```

- `a)` Indique el rango de instrucciones que representa el tiempo de vida de las variables i, h y mipuntero.
- `b)` Indique el rango de instrucciones que representa el alcance de las variables i, h y mipuntero.
- `c)` Indique si el programa anterior presenta un error al intentar escribir el valor de h. Justifique
- `d)` Indique si el programa anterior presenta un error al intentar asignar a i la resta de h con mipuntero. Justifique
- `e)` Determine si existe otra entidad que necesite ligar los atributos de alcance y tiempo de vida para justificar las respuestas anteriores. En ese caso indique cuál es la entidad y especifique su tiempo de vida y alcance.
- `f)` Especifique el tipo de variable de acuerdo a la ligadura con el l-valor de las variables que encontró en el ejercicio.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 9
Elija un lenguaje y escriba un ejemplo:
- `a)` En el cual el tiempo de vida de un identificador sea mayor que su alcance
- `b)` En el cual el tiempo de vida de un identificador sea menor que su alcance
- `c)` En el cual el tiempo de vida de un identificador sea igual que su alcance

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 10
Si tengo la siguiente declaración al comienzo de un procedimiento:

```c
int c; en C
var c:integer; en Pascal
```

- c: integer; en ADA
- Y ese procedimiento NO contiene definiciones de procedimientos internos. ¿Puedo asegurar que el alcance y el tiempo de vida de la variable “c” es siempre todo el procedimiento en donde se encuentra definida?. Analícelo y justifique la respuesta, para todos los casos.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 11

a) Responda Verdadero o Falso para cada opción. El tipo de dato de una variable es?

- `I)` Un string de caracteres que se usa para referenciar a la variable y operaciones que se pueden realizar sobre ella.
- `II)` Conjunto de valores que puede tomar y un rango de instrucciones en el que se conoce el nombre.
- `III)` Conjunto de valores que puede tomar y lugar de memoria asociado con la variable.
- `IV)` Conjunto de valores que puede tomar y conjunto de operaciones que se pueden realizar sobre esos valores.

b) Escriba la definición correcta de tipo de dato de una variable.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

