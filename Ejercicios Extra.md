# Resolución de Diagrama de Bloques

## Objetivo
Determinar la función de transferencia total \( C(s)/R(s) \) del sistema dado.

## Diagrama Inicial
*(Incluye aquí el diagrama de bloques proporcionado como una imagen).*

---

## Solución Paso a Paso

### Paso 1: Identificación de elementos clave
El sistema incluye:
- **Entrada**: \( R(s) \).
- **Salida**: \( C(s) \).
- **Bloques individuales**:
  - \( G_1 \): Bloque directo desde \( R(s) \) hacia la salida.
  - \( G_2 \): Bloque paralelo a \( G_1 \).
  - \( G_3 \): Bloque que conecta \( G_2 \) con la retroalimentación.
  - \( G_4 \): Bloque en el lazo de retroalimentación negativa.

---

### Paso 2: Simplificación de las ramas paralelas
Los bloques \( G_1 \) y \( G_2 \) están en una configuración de ramas paralelas. Para combinarlas, utilizamos la fórmula:

**Ganancia Paralela = \( G_1 + G_2 \)**

Esto crea un único bloque equivalente, denominado **Ganancia Paralela**.

---

### Paso 3: Análisis del lazo de retroalimentación
El sistema incluye un lazo de retroalimentación negativa con los bloques \( G_3 \) y \( G_4 \). Debido a que la retroalimentación es negativa, la ganancia de retroalimentación es \( G_3 - G_4 \).

Usamos la fórmula estándar para la función de transferencia de un sistema con retroalimentación negativa:

\[
H(s) = \frac{G_{\text{paralela}}}{1 + G_{\text{paralela}} \cdot G_{\text{retroalimentación}}}
\]

Donde:
- **Ganancia Directa** = \( G_1 + G_2 \)
- **Retroalimentación Total** = \( G_3 - G_4 \)

Sustituyendo en la fórmula, obtenemos:

\[
H(s) = \frac{G_1 + G_2}{1 + (G_1 + G_2) \cdot (G_3 - G_4)}
\]

---

### Paso 4: Función de transferencia total
Finalmente, la función de transferencia total del sistema es:

\[
\frac{C(s)}{R(s)} = \frac{G_1 + G_2}{1 + (G_1 + G_2) \cdot (G_3 - G_4)}
\]

---

## Resultado Final
La función de transferencia total es:

\[
\frac{C(s)}{R(s)} = \frac{G_1 + G_2}{1 + (G_1 + G_2) \cdot (G_3 - G_4)}
\]

---

## Conclusiones
1. El diagrama de bloques fue simplificado aplicando correctamente las propiedades de combinaciones en paralelo y retroalimentación negativa.
2. La fórmula de la función de transferencia total es clara, usando **Ganancia Directa** \( G_1 + G_2 \) y la **Retroalimentación Total** \( G_3 - G_4 \) para obtener el resultado final.
3. Este método es útil para simplificar sistemas más complejos con retroalimentación negativa, y puede ser adaptado a otros sistemas similares.
4. La función de transferencia obtenida describe cómo la salida \( C(s) \) responde a la entrada \( R(s) \), teniendo en cuenta todas las interacciones dentro del sistema.

---

