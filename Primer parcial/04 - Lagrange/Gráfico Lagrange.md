# Polinomios interpolantes de Lagrange
## Gráfico
### Ejemplo con ejercicio 1 de Lagrange
```python
import numpy as np
import matplotlib.pyplot as plt

# Definir los puntos
x = np.array([1,2,3])
y = np.array([1,4,9])

# Construir el polinomio interpolante de Lagrange
def lagrange_polynomial(x, y, x_val):
    n = len(x)
    polynomial = 0.0
    for i in range(n):
        term = y[i]
        for j in range(n):
            if i != j:
                term *= (x_val - x[j]) / (x[i] - x[j])
        polynomial += term
    return polynomial

# Crear un conjunto de valores x para graficar
x_vals = np.linspace(0, 4, 400)
y_pol = [lagrange_polynomial(x, y, xv) for xv in x_vals]

# Graficar el polinomio interpolante
plt.plot(x_vals, y_pol, label='Polinomio interpolante P(x)', color='red', linestyle='--')

# Marcar los puntos interpolados
plt.scatter(x, y, color='green', zorder=5)

# Añadir detalles al gráfico
plt.xlabel('x')
plt.ylabel('y')
plt.title('Polinomio interpolante de Lagrange')
plt.legend()
plt.grid(color='gray', linestyle='--', linewidth=0.5)
plt.show()
```
output:

![Ejercicio 1 Lagrange](https://i.imgur.com/csD5QZN.png)

### Ejemplo con ejercicio 9 de Lagrange (en el caso de que se busque comparar el polinomio con la función real)
```python
import numpy as np
import matplotlib.pyplot as plt

# Definir la función, el polinomio interpolante y los puntos a interpolar
def f(x):
    return np.sin(x)

def P(x):
    return -4 * x * (x - np.pi) / (np.pi ** 2)

def interpol_x():
    return [0, np.pi/2, np.pi]

def interpol_y():
    return [0, 1, 0]

# Crear un conjunto de valores x para graficar
x = np.linspace(0, np.pi, 400)
y = f(x)
y_pol = P(x)

# Graficar la función original y el polinomio interpolante
plt.plot(x, y, label='Función original f(x) = sin(x)', color='blue') # Comentar en el caso de que se quiera graficar solo el polinomio
plt.plot(x, y_pol, label='Polinomio interpolante P(x)', color='red', linestyle='--')

# Marcar los puntos interpolationados
plt.scatter(interpol_x(), interpol_y(), color='green', zorder=5)

# Añadir detalles al gráfico
plt.xlabel('x')
plt.ylabel('y')
plt.title('Aproximación de f(x) = sin(x) con polinomio de Lagrange de grado 2')
plt.legend()
plt.grid(color='gray', linestyle='--', linewidth=0.5)
plt.show()
```
output:

![Ejercicio 9 Lagrange](https://i.imgur.com/s8XJxve.png)
