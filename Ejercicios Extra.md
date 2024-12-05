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




# Resolución de Diagrama de Bloques

## Objetivo
Determinar la función de transferencia total \( Y(s)/X(s) \) para el sistema dado en el diagrama.

## Diagrama Inicial

![Diagrama de Bloques](ruta_del_diagrama) <!-- Sustituye 'ruta_del_diagrama' por el enlace o ruta de tu imagen -->

## Solución Paso a Paso

### Paso 1: Identificación de elementos clave
El sistema incluye:
- **Entrada**: \( X(s) \).
- **Salida**: \( Y(s) \).
- **Bloques individuales**:
  - \( G_1, G_2, G_3 \): Bloques de ganancia directa.
  - \( H_1, H_2, H_3 \): Bloques en la retroalimentación negativa.

---

### Paso 2: Simplificación del primer lazo de retroalimentación
La retroalimentación negativa formada por \( G_1 \) y \( H_1 \) se simplifica utilizando la fórmula de retroalimentación:

\[
T_1 = \frac{G_1}{1 + G_1 H_1}
\]

---

### Paso 3: Simplificación del segundo lazo de retroalimentación
La salida del bloque \( G_2 \) tiene una retroalimentación negativa a través de \( H_2 \). Aplicamos la fórmula de retroalimentación nuevamente:

\[
T_2 = \frac{G_2}{1 + G_2 H_2}
\]

---

### Paso 4: Simplificación del tercer lazo de retroalimentación
Finalmente, consideramos el bloque \( G_3 \) con retroalimentación negativa a través de \( H_3 \). La simplificación es:

\[
T_3 = \frac{G_3}{1 + G_3 H_3}
\]

---

### Paso 5: Combinación en serie
Los bloques simplificados \( T_1 \), \( T_2 \), y \( T_3 \) están en serie. La ganancia total del sistema se obtiene multiplicando las transferencias en serie:

\[
Y(s)/X(s) = T_1 \cdot T_2 \cdot T_3
\]

Sustituyendo los valores de \( T_1, T_2, \) y \( T_3 \), tenemos:

\[
Y(s)/X(s) = \frac{G_1}{1 + G_1 H_1} \cdot \frac{G_2}{1 + G_2 H_2} \cdot \frac{G_3}{1 + G_3 H_3}
\]

---

## Resultado Final
La función de transferencia total del sistema es:

\[
Y(s)/X(s) = \frac{G_1}{1 + G_1 H_1} \cdot \frac{G_2}{1 + G_2 H_2} \cdot \frac{G_3}{1 + G_3 H_3}
\]

---

## Conclusiones
1. El sistema se resolvió aplicando las propiedades de retroalimentación negativa y combinaciones en serie.
2. La descomposición paso a paso permitió simplificar el análisis y reducir el diagrama a una función de transferencia única.
3. Este método es útil para analizar sistemas más complejos al dividir el problema en partes manejables.

---



