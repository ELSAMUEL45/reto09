# reto10
# Punto 1: Suma/Resta de matrices con validación
```
def suma_resta_matrices(matriz1, matriz2, operacion):
    if len(matriz1) != len(matriz2) or len(matriz1[0]) != len(matriz2[0]):
        print("Error: Las matrices deben tener el mismo tamaño para sumar o restar.")
        return None
    resultado = []
    for i in range(len(matriz1)):
        fila = []
        for j in range(len(matriz1[0])):
            if operacion == "suma":
                fila.append(matriz1[i][j] + matriz2[i][j])
            elif operacion == "resta":
                fila.append(matriz1[i][j] - matriz2[i][j])
        resultado.append(fila)
    return resultado

# Ejemplo de uso
A = [[1, 2], [3, 4]]
B = [[5, 6], [7, 8]]
resultado = suma_resta_matrices(A, B, "suma")
print("Resultado suma:", resultado)
resultado = suma_resta_matrices(A, B, "resta")
print("Resultado resta:", resultado)  
```
# Punto 2: Producto de matrices con validación
```
def producto_matrices(matriz1, matriz2):
    if len(matriz1[0]) != len(matriz2):
        print("Error: El número de columnas de la primera matriz debe ser igual al número de filas de la segunda.")
        return None
    resultado = []
    for i in range(len(matriz1)):
        fila = []
        for j in range(len(matriz2[0])):
            suma = 0
            for k in range(len(matriz2)):
                suma += matriz1[i][k] * matriz2[k][j]
            fila.append(suma)
        resultado.append(fila)
    return resultado

# Ejemplo de uso
A = [[1, 2], [3, 4]]
B = [[2, 0], [1, 2]]
resultado = producto_matrices(A, B)
print("Resultado del producto:", resultado)
```
# Punto 3: Matriz transpuesta
```

def transpuesta(matriz):
    filas = len(matriz)
    columnas = len(matriz[0])
    transpuesta = []
    for j in range(columnas):
        fila = []
        for i in range(filas):
            fila.append(matriz[i][j])
        transpuesta.append(fila)
    return transpuesta

# Ejemplo de uso
A = [[1, 2, 3], [4, 5, 6]]
resultado = transpuesta(A)
print("Matriz transpuesta:", resultado)
```
# Punto 4: Suma de una columna dada de una matriz
```
def sumar_columna(matriz, columna):
    if columna < 0 or columna >= len(matriz[0]):
        print("Error: Índice de columna fuera de rango.")
        return None
    suma = 0
    for i in range(len(matriz)):
        suma += matriz[i][columna]
    return suma

# Ejemplo de uso
A = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
columna = 1
resultado = sumar_columna(A, columna)
print(f"Suma de la columna {columna}: {resultado}")
```
# Punto 5: Suma de una fila dada de una matriz
```
def sumar_fila(matriz, fila):
    if fila < 0 or fila >= len(matriz):
        print("Error: Índice de fila fuera de rango.")
        return None
    return sum(matriz[fila])

# Ejemplo de uso
A = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
fila = 2
resultado = sumar_fila(A, fila)
print(f"Suma de la fila {fila}: {resultado}")
```





