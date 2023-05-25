<h1 align="center"> 📝 Practica 8 Excepciones</h1>

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

<div align="center">

[Siguiente](/Documentos/Practica6.md)<br>
[Anterior](/Documentos/Practica8.md)

</div>

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

**`Objetivo`** Conocer e interpretar los distintos modelos de excepciones que implementan los lenguajes de programación

- [Ejercicio 1]()
- [Ejercicio 2]()
- [Ejercicio 3]()
- [Ejercicio 4]()
- [Ejercicio 5]()
- [Ejercicio 6]()
- [Ejercicio 7]()
- [Ejercicio 8]()
- [Ejercicio 9]()
- [Ejercicio 10]()
- [Ejercicio 11]()
- [Ejercicio 12]()
- [Ejercicio 13]()
- [Ejercicio 14]()

### Ejercicio 1

¿Explique claramente a qué se denomina excepción?

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 2

¿Qué debería proveer un lenguaje para el manejo de las excepciones? ¿Todos los lenguajes lo proveen?

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 3

¿Qué ocurre cuando un lenguaje no provee manejo de excepciones? ¿Se podría simular? Explique cómo lo haría

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 4: 
Cuando se termina de manejar la excepción, la acción que se toma luego es importante. Indique

01. ¿Qué modelos diferentes existen en este aspecto?

02. Dé ejemplos de lenguajes que utilizan cada uno de los modelos presentados anteriormente. Por cada uno responda respecto de la forma en que trabaja las excepciones.

- `a`. ¿Cómo se define?
- `b`. ¿Cómo se lanza?
- `c`. ¿Cómo se maneja?
- `d`. ¿Cuál es su criterio de continuación?

03. ¿Cuál de esos modelos es más inseguro y por qué?

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 5

La propagación de los errores, cuando no se encuentra ningún manejador asociado, no se implementa igual en todos los lenguajes. Realice la comparación entre el modelo de Java, Python y PL/1, respecto a este tema. Defina la forma en que se implementa en un lenguaje conocido por Ud.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 6

Sea el siguiente programa escrito en Pascal

```pascal
...
Procedure Manejador;
  Begin ... end;
Procedure P(X:Proc);
  begin
  ....
  if Error then X;
  ....
end;

Procedure A;
begin
  ....
  P(Manejador);
  ....
end;
....
```

¿Qué modelo de manejo de excepciones está simulando? ¿Qué necesitaría el programa para que encuadre con los lenguajes que no utilizan este modelo? Justifique la respuesta.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 7

Sea el siguiente programa escrito en Pascal

<table><td>

```pascal
Program Principal;
var x:int; b1,b2:boolean;

Procedure P (b1:boolean);
  var x:int;
  Procedure Manejador1
  begin
    x:=x + 1;
  end;
begin
  x:=1;
  if b1=true then Manejador1;
  x:=x+4;
end;

Procedure Manejador2;
begin
  x:=x * 100;
end;
```
</td><td>

```pascal
Begin
  x:=4;
  b2:=true;
  b1:=false;
  if b1=false then Manejador2;
  P(b);
  write (x);
End
```
</td></table>

- `a)` Implemente este ejercicio en PL/1 utilizando manejo de excepciones
- `b)` ¿Podría implementarlo en JAVA utilizando manejo de excepciones? En caso afirmativo, realícelo.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 8: Sean los siguientes, procedimientos de un programa escrito en JAVA

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

```java
public static void main (String[] argos){
  Double array_doubles[]= new double[500];
  for (int i=0; i<500; i++){
    array_doubles[i]=7*i;
  }
  for (int i=0 ; i<600 ; i=i+25){
    try{
      system.out.println(“El elemento en “+ i + ” es “ + acceso_por_indice (array_doubles,i));
    }
    catch(ArrayIndexOutOfBoundsException e){
      system.out.println(e.tostring());
    }
    catch(Exception a){
      system.out.println(a.tostring());
    }
    finally{
      system.out.println(“sentencia finally”);
    }
  }
}
Public static double acceso_por_indice (double [] v, int indice) throws Exception; ArrayIndexOutOfBoundsException{
  if ((indice>=0) && (indice<v.length)){
    Return v[indice];
  }
  else{
    if (indice<0){
      // caso excepcional
      Throw new ArrayIndexOutOfBoundsException(“ el índice” + indice + “ es un número negativo”);
      }
    else{
      // caso excepcional
      Throw new Exception(“ el indice” + indice + “ no es una posición válida”);
    }
  }
}
```

a) Analizar el ejemplo y decir qué manejadores ejecuta y en qué valores quedan las variables. JUSTIFIQUE LA RESPUESTA.

---

b) La excepción se propaga o se maneja en el mismo método? ¿Qué instrucción se agrega para poder propagarla y que lleve información?.

---

c) como modificaría el método “acceso_por_indice” para que maneje él mismo la excepción

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 9:

Indique diferencias y similitudes entre Phyton y Java con respecto al manejo de excepciones.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 10:

¿Qué modelo de excepciones implementa Ruby?. ¿Qué instrucciones específicas provee el lenguaje para manejo de excepciones y cómo se comportan cada una de ellas?

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 11:

Indique el mecanismo de excepciones de javascript.

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 12:

Sea el siguiente programa escrito en PYTHON::Indique el camino de ejecución

```python
#!/usr/bin/env python
#calc.py

def dividir():
  x = a / b
  print (("Resultado"), (x))

while True:
  try:
    a = int(input("Ingresa el primer numero: \n"))
    b = int(input("Ingresa el segundo numero: \n"))
    dividir()
    break
  except ZeroDivisionError:
    print ("No se permite dividir por cero")
  finally:
    print ("Vuelve a probar"
```

a) Describa qué caminos ejecuta para diferentes valores de ingreso


b) Agregar el uso de una excepción anónima

<img src= 'https://i.gifer.com/origin/8c/8cd3f1898255c045143e1da97fbabf10_w200.gif' height="20" width="100%">

### Ejercicio 13

Sea el siguiente código escrito en JAVA

```java
public class ExcepcionUno extends Exception {
  public ExcepcionUno(){
    super(); // constructor por defecto de Exception
  }
```