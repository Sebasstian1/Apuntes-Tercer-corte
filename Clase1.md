# Función de Transferencia: Conceptos Básicos

En esta clase, exploraremos el concepto de la función de transferencia, una herramienta fundamental en el análisis y diseño de sistemas dinámicos. Entenderemos su definición, su clasificación según el orden de sus polinomios y la relación con polos y ceros, aspectos esenciales para evaluar el comportamiento de un sistema.

---

## 1. Introducción a la Función de Transferencia

🔑 **Definición:** Una *función de transferencia* es la relación matemática que describe cómo un sistema dinámico transforma una entrada en una salida en el dominio de la frecuencia, representada como el cociente de dos polinomios en la variable $s$:
$$
G(s) = \frac{N(s)}{D(s)}
$$
donde $N(s)$ es el numerador (polinomio de ceros) y $D(s)$ es el denominador (polinomio de polos).

---

## 2. Clasificación de la Función de Transferencia

### 2.1 Función de Transferencia Impropria

🔑 **Definición:** Una función de transferencia es *impropria* si el grado del numerador es mayor o igual que el del denominador ($\deg(N(s)) \geq \deg(D(s))$).

### 2.2 Función de Transferencia Estrictamente Propia

🔑 **Definición:** Una función de transferencia es *estrictamente propia* si el grado del numerador es menor que el del denominador ($\deg(N(s)) < \deg(D(s))$).

### 2.3 Función de Transferencia Bipropia

🔑 **Definición:** Una función de transferencia es *bipropia* si el grado del numerador es igual al del denominador, pero incluye un término constante adicional para asegurar estabilidad.

---

## 3. Polos y Ceros

🔑 **Definición:** Los *polos* de una función de transferencia son los valores de $s$ que hacen que $D(s) = 0$. Representan la dinámica interna del sistema y determinan su estabilidad.

🔑 **Definición:** Los *ceros* de una función de transferencia son los valores de $s$ que hacen que $N(s) = 0$. Indican las frecuencias donde la respuesta del sistema se anula.

---

## 4. Ejemplos

💡 **Ejemplo 1:** Determine si la función de transferencia siguiente es impropria, estrictamente propia o bipropia:
$$
G(s) = \frac{s^2 + 3s + 5}{s^3 + 2s^2 + 4s + 1}
$$
**Solución:** 
El grado del numerador es 2 y el del denominador es 3, por lo tanto, la función es *estrictamente propia*.

💡 **Ejemplo 2:** Encuentre los polos y ceros de la función de transferencia:
$$
G(s) = \frac{s+3}{s^2 + 5s + 6}
$$
**Solución:**
- Ceros: Resolver $s+3=0$, obtenemos $s = -3$.
- Polos: Resolver $s^2 + 5s + 6 = 0$, obtenemos $s = -2, -3$.

---

## 5. Ecuaciones

💡 **Ejemplo:** Representación general de una función de transferencia:
$$
G(s) = \frac{N(s)}{D(s)}
$$

---

## 6. Figuras

![Figura 1. Polos y ceros en el plano complejo](./imagenes/polos_y_ceros.png)
Figura 1. Representación gráfica de polos y ceros en el plano complejo.

---

## 7. Tablas

| Tipo de Función         | Condición Matemática          | Ejemplo                               |
|-------------------------|------------------------------|---------------------------------------|
| Impropria              | $\deg(N(s)) \geq \deg(D(s))$ | $G(s) = \frac{s^3}{s^2+1}$           |
| Estrictamente Propia   | $\deg(N(s)) < \deg(D(s))$    | $G(s) = \frac{1}{s+1}$               |
| Bipropia               | $\deg(N(s)) = \deg(D(s))$    | $G(s) = \frac{s+2}{s+1}$             |
Tabla 1. Clasificación de funciones de transferencia.

---

## 8. Código

💡 **Ejemplo de código: Polos y ceros en MATLAB**
```matlab
% Definición de la función de transferencia
num = [1 3]; % Coeficientes del numerador
den = [1 5 6]; % Coeficientes del denominador
sys = tf(num, den);

% Cálculo de polos y ceros
poles = pole(sys);
zeros = zero(sys);

% Visualización en el plano complejo
pzmap(sys);
grid on;

