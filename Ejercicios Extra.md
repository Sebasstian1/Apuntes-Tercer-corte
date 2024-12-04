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
Los bloques \( G_1 \) y \( G_2 \) están en una configuración de **ramas paralelas**. Para combinarlas, utilizamos la fórmula de suma de ramas paralelas:

\[
G_{\text{paralela}} = G_1 + G_2
\]

Esto crea un único bloque equivalente denominado \( G_{\text{paralela}} \).

---

### Paso 3: Análisis del lazo de retroalimentación
El sistema incluye una **retroalimentación negativa** con los bloques \( G_3 \) y \( G_4 \). Para simplificar este lazo, aplicamos la fórmula de retroalimentación negativa:

\[
G_{\text{retroalimentación}} = \frac{G_{\text{directa}}}{1 + G_{\text{directa}} \cdot G_{\text{retroalimentación}}}
\]

En este caso:
- \( G_{\text{directa}} = G_{\text{paralela}} \).
- \( G_{\text{retroalimentación}} = G_3 \cdot G_4 \).

Sustituyendo, tenemos:

\[
G_{\text{retroalimentación}} = \frac{G_1 + G_2}{1 + (G_1 + G_2) \cdot G_3 \cdot G_4}
\]

---

### Paso 4: Función de transferencia total
Finalmente, la función de transferencia total \( C(s)/R(s) \) es igual a \( G_{\text{retroalimentación}} \):

\[
\frac{C(s)}{R(s)} = \frac{G_1 + G_2}{1 + (G_1 + G_2) \cdot G_3 \cdot G_4}
\]

---

## Resultado Final
La **función de transferencia total** del sistema es:

\[
\frac{C(s)}{R(s)} = \frac{G_1 + G_2}{1 + (G_1 + G_2) \cdot G_3 \cdot G_4}
\]

---

## Notas
- Este procedimiento detalla cada paso necesario para simplificar el diagrama de bloques y encontrar la función de transferencia.
- El resultado es completamente simbólico y puede adaptarse a sistemas similares cambiando los valores de \( G_1, G_2, G_3, \) y \( G_4 \).

