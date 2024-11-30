# Función de Transferencia

La función de transferencia es una herramienta fundamental en el análisis de sistemas dinámicos. Representa la relación entre la salida y la entrada de un sistema lineal e invariante en el tiempo (LTI) en el dominio de Laplace. Esta herramienta permite analizar la estabilidad, respuesta en frecuencia y el comportamiento global del sistema.

## 1. Clasificación de las Funciones de Transferencia

### 1.1 Función de Transferencia Impropia
Una función de transferencia es impropia si el grado del numerador es mayor que el grado del denominador.

### 1.2 Función de Transferencia Bipropia
Una función de transferencia es bipropia si el grado del numerador es igual al grado del denominador.

### 1.3 Función de Transferencia Estrictamente Propia
Una función de transferencia es estrictamente propia si el grado del numerador es menor que el grado del denominador.

## 2. Polos y Ceros

Los polos y ceros de una función de transferencia son esenciales para determinar la respuesta y estabilidad de un sistema.

- **Polos**: Valores de \(s\) que anulan el denominador \(D(s)\), es decir, hacen que \(D(s) = 0\).
- **Ceros**: Valores de \(s\) que anulan el numerador \(N(s)\), es decir, hacen que \(N(s) = 0\).

## 3. Ejemplos

### 💡 Ejemplo 1: Clasificación de Funciones de Transferencia
Determine si las siguientes funciones de transferencia son estrictamente propias, impropias o bipropias:

1. \( G(s) = \frac{s^3 + 2s}{s^2 + 1} \)
2. \( G(s) = \frac{s + 1}{s + 3} \)

**Solución:**

1. Para \( G(s) = \frac{s^3 + 2s}{s^2 + 1} \):
   - El numerador \(N(s)\) tiene un grado de 3.
   - El denominador \(D(s)\) tiene un grado de 2.
   - Como el grado del numerador es mayor que el del denominador (\(3 > 2\)), la función de transferencia es **impropia**.

2. Para \( G(s) = \frac{s + 1}{s + 3} \):
   - El numerador \(N(s)\) tiene un grado de 1.
   - El denominador \(D(s)\) tiene un grado de 1.
   - Como el grado del numerador es igual al del denominador (\(1 = 1\)), la función de transferencia es **bipropia**.

### 💡 Ejemplo 2: Polos y Ceros
Encuentre los polos y ceros de la función \( G(s) = \frac{s^2 + s}{s^2 + 4s + 3} \).

**Solución:**

1. **Ceros:** Los ceros se encuentran resolviendo \(N(s) = 0\):
   \[
   s^2 + s = s(s + 1) = 0 \implies s = 0, -1.
   \]

2. **Polos:** Los polos se encuentran resolviendo \(D(s) = 0\):
   \[
   s^2 + 4s + 3 = (s + 1)(s + 3) = 0 \implies s = -1, -3.
   \]

## 4. Ejercicios

### 📚 Ejercicio 1:
Determine si las siguientes funciones de transferencia son estrictamente propias, impropias o bipropias:

1. \( G(s) = \frac{s^4 + 2s^3}{s^2 + s} \)
2. \( G(s) = \frac{s + 2}{s^3 + s^2} \)

**Solución:**

1. Para \( G(s) = \frac{s^4 + 2s^3}{s^2 + s} \):
   - El numerador \(N(s)\) tiene un grado de 4.
   - El denominador \(D(s)\) tiene un grado de 2.
   - Como el grado del numerador es mayor que el del denominador (\(4 > 2\)), la función de transferencia es **impropia**.

2. Para \( G(s) = \frac{s + 2}{s^3 + s^2} \):
   - El numerador \(N(s)\) tiene un grado de 1.
   - El denominador \(D(s)\) tiene un grado de 3.
   - Como el grado del numerador es menor que el del denominador (\(1 < 3\)), la función de transferencia es **estrictamente propia**.

### 📚 Ejercicio 2:
Encuentre los polos y ceros de la función \( G(s) = \frac{s^3 + s^2}{s^2 + 2s + 1} \).

**Solución:**

1. **Ceros:** Resolviendo \(N(s) = 0\):
   \[
   s^3 + s^2 = s^2(s + 1) = 0 \implies s = 0, 0, -1.
   \]

2. **Polos:** Resolviendo \(D(s) = 0\):
   \[
   s^2 + 2s + 1 = (s + 1)^2 = 0 \implies s = -1, -1.
   \]

## 5. Conclusiones

- La función de transferencia es una herramienta fundamental para analizar sistemas dinámicos.
- La clasificación en estrictamente propias, impropias y bipropias depende de la relación entre los grados del numerador y el denominador.
- Los polos y ceros influyen directamente en la estabilidad y respuesta de un sistema.

## 6. Referencias

- Ogata, K. (2010). *Ingeniería de Control Moderno*. Pearson.
- Dorf, R. C., & Bishop, R. H. (2017). *Sistemas de Control Moderno*. Prentice Hall.
- Documentación de MATLAB: MathWorks.
