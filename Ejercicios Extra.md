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

\[
G_{\text{paralela}} = G_1 + G_2
\]

Esto crea un único bloque equivalente denominado **Ganancia Paralela**.

---

### Paso 3: Análisis del lazo de retroalimentación
El sistema incluye un lazo de retroalimentación negativa con los bloques \( G_3 \) y \( G_4 \). La retroalimentación se conecta de forma que la expresión para la ganancia total del sistema es:

\[
G_{\text{retroalimentación}} = 1 + (G_1 + G_2) \cdot G_3 \cdot G_4
\]

---

### Paso 4: Función de transferencia total
La función de transferencia total del sistema en lazo cerrado con retroalimentación negativa es:

\[
\frac{C(s)}{R(s)} = \frac{G_1 + G_2}{1 + (G_1 + G_2) \cdot G_3 \cdot G_4}
\]

---

## Resultado Final
La función de transferencia total es:

\[
\frac{C(s)}{R(s)} = \frac{G_1 + G_2}{1 + (G_1 + G_2) \cdot G_3 \cdot G_4}
\]

---

## Conclusiones
1. El diagrama de bloques fue simplificado de manera eficiente aplicando las propiedades de combinaciones en paralelo y retroalimentación negativa.
2. La fórmula obtenida para la función de transferencia describe cómo la salida \( C(s) \) responde a una entrada \( R(s) \), considerando todas las interacciones internas del sistema.
3. Este proceso puede aplicarse a otros sistemas con configuraciones similares para obtener la función de transferencia total de manera clara y estructurada.
