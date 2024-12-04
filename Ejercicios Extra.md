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
  - \( G1 \): Bloque directo desde \( R(s) \) hacia la salida.
  - \( G2 \): Bloque paralelo a \( G1 \).
  - \( G3 \): Bloque que conecta \( G2 \) con la retroalimentación.
  - \( G4 \): Bloque en el lazo de retroalimentación negativa.

---

### Paso 2: Simplificación de las ramas paralelas
Los bloques \( G1 \) y \( G2 \) están en una configuración de **ramas paralelas**. Para combinarlas, utilizamos la fórmula de suma de ramas paralelas:

\[
G_{\text{paralela}} = G1 + G2
\]

Esto crea un único bloque equivalente denominado \( Gparalela \).

---

### Paso 3: Análisis del lazo de retroalimentación
El sistema incluye una **retroalimentación negativa** con los bloques \( G3 \) y \( G4 \). Para simplificar este lazo, aplicamos la fórmula de retroalimentación negativa:

\[
G_{\text{retroalimentación}} = \frac{G_{\text{directa}}}{1 + G_{\text{directa}} \cdot G_{\text{retroalimentación}}}
\]

En este caso:
- \( Gdirecta = Gparalela \).
- \( Gretroalimentacion = G3 \cdot G4 \).

Sustituyendo, tenemos:

\[
G_{\text{retroalimentación}} = \frac{G1 + G2}{1 + (G1 + G2) \cdot G3 \cdot G4}
\]

---

### Paso 4: Función de transferencia total
Finalmente, la función de transferencia total \( C(s)/R(s) \) es igual a \( Gretroalimentacion \):

\[
\frac{C(s)}{R(s)} = \frac{G1 + G2}{1 + (G1 + G2) \cdot G3 \cdot G4}
\]

---

## Resultado Final
La **función de transferencia total** del sistema es:

\[
\frac{C(s)}{R(s)} = \frac{G1 + G2}{1 + (G1 + G2) \cdot G3 \cdot G4}
\]

---

## Notas
- Este procedimiento detalla cada paso necesario para simplificar el diagrama de bloques y encontrar la función de transferencia.
- El resultado es completamente simbólico y puede adaptarse a sistemas similares cambiando los valores de \( G1, G2, G3, \) y \( G4 \).

