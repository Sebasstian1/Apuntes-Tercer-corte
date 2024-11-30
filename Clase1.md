# Función de Transferencia: Conceptos Básicos

En esta clase, exploraremos el concepto de la función de transferencia, una herramienta fundamental en el análisis y diseño de sistemas dinámicos. Entenderemos su definición, su clasificación según el orden de sus polinomios y la relación con polos y ceros, aspectos esenciales para evaluar el comportamiento de un sistema.

---

## 1. Introducción a la Función de Transferencia

🔑 **Definición:** Una *función de transferencia* es la relación matemática que describe cómo un sistema dinámico transforma una entrada en una salida en el dominio de la frecuencia, representada como el cociente de dos polinomios en la variable \( s \):  
\[
G(s) = \frac{N(s)}{D(s)}
\]  
donde \( N(s) \) es el numerador (polinomio de ceros) y \( D(s) \) es el denominador (polinomio de polos).

---

## 2. Clasificación de la Función de Transferencia

### 2.1 Función de Transferencia Impropria

🔑 **Definición:** Una función de transferencia es *impropria* si el grado del numerador es mayor o igual que el del denominador (\( \deg(N(s)) \geq \deg(D(s)) \)).

### 2.2 Función de Transferencia Estrictamente Propia

🔑 **Definición:** Una función de transferencia es *estrictamente propia* si el grado del numerador es menor que el del denominador (\( \deg(N(s)) < \deg(D(s)) \)).

### 2.3 Función de Transferencia Bipropia

🔑 **Definición:** Una función de transferencia es *bipropia* si el grado del numerador es igual al del denominador, pero incluye un término constante adicional para asegurar estabilidad.

---

## 3. Polos y Ceros

🔑 **Definición:** Los *polos* de una función de transferencia son los valores de \( s \) que hacen que \( D(s) = 0 \). Representan la dinámica interna del sistema y determinan su estabilidad.

🔑 **Definición:** Los *ceros* de una función de transferencia son los valores de \( s \) que hacen que \( N(s) = 0 \). Indican las frecuencias donde la respuesta del sistema se anula.

---

## 4. Ejemplos

💡 **Ejemplo 1:** Determine si la función de transferencia siguiente es impropria, estrictamente propia o bipropia:  
\[
G(s) = \frac{s^2 + 3s + 5}{s^3 + 2s^2 + 4s + 1}
\]  
**Solución:**  
El grado del numerador es 2 y el del denominador es 3, por lo tanto, la función es *estrictamente propia*.

💡 **Ejemplo 2:** Encuentre los polos y ceros de la función de transferencia:  
\[
G(s) = \frac{s+3}{s^2 + 5s + 6}
\]  
**Solución:**  
- Ceros: Resolver \( s+3=0 \), obtenemos \( s = -3 \).  
- Polos: Resolver \( s^2 + 5s + 6 = 0 \), obtenemos \( s = -2, -3 \).

---

## 9. Ejercicios

📚 **Ejercicio 1:** Determine si las siguientes funciones de transferencia son estrictamente propias, impropias o bipropias:  
1. \( G(s) = \frac{s^3 + 2s}{s^2 + 1} \)  
2. \( G(s) = \frac{s+1}{s+3} \)  

**Solución:**  
1. Impropia (\( \deg(N(s)) = 3, \deg(D(s)) = 2 \)).  
2. Bipropia (\( \deg(N(s)) = \deg(D(s)) = 1 \)).

📚 **Ejercicio 2:** Encuentre los polos y ceros de la función:  
\[
G(s) = \frac{s^2 + s}{s^2 + 4s + 3}
\]  

**Solución:**  
- Ceros: \( s(s+1)=0 \Rightarrow s = 0, -1 \).  
- Polos: \( (s+1)(s+3)=0 \Rightarrow s = -1, -3 \).

---

## 10. Conclusiones

La función de transferencia es una herramienta crucial en el análisis de sistemas dinámicos. Permite identificar y clasificar sistemas en función de su comportamiento. Los polos y ceros son esenciales para determinar la estabilidad y la respuesta del sistema.

---

## 11. Referencias

- Ogata, K. (2010). *Ingeniería de Control Moderno*. Pearson.  
- Dorf, R. C., & Bishop, R. H. (2017). *Sistemas de Control Moderno*. Prentice Hall.  
- Documentación de MATLAB: [MathWorks](https://www.mathworks.com/help/control/)
