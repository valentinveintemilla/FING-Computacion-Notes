# Ecuaciones matriciales. Matriz inversa
Continuamos con las ecuaciones matriciales, y con la matriz inversa.

**Recordatorio**
Un sistema lineal (S) de m ecuaciones y n incógnitas, es equivalente a la ecuación
$$
AX = B
$$
donde
- A es la matriz ($m \times n$) de los coeficientes del sistema.
- X es la matriz columna ($n \times 1$) de las incógnitas.
- B es la matriz columna ($m \times 1$) de los términos independientes.

Como podemos ver, si desarrollo el producto $AX$ obtengo una matriz columna (pues al multiplicar una matriz $m \times n$ por otra $n \times 1$, nos quedamos con una matriz $m \times 1$) que coincide con la matriz columna de los términos independientes.

Esto es interesante, puesto que, en lugar de desarrollar el producto, nos gustaría hacer algo como:
$$
X = \frac{B}{A}
$$
Esto es totalmente incorrecto, aunque podemos realizar una operación similar:
$$
X = A^{-1}B \qquad \left(  \text{basado en que } \frac{x}{y} = xy^{-1} \right)
$$
Sin embargo, como sabemos, el producto de matrices generalmente no es conmutativo, por lo que también tenemos:
$$
X = BA^{-1}
$$
En este caso, la operación primitiva no es la división, es la inversa. La división esta compuesta por la inversa y el producto.

Igualmente, por ahora no lo escribiremos de ninguna manera, aunque es lo que queremos hacer.

Primeramente, tenemos que definir la noción de matriz inversa. Nos podemos basar en la definición matemática de inverso:
$$
y = x^{-1} \Longleftrightarrow xy = 1
$$
Tomando esta noción, vamos a definir el inverso de una matriz. Sin embargo, para esto tenemos que definir el equivalente a 1 en las matrices. Existe una matriz que cumple con las caracteristicas del 1 (como ser el neutro del producto), y esta es la matriz identidad.

# Matriz identidad
Se llama matriz identidad de tamaño $n \times n$ a la matriz $I_{n} = (s_{i,j})$ definida por
$$
\begin{align}
&s_{i,j} = \begin{cases}
1 \text{ si } i = j \\
0 \text{ si } i \neq j
\end{cases} \\ 
 \\
&I_{n} = \begin{pmatrix}
1 & 0 & 0 & \dots & 0 \\
0 & 1 & 0 & \dots & 0 \\
0 & 0 & 1 & \dots & 0 \\
\dots & \dots & \dots & \dots & \dots \\
0 & 0 & 0 & \dots & 1
\end{pmatrix}
\end{align}
$$
Básicamente, es una matriz en la que las únicas celdas que tienen 1 son las pertenecientes a la diagonal, siendo todo el resto 0. Algunos ejemplos:
$$
\begin{align}
&I_{1} = \begin{pmatrix}
1
\end{pmatrix} \\
&I_{2} = \begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} \\
&I_{3} = \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix} \\
&\dots
\end{align}
$$
## Propiedad
Para toda matriz $A \in M_{m \times n}$:
$$
I_{m} \cdot A = A \cdot I_{n} = A
$$
Es la matriz cuyo producto no cambia nada. Tenemos una matriz 1 para cada tamaño.
Esta matriz siempre es cuadrada y simétrica, no existe identidad rectangular.

De esta forma, cuando vamos a invertir matrices, nos vamos a restringir al caso de matrices cuadradas, solo para estas podemos aplicar inversión

Teniendo esto, podemos definir la matriz inversa.

# Matriz inversa
Una matriz $A \in M_{n \times n}$ (cuadrada) es invertible cuando existe $B \in M_{n \times n}$ tal que
$$
AB = BA = I_{n}
$$
y cuando B existe, es única y se escribe $B = A^{-1} \qquad (\ll \text{inversa de } A\gg)$ 

Como vemos, especificamos que tanto AB como BA tienen que ser iguales a la identidad, es la única forma de considerar a B la inversa de A y viceversa. De esta forma, necesitamos dos igualdades para saber que una matriz es invertible.

A continuación, vamos a demostrar que cuando B existe, es única.

## Demostración de la unicidad
Supongamos que A tenga dos inversas $B_{1}$ y $B_{2}$. Es decir
$$
AB_{1} = B_{1}A = AB_{2} = B_{2}A = I
$$
Tenemos que
$$
B_{1} = B_{1} \cdot I = B_{1}(AB_{2}) = (B_{1}A)B_{2} = IB_{2} = B_{2}
$$
Al final obtuvimos $B_{1} = B_{2}$ lo que demuestra la unicidad de la matriz inversa. Igualmente, no siempre existe (existen matrices que no tienen inverso).

### Ejemplo
$$
\begin{align}
&A = \begin{pmatrix}
2 & 1 \\
1 & 1
\end{pmatrix}

B = \begin{pmatrix}
1 & -1 \\
-1 & 2
\end{pmatrix} \\
 \\
&AB = \\
&\begin{pmatrix}
1 & -1 \\
-1 & 2
\end{pmatrix} \\

\begin{pmatrix}
2 & 1 \\
1 & 1
\end{pmatrix}

&\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} \\

&AB = I \\
 \\
&BA = \\
&\begin{pmatrix}
2 & 1 \\
1 & 1
\end{pmatrix} \\

\begin{pmatrix}
1 & -1 \\
-1 & 2
\end{pmatrix}

&\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix} \\

&BA = I
\end{align}
$$
Luego $B = A^{-1}$, y $A = B^{-1}$.
A y B son invertibles, y una es la inversa de la otra.

Si queremos un ejemplo sencillo de matriz no invertible es la matriz nula, puesto que no hay forma de que el producto de la matriz nula y otra matriz sea igual a la matriz identidad. En su lugar siempre será igual a la matriz nula.

### Ejemplo
¿Es $A = \begin{pmatrix} 1 & 1 & 2 \\ 1 & -1 & -1 \\ 0 & 0 & 0 \end{pmatrix}$?
$$
\begin{align}
&\begin{pmatrix}
? & ? & ? \\
? & ? & ? \\
? & ? & ?
\end{pmatrix} \\

\begin{pmatrix}
1 & 1 & 2 \\
1 & -1 & -1 \\
0 & 0 & 0
\end{pmatrix}

&\begin{pmatrix}
? & ? & ? \\
? & ? & ? \\
0 & 0 & 0
\end{pmatrix} \neq I
\end{align}
$$
Si desarrollamos el producto anterior, la última fila siempre será 0. De esta forma, siempre faltara el uno de la última fila, por lo que A no es invertible (es imposible obtener la identidad a partir del producto con A).
Para generalizar, cualquier matriz que tenga una fila o columna nula no es invertible.

**Moraleja**
Si A tiene una fila o una columna nula, entonces ==A no es invertible==.

Con los números que conocemos, el único número no invertible es 0, todos los demás se pueden invertir. No es el caso con las matrices, hay muchas que no se pueden invertir, incluidas las que mencionamos anteriormente.
Veremos que hay muchos ejemplos más de matrices no invertibles que no tienen filas ni columnas nulas.
$$
\begin{align}
&A = \begin{pmatrix}
1 & 1 & 1 \\
1 & 1 & 1 \\
1 & 1 & 1
\end{pmatrix} \\ \\

&AB = \\

&\begin{pmatrix}
 &  &  \\
 & B &  \\
 &  & 
\end{pmatrix} \\

\begin{pmatrix}
1 & 1 & 1 \\
1 & 1 & 1 \\
1 & 1 & 1
\end{pmatrix}

&\begin{pmatrix}
 & F &  \\
 & F &  \\
 & F & 
\end{pmatrix} \text{ donde } F = \begin{pmatrix} 1 & 1 & 1 \end{pmatrix}B \\
 \\
&AB \neq I
\end{align}
$$
A por cualquier otra matriz da como resultado una matriz cuyas filas son iguales. Esto lo dedujimos utilizando el producto de una fila y una matriz, que nos da otra fila.

Por esta razón, como la matriz identidad no tiene filas idénticas, concluimos que A no es invertible

Conclusión: $\begin{pmatrix} 1 & 1 & 1 \\ 1 & 1 & 1 \\ 1 & 1 & 1 \end{pmatrix}$ no es invertible.

A continuación, estudiaremos las propiedades de las matrices invertibles.

## Propiedades
0. $O_{n \times n}$ no es invertible.
En general, podemos decir que cuando una matriz tiene dos filas idénticas o dos columnas idénticas, no es invertible, ya que si tiene dos filas idénticas, el producto tendrá dos filas idénticas (por lo que no será la matriz identidad), y si tiene dos columnas idénticas, haciendo el producto al revés, el producto tendrá dos columnas idénticas (por lo que no será la matriz identidad).

1. $I_{n}$ es invertible, y $(I^{-1}) = I$
No especificamos el índice ya que se da para cualquier tamaño fijado).

2. Si A es invertible y $\lambda \neq 0$, entonces $\lambda \cdot A$ es invertible, y $(\lambda \cdot A)^{-1} = \frac{1}{\lambda} \cdot A^{-1}$
**Ejemplo**
$$
\begin{pmatrix}
4 & 0 & 0 \\
0 & 4 & 0 \\
0 & 0 & 4
\end{pmatrix}^{-1} = \begin{pmatrix}
\frac{1}{4} & 0 & 0 \\
0 & \frac{1}{4} & 0 \\
0 & 0 & \frac{1}{4}
\end{pmatrix}
$$

3. Si A y B son invertibles (y del mismo tamaño), entonces AB es invertible, y $(AB)^{-1} = B^{-1}A^{-1}$
La inversa también intercambia el orden de los productos.

4. Si A es invertible, entonces $A^{-1}$ es invertible y $(A^{-1})^{-1} = A$

5. Si A es invertible, entonces $A^{t}$ es invertible, y $(A^{t})^{-1} = (A^{-1})^{t}$

Ahora, realizaremos una demostración del punto 3 y 5:

### Demostración (3)
Supongamos que A, B son invertibles.
$$
\begin{align}
&(AB)(B^{-1}A^{-1}) = A(BB^{-1})A^{-1} = A\cancel{ I }A^{-1} = AA^{-1} = I \\
&(B^{-1}A^{-1})(AB) = B^{-1}(A^{-1}A)B = B^{-1}\cancel{ I }B = B^{-1}B = I
\end{align}
$$
Hay que hacerlo en ambos sentidos.

Esto quiere decir que ambas matrices, $AB$ y $B^{-1}A^{-1}$ son inversas mutuamente. De esta forma, demostramos el punto 3.

Luego: $(AB)^{-1} = B^{-1}A^{-1}$

El orden fue fundamental para lograr demostrar la propiedad

### Demostración (5)
$$
\begin{align}
&A^{t}(A^{-1})^{t} = (A^{-1}A)^{t} = (I)^{t} = I \\
&(A^{-1})^{t}A^{t} = (AA^{-1})^{t} = (I)^{t} = I
\end{align}
$$
Luego: $(A^{t})^{-1} = (A^{-1})^{t}$

IMPORTANTE:
$$
A^{t}B^{t} = (BA)^{t}
$$

Del mismo modo, podemos demostrar que I es invertible, lo que es trivial, ya que $II = II = I$, y de modo similar con la propiedad 2.

## Observación
Para verificar que B es la inversa de A, se necesita verificar dos igualdades:
$$
AB = I \text{ y } BA = I
$$
Como el producto de matrices no es conmutativo, necesariamente tenemos que verificar (a priori) ambas igualdades.

Esto se vuelve tedioso para matrices muy grandes.

Afortunadamente, sólo se necesita verificar una:

## Lema (admitido)
Para todas matrices $A, B \in M_{n \times n}$ tenemos que $AB = I \Longleftrightarrow BA = I$

De esta forma, cada vez que una se cumple, la otra se cumple también. Esto nos divide entre dos la cantidad de operaciones a realizar.

No lo vamos a demostrar, ya que su demostración es bastante compleja. Sin embargo, lo utilizaremos para facilitar la determinación de matrices invertibles.

La razón de que esto se cumple radica en que las matrices tienen dimensiones finitas.
Si consideramos matrices con dimensiones infinitas, esta propiedad deja de cumplirse. Afortunadamente, no abordaremos dichos tipos de matrices.

### Ejemplo
Queremos resolver el sistema
$$
(S):\begin{cases}
2x + y = 3 \\
x + y = -1
\end{cases}
$$
es decir: queremos resolver la ecuación
$$
AX = B, \text{ con } A = \begin{pmatrix}
2 & 1 \\
1 & 1
\end{pmatrix}, X = \begin{pmatrix}
x \\
y
\end{pmatrix}, B = \begin{pmatrix}
3 \\
-1
\end{pmatrix}
$$
Ya vimos que A es invertible y $A^{-1} = \begin{pmatrix} 1 & -1 \\ -1 & 2 \end{pmatrix}$.
En este caso, no es necesario aplicar el Teorema de Rouché-Frobenius, pues la matriz invertible nos resolverá el problema.

Tenemos que
$$
\begin{align}
&AX = B \\
&\implies \cancel{ A^{-1}A }X = A^{-1}B \\
&\Longleftrightarrow X = A^{-1}B \\
&\implies AX = AA^{-1}B = B
\end{align}
$$
Entonces, tengo derecho a multiplicar por la izquierda o por la derecha mis matrices por la inversa. Aquí obtuve una equivalencia: $AX = B \Longleftrightarrow X = A^{-1}B$. ==Esto nos da la solución del sistema: es Compatible Determinado==.
$$
Sol(S) = \{ A^{-1}B \}
$$
Dicha solución es una matriz columna (matriz por matriz columna).

De esta forma, cada vez que tengo una matriz que es invertible (por lo tanto, también tiene que ser cuadrada), el sistema será compatible determinado.

### Proposición
Todo sistema cuadrado (misma cantidad de ecuaciones y de incógnitas) $AX = B$ cuya matriz de coeficientes A es invertible es compatible determinado:
$$
Sol(S) = \{ A^{-1}B \}
$$
Esta propiedad no depende de B.

Tenemos la resolución de las ecuaciones de primer grado (con matrices), lo anterior es equivalente al $\frac{B}{A}$ que buscábamos obtener.

Esta proposición es buena, ya que si tengo un sistema cuadrado y conozco la inversa de la matriz de coeficientes, directamente tengo la solución (tengo que desarrollar el producto de la inversa de la matriz de coeficientes y la columna de términos independientes). Además, que sea compatible o no no está dado por la columna B (simplemente variarán los resultados).

Sin embargo, hay muchos casos donde la matriz de coeficientes no es invertible, pero igualmente tenemos una solución. Es decir, cuando la matriz de coeficientes no es invertible, no podemos determinar nada, pues depende de B (tenemos que escalerizar de modo usual).
Además, si no conocemos la inversa de A, calcular dicha matriz es más costoso que aplicar Rouché-Frobenius directamente.

**Observación**
Cuando a no es invertible, no se puede concluir nada.
Misma observación cuando A no es cuadrada (pues no podemos utilizar el "truco" de la inversa).

A continuación, veremos el algoritmo para invertir una matriz, el cual es una variante de Rouché-Frobenius.

### Ejemplo
Sea $A = \begin{pmatrix} 2 & 1 \\ 4 & 3 \end{pmatrix}$
Queremos determina (si existe) la matriz $X = \begin{pmatrix} x_{1,1} & x_{1,2} \\ x_{2,1} & x_{2,2} \end{pmatrix}$ tal que $AX = I$
De esta forma, tenemos que resolver el sistema $AX = I$, siendo X la matriz incógnita, tratándose de una ecuación entre dos matrices cuadradas.
$$
AX = \begin{pmatrix}
2x_{1,1} + x_{2,1} & 2x_{1,2} + x_{2,2} \\
4x_{1,1} + 3x_{2,1} & 4x_{1,2} + 3x_{2,2}
\end{pmatrix}
$$
A priori tengo cuatro ecuaciones con cuatro incógnitas, de modo que:
$$
\begin{cases}
2x_{1,1} + x_{2,1} = 1 \\
2x_{1,2} + x_{2,2} = 0 \\
4x_{1,1} + 3x_{2,1} = 0 \\
4x_{1,2} + 3x_{2,2} = 1
\end{cases}
$$
Sin embargo, podemos cortar el sistema en dos trozos, de forma que no tenemos un sistema cuatro por cuatro, sino que tenemos dos sistemas dos por dos.

La ecuación $AX = I$ se reduce a 2 sistemas:
$$
\begin{align}
&\begin{cases}
2x_{1,1} + x_{2,1} = 1 \\
4x_{1,1} + 3x_{2,1} = 0
\end{cases} = \left(
\begin{array}{cc|c}
2 & 1 & 1 \\
4 & 3 & 0
\end{array}
\right) \\
 \\
&A\begin{pmatrix} x_{1,1} \\ x_{2,1} \end{pmatrix} = \begin{pmatrix} 1 \\ 0 \end{pmatrix}
\end{align}
$$
Esto viene de que la primera columna de producto es igual a A por la primer columna de X ($AX^{1} = A\begin{pmatrix} x_{1,1} \\ x_{2,1} \end{pmatrix}$).
Podemos hacer lo mismo para obtener el segundo sistema (la segunda columna del producto de AX): $AX^{2} = A\begin{pmatrix} x_{1,2} \\ x_{2,2} \end{pmatrix}$
$$
\begin{align}
&\begin{cases}
2x_{1,2} + x_{2,2} = 0 \\
4x_{1,2} + 3x_{2,2} = 1
\end{cases} = \left(
\begin{array}{cc|c}
2 & 1 & 0 \\
4 & 3 & 1
\end{array}
\right) \\
 \\

&A\begin{pmatrix} x_{1,2} \\ x_{2,2} \end{pmatrix} = \begin{pmatrix} 0 \\ 1 \end{pmatrix}
\end{align}
$$
De esta forma, tenemos dos sistemas que tienen la misma matriz de coeficientes, el primero va contra la primer columna de la identidad (y resolviéndolo, obtendré la primer columna de la inversa), mientras que el segundo va con la segunda columna de la identidad (al resolverlo, obtengo la segunda columna de la inversa).
De esta forma, podemos generalizar en que teniendo un sistema $n \times n$, me quedan n sistemas, cada uno contra su j-ésima columna de la identidad.

Comenzamos por el primer sistema:
$$
\left(
\begin{array}{cc|c}
2 & 1 & 1 \\
4 & 3 & 0
\end{array}
\right)
$$
$$
\left(
\begin{array}{cc|c}
2 & 1 & 1 \\
0 & 1 & -2
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - 2F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cc|c}
2 & 0 & 3 \\
0 & 1 & -2
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cc|c}
1 & 0 & \frac{3}{2} \\
0 & 1 & -2
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{F_{1}}{2}
\end{align}
$$
En el primer sistema: $x_{1,1} = \frac{3}{2}, x_{2,1} = -2$ (primera columna de la matriz inversa de A).
$$
\begin{pmatrix} x_{1,1} \\ x_{2,1} \end{pmatrix} = \begin{pmatrix} \frac{3}{2} \\ -2 \end{pmatrix}
$$

Proseguimos con el segundo sistema:
$$
\left(
\begin{array}{cc|c}
2 & 1 & 0 \\
4 & 3 & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{cc|c}
2 & 1 & 0 \\
0 & 1 & 1
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - 2F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cc|c}
2 & 0 & -1 \\
0 & 1 & 1
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cc|c}
1 & 0 & -\frac{1}{2} \\
0 & 1 & 1
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{F_{1}}{2}
\end{align}
$$
En el primer sistema: $x_{1,2} = -\frac{1}{2}, x_{2,2} = 1$ (segunda columna de la matriz inversa de A).
$$
\begin{pmatrix} x_{1,2} \\ x_{2,2} \end{pmatrix} = \begin{pmatrix} -\frac{1}{2} \\ 1 \end{pmatrix}
$$
Conclusión: $X = A^{-1} = \begin{pmatrix} \frac{3}{2} & -\frac{1}{2} \\ -2 & 1 \end{pmatrix}$

Como vemos, las operaciones realizadas en ambas matrices son exactamente las mismas, puesto que las matrices de coeficientes son idénticas, únicamente cambian los resultados obtenidos en la columna de los términos independientes (columna de la identidad). Por esta razón, conviene resolver las dos matrices a la vez.

Para hallar la inversa, calculé cada una de sus columnas por separado, y para obtener una columna de la inversa, vimos que si calculamos el producto de una matriz y la j-ésima columna de su inversa, obtendremos la j-ésima columna de la identidad. Esto nos da un sistema lineal, habiendo n sistemas lineales, los cuales coincidirán en su matriz de los coeficientes, únicamente cambiando la columna de los términos independientes (j-ésima columna de la identidad correspondiente).

Como vemos, la idea es muy sencilla. Comenzamos queriendo resolver el sistema $AX = I$. Sin embargo, como es bastante complicado, resolvemos los sistemas $AX^{j} = I^{j}$, que son bastante más sencillos (y comparten la misma matriz de los coeficientes, por lo que hay que desarrollar exactamente las mismas operaciones). Por último, al haber resuelto todos los sistemas, simplemente uno todas las columnas obtenidas, y la matriz resultante será $A^{-1}$.

Se podían resolver ambos sistemas simultáneamente. Lo que haremos es, en lugar de tener varios sistemas con su columna j-ésima de la identidad correspondiente, resolvemos la matriz de los coeficientes, con la matriz identidad correspondiente (todas las columnas juntas).
De esta manera, resolvemos todas las columnas en una única matriz.

Al final, luego de escalerizar la matriz de los coeficientes, del lado de la matriz independiente nos quedará la matriz inversa que buscamos.
$$
\left(
\begin{array}{cc|cc}
2 & 1 & 1 & 0 \\
4 & 3 & 0 & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{cc|cc}
2 & 1 & 1 & 0 \\
0 & 1 & -2 & 1
\end{array}
\right)
\begin{align}
F_{2} \leftarrow F_{2} - 2F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cc|cc}
2 & 0 & 3 & -1 \\
0 & 1 & -2 & 1
\end{array}
\right)
\begin{align}
F_{1} \leftarrow F_{1} - F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cc|cc}
1 & 0 & \frac{3}{2} & -\frac{1}{2} \\
0 & 1 & -2 & 1
\end{array}
\right)
\begin{align}
F_{1} \leftarrow \frac{F_{1}}{2}
\end{align}
$$
$$
\implies A^{-1} = \begin{pmatrix}
\frac{3}{2} & -\frac{1}{2} \\
-2 & 1
\end{pmatrix}
$$
Este es el método de Rouché-Frobenius, donde utilizo una matriz de términos independientes, que es la matriz identidad correspondiente a la matriz que queremos invertir.

La próxima clase veremos el algoritmo completo, aunque ya tuvimos un primer acercamiento a la idea del algoritmo. Básicamente formaremos la matriz $(A|I)$, y aplicaremos Rouché-Frobenius hasta que obtengamos la identidad por la izquierda, quedando $(I|A^{-1})$.
Necesariamente quedarán n escalones. En caso de tener menos de n escalones, llegaremos a la conclusión de que la matriz no es invertible.