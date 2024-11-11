TP6
Resolver usando Pandas
Resolver los ejercicios del TP3 utilizando la librería Pandas.

Ejercicio 1: Cargar Datos de ventas.
El archivo datos.dat contiene el registro de las ventas realizadas.

Tiene un formato de ancho fijo:

fecha: 10 lugares
producto: 30 lugares
precio: 10 lugares
cantidad: 5 lugares
Hacer una funcion que cargue los datos en un DataFrame de Pandas.

def cargar_datos():
    pass # Implementar la función cargar_datos

datos = cargar_datos()
datos 
Ejercicio 2: Calcular el total de ventas.
Hacer una función que sume los importes vendidos (precio * cantidad) y las cantidades.

def calcular_totales(datos):
    pass # implementar

importe, cantidad = calcular_totales(datos)

print(f"Las ventas fueron de ${importe:2.f} en {cantidad} unidades")
Ejercicio 3: Listar las unidades vendidas.
Listar cuántas unidades se vendieron en total para cada producto

def unidades_vendidas(datos):
    pass

unidades_vendidas(datos)
Ejercicio 4: Listar el precio promedio por producto.
Hacer un listado del precio promedio por producto.

def precio_promedio(datos):
    pass # Implementar

precio_promedio(datos)
Ejercicio 5: Ranking de productos
Realizar un listado de los 3 productos más vendidos ordenados por la cantidad de unidades vendidas (ordenadas de mayor a menor)

def ranking_productos(datos, top=3):
    pass # Implementar

ranking_productos(datos)
Ejercicio 6: Listar las ventas por mes
Realizar un listado del total de unidades vendidas por producto separado por mes.

def ventas_por_mes(datos):
    pass # Implementar

ventas_por_mes(datos)
Ejercicio 7: Informe general
Mostrar un listado de productos ordenados alfabeticamente que contengan el precio promedio, la cantidad de unidades vendidas y el importe total vendido para cada producto

def resumen_ventas(datos):
    pass # Implementar

resumen_ventas(datos)
Resolver usando NumPy
Resolver el ejercicio 2 del tp1 usando NumPy
Ejercicio 8
Escribe una función en Python que encuentre los valores de a, b, y c para que la función cuadrática f(x) = a x^2 + b x + c pase exactamente por los siguientes puntos:

x	y
0	0
1	8
2	12
3	12
5	0
Requisitos:
La función debe explorar posibles valores de a, b, y c utilizando un método de prueba y error.
Debe devolver los valores que hagan que la diferencia entre la función f(x) y los valores medidos y sea exactamente cero para cada punto.
Pista: Los valores de a, b, y c son números pequeños.

La idea es implementar el mismo algoritmo que se uso en el TP1 pero usando NumPy en lugar de Python puro.

import numpy as np
def f(x, coeficientes):
    a,b,c = coeficientes
    return a*x**2 + b*x + c

def error(y, y_pred):
    return y - y_pred

X = np.array([0,1,2,3,5])
Y = np.array([0,8,12,12,0])

def buscar_coeficientes():
    pass # Implementar

coeficientes = buscar_coeficientes()
coeficientes
(-2, 10, 0)
Ejercicio 9: Resolver el ejercicio 3 del TP1 usando NumPy
Buscar los coeficientes de la función que minimice la suma de los cuadrados de las diferencias entre los valores medidos y los valores de la función.

Crear un array con los coeficientes elegidos al azar (usar randint(-10,10,3)).
Calcular el valor de la función y el error correspondiente.
Mientras que el error sea mayor a 1:
Definir nuevos coeficientes agregándoles un pequeño valor al azar a los coeficientes actuales (aprendizaje = 0.001).
Si el error para los nuevos coeficientes es menor que el anterior, reemplazar los coeficientes actuales por los nuevos.
import numpy as np
from numpy.random import randint

def f(x, coeficientes):
    a,b,c = coeficientes
    return a*x**2 + b*x + c

def error(y, y_pred):
    return np.sum((y - y_pred)**2)

X = np.array([0, 1, 2, 3, 5])
Y = np.array([0, 8,12,11, 1]) # Observar que no son los mismos valores que en el ejemplo anterior

def buscar_coeficientes():
    pass # Implementar


coeficientes = buscar_coeficientes()
coeficientes
Los coeficientes son [-1.781  8.961  0.615] y el error es 0.9958049999998968
array([-1.781,  8.961,  0.615])
