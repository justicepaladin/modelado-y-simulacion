# Polinomio Interpolante de Lagrange, ej3

## Paso 1: Identificar los puntos
Los puntos son:
- $(x_1, y_1) = (0, 1)$
- $(x_2, y_2) = (1, 2)$
- $(x_3, y_3) = (2, b)$
- $(x_4, y_4) = (3, 2)$
- $(x_5, y_5) = (4, 3)$

## Paso 2: Construir el polinomio interpolante de Lagrange
### 2a. Polinomio de Lagrange
$$
P(x) = \sum_{i=1}^{5} y_i \cdot L_i(x)
$$
donde $L_i(x)$ son los términos de Lagrange.

### 2b. Términos de Lagrange

$$L_i(x)=\prod_{\substack{i=1 \\\\ i \ne j}}^{n} \frac{x-x_j}{x_i-x_j}$$

## Paso 3: Calcular los términos de Lagrange

### Término $L_1(x)$

$$L_1(x) = \frac{(x - 1)(x - 2)(x - 3)(x - 4)}{24}$$

### Término $L_2(x)$

$$L_2(x) = \frac{x(x - 2)(x - 3)(x - 4)}{-6}$$

### Término $L_3(x)$

$$L_3(x) = \frac{x(x - 1)(x - 3)(x - 4)}{4}$$

### Término $L_4(x)$

$$L_4(x) = \frac{x(x - 1)(x - 2)(x - 4)}{-6}$$

### Término $L_5(x)$

$$L_5(x) = \frac{x(x - 1)(x - 2)(x - 3)}{24}$$

## Paso 4: armar el polinomio de Lagrange

$$P(x)=y_1L_1(x)+y_2L_2(x)+y_3L_3(x)+y_4L_4(x)+y_5L_5(x)$$

En donde $y_1=1,y_2=2,y_3=b(este\ es\ el\ que\ desconocemos),y_4=2,y_5=3$

**Evito escribir todo el polinomio porque sino todo me queda como un choclo gigante.**

## Paso 5: Evaluar el polinomio en el punto $(2,b)$
Teniendo en cuenta que el polinomio ya está armado, lo que hay que hacer es evaluar en el punto $(2,b)$ para despejar la incógnita $b$.

### $L_1(2)$

$$L_1(2) = \frac{(2 - 1)(2 - 2)(2 - 3)(2 - 4)}{24} \implies$$

$$\implies L_1(2)=0$$

### $L_2(2)$

$$L_2(2) = \frac{2(2 - 2)(2 - 3)(2 - 4)}{-6} = 0$$

### $L_3(2)$

$$L_3(2) = \frac{2(2 - 1)(2 - 3)(2 - 4)}{4} = 1$$

### $L_4(2)$

$$L_4(2) = \frac{2(2 - 1)(2 - 2)(2 - 4)}{-6} = 0$$

### $L_5(2)$

$$L_5(2) = \frac{2(2 - 1)(2 - 2)(2 - 3)}{24} = 0$$

Simplificando cada término:

$$P(2)=1*0+2*0+b*1+2*0+3*0$$

