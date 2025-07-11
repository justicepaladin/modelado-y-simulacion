# Aitken
## Ejercicio 1
Dada la función $f(x)=\frac{\pi}{2}x^2-x-2$, con $x_0=1.4$, hallar $g(x)$.
### Interpretación
El método de Aitken es una técnica numérica utilizada para mejorar la velocidad de convergencia de una secuencia que converge lentamente hacia un límite. En este caso, se utiliza para acelerar la convergencia hacia una raíz de la función dada.
### Paso 1: Transformación de la función
Para aplicar el método de Aceleración de Aitken, primero necesitamos reorganizar la función en la forma $g(x)$, de modo que $x=g(x)$.

Entonces, hacemos $f(x)=0$
$0=\frac{\pi}{2}x^2-x-2$
Se hace el despejo de $x$... 
$\frac{\pi}{2}x^2=x+2$
$x^2=\frac{2}{\pi}(x+2)$
...y obtenemos lo siguiente:
$x=\sqrt{\frac{2}{\pi}(x+2)} \implies$
$\implies Si$ $x=g(x) \implies$
 $\implies g(x)=\sqrt{\frac{2}{\pi}(x+2)}$
 Acá ya tenemos nuestra $g(x)$.
 ### Paso 2: Inicialización de variables
 Comenzamos con un valor inicial $x_0$​. En este caso, $x_0​=1.4$.
 ### Paso 3: Inicio de la secuencia iterativa
 Acá usamos la función $g(x)$ para generar una secuencia de valores de la siguiente forma: 
$x_{n+1}=g(x_n)$ 
### Paso 4: Aplicación de la formula de Aitken
Para cada trío de valores consecutivos ($x_{n},x_{n+1},x_{n+2}$), aplicamos la formula de Aitken: $$x^\ast_n = x_n-\frac{(x_{n+1}-x_n)^2}{x_{n+2}-2x_{n+1}+x_n}$$ Este nuevo valor $x^\ast_n$ converge más rápidamente hacia el límite que la secuencia original.
#### Iteración del proceso
Para seguir iterando, usamos $x^\ast_n$ como el nuevo valor inicial y repetimos el proceso hasta alcanzar la convergencia lineal.
#### Iteraciones (completar)
| Iteración | $x_n$ | $x_{n+1} = g(x_n)$ | $x_{n+2} = g(x_{n+1})$ | $x^*_n$ (Aitken) |
| --------- | ----- | ------------------ | ---------------------- | ---------------- |
| 0         | 1.4   | 1.532              | 1.583                  | 1.587            |
| 1         | 1.587 | 1.583              | 1.587                  | 1.587            |

#### ¿Cuándo re mil poronga dejo de iterar?
Para entender hasta dónde puedo iterar, tengo que tener en cuenta la **tolerancia en el error absoluto**. Entonces, nos detenemos cuando la diferencia entre dos iteraciones consecutivas es **menor que una tolerancia predefinida** (por ejemplo, $ϵ=10^{−6}$) $$|x_{n+1}-x_n|<ϵ$$ Ahora, si tenemos una raíz cerca del cero, podemos usar la **tolerancia en el error relativo**$$\frac{|x_{n+1}-x_n|}{|x_{n+1}|} < ϵ$$Teniendo en cuenta todo esto, en el parcial/final hay que justificar la tolerancia elegida de la siguiente forma: 
*Las iteraciones se detienen cuando $|x_{n+1}-x_n|<10^{-6}$*
### Paso final: gráfico
![Ejercicio 1 Aitken](https://i.imgur.com/hoLlfZB.png)
Un punto es $x_0=1.4$, y el otro es la raíz aproximada utilizando la aceleración de Aitken.
