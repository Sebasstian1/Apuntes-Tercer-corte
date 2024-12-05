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

## Descripción del Sistema

En este ejercicio, tenemos un sistema con tres bloques de ganancia \( G_1 \), \( G_2 \), \( G_3 \), y tres lazos de retroalimentación \( H_1 \), \( H_2 \), \( H_3 \). El objetivo es encontrar la función de transferencia del sistema utilizando la regla de Mason.

### Diagrama de Bloques

El sistema tiene la siguiente estructura:

- **Entrada:** \( X(s) \)
- **Salida:** \( Y(s) \)
- **Bloques de ganancia:** \( G_1 \), \( G_2 \), \( G_3 \)
- **Lazos de retroalimentación:** \( H_1 \), \( H_2 \), \( H_3 \)

El diagrama de bloques muestra las interacciones entre los bloques y los lazos de retroalimentación.

## Regla de Mason

La regla de Mason se utiliza para calcular la función de transferencia \( G(s) \) de un sistema con retroalimentación. La fórmula general para la función de transferencia es la siguiente:

**Función de Transferencia General:**

La función de transferencia \( G(s) \) de un sistema con retroalimentación se obtiene con la siguiente fórmula:

1. El **numerador** es la suma de las ganancias de las rutas directas (del origen de la entrada hasta la salida), considerando todos los lazos de retroalimentación.
   
2. El **denominador** es 1 más la suma de los productos de cada lazo de retroalimentación que afecta al sistema, considerando las interacciones de los bloques de ganancia con los lazos de retroalimentación.

### Numerador

El numerador de la función de transferencia está compuesto por las rutas directas desde la entrada \( X(s) \) hasta la salida \( Y(s) \), considerando las interacciones de los bloques y los lazos de retroalimentación. Para este sistema, tenemos dos rutas:

1. La ruta directa que va desde la entrada \( X(s) \) a la salida \( Y(s) \) pasando por los tres bloques \( G_1 \), \( G_2 \), y \( G_3 \).
2. La ruta que pasa solo por los bloques \( G_1 \) y \( G_3 \).

Por lo tanto, el numerador es la suma de las siguientes rutas:

- \( G_1 G_2 G_3 \)
- \( G_1 G_3 \)

### Denominador

El denominador se obtiene considerando los lazos de retroalimentación y sus interacciones. Los términos involucrados son:

1. El primer término corresponde a la interacción de los lazos de retroalimentación \( H_1 \), \( H_2 \), y \( H_3 \).
2. El segundo término es la interacción de los bloques \( G_1 \) y \( G_2 \) con \( H_1 \).
3. El tercer término corresponde a la interacción entre los bloques \( G_2 \) y \( G_3 \) con los lazos de retroalimentación \( H_2 \) y \( H_3 \).
4. El cuarto término involucra la interacción de todos los bloques y lazos de retroalimentación \( H_1 \), \( H_2 \), y \( H_3 \).

Por lo tanto, el denominador se expresa como la suma de los siguientes términos:

- 1
- \( G_2 H_2 \)
- \( G_3 H_3 \)
- \( G_1 G_2 H_1 \)
- \( G_2 G_3 H_2 H_3 \)
- \( G_1 G_2 G_3 H_1 H_2 H_3 \)

### Función de Transferencia Final

Finalmente, la función de transferencia del sistema es la relación entre el numerador y el denominador. Se puede escribir de la siguiente forma:

**Función de Transferencia:**

\[
G(s) = \frac{G_1 G_2 G_3 + G_1 G_3}{1 + G_2 H_2 + G_3 H_3 + G_1 G_2 H_1 + G_2 G_3 H_2 H_3 + G_1 G_2 G_3 H_1 H_2 H_3}
\]

Este es el resultado final de la función de transferencia utilizando la regla de Mason.



