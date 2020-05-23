Introducción a Python
==
Por: Fernando Jiménez T.
Tips antes de comenzar
--
1. Usar *Markdown* para escribir texto y *Code* para escribir en el lenguaje **Python**.
2. Jupyter notebook es compatible con latex (usar *Markdown* para usar la sintaxis de latex.)
$$A = \{ (x,y) \in \mathbb{R}^2 | x \neq 0 \text{ e } y >0 \}$$
Para saber más de *Markdown* se puede visitar: https://www.markdownguide.org/extended-syntax/ o https://markdown-guide.readthedocs.io/en/latest/basics.html#markdown-basics.
3. Para asignar valores a ciertas variables se puede utilizar **=**. Además se pueden realizar operaciones simples (**+,-.x,/,etc**).
4. Para añadir comentarios en el código se puede utilizar el **#**.

## Porqué usar Anaconda?
Anaconda es una fuente de distribución de *Python* y *R*. Es muy usado para *data sicence*, *machinle learning*, *deep learning*, etc. Cuenta con más de 300 librerias muy útiles para los programadores. Además de ser una plataforma gratuita y compatible con cualquier sistema operativo, utiliza la interfaz de *jupyter notebook* para crear documentos (pdf,tex,py,md,...).

## Porqué programar en Python?
Python es un lenguaje de programación que se a vuelto muy popular debido a la estructura de sus códigos. A diferencia de lenguajes como C o C++, la escritura tiende a ser muy compacta.
Python puede ser usado para crear aplicaciones web, sistemas de bases de datos, optimización matemática, entre otros.
Se puede programar en este lenguaje en cualquier sistema operativo (Windows, Mac, Linux, Raspberry Pi, etc). Utiliza una sintaxis similar al lenguaje Inglés.

## Instalación
- Anaconda: https://www.anaconda.com/products/individual

## Operaciones Básicas


```python
# Suma
2+3
# Resta
2-3
# División
2/3
# Producto
2*3
# Exponente
5**2
# Módulo
28%5
# Comparaciones
4 > 2 or 4 <= 2
4 == 2
4!= 2
```

## Tipos de variables
Las operaciones básicas no se pueden realizar entre variables tipo *string* y variables tipo *float* o *integer*.


```python
# String
x = "Hola"
# Integer
x = 1
# Float
x = 2.0
```

## Sintaxis
Se deben respetar los espacions.


```python
if 5 > 2:
  print("Five is greater than two!")
"""
En este caso si coloco a la misma altura del if el print, saldrá un error.
Se puede usar tab para alinear los códigos.
"""
if 5 > 2:
print("Five is greater than two!")
```

## Importar librerías


```python
import numpy as np
from scipy import sparse,linalg
```

### Ejemplo:


```python
# Crear un vector x usando la libreria numpy
x = np.array([1,2,3,4])
# Crear un vector de unos
N=50 # Dimension del vector
b = np.ones(N)
# Crear un vector aleatorio uniforme (0,1) de dimensión N
b = np.random.random(N)
# Crear tres vectores aleatorios de vectores aleatorios uniformes (0,1) de dimensión 4. Matriz
C = np.random.random((3,4))
# Producto de una matriz por un vector usando numpy
y = np.dot(C,x)
# Producto de dos matrices
D = 2*np.ones((4,3))
A = np.dot(C,D)
# Producto de dos matrices componente a componente
D = np.ones((3,3))
B = np.multiply(A,D)
# Matriz sparse de dimension N
A = sparse.diags([-1,2,-1],[-1,0,1], shape=(N,N)).toarray()
# Resolver el sistema Ax=b usando el solver por defecto
x = linalg.solve(A,b)
# Resolver el sistema usando factorización LU
P, L, U = linalg.lu(A)
y = linalg.solve(L,b)
x = linalg.solve(U,y)
```

Referencias:
==
1. https://dzone.com/articles/python-anaconda-tutorial-everything-you-need-to-kn
2. https://www.w3schools.com/python/python_intro.asp
3. 
