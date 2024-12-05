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
Determinar la función de transferencia total **Y(s)/X(s)** del sistema utilizando la **Regla de Mason**.

---

## Diagrama Inicial

![Diagrama de Bloques](ruta-del-diagrama.png)

---

## Solución Paso a Paso

### Paso 1: Identificación de trayectorias hacia adelante
Las trayectorias hacia adelante son las rutas que conectan la entrada X(s) con la salida Y(s) sin regresar a un nodo previo:

- Trayectoria P1: G1 × G2 × G3.

---

### Paso 2: Identificación de lazos individuales
Los lazos individuales son aquellos en los que una señal regresa al mismo nodo. Para este sistema, los lazos son:

1. Lazo L1: - G1 × H1  
2. Lazo L2: - G2 × H2  
3. Lazo L3: - G3 × H3

---

### Paso 3: Determinante total (Δ)
El determinante del sistema, que se representa como Δ, se calcula con la fórmula:

Δ = 1 - (Suma de los lazos individuales)

Sustituyendo los valores de los lazos:

Δ = 1 + (G1 × H1) + (G2 × H2) + (G3 × H3)

---

### Paso 4: Determinante para cada trayectoria (Δi)
En este caso, no hay lazos independientes entre las trayectorias hacia adelante, por lo que:

Δ1 = Δ

---

### Paso 5: Función de transferencia total
La función de transferencia total se obtiene usando la fórmula general de la **Regla de Mason**:

Y(s)/X(s) = (Suma de cada trayectoria hacia adelante (Pi) × Δi) / Δ

Para este sistema:

Y(s)/X(s) = (P1 × Δ1) / Δ

Sustituyendo P1 y Δ1:

Y(s)/X(s) = (G1 × G2 × G3) / Δ

Finalmente, sustituyendo el valor de Δ:

Y(s)/X(s) = (G1 × G2 × G3) / [1 + (G1 × H1) + (G2 × H2) + (G3 × H3)]

---

## Resultado Final
La función de transferencia total del sistema es:

Y(s)/X(s) = (G1 × G2 × G3) / [1 + (G1 × H1) + (G2 × H2) + (G3 × H3)]

---

## Conclusiones
1. La **Regla de Mason** permite calcular la función de transferencia de manera sistemática.
2. En este sistema, los lazos de retroalimentación agregan términos al denominador, que representan sus efectos acumulativos.
3. Este análisis asegura que todas las trayectorias y lazos sean considerados de forma adecuada.

---

### Notas:
- Reemplaza `ruta-del-diagrama.png` con la URL o ubicación exacta del diagrama en tu repositorio.


