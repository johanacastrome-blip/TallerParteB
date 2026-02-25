# TallerParteB
#B1
# Realice un programa que calcule la potencia que consume un circuito ingresando por teclado el
# valor de corriente y voltaje.

V = int(input('Valor de voltaje '))
I = int(input('Valor de corriente '))
P = I * V
print(f'Valor de potencia {P:.2f}W')

=============================================================================================
#B2
# Realice un programa que calcule X números aleatorios en un rango determinado por el usuario.

import random

print('Generador de numero aleatorio')
N = int(input('Cantidad de numeros: '))
x = int(input('Desde: '))
y = int(input('Hasta: '))
for i in range(N):
  numero = random.randint(x, y)
  print(f'Numero aleatorio {i + 1}: {numero}')
=============================================================================================
# B3
# Realice un programa para el cálculo de volúmenes (Prisma, Pirámide, Cono truncado, Cilindro)
# donde el usuario pueda seleccionar el sólido y los parámetros de cada volumen.
import numpy as np

print('Calculador de volumen\nSelecionar solido:\n1. Prisma\n2. Pirámide\n3. Cono truncado\n4. Cilindro')
seleccion = int(input('Ingresar numero (ej: 1 para prisma): '))
#print(seleccion)
if seleccion == 1:
  l = int(input('Valor del largo: '))
  a = int(input('Valor del ancho: '))
  h = int(input('Valor de la altura: '))
  v = l * a * h
  print(f'El volumen del prisma es {v:.2f}m^3')

elif seleccion == 2:
  l = int(input('Valor del largo: '))
  a = int(input('Valor del ancho: '))
  h = int(input('Valor de la altura: '))
  v = (1 / 3) * l * a * h
  print(f'El volumen de la piramide es {v:2f}m^3')

elif seleccion == 3:
  h = int(input('Valor de la altura: '))
  R = int(input('Valor radio de la base mayor: '))
  r = int(input('Valor radio de la base menor: '))
  v = (1/3) * np.pi * h * (R**2 + R * r + r**2)
  print(f'El volumen del cono truncado es {v:.2f}m^3')

elif seleccion == 4:
  h = int(input('Valor de la altura: '))
  r = int(input('Valor del radio: '))
  v = np.pi * r**2 * h
  print(f'El volumen del cilindro es {v:.2f}m^3')

else:
  print('Numero fuera de rango')
=============================================================================================
# B4
# Realice un programa que le permita al usuario escoger entre robot Cilíndrico, Cartesiano y esférico,
# donde como respuesta a la selección conteste con el tipo y número de articulaciones que posee.

print('Articulaciiones robóticas')
print('1. Cilíndrico\n2. Cartesiano\n3. Esférico')
selec = int(input('Selecionar tipo de robot (ej: 1 para cilíndrico): '))

print('\nRespuesta:\n')
if selec == 1:
  print('Un robot cilíndrico tiene 3 articulaciones, una rotacional y dos prismáticas.')
elif selec == 2:
  print('Un robot cartesiano tiene 3 articulaciones prismáticas.')
elif selec == 3:
  print('Un robot esférico tiene 3 articulaciones, dos rotacionales y una prismatica.')
else:
  print('Numero fuera de rango')
=============================================================================================
# B5
# Escribir un programa que realice la pregunta ¿Desea continuar Si/No? y que no deje de hacerla
# hasta que el usuario teclee No.

while(1):
  resp = input('¿Desea continuar Si/No?')
  if resp == 'No':
    break
