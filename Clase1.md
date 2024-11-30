# Función de Transferencia

La función de transferencia es una representación matemática de la relación entre la salida y la entrada de un sistema dinámico, en el dominio de Laplace. Es una herramienta fundamental en el análisis y diseño de sistemas de control, ya que permite estudiar el comportamiento del sistema ante diferentes entradas.

## 1. Tipos de Funciones de Transferencia

### 1.1 Funciones Impropias, Estrictamente Propias y Bipropias

Existen tres tipos principales de funciones de transferencia en cuanto a la relación entre los grados del numerador y el denominador:

- **Función Impropria:** Cuando el grado del numerador es mayor que el grado del denominador.
- **Función Estrictamente Propia:** Cuando el grado del numerador es menor que el grado del denominador.
- **Función Bipropia:** Cuando el grado del numerador es igual al grado del denominador.

#### Ejemplo de Función Impropria
Si tenemos una función de transferencia:

$$
G(s) = \frac{s^3 + 2s}{s^2 + 1}
$$

Aquí, el grado del numerador (3) es mayor que el grado del denominador (2), por lo que esta es una **función impropia**.

#### Ejemplo de Función Bipropia
Si tenemos una función de transferencia:

$$
G(s) = \frac{s + 1}{s + 3}
$$

Aquí, el grado del numerador (1) es igual al grado del denominador (1), por lo que esta es una **función bipropia**.

#### Ejemplo de Función Estrictamente Propia
Si tenemos una función de transferencia:

$$
G(s) = \frac{s}{s^2 + 2s + 3}
$$

Aquí, el grado del numerador (1) es menor que el grado del denominador (2), por lo que esta es una **función estrictamente propia**.

## 2. Polos y Ceros de una Función de Transferencia

Los **ceros** de una función de transferencia son los valores de \( s \) que hacen que el numerador sea igual a cero, mientras que los **polos** son los valores de \( s \) que hacen que el denominador sea igual a cero.

### Ejemplo de Polos y Ceros

Para la función de transferencia:

$$
G(s) = \frac{s^2 + s}{s^2 + 4s + 3}
$$

**Ceros:** Los ceros de la función se encuentran al resolver:

$$
s(s + 1) = 0 \quad \Rightarrow \quad s = 0, -1
$$

**Polos:** Los polos de la función se encuentran al resolver:

$$
(s + 1)(s + 3) = 0 \quad \Rightarrow \quad s = -1, -3
$$

## 3. Ejemplos

### 💡 Ejemplo 1: Clasificación de Funciones de Transferencia

Determina si las siguientes funciones de transferencia son impropias, estrictamente propias o bipropias:

- G(s) = (s^3 + 2s) / (s^2 + 1)  
- G(s) = (s + 1) / (s + 3)  
- G(s) = s / (s^2 + 2s + 3)

**Solución:**
Función Impropria: Para 
𝐺
(
𝑠
)
=
𝑠
3
+
2
𝑠
𝑠
2
+
1
G(s)= 
s 
2
 +1
s 
3
 +2s
​
 , el grado del numerador (3) es mayor que el grado del denominador (2), por lo que esta es una función impropia.

Función Bipropia: Para 
𝐺
(
𝑠
)
=
𝑠
+
1
𝑠
+
3
G(s)= 
s+3
s+1
​
 , el grado del numerador (1) es igual al grado del denominador (1), por lo que esta es una función bipropia.

Función Estrictamente Propia: Para 
𝐺
(
𝑠
)
=
𝑠
𝑠
2
+
2
𝑠
+
3
G(s)= 
s 
2
 +2s+3
s
​
 , el grado del numerador (1) es menor que el grado del denominador (2), por lo que esta es una función estrictamente propia.

### 💡 Ejemplo 2: Cálculo de Polos y Ceros

Encuentra los polos y ceros de la función de transferencia:

$$
G(s) = \frac{s^2 + s}{s^2 + 4s + 3}
$$

**Solución:**

- **Ceros:** \( s(s + 1) = 0  \quad \Rightarrow \quad s = 0, -1 \)
- **Polos:** \( (s + 1)(s + 3) = 0  \quad \Rightarrow \quad s = -1, -3 \)

## 4. Conclusiones

La función de transferencia es una herramienta crucial en el análisis de sistemas dinámicos. Permite identificar y clasificar sistemas en función de su comportamiento. Los polos y ceros son esenciales para determinar la estabilidad y la respuesta del sistema.

## 5. Referencias

- Ogata, K. (2010). *Ingeniería de Control Moderno*. Pearson.
- Dorf, R. C., & Bishop, R. H. (2017). *Sistemas de Control Moderno*. Prentice Hall.
- Documentación de MATLAB: MathWorks.
