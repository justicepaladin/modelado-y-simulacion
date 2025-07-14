# Polinomios interpolantes de Lagrange
## Ejercicio 1
Hallar el polinomio que pasa por los puntos $(1,1),(2,4),(3,9)$. Luego, graficar la función con su polinomio interpolante.
### Paso 1: identificar los puntos
Los puntos dados son los siguientes:
- Punto 1: $(x_1,y_1)=(1,1)$
- Punto 2: $(x_2,y_2)=(2,4)$
- Punto 3: $(x_3,y_3)=(3,9)$
### Paso 2: construir los términos de Lagrange
El polinomio interpolante de Lagrange se construye como:

$$P(x)=\sum_{i=1}^{n} y_i*L_i(x)$$

En donde $L_i(x)$ son los términos de Lagrange, y n la cantidad de puntos.
Para cada punto $x_i$, el término de Lagrange $L(x)$ se construye de la siguiente forma:

$$L_i(x)=\prod_{\substack{i=1 \\\\ i \ne j}}^{n} \frac{x-x_j}{x_i-x_j}$$

#### Término L_1(x) para el punto 1
$$L_1(x)=\frac{(x-x_2)(x-x_3)}{(x_1-x_2)(x_1-x_3)}=\frac{(x-2)(x-3)}{(1-2)(1-3)}=\frac{(x-2)(x-3)}{2}$$
#### Término L_2(x) para el punto 2
$$L_2(x)=\frac{(x-x_1)(x-x_3)}{(x_2-x_1)(x_2-x_3)}=\frac{(x-1)(x-3)}{(2-1)(2-3)}=\frac{(x-1)(x-3)}{-1}$$
#### Término L_3(x) para el punto 3
$$L_3(x)=\frac{(x-x_1)(x-x_2)}{(x_3-x_1)(x_3-x_2)}=\frac{(x-1)(x-2)}{(3-1)(3-2)}=\frac{(x-1)(x-2)}{2}$$
### Paso 3: combinar los términos y armar el polinomio
El polinomio interpolante de Lagrange $P(x)$ es: 

$$P(x)=y_1 L_1(x) + y_2 L_2(x) + y_3 L_3(x)\implies reemplazo\ por\ valores\ obtenidos$$

$$\implies P(x)=1*\frac{(x-2)(x-3)}{2}+4*\frac{(x-1)(x-3)}{-1}+9*\frac{(x-1)(x-2)}{2}$$

#### Simplificación de términos
##### Término 1
$$1*\frac{(x-2)(x-3)}{2}=\frac{x^2-5x+6}{2}$$
##### Término 2
$$4*\frac{(x-1)(x-3)}{-1}=-4(x^2-4x+3)=-4x^2+16x-12$$
##### Término 3
$$9*\frac{(x-1)(x-2)}{2}=\frac{9(x^2-3x+2)}{2}$$
#### Combinación de todos los términos
$$P(x)=\frac{x^2-5x+6}{2}-4x^2+16x-12+\frac{9(x^2-3x+2)}{2} \implies$$
$$\implies P(x)=\frac{x^2-5x+6-8x^2+32x-24+9x^2-27x+18}{2} \implies$$
$$\implies P(x)=\frac{(1-8+9)x^2+(-5+32-27)x+(6-24+18)}{2}\implies$$
$$\implies P(x) = \frac{2x^2+0x+0}{2} = x^2$$
### Paso 4: verificar el resultado
El polinomio interpolante es $P(x)=x^2$, que pasa por los puntos (1,1),(2,4),(3,9).
### Paso 5: gráfico
![Ejercicio 1 Lagrange](https://i.imgur.com/csD5QZN.png)

## Ejercicio 9
Aproximar $f(x)=sin(x)$ con $x\ \epsilon \ [0,\pi]$. Use un polinomio de Lagrange de grado 2.
### Paso 1: definición de puntos
- $x_1=0$
- $x_2=\frac{\pi}{2}$
- $x_3=\pi$

Ahora, evalúo en $y$
- $y_1=f(x_1)=sin(0)=0$
- $y_2=f(x_2)=sin(\frac{\pi}{2})=1$
- $y_3=f(x_3)=sin(\pi)=0$
#### Puntos por los cuales pasa el polinomio
- $P_1=(0,0)$
- $P_2=(\frac{\pi}{2},1)$
- $P_3=(\pi,0)$

### Paso 2: construir los términos de Lagrange
El polinomio interpolante de Lagrange se construye como:

$$P(x)=\sum_{i=1}^{n} y_i*L_i(x)$$

En donde $L_i(x)$ son los términos de Lagrange, y n la cantidad de puntos.
Para cada punto $x_i$, el término de Lagrange $L(x)$ se construye de la siguiente forma:

$$L_i(x)=\prod_{\substack{i=1 \\\\ i \ne j}}^{n} \frac{x-x_j}{x_i-x_j}$$

#### Término $L_1(x)$ para el punto 1
$$L_1(x)=\frac{(x-x_2)(x-x_3)}{(x_1-x_2)(x_1-x_3)} = \frac{(x-\frac{\pi}{2})(x-\pi)}{(-\frac{\pi}{2})(-\pi)}=\frac{(x-\frac{\pi}{2})(x-\pi)}{\frac{\pi^2}{2}}$$
Despeje final:
$$L_1(x)=\frac{2((x-\frac{\pi}{2})(x-\pi))}{\pi^2}$$
#### Término $L_2(x)$ para el punto 2
$$L_2(x)=\frac{(x-x_1)(x-x_3)}{(x_2-x_1)(x_2-x_3)}=\frac{(x-0)(x-\pi)}{(\frac{\pi}{2})(-\frac{\pi}{2})}=\frac{x(x-\pi)}{-\frac{\pi^2}{4}}=\frac{4x(x-\pi)}{\pi^2}$$
Despeje final
$$L_2(x)=-\frac{4x(x-\pi)}{\pi^2}$$
#### Término $L_3(x)\ \text{para el punto 3}$
$$L_3(x)=\frac{(x-x_1)(x-x_2)}{(x_3-x_1)(x_3-x_2)}=\frac{(x-0)(x-\frac{\pi}{2})}{\pi(\pi-\frac{\pi}{2})}=\frac{x(x-\frac{\pi}{2})}{\pi^2-\frac{\pi^2}{2}}$$
Despeje final:
$$L_3(x)=\frac{x(x-\frac{\pi}{2})}{\frac{\pi^2}{2}}=\frac{2x(x-\frac{\pi}{2})}{\pi^2}$$
#### Observación
Hice que los denominadores de los tres términos coincidan, algo que va a facilitar al armado del polinomio
### Paso 3: Armado del polinomio de lagrange
El polinomio interpolante de Lagrange $P(x)$ es:

$$P(x)=y_1 L_1(x) + y_2 L_2(x) + y_3 L_3(x)\implies \text{reemplazo por lo obtenido}$$

$$\text{recordar que}\
\begin{cases}
y_1=0\\\\y_2=1\\\\y_3=0
\end{cases}
$$

$$\implies P(x)=L_2(x) \implies P(x)= -\frac{4x(x-\pi)}{\pi^2}$$

### Paso 4: gráfico
![Ejercicio 9 de Lagrange](https://i.imgur.com/UeZK4fG.png)

