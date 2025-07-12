# Aitken
## Simulación de g(x)
Ejemplo con ejercicio 1: Dada la función $f(x)=\frac{\pi}{2}x^2-x-2$, con $x_0=1.4$, hallar $g(x)$.
```python
import numpy as np
import matplotlib.pyplot as plt

# Función g(x)
def g(x):
    return np.sqrt((2 / np.pi) * (x + 2))

# Método de Aitken
def aitken_acceleration(g, x0, tol=1e-6, max_iter=100):
    x = x0
    iter_values = [x0]
    for i in range(max_iter):
        x1 = g(x)
        x2 = g(x1)
        denominator = x2 - 2 * x1 + x
        if abs(denominator) < 1e-12:
            break  # Evita división por cero
        x_acc = x - (x1 - x)**2 / denominator
        iter_values.append(x_acc)
        if abs(x_acc - x) < tol:
            print("✅ Tolerancia alcanzada en iteración", i + 1)
            return x_acc, iter_values
        x = x_acc
    return x, iter_values

# Ejecutar
x0 = 1.4
root, iter_values = aitken_acceleration(g, x0)

# Gráfico sin errores de LaTeX
x_vals = np.linspace(0, 4, 400)
y_vals = np.sqrt((2 / np.pi) * (x_vals + 2))

plt.figure(figsize=(8, 5))
plt.plot(x_vals, y_vals, label=r'$g(x) = \sqrt{\frac{2}{\pi}(x + 2)}$')  # LaTeX válido
plt.scatter(iter_values, [g(x) for x in iter_values], color='red', zorder=5)
plt.plot(iter_values, [g(x) for x in iter_values], color='red', linestyle='--', zorder=5)
plt.axhline(0, color='black', linewidth=0.5)
plt.axvline(0, color='black', linewidth=0.5)
plt.grid(color='gray', linestyle='--', linewidth=0.5)
plt.title('Método de Aceleración de Aitken')
plt.xlabel('x')
plt.ylabel('g(x)')
plt.legend()
plt.show()

print(f"La raíz aproximada es: {root}")
```

Output:
```
✅ Tolerancia alcanzada en iteración 3
```
![Ejercicio 1 Aitken](https://i.imgur.com/hoLlfZB.png)
```
La raíz aproximada es: 1.4907265051283962
```