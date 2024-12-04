# Resolución de Diagrama de Bloques

## Objetivo
Determinar la función de transferencia total \( C(s)/R(s) \) del sistema dado.

## Diagrama Inicial
*(Incluye aquí el diagrama de bloques proporcionado como una imagen).*

---

## Solución Paso a Paso

### Paso 1: Identificación de elementos clave
En este sistema, los elementos clave son:
- **Entrada**: R(s), la señal de entrada.
- **Salida**: C(s), la señal de salida.
- **Bloques individuales**:
  - \( G_1 \): Bloque directo desde R(s) hacia la salida.
  - \( G_2 \): Bloque paralelo a \( G_1 \).
  - \( G_3 \): Bloque que conecta \( G_2 \) con la retroalimentación.
  - \( G_4 \): Bloque en el lazo de retroalimentación negativa.

---

### Paso 2: Simplificación de las ramas paralelas
Los bloques \( G_1 \) y \( G_2 \) están en una configuración de ramas paralelas. Para combinar estos bloques, sumamos sus ganancias. El bloque equivalente a la configuración en paralelo se denomina **Ganancia Paralela**. Esto simplifica la combinación de los dos bloques en uno solo.

---

### Paso 3: Análisis del lazo de retroalimentación
El sistema tiene un lazo de retroalimentación negativa, que involucra los bloques \( G_3 \) y \( G_4 \). La retroalimentación negativa afecta la función de transferencia del sistema. La retroalimentación total se calcula multiplicando las ganancias \( G_3 \) y \( G_4 \), y luego combinándola con la ganancia paralela de los bloques \( G_1 \) y \( G_2 \).

---

### Paso 4: Función de transferencia total
La función de transferencia del sistema se obtiene dividiendo la ganancia paralela (es decir, la suma de \( G_1 \) y \( G_2 \)) por una expresión que incluye tanto la ganancia paralela como la retroalimentación total. Esta fórmula describe cómo la salida \( C(s) \) responde a la entrada \( R(s) \), considerando la interacción de los bloques dentro del sistema.

---

## Resultado Final
La función de transferencia total del sistema se obtiene como resultado de la simplificación de los bloques en paralelo y la retroalimentación negativa.

---

## Conclusiones
1. El diagrama de bloques se simplificó de manera eficiente aplicando las propiedades de combinación de bloques en paralelo y retroalimentación negativa.
2. La función de transferencia obtenida muestra cómo la salida \( C(s) \) se relaciona con la entrada \( R(s) \), teniendo en cuenta las interacciones dentro del sistema.
3. Este proceso de simplificación es útil para sistemas más complejos, permitiendo un análisis más directo de su comportamiento.
4. El método puede ser aplicado a cualquier sistema con configuraciones de bloques similares para obtener la función de transferencia total de manera clara y estructurada.
