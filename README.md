# parcial2fundamentos
import random

def generar_numeros():
    # Generar un vector de 50 números enteros aleatorios entre 1 y 20
    primer_vector = [random.randint(1, 20) for _ in range(50)]
    
    # Eliminar duplicados y guardar en el segundo vector
    segundo_vector = list(set(primer_vector))
    
    # Contar la cantidad de veces que se repiten los números del segundo vector en el primer vector
    repeticiones = {num: primer_vector.count(num) for num in segundo_vector}
    
    # Leer un número por teclado
    numero_a_buscar = int(input("Ingrese un número para buscar su frecuencia en el primer vector: "))
    
    # Contar cuántas veces se repite el número ingresado en el primer vector
    repeticiones_numero_ingresado = primer_vector.count(numero_a_buscar)
    
    # Contar el número de elementos en cada vector
    elementos_primer_vector = len(primer_vector)
    elementos_segundo_vector = len(segundo_vector)
    
    return (primer_vector, segundo_vector, repeticiones, repeticiones_numero_ingresado, elementos_primer_vector, elementos_segundo_vector)

# Ejecutar la función y obtener los resultados
primer_vector, segundo_vector, repeticiones, repeticiones_numero_ingresado, elementos_primer_vector, elementos_segundo_vector = generar_numeros()

# Imprimir los resultados
print("Primer vector:", primer_vector)
print("Segundo vector:", segundo_vector)
print("Repeticiones de números del segundo vector en el primer vector:", repeticiones)
print("El número ingresado se repite", repeticiones_numero_ingresado, "veces en el primer vector.")
print("Cantidad de elementos en el primer vector:", elementos_primer_vector)
print("Cantidad de elementos en el segundo vector:", elementos_segundo_vector)
