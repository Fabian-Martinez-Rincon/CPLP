<div align="center">

[![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/Nomadiix/CPLP)
[![GitHub stars](https://img.shields.io/github/stars/Nomadiix/CPLP)](https://github.com/FabianMartinez1234567/CPLP/stargazers/)
[![GitHub repo size in bytes](https://img.shields.io/github/repo-size/Nomadiix/CPLP)](https://github.com/Nomadiix/CPLP)
 </div>

<h1 align="center"> 🧠 CPLP</h1>
<div align="center">
<img src="https://media.giphy.com/media/3oz8xNkfjM07d7dK0w/giphy.gif"/>
</div>

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

- [TP Integrador](/Documentos/tpIntegrador.md)
- [EBNF](/Documentos/EBNF.md)
- [Teoria](/Documentos/Teoria.md)
- [Practica 1 Teoria](/Documentos/Practica1.md)
- [Practica 2 BNF/EBNF](/Documentos/Practica2.md)
- [Practica 3 Semantica Estatica/Dinamica](/Documentos/Practica3.md)
- [Practica 4 Variables](/Documentos/Practica4.md)
- [Practica 5 Pilas de ejecución (Esta la hice full en papel)](/Documentos/Practica5.md)
- [Practica 6 Parametros](/Documentos/Practica6.md)
- [Practica 7 Sistemas y tipos de Datos](/Documentos/Practica7.md)
- [Practica 8 Excepciones](/Documentos/Practica8.md)
- [Practica 9 Estructuras de control y sentencias](/Documentos/Practica9.md)

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

# 💻 Resumen Practica 6 Párametros

Ateriormente hicimos la practica de pila estatica y dinamica, ahora le vamos a agregar parametros, que son los siguientes:


<table>
<tr><td>Parametro</td><td>Descripción</td><td>Ejemplo</td></tr>
<tr><td>Valor</td><td>

Trabajamos con una copia del valor recibido 
- x = 3

</td><td>

```ada
procedura rutina(x:integer);
begin
  x = x + 1
end;

a = 3;
rutina(a);
```

</td></tr>
<tr><td>Referencia</td><td>

Trabajamos siempre modificando el valor original
- a <--- x

</td><td>

```ada
procedura rutina(io x:integer);
begin
  x = x + 1
end;

a = 3;
rutina(a);
```

</td></tr>
<tr><td>Nombre</td><td>
Tomamos el contexto completo, y trabajamos con las variables originales al contexto (Hay te estar atentos si las variables se modifican por referencia o si son globales)

- x ↑ r1 [ y + r2 [y] ]

</td><td>

```ada
Procedure main;
y: integer;
r1:array[1..6] of integer;
r2:array[1..5] of integer;

procedura rutina(nombre x:integer);
begin
  x = x + 1
end;

rutina(r1[ y + r2 [y]]);
```

</td></tr>
<tr><td>Valor-Resultado</td><td>

Es igual al pasaje por valor solo que este trabaja con la copia y al final del proceso, retorna el valor modificado a la variable original. (El valor esta en el)
- x(a) = 3 

</td><td>

```ada
procedura rutina(valor-resultado x:integer);
begin
  x = x + 1
end;
a = 3;
rutina(a); //VR = 4
```

</td></tr>
</table>

### Datos a tener en cuenta

- El arbol de anidamiento simplemente para saber que función esta contenida en otra, no es necesario para la practica.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">


# 👾 Resumen Practica 7 Tipos de Datos

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">


# 🤖 Resumen Practica 8 Excepciones

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">


# ♟️ Resumen Practica 9 Estructuras de Control

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">


# 🎲 Resumen Practica 10 Paradigmas
