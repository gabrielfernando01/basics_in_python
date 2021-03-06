![](https://raw.githubusercontent.com/gabrielfernando01/basics_in_python/master/image/list.png)

# list Python - Listas en Python: El tipo list y operaciones más comunes.

La clase list en Python es una de las más utilizadas por su naturaleza, dinamismo, fácil manejo y potencia. Para esta parte los ejemplos o bloques de código los encuentras en el fichero: list.py de esta misma carpeta

## ¿Qué es una lista?

Las listas en Python son un tipo **contenedor,** compuesto, que **se usan para almacenar conjuntos de elementos relacionados** que no necesariamente tienen que ser del mismo tipo. 

Junto a las clases _tuple, range_ y _str,_ **son uno de los tipos de secuencia en Python,** con la particularidad de que son _mutables._ Esto quiere decir que su contenido puede ser modificado después de haber sido creada.

Para crear una lista en Python, simplemente hay que encerrar una secuencia de elementos por comas entre paréntesis cuadrados <code>[]</code>.

Por ejemplo para crear una lista del 1 al 10 escribimos:

```
>>> numeros = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

Las listas también se pueden crear usando el constructor de la clase, <code>list(iterable)</code>. En este caso, el constructor crea una lista cuyos elementos son los mismos y están en el mismo orden que los items del iterable. El objeto _iterable_ puede ser una secuencia, o un contenedor que soporte la iteración o un objeto iterador.

Por ejemplo, el tipo _str_ también es un tipo secuencia. Si pasamos un string al constructor $list()$ creará una lista cuyos elementos son cada uno de los caracteres de la cadena:

```
>>> vowels = list('aeiou')
>>> vowels
['a', 'e', 'i', 'o', '']
```

Dos alternativas para crear una lista vacía:

```
>>> lista1 = []		# Opción 1
>>> lista2 = list()	# Opción 2
```

Una vez que sabes como crear listas, es importante saber como acceder a ellas.

**Acceso a los elementos de una lista indicando un paso con el operador [::]**

```
>>> letras = list('abcdefghijk')
>>> letras[::2]
```

***
### for list Python - Recorrer una lista

Podemos ocupar el bucle for en Python para recorrer los elementos de una secuencia. En el caso de listas utilizamos la siguiente estructura:

```
>>> colors = ['azul', 'blanco', 'negro']
>>> for color in colors:
		print(color)
		
azul
blanco
negro
```

***
## Añadir elementos a una lista en Python, metodo append() y extend().

Las listas son elementos mutables, es decir, sus elementos pueden ser modificados (se pueden añadir nuevos items, actualizar o eliminar).

Para añadir un nuevo elemento a una lista se utiliza el método <code>append()</code> y para añadir varios elementos, el método <code>extend()</code>:

```
vowels = ['a']
vowels.append('e')				# Añade un elemento
vowels

vowels.extend(['i', 'o', 'u'])	# Añade un grupo de elementos
vowels
```

## Modificar elementos de una lista.

Es posible modificar un elemento de una lista en Python con el operador de asignación <code>=</code>. Para ello, lo único que necesitamos conocer es el índice del elemento que quieres modificar o el rango de índices:

```
>>> vowels = list('oooou')

# Actualizar el elemento del indice 0
>>> vowels[0] = 'a'
>>> vowels
['a', 'o', 'o', 'o', 'u']

# Actualizar los elementos entre las posiciones 1 y 2.
>>> vowels[1:3] = ['e', 'i']
>>> vowels
['a', 'e', 'i', 'o', 'u']
```

## Eliminar elementos de una lista

Además de la sentencia $del$, podemos usar el método <code>remove()</code> y <code>pop([i])</code>. <code>remove()</code> elimina la primera ocurrencia que se encuentre del elemento en una lista. Por su parte, <code>pop([i])</code> obtiene el elemento cuyo indice sea igual a <code>i</code> y lo elimina de la lista. Si no se especifica ningún índice, recuperara y elimina el último elemento.

```
# Elimina el elemento i
>>> vowels = list('aeiou')
>>> del vowels[1]
>>> vowels
['a', 'i', 'o', 'u']

# Elimina todos los elementos
>>> del vowels[:]
>>> vowels
[]

letters = list('abkav')

# Elimina la primera occurrencia del caracter
>>> letters.revome('a')
>>> letters
['b', 'k', 'a', 'v']

# Obtiene y elimina el último elemento
>>> letters.pop()
'v'

>>> letters
['b', 'k', 'a']
```

Es posible eliminar todos los elementos de una lista a través del método <code>clear()</code>.

```
>>> letters = ['a', 'b', 'c']
>>> letters.clear()
>>> letters
[]
```

El código anterior es equivalente a <code>del letters[:]</code>

### Longitud (len) de una lista en Python

Como cualquier tipo de secuencia, para conocer la longitud de una lista en Python se hace uso de la función <code>len()</code>. Esta función devuelve el número de elementos de una lista:

```
>>> vowels = list('aeiou')
>>> len(vowels)
5
```

## sort list Python

Las listas son secuencias ordenadas. Esto quiere decir que sus elementos siempre se devuelven en el mismo orden en que fueron añadidos.

No obstante, es posible ordenar los elementos de una lista con el método <code>sort()</code>. El método <code>sort()</code> ordena los elementos de la lista utilizando únicamente el operador <code><</code> y modifica la lista actual (no se obtine una lista nueva):

```
# Lista desordenada de números enteros
>>> numbers = [3, 2, 6, 1, 7, 4]

# Identidad del objeto número
>>> id(numbers)
4475439216

# Se llama al método sort() para ordenar los elementos de la lista
>>> numbers.sort()
>>> numbers
['1', '2', '3', '4', '5',  '6', '7']

# Se comprueba que la identidad del objeto número es la misma
>>> id(number)
4475439216
```

## Listado de métodos de la clase list  

La lista completa de métodos de la clase list.

![](https://raw.githubusercontent.com/gabrielfernando01/basics_in_python/master/image/list_methods.png)
