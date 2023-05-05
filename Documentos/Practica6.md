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

### `a)` Complete el siguiente cuadro según lo correspondiente a cada lenguaje

| Tipo de pasaje de parámetros | Lenguaje |
| ---------------------------- | -------- |
| | ADA |
| | C |
| | Rubi |
| | JAVA |
| | Python |

### `b)` Ada es más seguro que Pascal, respecto al pasaje de parámetros en las funciones. Explique por qué.
### `c)` Explique cómo maneja Ada los tipos de parámetros in-out de acuerdo al tipo de dato

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 4 Sea el siguiente programa escrito en Pascal-like

<table><td>

```pas
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

```pas
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

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 5

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 6

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 7

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 8

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 9

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 10

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">