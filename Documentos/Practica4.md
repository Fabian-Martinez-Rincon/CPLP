<h1 align="center"> 📝 Practica 4</h1>

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

<div align="center">

[Siguiente](/Documentos/Practica3.md)<br>
[Anterior](/Documentos/Practica5.md)

</div>

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">


**`Objetivo`**: Conocer el manejo de identificadores en memoria y como lo definen e implementan los diferentes lenguajes

- [Ejercicio 1](#ejercicio-1)
- [Ejercicio 2](#ejercicio-2)
- [Ejercicio 3](#ejercicio-3)
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

#### Ejercicio 1: a) Tome una de las variables de la línea 3 del siguiente código e indique y defina cuales son sus atributos:

```pas
1.Procedure Practica4();
2.var
3.  a,i:integer
4.  p:puntero
5.Begin
6.  a:=0;
7.  new(p);
8.  p:= ^i
9.  for i:=1 to 9 do
10. a:=a+i;
11.end;
12....
13.p:= ^a;
14....
15.dispose(p);
16.end;
```

b) Compare los atributos de la variable del punto a) con los atributos de la variable de la línea 4. Que dato contiene esta variable?,

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 2

#### a. Indique cuales son las diferentes formas de inicializar una variable en el momento de la declaración de la misma.

#### b. Analice en los lenguajes: Java, C, Phyton y Ruby las diferentes formas de inicialización de variables que poseen. Realice un cuadro comparativo de esta característica.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 3: Explique los siguientes conceptos asociados al atributo l-valor de una:
- `a` Variable estática.
- `b` Variable automática o semiestática.
- `c` Variable dinámica.
- `d` Variable semidinámica.

De al menos un ejemplo de cada uno.

Investigue sobre que tipos de variables respecto de su l-valor hay en los lenguajes C y Ada.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 4:
a. ¿A qué se denomina variable local y a qué se denomina variable global?
b. ¿Una variable local puede ser estática respecto de su l-valor? En caso afirmativo dé un ejemplo
c. Una variable global ¿siempre es estática? Justifique la respuesta.
d. Indique qué diferencia hay entre una variable estática respecto de su l-valor y una constante

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 5:
#### a. En Ada hay dos tipos de constantes, las numéricas y las comunes. Indique a que se debe dicha clasificación.


#### b. En base a lo respondido en el punto a), determine el momento de ligadura de las constantes del siguiente código:

- `H` constant Float:= 3,5;
- `I` constant:= 2;
- `K` constant float:= H*I;

### Ejercicio 6: Sea el siguiente archivo con funciones de C:

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

### Ejercicio 7: Sea el siguiente segmento de código escrito en Java, indique para los identificadores si son globales o locales.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">