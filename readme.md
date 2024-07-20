# Prueba 1 Mínimos cuadrados

## Cambios realizados:

### Funciones der_parcial_0_exp der_parcial_1_exp der_parcial_2_exp
La función der_parcial_0_exp se cambio por la derivada parcial de f respecto a "a" dando \Sumatoria(x^2(y-ax^2-bx-c)) = 0 </br>
La función der_parcial_1_exp se cambio por la derivada parcial de f respecto a "b" dando \Sumatoria(x(y-ax^2-bx-c)) = 0 </br>
La función der_parcial_1_exp se cambio por la derivada parcial de f respecto a "c" dando \Sumatoria((y-ax^2-bx-c)) = 0 </br>

En código se cambio el c_ind a y, debido a que se despeja la ecuación

### Funcione curva
La función curva fue modificada para usar a2 * x**2 + a1 * x + a0, una función cuadrática</br>
![image.png](./assets/output.png)

# Pregunta 10

## Cambios
### Función calc determinante:
Se utiliza la función descomposición_LU y un ciclo for</br>
L, U  = descomposicion_LU(A)</br>
sumatoria = 1</br>
for i in range(len(U)):</br>
    sumatoria *= U[i][i]</br>
return sumatoria

# Pregunta 12
## Cambios
Lista de cambios realizados </br>
Descripción del cambio 1 (archivo) [líneas] </br>
En las funciones de gauss_jacobi y  gauss_seidel se añadió la lista xs, la cual guarda los valores con xs.append(x.copy()) </br>
también se le añadió al return de np.linalg.norm en ambos: </br>
if np.linalg.norm(x_new - x) < tol: </br>
            return x_new, xs </br>
y se lo retornó en ambas partes. </br>
Descripción del cambio 2 (archivo) [líneas] </br>
Ahora se debía poner las 2 variables a las que debía retornar la función </br>
x, xs = gauss_seidel(A=A, b=b, x0=[1]*n, tol=1e-5, max_iter=1000) </br>
tanto gauss seidel como gauss jacob </br>
Para graficar se usaba esto: </br>
x, y = zip(*xs) </br>
 </br>
new_x = [] </br>
for xi in x: </br>
    new_x.append(float(xi)) </br>
 </br>
new_y = [] </br>
for yi in y: </br>
    new_y.append(float(yi)) </br>
fig, ax = plt.subplots(figsize=(10,7)) </br>
ax.plot(new_x, new_y, color='blue', label='Datos predecidos') </br>
ax.legend() </br>
Se toma xs, se lo hace unzip, luego se transforma sus valores a flotantes para luego pasarlos a plot. </br>
 </br>