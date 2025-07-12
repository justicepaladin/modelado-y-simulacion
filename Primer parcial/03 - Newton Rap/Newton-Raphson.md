# Newton-Raphson
## Ejercicio 1
Resolver: $f(x)=(x-1)^2$, con $x_0=0$
### Intepretación
El método de Newton-Raphson es un método iterativo utilizado para encontrar raíces de funciones, es decir, valores de $x$ donde la función $f(x)$ se cruza con el eje x $(f(x)=0)$.
### Paso 1: Recordar la formula de Newton-Raphson
$$x_{n+1}=x_n-\frac{f(x_n)}{f'(x_n)}$$
### Paso 2: Obtener $f'(x)$

$$f(x)=(x-1)^2 \implies f'(x)=2(x-1)$$

### Paso 3: comenzar a iterar
Para comprender, muestro las primeras dos iteraciones
#### Iteración $n = 0$
* $x_0 = 0$
* $f(x_0)=(0-1)^2=1$
* $f'(x_0)=2(0-1)=-2$
* con estos dos vaores, obtengo el nuevo valor de $x$, o sea, $x_1$

$$x_1=x_0 - \frac{f(x_0)}{f'(x_0)}=0-\frac{1}{(-2)} \implies x_1 = 0.5$$

#### Iteración $n=1$
* $x_1=0.5$
* $f(x_1)=0.25$
* $f'(x_1)=-1$
* ahora, busco $x_2$
$$x_2=x_1-\frac{f(x_1)}{f'(x_1)} \implies x_2=0.75$$

#### Tabla de todas las iteraciones
| Iteración | $x_n$   | $f(x_n)$     | $f'(x_n)$ | $x_{n+1}$ |
| --------- | ------- | ------------ | --------- | --------- |
| 0         | 0       | 1            | -2        | 0.5       |
| 1         | 0.5     | 0.25         | -1        | 0.75      |
| 2         | 0.75    | 0.0625       | -0.5      | 0.875     |
| 3         | 0.875   | 0.015625     | -0.25     | 0.9375    |
| 4         | 0.9375  | 0.00390625   | -0.125    | 0.96875   |
| 5         | 0.96875 | 0.0009765625 | -0.0625   | 0.984375  |

### Paso 4: observar la convergencia
El método converge hacia $x=1$, pero lo hace lentamente porque la función $f(x)=(x−1)^2$ es convexa y su derivada en el mínimo es cero. Esto hace que el método de Newton-Raphson converja linealmente en este caso (en lugar de cuadráticamente).
### Paso 5: gráfico
![Ejercicio 1 NR](https://i.postimg.cc/G2kp7sNf/descarga.png)