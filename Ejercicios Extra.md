# Resolución de Diagrama de Bloques

## Objetivo
Determinar la función de transferencia total \( \frac{C(s)}{R(s)} \) del sistema dado.

## Diagrama Inicial
*(Inserta aquí el diagrama proporcionado como imagen.)*

## Solución Paso a Paso

### Paso 1: Identificar los bloques y sus relaciones
El diagrama tiene los siguientes elementos:
- **Bloques**:
  - \( G_1 \): Bloque principal en la rama directa.
  - \( G_2 \): Bloque paralelo a \( G_1 \).
  - \( G_3 \): Conecta \( G_2 \) con la retroalimentación.
  - \( G_4 \): Bloque en el lazo de retroalimentación.
- **Entradas y salidas**:
  - Entrada: \( R(s) \).
  - Salida: \( C(s) \).

### Paso 2: Simplificar las ramas paralelas
Las ramas \( G_1 \) y \( G_2 \) están en paralelo. La combinación se calcula como:

\[
G_{\text{paralela}} = G_1 + G_2
\]

### Paso 3: Retroalimentación con \( G_3 \) y \( G_4 \)
El sistema tiene retroalimentación negativa que incluye \( G_{\text{paralela}} \), \( G_3 \), y \( G_4 \). La función equivalente de la retroalimentación es:

\[
G_{\text{retroalimentación}} = \frac{G_{\text{paralela}}}{1 + G_{\text{paralela}} \cdot G_3 \cdot G_4}
\]

### Paso 4: Función de transferencia total
La función de transferencia total del sistema es igual a \( G_{\text{retroalimentación}} \), lo que da:

\[
\frac{C(s)}{R(s)} = \frac{G_1 + G_2}{1 + (G_1 + G_2) \cdot G_3 \cdot G_4}
\]

## Código en Python
El siguiente código en Python simplifica y valida los cálculos simbólicamente:

```python
from sympy import symbols, simplify

# Declarar las variables simbólicas
s = symbols('s')  # Variable de Laplace
G1, G2, G3, G4 = symbols('G1 G2 G3 G4')  # Bloques del sistema

# Calcular la combinación en paralelo
G_paralela = G1 + G2

# Calcular la función equivalente con retroalimentación
G_retroalimentacion = G_paralela / (1 + G_paralela * G3 * G4)

# Simplificar la función de transferencia total
C_R = simplify(G_retroalimentacion)
print("La función de transferencia total es:")
print(C_R)

