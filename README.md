# ejercicios-de-listas

¿Qué es una lista?
Una lista es una estructura de datos y un tipo de dato en python con características especiales. Lo especial de las listas en Python es que nos permiten almacenar cualquier tipo de valor como enteros, cadenas y hasta otras funciones; por ejemplo:

lista = [1, 2.5, 'DevCode', [5,6] ,4]
Una lista es un arreglo de elementos donde podemos ingresar cualquier tipo de dato, para acceder a estos datos podemos hacer mediante un índice.

print lista[0] # 1
print lista[1] # 2.5
print lista[2] # DevCode
print lista[3] # [5,6]
print lista[3][0] # 5
print lista[3][1] # 6
print lista[1:3] # [2.5, 'DevCode']
print lista[1:6] # [2.5, 'DevCode', [5, 6], 4]
print lista[1:6:2] # [2.5, [5, 6]]
Como pueden darse cuenta podemos hasta insertar una lista dentro de otra lista.

Si no quieres estar imprimir uno por uno los elementos de una lista, puedes recorrerlo utilizando un for.

for element in lista:
    print element
Métodos de las Listas
Las listas en Python  tienen muchos métodos que podemos utilizar, entre todos ellos vamos a nombrar los más importantes. Para esto utilizaremos esta lista de ejemplo.

my_list = [2, 5, 'DevCode', 1.2, 5]
Sobre esta vamos a realizar diferentes métodos que son propios de las listas.

------------------------------------------------------------------------------------------
Append()
Este método nos permite agregar nuevos elementos a una lista.

my_list.append(10) # [2, 5, 'DevCode', 1.2, 5, 10]
my_list.append([2,5]) # [2, 5, 'DevCode', 1.2, 5, [2, 5]]
Podemos agregar cualquier tipo de elemento a una lista, pero tengan en cuenta lo que pasa cuando agregamos una lista dentro de otra, esta lista se agrega como uno y solo un elemento.

---------------------------------------------------------------------------------------------
Extend()
Extend también nos permite agregar elementos dentro de una lista, pero a diferencia de append al momento de agregar una lista, cada elemento de esta lista se agrega como un elemento más dentro de la otra lista.

my_list.extend([2,5]) # [2, 5, 'DevCode', 1.2, 5, 2, 5]
Remove()
El método remove va a remover un elemento que se le pase como parámentro de la lista a donde se le esté aplicando.

my_list.remove(2) # [5, 'DevCode', 1.2, 5]
En este ejemplo estamos removiendo el elemento 2, de la lista que tiene por nombre "my_list".

-----------------------------------------------------------------------------------------------
Index()
Index devuelve el número de indice del elemento que le pasemos por parámetro.

my_list.index('DevCode') # 2
Aquí estamos preguntando por el indice de la cadena 'DevCode' dentro de la lista "my_list", esto devuelve 2.

-----------------------------------------------------------------------------------------------
Count()
Para saber cuántas veces un elemento de una lista se repite podemos utilizar el metodo count().

my_list.count(5) # 2
Contamos cuantas veces se repite el número 5 dentro de la lista, y esto devuelve 2.

----------------------------------------------------------------------------------------------
Reverse()
También podemos invertir los elementos  de una lista.

my_list.reverse() # [5, 1.2, 'DevCode', 5, 2]
------------------------------------------------------------------------------
Métodos de las listas
append()
Añade un ítem al final de la lista:


lista = [1,2,3,4,5]
lista.append(6)
lista

[1, 2, 3, 4, 5, 6]
------------------------------------------------------------------------------
clear()
Vacía todos los ítems de una lista:


lista.clear()
lista

[]

------------------------------------------------------------------------------
extend()
Une una lista a otra:


l1 = [1,2,3]
l2 = [4,5,6]
l1.extend(l2)
l1

[1, 2, 3, 4, 5, 6]

------------------------------------------------------------------------------
count()
Cuenta el número de veces que aparece un ítem:


["Hola", "mundo", "mundo"].count("Hola")

1

------------------------------------------------------------------------------
index()
Devuelve el índice en el que aparece un ítem (error si no aparece):


["Hola", "mundo", "mundo"].index("mundo")

1
------------------------------------------------------------------------------
insert()
Agrega un ítem a la lista en un índice específico:

Primera posición (0):


l = [1,2,3]
l.insert(0,0)
l

[0, 1, 2, 3]
Penúltima posición (-1):


l = [5,10,15,25]
l.insert(-1,20) 
l

[5, 10, 15, 20, 25]
Última posición en una lista con len():


l = [5,10,15,25]
n = len(l)
l.insert(n,30)
l

[5, 10, 15, 20, 25, 30]
Una posición fuera de rango añade el elemento al final de la lista (999):


l.insert(999, 35)
l

[5, 10, 15, 20, 25, 30, 35]
------------------------------------------------------------------------------
pop()
Extrae un ítem de la lista y lo borra:


l = [10,20,30,40,50]
print(l.pop())
print(l)

50
[10, 20, 30, 40]
Podemos indicarle un índice con el elemento a sacar (0 es el primer ítem):


print(l.pop(0))
print(l)

10
[20, 30, 40]

------------------------------------------------------------------------------
remove()
Borra el primer ítem de la lista cuyo valor concuerde con el que indicamos:


l = [20,30,30,30,40]
l.remove(30)
print(l)

[20, 30, 30, 40]

------------------------------------------------------------------------------
reverse()
Le da la vuelta a la lista actual:


l.reverse()
print(l)

[40, 30, 30, 20]
Las cadenas no tienen el método .reverse() pero podemos simularlo haciendo unas conversiones:


lista = list("Hola mundo")
lista.reverse()
cadena = "".join(lista)
cadena    

'odnum aloH'

------------------------------------------------------------------------------
sort()
Ordena automáticamente los ítems de una lista por su valor de menor a mayor:


lista = [5,-10,35,0,-65,100]
lista.sort()
lista

[-65, -10, 0, 5, 35, 100]
Podemos utilizar el argumento reverse=True para indicar que la ordene del revés:


lista.sort(reverse=True)
lista

[100, 35, 5, 0, -10, -65]
