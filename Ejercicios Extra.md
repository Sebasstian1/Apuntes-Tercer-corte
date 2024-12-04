# Resolución de Diagrama de Bloques

## Objetivo
Determinar la función de transferencia total \( C(s)/R(s) \) del sistema dado.

## Diagrama Inicial
*(Incluye aquí el diagrama de bloques proporcionado como una imagen).*

---

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
Los bloques G1 y G2 están en una configuración de ramas paralelas. Para combinarlas, utilizamos la fórmula:

**Ganancia Paralela = G1 + G2**

Esto crea un único bloque equivalente, denominado **Ganancia Paralela**.

---

### Paso 3: Análisis del lazo de retroalimentación
El sistema incluye un lazo de retroalimentación negativa con los bloques G3 y G4. Para simplificar este lazo, usamos la fórmula:

**Ganancia Total del Sistema = Ganancia Directa / (1 + Ganancia Directa * Retroalimentación Total)**

En este caso:
- **Ganancia Directa** = Ganancia Paralela
- **Retroalimentación Total** = G3 * G4

Sustituyendo, obtenemos:

**Ganancia Total del Sistema = (G1 + G2) / [1 + (G1 + G2) * (G3 * G4)]**

---

### Paso 4: Función de transferencia total
Finalmente, la función de transferencia total del sistema es:

**C(s) / R(s) = (G1 + G2) / [1 + (G1 + G2) * (G3 * G4)]**

---

## Resultado Final
La función de transferencia total es:

**C(s) / R(s) = (G1 + G2) / [1 + (G1 + G2) * (G3 * G4)]**

---

## Notas
- Este procedimiento detalla cada paso necesario para simplificar el diagrama de bloques.
- Los términos han sido simplificados para mayor claridad:
  - **Retroalimentación Total** se refiere a \( G3 \cdot G4 \).
  - **Ganancia Directa** es \( G1 + G2 \).
- Este método es general y puede aplicarse a sistemas similares.
