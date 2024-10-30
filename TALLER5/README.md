# Teoría Cuántica, Observables y Medidas

Autor: Santiago Díaz

## Especificaciones de Librerías

Para el desarrollo de esta tarea fue necesario instalar las siguientes librerías:

1. **Numpy**: Manipulación numérica y arrays multidimensionales.
2. **ipywidgets**: Creación de interfaces interactivas en Jupyter Notebooks.
3. **matplotlib**: Visualización de datos y gráficos 2D.

## Especificaciones de Contenido

Este archivo contiene el desarrollo de la tarea propuesta por el programa de CNYT sobre los temas de teoría cuántica, observables y medidas. Se simuló el primer sistema cuántico descrito en la sección 4.1, se solucionaron los retos propuestos y se resolvieron los ejercicios 4.3.1, 4.3.2, 4.4.1, 4.4.2, 4.5.2 y 4.5.3.

## Especificaciones de Ejecución

### Simulación

En la simulación, se pueden experimentar con los valores de la cantidad de componentes del ket (n) y los valores del ket (ket). Además, es posible variar el valor de la posición del ket (i) para calcular su probabilidad.

En la segunda parte de la simulación, se pueden variar los valores de los dos estados y observar cómo cambia la probabilidad de transición.

Para ambos casos de simulación, los valores que se pueden modificar para experimentar el comportamiento cuántico de un sistema de una partícula por medio de la interfaz generada.

### Retos

### Descripción de Funciones.

### 1. `normalizar(ket)`
Esta función toma un vector de estado cuántico (ket) y lo normaliza. Calcula la norma del ket usando `np.linalg.norm()`, y si la norma es cero, lanza un error. Devuelve el ket normalizado dividiendo cada componente por la norma.

### 2. `prob_transicion(ket1, ket2)`
Esta función calcula la probabilidad de transición entre dos kets. Utiliza el producto interno (o braket) entre `ket2` y `ket1`, y devuelve el cuadrado del valor absoluto de este producto, que representa la probabilidad de encontrar el sistema en el estado `ket2` dado que estaba en el estado `ket1`.

### 3. `es_hermitiana(matriz)`
Esta función verifica si una matriz es hermitiana. Una matriz es hermitiana si es igual a su conjugada transpuesta. Utiliza `np.allclose()` para comprobar la igualdad de manera numérica.

### 4. `valor_esperado(matriz, ket)`
Esta función calcula el valor esperado de un operador (matriz) dado un estado cuántico (ket). Realiza el producto interno del ket con la matriz aplicada al ket, lo que da el valor esperado correspondiente.

### 5. `varianza(matriz, ket)`
Esta función calcula la varianza de una observable representada por una matriz para un estado cuántico dado. Calcula primero el valor esperado del operador y luego el valor esperado del operador al cuadrado, restando el cuadrado del valor esperado para obtener la varianza.

### 6. `es_unitaria(matriz)`
Esta función verifica si una matriz es unitaria. Una matriz es unitaria si el producto de su conjugada transpuesta y ella misma es igual a la matriz identidad. Utiliza `np.allclose()` para confirmar la igualdad.

### 7. `calcular_probabilidad_transicion(ket1, ket2)`
Esta función calcula la probabilidad de transición entre dos kets, `ket1` y `ket2`. Primero, normaliza ambos kets utilizando la función `normalizar`. Luego, calcula la probabilidad de transición utilizando la función `prob_transicion` con los kets normalizados. Finalmente, devuelve la probabilidad calculada.

### 8. `calcular_observable(matriz, ket)`
Esta función calcula el valor esperado y la varianza de una observable representada por una matriz para un estado cuántico dado. Primero, normaliza el ket y verifica que la matriz sea cuadrada y hermitiana. Luego, calcula el valor esperado y la varianza utilizando las funciones `valor_esperado` y `varianza`, respectivamente. Devuelve ambos resultados.

### 9. `calcular_valores_propios_probabilidades(matriz_observable, ket)`
Esta función calcula los valores propios de una matriz observable hermitiana y las probabilidades de encontrar el estado `ket` en cada uno de los vectores propios correspondientes. Verifica que la matriz sea hermitiana y utiliza `np.linalg.eigh` para obtener los valores y vectores propios. Luego, normaliza el ket y calcula las probabilidades de transición entre el ket y cada vector propio, devolviendo tanto los valores propios como las probabilidades.

### 10. `evolucionar_estado(estado_inicial, matrices_unitarias)`
Esta función evoluciona un estado cuántico inicial a través de una serie de matrices unitarias. Toma un estado inicial y una lista de matrices unitarias. Para cada matriz, verifica que sea unitaria y aplica la matriz al estado final, normalizándolo en cada paso. Devuelve el estado final resultante después de aplicar todas las matrices.



### Ejercicios y Problemas

Al igual que los retos, los problemas propuestos pueden ejecutarse de manera sencilla y se pueden analizar los resultados que se obtienen con los datos iniciales propuestos en el código. Como se mencionó anteriormente en el caso de los retos, si se desea experimentar con los valores propuestos, es posible hacerlo.

