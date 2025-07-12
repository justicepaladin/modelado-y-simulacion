# Newton-Raphson
## Gráfico
### Ejemplo con ejercicio 1 de NR
```python
import numpy as np
import matplotlib.pyplot as plt

# Definir la función y su derivada
def f(x):
    return (x - 1)**2

def df(x):
    return 2*(x - 1)

# Puntos de la iteración
x_values = [0, 0.5, 0.75, 0.875]  # x0, x1, x2, x3
y_values = [f(x) for x in x_values]

# Graficar la función
x = np.linspace(-0.5, 2, 400)
plt.plot(x, f(x), label='f(x) = (x - 1)^2')

# Graficar los puntos de iteración
plt.scatter(x_values, y_values, color='red', zorder=5)
plt.plot(x_values, y_values, color='red', linestyle='--', zorder=5)

# Anotar los puntos
for i, x in enumerate(x_values):
    plt.annotate(f'x={x}', (x, f(x)), textcoords="offset points", xytext=(0,10), ha='center')

plt.axhline(0, color='black', linewidth=0.5)
plt.axvline(0, color='black', linewidth=0.5)
plt.grid(color='gray', linestyle='--', linewidth=0.5)
plt.title('Método de Newton-Raphson para f(x) = (x - 1)^2')
plt.xlabel('x')
plt.ylabel('f(x)')
plt.legend()
plt.show()
```
output:

![Ejercicio 1 NR](https://i.postimg.cc/G2kp7sNf/descarga.png)