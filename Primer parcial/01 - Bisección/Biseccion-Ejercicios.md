# Búsqueda binaria de raíces (Bisección)
## Ejercicio 1
Para cada una de las funciones halle un intervalo $[a, b]$ de manera tal que $f(a)$ y $f(b)$ tengan signo contrario.
### a) $f(x)=e^x-2-x$
#### Paso 1: Identificar un intervalo donde  f(a)  y  f(b)  tengan signo contrario

-   **Elección del intervalo**: Comenzamos probando valores simples. Elegimos $a=0$ y $b=π/2$.
    
-   **Evaluación en los extremos**:
    
    -   $f(0)=cos(0)−0=1−0=1$
        
    -   $f(π/2)=cos(π/2)−(π/2)=0−(π/2)≈−1.5708$
        
-   **Resultado**: $f(0)=1$ y $f(π/2)≈−1.5708$. Tienen signos opuestos.
    

#### Paso 2: Aplicar el método de bisección

-   **Cálculo del punto medio**: $c=(0+π/2)/2=π/4≈0.7854$
    
-   **Evaluación en el punto medio**:
    
    -   $f(π/4)=cos(π/4)−(π/4)≈0.7071−0.7854≈−0.0783$
        
-   **Comparación de signos**:
    
    -   $f(0)=1 (positivo)$
        
    -   $f(π/4)≈−0.0783 (negativo)$
        
-   **Actualización del intervalo**: Dado que $f(a)$ y $f(c)$ tienen signos opuestos, actualizamos $b=c=π/4$.
    

#### Paso 3: Iterar el proceso

-   **Nuevo punto medio**: $c=(0+π/4)/2=π/8≈0.3927$
    
-   **Evaluación en el nuevo punto medio**:
    
    -   $f(π/8)=cos(π/8)−(π/8)≈0.9239−0.3927≈0.5312$
        
-   **Comparación de signos**:
    
    -   $f(π/8)≈0.5312 (positivo)$
        
    -   $f(π/4)≈−0.0783 (negativo)$
        
-   **Actualización del intervalo**: Ahora $f(c)$ y $f(b)$ tienen signos opuestos, así que actualizamos $a=c=π/8$.
    

#### Paso 4: Continuar iterando hasta alcanzar la tolerancia

Repetimos el proceso de calcular el punto medio, evaluar la función y actualizar el intervalo. En cada iteración, el intervalo se reduce a la mitad, acercándonos a la raíz.

#### Conclusión:

El método de bisección converge a una raíz en el intervalo inicial [0,π/2]. La raíz aproximada se encuentra cerca de x≈0.739.
### b) $f(x)=cos(x)+x$
#### Paso 1: Identificar un intervalo donde  f(a)  y  f(b)  tengan signo contrario

-   **Elección del intervalo**: Probamos valores simples. Elegimos $a=−π/2$ y $b=0$.
    
-   **Evaluación en los extremos**:
    
    -   $f(−π/2)=cos(−π/2)+(−π/2)=0−(π/2)≈−1.5708$
        
    -   $f(0)=cos(0)+0=1+0=1$
        
-   **Resultado**: $f(−π/2)≈−1.5708$ y $f(0)=1$. Tienen signos opuestos.
    

#### Paso 2: Aplicar el método de bisección

-   **Cálculo del punto medio**: $c=(−π/2+0)/2=−π/4≈−0.7854$
    
-   **Evaluación en el punto medio**:
    
    -   $f(−π/4)=cos(−π/4)+(−π/4)≈0.7071−0.7854≈−0.0783$
        
-   **Comparación de signos**:
    
    -   $f(−π/2)≈−1.5708 (negativo)$
        
    -   $f(−π/4)≈−0.0783 (negativo)$
        
-   **Actualización del intervalo**: Ambos valores son negativos, así que actualizamos $a=c=−π/4$.
    

#### Paso 3: Iterar el proceso

-   **Nuevo punto medio**: $c=(−π/4+0)/2=−π/8≈−0.3927$
    
-   **Evaluación en el nuevo punto medio**:
    
    -   $f(−π/8)=cos(−π/8)+(−π/8)≈0.9239−0.3927≈0.5312$
        
-   **Comparación de signos**:
    
    -   $f(−π/8)≈0.5312$ $(positivo)$
        
    -   $f(−π/4)≈−0.0783$ $(negativo)$
        
-   **Actualización del intervalo**: Actualizamos $b=c=−π/8$.
    

#### Paso 4: Continuar iterando hasta alcanzar la tolerancia

Repetimos el proceso de calcular el punto medio, evaluar la función y actualizar el intervalo. En cada iteración, el intervalo se reduce a la mitad, acercándonos a la raíz.

#### Conclusión:

El método de bisección converge a una raíz en el intervalo inicial [−π/2,0]. La raíz aproximada se encuentra cerca de x≈−0.739.

### Ejercicios c) y d) pendientes.

## Ejercicio 2

Sea $f(x)=3(x-1)(x-\frac{1}{2})(x-1)$, aplique el método de la búsqueda binaria de raíces en los siguientes intervalos:
### a) $[-1, 1.5]$
#### Paso 1: Verificar el Teorema de Bolzano

-   **Función**: $f(x)=3(x+1)(x−\frac{1}{2})(x−1)$
    
-   **Intervalo**: $[−1,1.5]$
    
-   **Evaluar en los extremos**:
    
    -   $f(−1)=0$
        
    -   $f(1.5)=3.75$
        
-   **Resultado**: $f(−1)=0$ y $f(1.5)=3.75$. No tienen signos opuestos.
    

#### Conclusión:

No se puede aplicar el método de bisección en el intervalo $[−1,1.5]$ ya que no se cumple la condición de Bolzano $(f(a)⋅f(b)<0)$.
### b) $[-1.25, 2.5]$
#### Paso 1: Verificar el Teorema de Bolzano

-   **Función**: $f(x)=3(x+1)(x−21​)(x−1)$
    
-   **Intervalo**: $[−1.25,2.5]$
    
-   **Evaluar en los extremos**:
    
    -   $f(−1.25)≈−3.164$
        
    -   $f(2.5)=31.5$
        
-   **Resultado**: $f(−1.25)≈−3.164$ y $f(2.5)=31.5$. Tienen signos opuestos
- **Procedimiento a seguir**: Se puede aplicar el método de bisección con esta función y este intervalo, ya que se cumple el método de Bolzano $(f(a)⋅f(b)<0)$.
- 
#### Paso 2: Aplicar el método de bisección
| Iteración | a          | b          | c          | f(c)                 | Intervalo Actualizado     |
| --------- | ---------- | ---------- | ---------- | -------------------- | ------------------------- |
| 1         | -1.25      | 2.5        | 0.625      | -0.703125            | \[0.625, 2.5]             |
| 2         | 0.625      | 2.5        | 1.5625     | 4.306640625          | \[0.625, 1.5625]          |
| 3         | 0.625      | 1.5625     | 1.09375    | 1.2353515625         | \[0.625, 1.09375]         |
| 4         | 0.625      | 1.09375    | 0.859375   | 0.1953125            | \[0.625, 0.859375]        |
| 5         | 0.625      | 0.859375   | 0.7421875  | -0.2568359375        | \[0.7421875, 0.859375]    |
| 6         | 0.7421875  | 0.859375   | 0.80078125 | -0.03076171875       | \[0.80078125, 0.859375]   |
| 7         | 0.80078125 | 0.859375   | 0.82907715 | 0.082275390625       | \[0.80078125, 0.82907715] |
| 8         | 0.80078125 | 0.82907715 | 0.8149292  | 0.0257568359375      | \[0.80078125, 0.8149292]  |
| 9         | 0.80078125 | 0.8149292  | 0.80785523 | -0.00250244140625    | \[0.80785523, 0.8149292]  |
| 10        | 0.80785523 | 0.8149292  | 0.81139222 | 0.011626434326171875 | \[0.80785523, 0.81139222] |
#### Conclusión:

El método de bisección converge a una raíz en el intervalo $[−1.25,2.5]$. La raíz aproximada es $x≈0.809$ con una tolerancia de $10^{-4}$.

## Ejercicios 3 - 10 pendientes.