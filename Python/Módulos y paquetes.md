Al igual que otros lenguajes de programación, Python permite a los usuarios hacer
definiciones y declaraciones en un fichero para utilizarlas posteriormente. A estos
ficheros se les conoce como módulos.
Para generar un módulo, tan sólo tenemos que guardar el código que deseemos
reutilizar en un fichero nombre.py, y para importarlo, utilizaremos la sentencia:

```python
import nombre
```

Sin embargo, esto no incluye las funciones definidas en nombre directamente en el
espacio de nombres actual, si no que para acceder a ellas deberemos hacer referencia
al módulo al que pertenecen:

```python
nombre.funcion()
```

 Veamos un ejemplo, tenemos los siguientes archivos:

![[modulos python.png]]

Si queremos no tener que utilizar la notación modulo.funcion(), necesitaremos
importar las funciones que vayamos a querer utilizar de dicho módulo. Siguiendo el
ejemplo anterior, se haría mediante la siguiente sentencia:

```python
from calculadora import suma,resta,producto
a=5
b=3
print("5+3 =",suma(a,b))
print("5-3 =",resta(a,b))
print("5*3 =",producto(a,b))
```

Si queremos importar todas las funciones de un módulo concreto, podemos utilizar
también el operador *:

```python
from calculadora import *
```

