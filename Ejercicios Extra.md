# Resolución de Diagrama de Bloques

## Objetivo
Determinar la función de transferencia total C(s)/R(s) del sistema dado.

## Diagrama Inicial

![image](https://github.com/user-attachments/assets/93f7e654-f39a-416c-a973-5063d7461ec7)


## Solución Paso a Paso

### Paso 1: Identificación de elementos clave
El sistema incluye:
- **Entrada**: R(s).
- **Salida**: C(s).
- **Bloques individuales**:
  - G1: Bloque directo desde R(s) hacia la salida.
  - G2: Bloque paralelo a G1.
  - G3: Bloque que conecta G2 con la retroalimentación.
  - G4: Bloque en el lazo de retroalimentación negativa.

---

### Paso 2: Simplificación de las ramas paralelas
Los bloques G1 y G2 están en una configuración de ramas paralelas. Para combinarlas, sumamos las ganancias de ambos bloques. Es decir, la **Ganancia Paralela** es igual a la suma de G1 y G2. Esto crea un único bloque equivalente, denominado **Ganancia Paralela**.

La expresión para la ganancia en paralelo sería:

**Ganancia Paralela = G1 + G2**

---

### Paso 3: Análisis del lazo de retroalimentación
El sistema tiene un lazo de retroalimentación negativa que involucra los bloques G3 y G4. La retroalimentación total se calcula como la diferencia entre G3 y G4. Para simplificar este lazo, utilizamos la siguiente fórmula:

**Ganancia Total del Sistema = Ganancia Directa / (1 + Ganancia Directa * Retroalimentación Total)**

Donde:
- **Ganancia Directa** = Ganancia Paralela = G1 + G2
- **Retroalimentación Total** = (G3 - G4)

Sustituyendo estos valores en la fórmula, obtenemos la expresión para la ganancia total del sistema:

**Ganancia Total del Sistema = (G1 + G2) / [1 + (G1 + G2) * (G3 - G4)]**

---

### Paso 4: Función de transferencia total
Finalmente, la función de transferencia total del sistema es la relación entre la salida C(s) y la entrada R(s), que está dada por la ganancia total del sistema. Por lo tanto, la función de transferencia es:

**C(s) / R(s) = (G1 + G2) / [1 + (G1 + G2) * (G3 - G4)]**

---

## Resultado Final
La función de transferencia total del sistema es:

**C(s) / R(s) = (G1 + G2) / [1 + (G1 + G2) * (G3 - G4)]**

---

## Conclusiones
1. El diagrama de bloques fue simplificado de manera eficiente aplicando las propiedades de combinaciones en paralelo y retroalimentación negativa.
2. El uso de conceptos como **Ganancia Directa** y **Retroalimentación Total** permitió reducir el sistema a una fórmula única, facilitando el análisis.
3. Este método puede aplicarse a sistemas similares con configuraciones de bloques más complejas, siguiendo los pasos de simplificación uno a uno.
4. La función de transferencia obtenida describe cómo la salida C(s) responde a una entrada R(s) considerando todas las interacciones internas del sistema.




# Resolución del Diagrama con la Regla de Mason

## Objetivo
Determinar la función de transferencia total \( Y(s)/X(s) \) del sistema utilizando la **Regla de Mason**.

## Diagrama Inicial

![Diagrama de Flujo de Señal](ruta_del_diagrama) <!-- Sustituye 'ruta_del_diagrama' con el enlace o ruta de la imagen -->

## Solución Paso a Paso

### Paso 1: Identificación de trayectorias hacia adelante
La **Regla de Mason** requiere identificar todas las trayectorias hacia adelante del sistema:

1. **Trayectoria \( P_1 \):**
   \[
   P_1 = G_1 \cdot G_2 \cdot G_3
   \]

### Paso 2: Identificación de lazos individuales
Los **lazos individuales** del sistema son aquellos en los que una señal regresa al mismo nodo sin cruzarse. En este caso:

1. **Lazo \( L_1 \):**
   \[
   L_1 = -G_1 \cdot H_1
   \]

2. **Lazo \( L_2 \):**
   \[
   L_2 = -G_2 \cdot H_2
   \]

3. **Lazo \( L_3 \):**
   \[
   L_3 = -G_3 \cdot H_3
   \]

### Paso 3: Ganancia de trayectorias no tocadas
No hay lazos que sean independientes entre sí (lazos no tocados).

### Paso 4: Determinación del determinante total (\( \Delta \))
El determinante del sistema (\( \Delta \)) se calcula como:

\[
\Delta = 1 - (L_1 + L_2 + L_3)
\]

### Paso 5: Determinante para cada trayectoria (\( \Delta_i \))
Para esta solución, cada \( \Delta_i \) es igual a \( \Delta \), ya que no hay lazos que afecten de forma independiente las trayectorias hacia adelante.

### Paso 6: Función de transferencia total
Usando la fórmula de la **Regla de Mason**:

\[
Y(s)/X(s) = \frac{\sum_{i=1}^N P_i \cdot \Delta_i}{\Delta}
\]

Sustituyendo los valores obtenidos:

\[
Y(s)/X(s) = \frac{P_1}{\Delta}
\]

Sustituyendo \( P_1 \) y \( \Delta \):

\[
Y(s)/X(s) = \frac{G_1 \cdot G_2 \cdot G_3}{1 - (L_1 + L_2 + L_3)}
\]

Sustituyendo los valores de \( L_1, L_2, L_3 \):

\[
Y(s)/X(s) = \frac{G_1 \cdot G_2 \cdot G_3}{1 + G_1 H_1 + G_2 H_2 + G_3 H_3}
\]

---

## Resultado Final
La función de transferencia total del sistema es:

\[
Y(s)/X(s) = \frac{G_1 \cdot G_2 \cdot G_3}{1 + G_1 H_1 + G_2 H_2 + G_3 H_3}
\]

---

## Conclusiones
1. La **Regla de Mason** simplifica la resolución de sistemas representados mediante diagramas de flujo de señal.
2. Este análisis permitió obtener la función de transferencia total considerando todos los lazos de retroalimentación del sistema.
3. La estructura del sistema se respetó, facilitando la identificación de trayectorias hacia adelante y lazos individuales.

---
