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