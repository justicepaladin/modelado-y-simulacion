# Polinomio Interpolante de Lagrange, ej3

## Paso 1: Identificar los puntos
Los puntos son:
- $(x_1, y_1) = (0, 1)$
- $(x_2, y_2) = (1, 2)$
- $(x_3, y_3) = (3, 2)$
- $(x_4, y_4) = (4, 3)$
- $(x_5, y_5) = (2, b) \impliedby \text{este es el punto que desconocemos, así que lo dejamos para el final}$

## Paso 2: Construir el polinomio interpolante de Lagrange
### 2a. Polinomio de Lagrange

$$P(x) = \sum_{i=1}^{n} y_i \cdot L_i(x)$$

donde $L_i(x)$ son los términos de Lagrange.

### 2b. Términos de Lagrange
$$L_i(x)=\prod_{\substack{i=1 \\\\ i \ne j}}^{n} \frac{x-x_j}{x_i-x_j}$$
### 2c. ¿Cómo voy a encarar esto?
Acá lo que vamos a hacer es usar los puntos $P_1,P_2,P_3\ \text{y}\ P_4$, ya que de estos conozco sus componentes en x y en y. Por ende, obtendremos un polinomio de Lagrange de grado 3.

## Paso 3: Calcular los términos de Lagrange

### Término $L_1(x)$

$$L_1(x) = \frac{(x-x_2)(x-x_3)(x-x_4)}{(x_1-x_2)(x_1-x_3)(x_1-x_4)}=\frac{(x-1)(x-3)(x-4)}{(0-1)(0-3)(0-4)}=\frac{(x-1)(x-3)(x-4)}{-12}$$

### Término $L_2(x)$

$$L_2(x) = \frac{(x-x_1)(x-x_3)(x-x_4)}{(x_2-x_1)(x_2-x_3)(x_2-x_4)}=\frac{(x-0)(x-3)(x-4)}{(1-0)(1-3)(1-4)}=\frac{x(x-3)(x-4)}{6}$$

### Término $L_3(x)$

$$L_3(x) = \frac{(x-x_1)(x-x_2)(x-x_4)}{(x_3-x_1)(x_3-x_2)(x_3-x_4)}=\frac{(x-0)(x-1)(x-4)}{(3-0)(3-1)(3-4)}=\frac{x(x-1)(x-4)}{-6}$$

### Término $L_4(x)$

$$L_4(x) = \frac{(x-x_1)(x-x_2)(x-x_3)}{(x_4-x_1)(x_4-x_2)(x_4-x_3)}=\frac{(x-0)(x-1)(x-3)}{(4-0)(4-1)(4-3)}=\frac{x(x-1)(x-3)}{12}$$

## Paso 4: armar el polinomio de Lagrange

$$P(x)=y_1L_1(x)+y_2L_2(x)+y_3L_3(x)+y_4L_4(x)$$

En donde $y_1=1,y_2=2,y_3=2,y_4=3$

### Polinomio completo sin simplificar

$$P(x)=-\frac{(x-1)(x-3)(x-4)}{12}+2*\frac{x(x-3)(x-4)}{6}-2*\frac{x(x-1)(x-4)}{6}+3*\frac{x(x-1)(x-3)}{12}$$

No lo desarrollo ahorapara evitar problemas (me había dado mal por error de despeje xdxdxd)
## Paso 5: evaluar en el punto en donde se encuentra la incógnita
Como ya tenemos el polinomio hecho, ahora toca evaluarlo en el punto $(2,b)$, ya que $P(2)=b$

$$P(2)=b=-\frac{(2-1)(2-3)(2-4)}{12}+2*\frac{2(2-3)(2-4)}{6}-2*\frac{2(2-1)(2-4)}{6}+3*\frac{2(2-1)(2-3)}{12} \implies$$

$$\implies b = -\frac{1*(-1) * (-2)}{12}+\frac{2*(-1)(-2)}{3}-\frac{2 * 1 * (-2)}{3}+3*\frac{2 * 1 * (-1)}{12}\implies $$

$$\color{green}{\implies b = 2}$$

$$\text{Ahora que tenemos}\ b=2 \implies \text{Ahora tengo el punto }P_5\ \text{completo}$$

$$P_5=(2,2)$$

## Paso 6: Graficar
### Ahora desarrollo todo el polinomio para simular el gráfico ~~(la concha puta de mi madre)~~

$y_1L_1(x)=-\frac{(x-1)(x-3)(x-4)}{12}=\frac{-x^3+8x^2-19x+12}{12}=\frac{-x^3}{12}+\frac{2x^2}{3}-\frac{19x}{12}+1$

$y_2L_2(x)=2*\frac{x(x-3)(x-4)}{6}=\frac{x(x-3)(x-4)}{3}=\frac{x^3-7x^2+12x}{3}=\frac{x^3}{3}-\frac{7x^2}{3}+4x$

$y_3L_3(x)=-2*\frac{x(x-1)(x-4)}{6}=\frac{-x(x-1)(x-4)}{3}=\frac{-x^3+5x^2-4x}{3}=\frac{-x^3}{3}+\frac{5x^2}{3}-\frac{4x}{3}$

$y_4L_4(x)=3*\frac{x(x-1)(x-3)}{12}=\frac{x^3-4x^2+3x}{4}=\frac{x^3}{4}-x^2+\frac{3x}{4}$

### Ahora junto todos los componentes del polinomio de mierda este

$P(x)=-\frac{x^3}{12}+\frac{2x^2}{3}-\frac{19x}{12}+1+\frac{x^3}{3}-\frac{7x^2}{3}+4x-\frac{x^3}{3}+\frac{5x^2}{3}-\frac{4x}{3}+\frac{x^3}{4}-x^2+\frac{3x}{4}\implies$

$\implies {P(x)=\color{green}-\frac{x^3}{12}+\frac{x^3}{3}-\frac{x^3}{3}+\frac{x^3}{4} \color{blue}+\frac{2x^2}{3}-\frac{7x^2}{3}+\frac{5x^2}{3}-x^2\color{red}-\frac{19x}{12}+4x-\frac{4x}{3}+\frac{3x}{4}}+1\implies$

$$\implies P(x)=\frac{x^3}{6}-x^2+\frac{11x}{6}+1 \impliedby$$

$$\text{Este es el polinomio de Lagrange simplificado}$$

### Ahora si, a graficar
![Ejercicio 3 Lagrange](https://i.imgur.com/5GBX0bX.png)
