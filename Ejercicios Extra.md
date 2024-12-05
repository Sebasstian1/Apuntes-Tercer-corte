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

# Resolución de Diagrama de Bloques - Regla de Mason

## Objetivo
Determinar la función de transferencia total G(s) del sistema dado utilizando la regla de Mason.

## Diagrama Inicial

![image](https://github.com/user-attachments/assets/7859b619-e9a8-4b1c-9dc0-bbab6726a391)


## Solución Paso a Paso

### Paso 1: Identificación de elementos clave
El sistema incluye:
- **Entrada**: X(s).
- **Salida**: Y(s).
- **Bloques individuales**:
  - G1: Bloque de ganancia G1.
  - G2: Bloque de ganancia G2.
  - G3: Bloque de ganancia G3.
  - H1: Bloque de retroalimentación H1.
  - H2: Bloque de retroalimentación H2.
  - H3: Bloque de retroalimentación H3.

### Paso 2: Aplicación de la regla de Mason
La regla de Mason establece que la función de transferencia de un sistema con retroalimentación es:

**G(s) = (Suma de productos de las ganancias de los caminos no tocados por un bucle) / (1 + Suma de productos de las ganancias de los caminos tocados por un bucle)**

#### Numerador:
- La primera parte del numerador corresponde al producto de las ganancias de los caminos no tocados por un bucle:
  - **G1 * G2 * G3** y **G1 * G3**.

Por lo tanto, el numerador es:

**G1 * G2 * G3 + G1 * G3**

#### Denominador:
- El denominador corresponde a la suma de los efectos de los bucles:
  - **1**: El término básico.
  - **G2 * H2**: Producto del camino con retroalimentación H2.
  - **G3 * H3**: Producto del camino con retroalimentación H3.
  - **G1 * G2 * H1**: Producto del camino con retroalimentación H1.
  - **G2 * G3 * H2 * H3**: Producto de los caminos con retroalimentación combinada.
  - **G1 * G2 * G3 * H1 * H2 * H3**: Producto de todos los caminos con retroalimentación combinada.

Por lo tanto, el denominador es:

**1 + G2 * H2 + G3 * H3 + G1 * G2 * H1 + G2 * G3 * H2 * H3 + G1 * G2 * G3 * H1 * H2 * H3**

### Paso 3: Función de transferencia total
Finalmente, la función de transferencia total del sistema es la relación entre la salida Y(s) y la entrada X(s), que se obtiene de la fórmula de la regla de Mason. Por lo tanto, la función de transferencia es:

**G(s) = (G1 * G2 * G3 + G1 * G3) / (1 + G2 * H2 + G3 * H3 + G1 * G2 * H1 + G2 * G3 * H2 * H3 + G1 * G2 * G3 * H1 * H2 * H3)**

## Resultado Final
La función de transferencia total del sistema es:

**G(s) = (G1 * G2 * G3 + G1 * G3) / (1 + G2 * H2 + G3 * H3 + G1 * G2 * H1 + G2 * G3 * H2 * H3 + G1 * G2 * G3 * H1 * H2 * H3)**

## Conclusiones
1. El diagrama de bloques fue simplificado utilizando la regla de Mason para obtener la función de transferencia total.
2. El procedimiento ha permitido derivar la ecuación general del sistema de una manera eficiente, considerando los efectos de retroalimentación en los diferentes caminos.
3. Esta metodología es útil para sistemas más complejos que involucran varios bloques y retroalimentaciones, y puede aplicarse a sistemas con configuraciones de bloques más complejas.




