<h1 align="center"> 📝 Practica 6</h1>

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

<div align="center">

[Siguiente](/Documentos/Practica5.md)<br>
[Anterior](/Documentos/Practica7.md)

</div>

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

**`Objetivo`** Descubrir las técnicas existentes para pasaje de parámetros entre unidades y sus diferencias esenciales de acuerdo al lenguaje que lo implementa


- [Ejercicio 1 Explique brevemente los siguientes conceptos](#ejercicio-1)
- [Ejercicio 2  Unir los siguientes puntos según corresponda](#ejercicio-2)
- [Ejercicio 3 Complete el siguiente cuadro según lo correspondiente a cada lenguaje](#ejercicio-3)
- [Ejercicio 4 Sea el siguiente programa escrito en Pascal-like](#ejercicio-4)
- [Ejercicio 5 Suponiendo que se está ejecutando un programa con el siguiente registro](#ejercicio-5)
- [Ejercicio 6 Indique con un ejemplo el comportamiento del parámetro por nombre](#ejercicio-6)
- [Ejercicio 7 Realice la pila de ejecución del siguiente programa](#ejercicio-7)
- [Ejercicio 8 Indique las diferencias entre los pasaje de subprogramas como parámetros](#ejercicio-8)
- [Ejercicio 9 Sea el siguiente código escrito en Pascal like](#ejercicio-9)
- [Ejercicio 10](#ejercicio-10)

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 1 Explique brevemente los siguientes conceptos
- **`Parámetro`** 
- **`Parámetro real`** 
- **`Parámetro formal`** 

#### Ligadura
- **`Ligadura posicional`**  Se corresponden con la posición que ocupan en la lista
- **`Ligadura por palabra clave o nombre`** Se corresponden con el nombre por lo tanto pueden estar colocados indistintamente en la list
- En `Ada` pueden mezclarse ambos métodos. 
- En `C++` y en `Ada` los parámetros formales pueden tener valores por defecto, con lo cual a veces no es necesario listarlos todos en la 
invocación

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 2  Unir los siguientes puntos según corresponda y de una definición y un ejemplo de cada par.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 3

#### `a)` Complete el siguiente cuadro según lo correspondiente a cada lenguaje

| Tipo de pasaje de parámetros | Lenguaje |
| ---------------------------- | -------- |
| | ADA |
| | C |
| | Rubi |
| | JAVA |
| | Python |

---

#### `b)` Ada es más seguro que Pascal, respecto al pasaje de parámetros en las funciones. Explique por qué.

---

#### `c)` Explique cómo maneja Ada los tipos de parámetros in-out de acuerdo al tipo de dato

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 4 Sea el siguiente programa escrito en Pascal-like

<table><td>

```pascal
Procedure Main;
    var j, m, i: integer;
Procedure Recibe (x:integer; y:integer);
begin
    m:= m + 1 + y;
    x:=i + x + j;
    y:=m - 1;
    write (x, y, i, j, m);
end;
```

</td><td>

```pascal
Procedure Dos;
    var m:integer;
begin
    m:= 5;
    Recibe(i, j);
    write (i, j, m);
    end;
    begin
    m:= 2;
    i:=1; j:=3;
    Dos;
    write (i, j, m);
end.
```
</td>
</table>

#### a- Arme el árbol de anidamiento sintáctico y el registro de activación de cada una de las unidades.

---

#### b- Decir qué imprime el programa suponiendo que para todas las variables que se pasan el pasaje de parámetros es por: (Deberá hacer la pila estática y dinámica para cada caso)
- **`i)`** Referencia. 
- **`ii)`** Valor 
- **`iii)`** Valor Resultado 
- **`iv)`** Nombre 
- **`v)`** Resultado.

---

#### c- ¿Existió algún caso que no pudo realizarlo porque saltó algún tipo de error? Diga cuál y por qué.

---

#### d- ¿Dará el mismo resultado si se trata de un lenguaje que sigue la cadena dinámica? Justifique la respuesta realizando las pilas de activación

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 5

Suponiendo que se está ejecutando un programa con el siguiente registro de activación en memoria y se llama al procedimiento rutina(iter,vec,a). Determine el tipo de parámetro que se deben utilizar en el llamado para que los resultados sean los siguientes:

- **`a)`** (4,6,7),(4,6,7), 2, 2
- **`b)`** (3,5,6),(4,6,7), 2, 2
- **`c)`** (3,5,6),(5,5,6), 0, -1

| PR |
| -- |
| LD |
| LE |
| Iter: true |
| Vec:[3,5,6] |
| a: -1 |
| Rutina() |
| VR |

```pascal
......
procedura rutina(tipoParam iteracion,tipoParam vector,tipoParam vit):
    while iteracion begin
        vit = a+1
        vector[vit] = vector[vit]+1
        iteracion = (vector[vit] mod 2)==0
    end
    print vec
    print vector
    print vit
print a
.....

rutina(iter,vec,a)
```

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 6 
Indique con un ejemplo el comportamiento del parámetro por nombre (en el parámetro formal) para los siguientes casos de parámetros reales:
- Un valor entero.
- Una constante.
- Un elemento de un arreglo.
- una expresión.

Que sucede en cada caso?

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 7

Realice la pila de ejecución del siguiente programa: 
- **`a)`** siguiendo la cadena estática 
- **`b)`** siguiendo la cadena dinámica

<table><td>

```pascal
Procedure Uno;
    y, z: integer;
    r1:array[1..6] of integer;
    r2:array[1..5] of integer;
Procedure Dos( nombre x, t:integer; var io:integer; valor-resultado y:integer);
    Procedure Dos( nombre t1:integer);
        Procedure Tres;
        begin
            y:= y + 1;
            z:= z + 1;
        end;
    begin
        t1:= t1 + 1;
        t:= t + 1;
        Tres;
        t1:= t1 + 2;
        t:= t + 2;
    end
begin
    x:= x + 1;
    t:= t + 1;
    io:= io + 1;
    x:= x + 2;
    if z =2 then Dos ( t );
end

begin
    for y:= 1 to 6 do r1(y):= 2;
    for y:= 1 to 5 do r2(y):= 1;
    z:= 2;
    y:= 1;
    Dos( r1( y + r2( y )), r2( z ), y, z);
    for y:= 1 to 6 do write (r1(y));
    for y:= 1 to 5 do write (r2(y));
end
```
</td><td>


</td>
</table>

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 8

#### a) Indique las diferencias entre los pasaje de subprogramas como parámetros deep y shallow

#### b) Realice la pila estática y dinámica tanto con el pasaje de parámetros deep y shallow para el siguiente código

<table><td>

```pascal
Program A
    Var x:integer;
    Var y: char;

Procedure B;
    Var h:integer;
Begin
    h:=1+x;
    Write (y);
    C(D);
    Write (y);
End;

Procedure C (Subrutina S);
    Var x:integer;
    Var y: char;
Begin
    x:=3;
    y:= "b";
    x:=S(x,y)
    y:= "j";
    Write (x,y);
End
```

</td><td>

```pascal
Function D (j:integer, k:char);
Begin
    j:=j+x;
    k:=y;
    Write (k);
    Return j;
End;
BEGIN
        x:=0;
        y:="a";
        B();
        Write (x,y);
END
```
</td>

</table>

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 9

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 10

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">