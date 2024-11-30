# Función de Transferencia Estable utilizando la Regla de Mason

En este programa se utilizará la **Regla de Mason** para analizar el sistema de control a partir de un diagrama de bloques. Primero, se presenta la estructura básica del sistema, luego se aplican las reglas de Mason para encontrar la función de transferencia.

## 1. Diagrama de Bloques

El sistema tiene dos bloques principales \( G_1(s) \) y \( G_2(s) \), que están conectados a lazos de retroalimentación \( H_1(s) \) y \( H_2(s) \), respectivamente.

**Estructura del Diagrama:**

- **Bloque \( G_1(s) \)** está conectado a un lazo de retroalimentación \( H_1(s) \).
- **Bloque \( G_2(s) \)** está conectado a un lazo de retroalimentación \( H_2(s) \).

### Caminos Directos

En este sistema, hay tres caminos directos:

1. **Camino 1:** \( G_1(s) \)
2. **Camino 2:** \( G_2(s) \)
3. **Camino 3:** \( G_1(s) \cdot G_2(s) \)

### Lazos de Retroalimentación

Los lazos de retroalimentación en este sistema son:

1. **Lazo 1:** \( H_1(s) \)
2. **Lazo 2:** \( H_2(s) \)

---

## 2. Aplicación de la Regla de Mason

La **Regla de Mason** nos permite calcular la función de transferencia total \( T(s) \) del sistema a partir de los caminos y los lazos de retroalimentación identificados.

La fórmula general de la función de transferencia utilizando la Regla de Mason es:

\[
T(s) = \frac{\text{Suma de los productos de los caminos no bloqueados}}{\text{1 - Suma de los lazos de retroalimentación}}
\]

### Paso 1: Identificar los Caminos y Lazos

- **Caminos Directos:**
    - \( G_1(s) \)
    - \( G_2(s) \)
    - \( G_1(s) \cdot G_2(s) \)

- **Lazos de Retroalimentación:**
    - \( H_1(s) \)
    - \( H_2(s) \)

### Paso 2: Aplicar la Regla de Mason

Para obtener la función de transferencia del sistema, se toma el producto de los caminos no bloqueados y se divide entre la suma de los lazos de retroalimentación.

### Fórmulas para cada camino:

- **Camino 1:** \( G_1(s) \)
- **Camino 2:** \( G_2(s) \)
- **Camino 3:** \( G_1(s) \cdot G_2(s) \)

### Lazos de retroalimentación:

- **Lazo 1:** \( H_1(s) \)
- **Lazo 2:** \( H_2(s) \)

---

## 3. Función de Transferencia

La **función de transferencia** total \( T(s) \) será la siguiente:

\[
T(s) = \frac{G_1(s) + G_2(s) + G_1(s) \cdot G_2(s)}{1 - (H_1(s) + H_2(s))}
\]

Donde \( G_1(s) \), \( G_2(s) \), \( H_1(s) \), y \( H_2(s) \) son las funciones de transferencia de los bloques y los lazos de retroalimentación, respectivamente.

---

## 4. Ejemplo Numérico

Supongamos que las funciones de transferencia de los bloques son:

- \( G_1(s) = \frac{5}{s+1} \)
- \( G_2(s) = \frac{3}{s+2} \)

Y los lazos de retroalimentación son:

- \( H_1(s) = \frac{1}{s+3} \)
- \( H_2(s) = \frac{2}{s+4} \)

Sustituyendo estos valores en la fórmula:

\[
T(s) = \frac{\frac{5}{s+1} + \frac{3}{s+2} + \frac{5}{(s+1)(s+2)}}{1 - \left( \frac{1}{s+3} + \frac{2}{s+4} \right)}
\]

Este es el cálculo final de la función de transferencia usando la Regla de Mason.

---

## 5. Conclusión

La **Regla de Mason** es una herramienta poderosa para analizar sistemas de control complejos representados en diagramas de bloques. Nos permite calcular la función de transferencia del sistema a partir de los caminos directos y los lazos de retroalimentación, simplificando el proceso de análisis.

---

**Nota:** Puedes adaptar este programa y los valores de las funciones de transferencia para analizar sistemas más complejos o específicos.
