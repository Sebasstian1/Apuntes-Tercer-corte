# EJERCICIO 1

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




# EJERCICIO 2

# Ejercicio de la Regla de Mason

## Diagrama de Bloques

El sistema tiene tres bloques \( G_1 \), \( G_2 \), y \( G_3 \), con tres lazos de retroalimentación \( H_1 \), \( H_2 \), y \( H_3 \). El diagrama de bloques es el siguiente:

- \( X(s) \) es la entrada del sistema.
- \( Y(s) \) es la salida del sistema.
- Los lazos de retroalimentación están presentes en los bloques \( G_1 \), \( G_2 \), y \( G_3 \) con \( H_1 \), \( H_2 \), y \( H_3 \), respectivamente.

## Regla de Mason

La **Regla de Mason** se utiliza para encontrar la función de transferencia de un sistema con retroalimentación. La fórmula general es:

**Función de Transferencia:**

La función de transferencia \( G(s) \) se calcula con la siguiente fórmula:

**Numerador:**

El numerador está compuesto por las rutas directas desde la entrada \( X(s) \) hasta la salida \( Y(s) \). En este caso, tenemos dos rutas:

1. La ruta \( G_1 G_2 G_3 \), que pasa por los tres bloques.
2. La ruta \( G_1 G_3 \), que pasa solo por los bloques \( G_1 \) y \( G_3 \).

Por lo tanto, el numerador es:

- \( (G_1 G_2 G_3)(1) + (G_1 G_3)(1) \)

**Denominador:**

El denominador se calcula considerando los lazos de retroalimentación y las interacciones entre los bloques. Se obtiene al sumar los siguientes términos:

1. El primer término es **1**, que corresponde a la entrada del sistema.
2. El segundo término es \( G_2 H_2 \), que corresponde al lazo de retroalimentación de \( G_2 \) y \( H_2 \).
3. El tercer término es \( G_3 H_3 \), que corresponde al lazo de retroalimentación de \( G_3 \) y \( H_3 \).
4. El cuarto término es \( G_1 G_2 H_1 \), que corresponde a la interacción entre \( G_1 \), \( G_2 \), y el lazo de retroalimentación \( H_1 \).
5. El quinto término es \( G_2 G_3 H_2 H_3 \), que corresponde a la interacción entre \( G_2 \), \( G_3 \), y los lazos de retroalimentación \( H_2 \) y \( H_3 \).
6. El sexto término es \( G_1 G_2 G_3 H_1 H_2 H_3 \), que corresponde a la interacción entre todos los bloques y todos los lazos de retroalimentación.

El denominador es:

- \( 1 + G_2 H_2 + G_3 H_3 + G_1 G_2 H_1 + G_2 G_3 H_2 H_3 + G_1 G_2 G_3 H_1 H_2 H_3 \)

**Función de Transferencia Final:**

Finalmente, la función de transferencia del sistema es la relación entre el numerador y el denominador:

- \( G(s) = \frac{(G_1 G_2 G_3)(1) + (G_1 G_3)(1)}{1 + G_2 H_2 + G_3 H_3 + G_1 G_2 H_1 + G_2 G_3 H_2 H_3 + G_1 G_2 G_3 H_1 H_2 H_3} \)

### Notas:
- Reemplaza `ruta-del-diagrama.png` con la URL o ubicación exacta del diagrama en tu repositorio.


