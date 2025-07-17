# Integración numérica - Reglas de Newton Cotes
## Ejercicio 1
Sea $\int_0^\frac{\pi}{2} (6+3cos(x))\: \mathrm{d}x$
a) Usar la regla del trapecio para aproximar la solución con n = 2, n = 4
b) Usar la regla de Simpson (1/3) con n = 4
c) Usar la regla de Simpson (3/8) con n = 3, n = 6
### a) Usar la regla del trapecio para aproximar la solución con n = 2, n = 4
La regla del trapecio se basa en aproximar el área bajo la curva mediante trapezoides. La fórmula para la regla del trapecio compuesto es:

$$\int_a^b f(x)\: \mathrm{d}x\approx\frac{h}{2}\left[f(x_0)+2\sum_{i=1}^{n-1}f(x_i)+f(x_n)\right]$$

$$\text{En donde }h=\frac{b-a}{n}$$

#### Con n = 2
1. **Intervalo y paso**: $a = 0, b = \frac{\pi}{2}, n = 2, h = \frac{\pi}{4}$
2. **Puntos y evaluación**
- $x_0=a=0$
- $x_1=x_0+h=\frac{\pi}{4}$
- $x_2=x_1+h=\frac{\pi}{2}$
3. **Evaluación de la función**
- $f(x_0)=6+3cos(0)=6$
- $f(x_1)=6+3cos(\frac{\pi}{4})\approx8.1213203$
- $f(x_2)=6+3cos(\frac{\pi}{2})\approx6$

	Tabla de resultados
	
	$$x_n$|$\text{valor}$|$f(x_n)$
	---|:---:|---:
	$$x_0$|0|9
	$$x_1$|$\frac{\pi}{4}$|8.1213203
	$$x_2$|$\frac{\pi}{2}$|6

4. **Aplicar la formula**

$$\text{Area}=\int_0^\frac{\pi}{2} (6+3cos(x))\: \mathrm{d}x \approx \frac{\pi/4}{2}\left[ f(x_0)+2 * f(x_1)+f(x_2) \right] \approx \frac{\pi}{8}\left[9+2 * 8.1213203+6 \right]\implies$$

$$\implies\color{green}\text{Area}\approx12.26895627$$

#### Con n = 4
1. **Intervalo y paso**: $a = 0, b = \frac{\pi}{2}, n = 4, h = \frac{\pi}{8}$
2. **Puntos y evaluación**
- $x_0=a=0$
- $x_1=x_0+h=\frac{\pi}{8}$
- $x_2=x_1+h=\frac{\pi}{4}$
- $x_3=x_2+h=\frac{3\pi}{8}$
- $x_4=x_3+h=\frac{\pi}{2}$
3. **Evaluación de la función**
- $f(x_0)=6+3cos(0)=6$
- $f(x_1)=6+3cos(\frac{\pi}{8})\approx8.7716385$
- $f(x_2)=6+3cos(\frac{\pi}{4})\approx8.1213203$
- $f(x_3)=6+3cos(\frac{3\pi}{8})\approx7.1480502$
- $f(x_4)=6+3cos(\frac{\pi}{2})\approx6$

	Tabla de resultados
	
	$$x_n$|$\text{valor}$|$f(x_n)$
	---|:---:|---:
	$$x_0$|0|9
	$$x_1$|$\frac{\pi}{4}$|8.7716385
	$$x_2$|$\frac{\pi}{4}$|8.1213203
	$$x_3$|$\frac{3\pi}{8}$|7.1480502
	$$x_4$|$\frac{\pi}{2}$|6

4. **Aplicar la formula**

$$\text{Area}=\int_0^\frac{\pi}{2} (6+3cos(x))\: \mathrm{d}x \approx \frac{\pi/8}{2}\left[ f(x_0)+2 * (f(x_1)+f(x_2)+f(x_3))+f(x_4) \right]\approx \frac{\pi}{16}\left[9+2 * (8.7716385+8.1213203+7.1480502) +6 \right]\implies$$

$$\implies \color{green}Area=12.38612527$$

### b) Usar la regla de Simpson (1/3) con n = 4
La regla de Simpson 1/3 se aplica a intervalos pares y se formula como:

$$\int_a^b f(x)\: \mathrm{d}x\approx\frac{h}{3}\left[f(x_0)+4\sum_{i=1,3,5...}^{n-1}f(x_i)+2\sum_{i=2,4,6...}^{n-2}f(x_i)+f(x_n)\right]$$

#### Con n = 4
1. **Intervalo y paso**: $a=0,b=\frac{\pi}{2},n=4,h=\frac{\pi}{8}$
2. **Puntos y evaluación**: los mismos que en el punto a de la regla del trapecio
- $x_0=a=0$
- $x_1=x_0+h=\frac{\pi}{8}$
- $x_2=x_1+h=\frac{\pi}{4}$
- $x_3=x_2+h=\frac{3\pi}{8}$
- $x_4=x_3+h=\frac{\pi}{2}$
3.  **Evaluación de la función**: los mismos valores que en el punto a de la regla del trapecio
- $f(x_0)=6+3cos(0)=6$
- $f(x_1)=6+3cos(\frac{\pi}{8})\approx8.7716385$
- $f(x_2)=6+3cos(\frac{\pi}{4})\approx8.1213203$
- $f(x_3)=6+3cos(\frac{3\pi}{8})\approx7.1480502$
- $f(x_4)=6+3cos(\frac{\pi}{2})\approx6$

	Tabla de resultados
	
	$$x_n$|$\text{valor}$|$f(x_n)$
	---|:---:|---:
	$$x_0$|0|9
	$$x_1$|$\frac{\pi}{8}$|8.7716385
	$$x_2$|$\frac{\pi}{4}$|8.1213203
	$$x_3$|$\frac{3\pi}{8}$|7.1480502
	$$x_4$|$\frac{\pi}{2}$|6

4. **Aplicar la formula**

$$\text{Area}=\int_0^\frac{\pi}{2} (6+3cos(x))\: \mathrm{d}x\approx \frac{\pi/8}{3}\left[f(x_0)+4(f(x_1)+f(x_3))+2(f(x_2))+f(x_4)\right]\approx \frac{\pi}{24} \left[9+4 * (8.7716385 + 7.1480502) + 2 * 8.1213203 + 6 \right]\implies$$

$$\implies\color{green}Area=12.4251816$$

### c) Usar la regla de Simpson (3/8) con n = 3, n = 6
La regla de Simpson 3/8 se aplica a intervalos múltiplos de 3 y se formula como:

$$\int_a^b f(x)\: \mathrm{d}x \approx \frac{3h}{8} \left[ f(x_0) + 3\sum_{impares}^{}f(x_i) +3\sum_{pares}^{}f(x_i) + 2\sum_{\text{mult. de 3}}^{}f(x_i) + f(x_n)\right]$$

#### n = 3
1. **Intervalo y paso**: $a=0,b=\frac{\pi}{2},n=3,h=\frac{\pi}{6}$
2. **Puntos y evaluación**:
- $x_0 = a = 0$
- $x_1 = x_0 + h =\frac{\pi}{6}$
- $x_2=x_1+h=\frac{\pi}{3}$
- $x_3=x_2+h=\frac{\pi}{2}$
3.  **Evaluación de la función**: 
- $f(x_0)=6+3cos(0)=9$
- $f(x_1)=6+3cos(\frac{\pi}{6}) \approx8.598076$
- $f(x_2)=6+3cos(\frac{\pi}{3})\approx7.5$
- $f(x_3)=6+3cos(\frac{\pi}{2})\approx6$

	Tabla de resultados
	
	$$x_n$|$\text{valor}$|$f(x_n)$
	---|:---:|---:
	$$x_0$|0|9
	$$x_1$|$\frac{\pi}{6}$|8.598076
	$$x_2$|$\frac{\pi}{3}$|7.5
	$$x_3$|$\frac{\pi}{2}$|6

4. **Aplicar la formula**

$$\text{Area}=\int_0^\frac{\pi}{2} (6+3cos(x))\: \mathrm{d}x\approx \frac{3 * \pi/6}{8} \left[ f(x_0) + 3 * (f(x_1)) + 3 * (f(x_2)) + f(x_3) \right] \approx \frac{\pi}{16} \left[9 + 3 * (8.598076) + 3 * (7.5) + 6 \right] \implies$$

$$\implies \color{green}\text{Area}=12.42779261$$

#### n = 6
1. **Intervalo y paso**: $a=0,b=\frac{\pi}{2},n=6,h=\frac{\pi}{12}$
2. **Puntos y evaluación**:
- $x_0 = a = 0$
- $x_1 = x_0 + h =\frac{\pi}{12}$
- $x_2 = x_1 + h =\frac{\pi}{6}$
- $x_3 = x_2 + h =\frac{\pi}{4}$
- $x_4=x_3+h=\frac{\pi}{3}$
- $x_5=x_4+h=\frac{5\pi}{12}$
- $x_6=x_5+h=\frac{\pi}{2}$
3.  **Evaluación de la función**: 
- $f(x_0)=6+3cos(0)=9$
- $f(x_1)=6+3cos(\frac{\pi}{12}) \approx8.897777$
- $f(x_2)=6+3cos(\frac{\pi}{6}) \approx8.598076$
- $f(x_3)=6+3cos(\frac{\pi}{4})\approx8.1213203$
- $f(x_4)=6+3cos(\frac{\pi}{3})\approx7.5$
- $f(x_5)=6+3cos(\frac{5\pi}{12})\approx6.776457$
- $f(x_3)=6+3cos(\frac{\pi}{2})\approx6$

	Tabla de resultados
	
	$$x_n$|$\text{valor}$|$f(x_n)$
	---|:---:|---:
	$$x_0$|0|9
	$$x_1$|$\frac{\pi}{12}$|8.897777
	$$x_2$|$\frac{\pi}{6}$|8.598076
	$$x_3$|$\frac{\pi}{4}$|8.1213203
	$$x_4$|$\frac{\pi}{3}$|7.5
	$$x_5$|$\frac{5\pi}{12}$|6.776457
	$$x_6$|$\frac{\pi}{2}$|6

4. **Aplicar la formula**

$$\text{Area}=\int_0^\frac{\pi}{2} (6+3cos(x))\: \mathrm{d}x\approx \frac{3 * \pi/6}{8} \left[ f(x_0) + 3 * (f(x_1)+f(x_3) + f(x_5)) + 3 (f(x_2) + f(x_4)) + 2 * f(x_3) + f(x_6) )\right] \approx \frac{\pi}{16} \left[9+3 * (8.897777 + 8.1213203 + 6.776457) + 3 * (8.598076 + 7.5) + 2 * (8.1213203) + 6 \right]$$

$$\color{red}\text{Revisar este último, creo que está mal}$$
