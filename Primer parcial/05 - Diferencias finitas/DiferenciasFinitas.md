# Diferencias finitas
## Ejercicio 1
Use diferencias finitas centrales para hallar la derivada aproximada de $f(x)=sin(x)$, en cada punto de x = [0, 0.1, 0.2, 0.3, 0.4, 0.5], con h = 0.1.
### Datos
- $f(x)=sin(x)$
- $\text{Puntos }x = [0, 0.1, 0.2, 0.3, 0.4, 0.5]$
- $h=0.1$
- $\text{Nota: se trabaja con Radianes.}$
- $\text{Nota 2: uso hasta 6 decimales.}$
### Formula de diferencias finitas
$$f'(x) \approx \frac{f(x+h)-f(x-h)}{2h}$$
### Paso 1: realización de los cálculos
#### Para x = 0
- x + h = 0 + 0.1 = 0.1
- x - h = 0 - 0.1 = -0.1
- $f(0.1)=sin(0.1)$
- $f(-0.1)=sin(-0.1)$
- $f'(0) \approx \frac{sin(0.1)-sin(-0.1)}{2 * 0.1} \approx 0.998334$
#### Para x = 0.1
- x + h = 0.1 + 0.1 = 0.2
- x - h = 0.1 - 0.1 = 0
- $f(0.2)=sin(0.2)$
- $f(0)=sin(0)$
- $f'(0.1) \approx \frac{sin(0.2)-sin(0)}{2 * 0.1} \approx 0.993347$
#### Para x = 0.2
- x + h = 0.2 + 0.1 = 0.3
- x - h = 0.2 - 0.1 = 0.1
- $f(0.3)=sin(0.3)$
- $f(0.1)=sin(0.1)$
- $f'(0.2) \approx \frac{sin(0.3)-sin(0.1)}{2 * 0.1} \approx 0.978434$
#### Para x = 0.3
- x + h = 0.3 + 0.1 = 0.4
- x - h = 0.3 - 0.1 = 0.2
- $f(0.4)=sin(0.4)$
- $f(0.2)=sin(0.2)$
- $f'(0.3) \approx \frac{sin(0.4)-sin(0.2)}{2 * 0.1} \approx 0.953745$
#### Para x = 0.4
- x + h = 0.4 + 0.1 = 0.5
- x - h = 0.4 - 0.1 = 0.3
- $f(0.5)=sin(0.5)$
- $f(0.3)=sin(0.3)$
- $f'(0.4) \approx \frac{sin(0.5)-sin(0.3)}{2 * 0.1} \approx 0.919527$
#### Para x = 0.5
- x + h = 0.5 + 0.1 = 0.6
- x - h = 0.5 - 0.1 = 0.4
- $f(0.6)=sin(0.6)$
- $f(0.4)=sin(0.4)$
- $f'(0.5) \approx \frac{sin(0.6)-sin(0.4)}{2 * 0.1} \approx 0.87612$
### Paso 2: interpretación
Los valores obtenidos son aproximaciones de la derivada de $sin(x)$, que en realidad es $cos(x)$. Los resultados deberían acercarse a los valores exactos de $cos(x)$ en cada punto.
### Paso 3: comparación con la derivada exacta
$x$|$f'(x)$|$cos(x)$
---|:---:|---:
0|0.998334|1
0.1|0.993347|0.995004
0.2|0.978434|0.980067
0.3|0.953745|0.955336
0.4|0.919527|0.921061
0.5|0.87612|0.877583
## Ejercicio 4
Dada la función $f(x)=e^xsin(x)$
a) Hallar $f'(1)$ usando diferencias finitas centrales y h = 0.01
b) Hallar el error absoluto
c) Hallar $f''(1)$ usando diferencias finitas centrales
### a) Hallar $f'(1)$ usando diferencias finitas centrales y h = 0.01
#### Paso 1: defino la función y sus puntos
- $f(x)=e^xsin(x)$
- x = 1
- h = 0.01
#### Paso 2: calcular $f(x+h)$, $f(x-h)$ y $f(x)$
- $x + h = 1 + 0.01 = 1.01$
- $x - h = 1 - 0.01 = 0.99$
- $f(1.01)=e^{1.01}sin(1.01)\approx 2.325062$
- $f(0.99)=e^{0.99}sin(0.99)\approx 2.249941$
- $f(1)=e^1sin(1)$
#### Paso 3: aplicar la formula de diferencias finitas centradas y realizar el cálculo
$$f'(x) \approx \frac{f(x+h)-f(x-h)}{2h} \implies$$
$$\implies f'(1) \approx \frac{f(1.01)-f(0.99)}{2 * 0.01}  \approx \frac{e^{1.01}sin(1.01)-e^{0.99}sin(0.99)}{2 * 0.01}\approx \frac{2.325062 - 2.249941}{0.02}\implies$$
$$\implies \color{green}f'(1)\approx 3.75605$$
### b) Hallar el error absoluto
#### Paso 1: calcular el valor exacto de $f'(1)$
Derivada analítica anashe:
$$f'(x)= e^{x}sin(x)+e^{x}cos(x)$$
Ahora calculo $f'(1)$
$$f'(1)= e^{1}sin(1)+e^{1}cos(1)\approx 3.756049$$
#### Paso 2: calcular el error absoluto
$$E=|f'(\text{x exacto})-f'(\text{x aproximado})| = |3.756049-3.75605|=\color{green}0.000001$$
### c) Hallar $f''(1)$ usando diferencias finitas centrales
#### Paso 1: defino la función y sus puntos
- $f(x)=e^xsin(x)$
- x = 1
- h = 0.01
#### Paso 2: calcular $f(x+h)$, $f(x-h)$ y $f(x)$
- $x + h = 1 + 0.01 = 1.01$
- $x - h = 1 - 0.01 = 0.99$
- $f(1.01)=e^{1.01}sin(1.01)\approx 2.325062$
- $f(0.99)=e^{0.99}sin(0.99)\approx 2.249941$
- $f(1)=e^1sin(1)\approx2.287355$
#### Paso 3: aplicar la Formula de diferencias finitas centradas para la segunda derivada y realizar el cálculo
$$f''(x)\approx \frac{f(x+h)-2f(x)+f(x-h)}{h^2}\implies$$
$$\implies f''(1)\approx \frac{f(1.01)-2f(1)+f(0.99)}{(0.01)^2}\approx\frac{e^{1.01}sin(1.01)-2 * e^1sin(1)+e^{0.99}sin(0.99)}{(0.01)^2}\approx\frac{2.325062-2 * 2.287355+2.249941}{(0.01)^2}\implies$$
$$\implies \color{green}f''(1)\approx2.93$$
