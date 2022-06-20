![](https://raw.githubusercontent.com/gabrielfernando01/basics_in_python/master/image/lambda.png)

# Funciones lambda en Python. map(), filter() y reduce()

Vamos a describir a detalle **qué son las funciones lambda en Python**, también conocidas como _funciones anónimas_.

## ¿Qué son las funciones lambda en Python?

En Python, las _funciones lambda_ son también conocidas como _funciones anónimas_ por que se definen sin un nombre.

Una función en Python se define con la palabra reservada <code>def</code>. Sin embargo, una _función anónima_ se define con la palabra reservada <code>lambda</code>.

## Cómo se define una función anónima en Python

La sintaxis para definir una _función lambda_ es la siguiente:

```
lambda parametros: expresion
```

Principales características de la _función anónima:_

- Son funciones que pueden definir cualquier número de parámetros pero una única expresión. Esta expresión es evaluada y devuelta.
- Se pueden usar en cualquier lugar en el que una función sea requerida.
- Estas funciones están restringidas al uso de una sola expresión.
- Se suelen usar en combinación con otras funciones, generalmente como argumentos de otra función.

Ejemplo:

```
cuadrado = lambda x: x ** 2
```

En el ejemplo anerior, <code>x</code> es el parámetro y <code>x ** 2</code> la expresión que se evalúa y se devuelve.

La función no tiene nombre y toda la definición devuelve una función que se asigna al identificador <code>cuadrado</code>.

En el siguiente ejemplo se aprecian las similitudes y diferencias de usar una _función anónima_ de una función típica:

```
>>> def cuadrado(x):
...     return x ** 2
 
>>> cuad = lambda x: x ** 2

>>> print(cuadrado(3))
9

>>> print(cuad(5))
25
```

## Ejemplos de uso comunes de funciones lambda: map(), filter() y reduce()

### map()

La función <code>map()</code> en Python aplica una función a cada uno de los elementos de una lista.

```
map(una_funcion, una_lista)
```
