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

**G_paralela = G1 + G2**

Esto crea un único bloque equivalente, denominado **G_paralela**.

---

### Paso 3: Análisis del lazo de retroalimentación
El sistema incluye un lazo de retroalimentación negativa con los bloques G3 y G4. Para simplificar este lazo, usamos la fórmula:

**G_retro = G_directa / (1 + G_directa * G_feedback)**

En este caso:
- G_directa = G_paralela
- G_feedback = G3 * G4

Sustituyendo, obtenemos:

**G_retro = (G1 + G2) / [1 + (G1 + G2) * G3 * G4]**

---

### Paso 4: Función de transferencia total
Finalmente, la función de transferencia total del sistema es:

**C(s) / R(s) = (G1 + G2) / [1 + (G1 + G2) * G3 * G4]**

---

## Resultado Final
La función de transferencia total es:

**C(s) / R(s) = (G1 + G2) / [1 + (G1 + G2) * G3 * G4]**

---

## Notas
- Este procedimiento detalla cada paso necesario para simplificar el diagrama de bloques.
- El resultado es simbólico y puede adaptarse a sistemas similares modificando los valores de G1, G2, G3 y G4.
