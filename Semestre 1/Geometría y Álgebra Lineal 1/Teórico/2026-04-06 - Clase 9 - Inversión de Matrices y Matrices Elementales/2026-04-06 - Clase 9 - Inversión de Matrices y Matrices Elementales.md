Continuamos con la inversión de matrices.
# Inversión de matrices

> [!Recordatorio]
> Una matriz cuadrada $A \in M_{n \times n}$ es invertible cuando existe $B \in M_{n \times n}$ tal que
> $$
> AB = I \text{ y } BA = I
> $$

> [!Observación]
> 1. Cuando B existe, es única y se escribe $A^{-1}$
> 2. Solo se necesita verificar una de las igualdades $AB = I$ y $BA = I$, pues son equivalentes (por un lema admitido).

Ahora, estudiaremos el algoritmo de inversión de matrices:

Dada una matriz $A \in M_{n \times n}$, queremos hallar (si existe) una matriz $X \in M_{n \times n}$ tal que $AX = I_{n}$.
$$
X = \begin{pmatrix}
X^{1} & X^{2} & \dots & X^{n} \\
\dots & \dots & \dots & \dots \\
\dots & \dots & \dots & \dots
\end{pmatrix}
$$
$$
AX = \begin{pmatrix}
AX^{1} & AX^{2} & \dots & AX^{n} \\
\dots & \dots & \dots & \dots \\
\dots & \dots & \dots & \dots
\end{pmatrix}
$$
Aclaración: recordemos que los exponentes en matrices indican el número de columna, de modo que $X^{1} = \text{primer columna de X}$, $AX^{1} = \text{A por primer columna de X}$.
De esta forma, resolver $AX = I_{n}$ se reduce a resolver n sistemas lineales, que son:
$$
\begin{align}
&AX^{1} = I^{1}_{n} = \begin{pmatrix} 
1 \\
0 \\
\dots \\
0
\end{pmatrix} &\left( \begin{array}{c|c}
A & 1 \\
 & 0 \\
 & \dots \\
 & 0
\end{array} \right) \\
&\dots &\dots \\
&AX^{n} = I^{n}_{n} = \begin{pmatrix}
0 \\
0 \\
\dots \\
1
\end{pmatrix} &\left( \begin{array}{c|c}
A & 0 \\
 & 0 \\
 & \dots \\
 & 1
\end{array} \right)
\end{align}
$$
Así tendremos n matrices ampliadas, teniendo que resolver estos sistemas en paralelo. Sin embargo, como se trata de un problema de escalerización, y las operaciones serán idénticas para todas las matrices ampliadas, existe un método más eficiente, tratándose de la resolución en paralelo:
$$
\begin{align}
&\left( \begin{array}{c|c}
A & I^{1}_{n}
\end{array} \right) &\dots &&\left( \begin{array}{c|c}
A & I^{n}_{n}
\end{array} \right) \\
&\big\downarrow \\
&\left( \begin{array}{c|c}
E & B^{1}
\end{array} \right) &\dots &&\left( \begin{array}{c|c}
E & B^{n}
\end{array} \right)
\end{align}
$$
Al resolver en paralelo cada matriz ampliada, obtendremos una forma escalerizada de $A$ y una matriz columna surgida de la resolución, llamada $B$ (la columna depende de la columna identidad manejada anteriormente). Al final, si $E$ tiene n escalones, sabremos que todos los sistemas son compatibles determinados, y además, si $E$ es escalerizada reducida con n escalones, entonces es equivalente a la identidad, de forma que todas las matrices columna $B$ serán matrices columna de $A^{-1}$.

Esto es muy pesado en la práctica, por lo que simplemente juntamos todo en una única matriz ampliada, que en lugar de tener una columna de la identidad, tiene a la identidad completa:
$$
\begin{align}
&\left( \begin{array}{c|c}
A & I_{n}
\end{array} \right) \\
&\big\downarrow \\
&\left( \begin{array}{c|c}
E & B
\end{array} \right)
\end{align}
$$
Aquí realizamos una sola vez la escalerización, en lugar de hacerla n veces.

Esto nos da el algoritmo de inversión de matrices (también nos permite saber si la matriz es invertible).

---
# Método de cálculo de $A^{-1}$

> [!Algoritmo de cálculo de matriz inversa]
> Dada una matriz $A \in M_{n \times n}$
> 1. Formar la matriz doble $\left( \begin{array}{c|c} A & I_{n} \end{array} \right)$
> 2. Aplicar el método de escalerización de Rouché-Frobenius a la matriz doble $\left( \begin{array}{c|c} A & I_{n} \end{array} \right)$ hasta que la parte izquierda esté en forma escalerizada:
> $$
> \left( \begin{array}{c|c} A & I_{n} \end{array} \right) \longrightarrow \left( \begin{array}{c|c} E & B \end{array} \right)
> $$
> Desde aquí, podemos desarrollar dos conclusiones:
> - Si $E$ tiene n escalones, entonces $A$ es invertible y si $E$ está en forma reducida, tenemos que $E = I_{n}$ y $B = A^{-1}$.
> - Si $E$ tiene menos de n escalones (no es compatible o es compatible indeterminado), entonces $A$ no es invertible.

## Ejemplo
Invertir $A = \begin{pmatrix} 1 & 0 & 2 \\ 2 & 1 & 3 \\ -1 & 1 & -1 \end{pmatrix}$
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 2 & 1 & 0 & 0 \\
2 & 1 & 3 & 0 & 1 & 0 \\
-1 & 1 & -1 & 0 & 0 & 1
\end{array}
\right)
$$
Resolveremos n sistemas lineales al mismo tiempo:
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 2 & 1 & 0 & 0 \\
0 & 1 & -1 & -2 & 1 & 0 \\
0 & 1 & 1 & 1 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - 2F_{1} \\
&F_{3} \leftarrow F_{3} + F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 2 & 1 & 0 & 0 \\
0 & 1 & -1 & -2 & 1 & 0 \\
0 & 0 & 2 & 3 & -1 & 1
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{2}
\end{align}
$$
==Hasta aquí, logramos escalerizar la matriz A, por lo que en este punto podemos determinar que la misma es invertible==. Ahora estamos seguros de que A es invertible. ==Si no tuviera n escalones, no sería necesario proseguir con el cálculo==. Como es invertible, proseguiremos.
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 2 & 1 & 0 & 0 \\
0 & 1 & -1 & -2 & 1 & 0 \\
0 & 0 & 1 & \frac{3}{2} & -\frac{1}{2} & \frac{1}{2}
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow \frac{1}{2}F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 0 & -2 & 1 & -1 \\
0 & 1 & 0 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
0 & 0 & 1 & \frac{3}{2} & -\frac{1}{2} & \frac{1}{2}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - 2F_{3} \\
&F_{2} \leftarrow F_{2} + F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|ccc}
1 & 0 & 0 & -2 & 1 & -1 \\
0 & 1 & 0 & -\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
0 & 0 & 1 & \frac{3}{2} & -\frac{1}{2} & \frac{1}{2}
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{array}
\right) = I_{3}

\qquad

\left(
\begin{array}{ccc}
-2 & 1 & -1 \\
-\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\frac{3}{2} & -\frac{1}{2} & \frac{1}{2}
\end{array}
\right) = A^{-1}
$$
**Conclusión**
A es invertible y
$$
A^{-1} = \left(
\begin{array}{ccc}
-2 & 1 & -1 \\
-\frac{1}{2} & \frac{1}{2} & \frac{1}{2} \\
\frac{3}{2} & -\frac{1}{2} & \frac{1}{2}
\end{array}
\right)
$$
En realidad, seguimos aplicando el algoritmo Rouché-Frobenius que utilizamos para escalerizar, pero con el objetivo de encontrar la inversa de una matriz.

**Verificación**:
$$
\begin{align}
&AA^{-1} = \text{?} \\
&A^{-1}A = \text{?}
\end{align}
$$

A continuación, hablaremos del rango. Anteriormente, no justificamos lo que sucede cuando $E$ tiene un rango menor que n. En este caso, sucede que el sistema es incompatible o es compatible indeterminado, siendo imposible de invertir, ya que existe una única inversa (en caso de existir). Lo justificaremos con la noción de rango.

> [!Recordatorio]
> El rango de una matriz $A$ es el número de escalones de cualquier forma escalerizada.
> (Este número no depende de la forma escalerizada).

---
## Proposición
Una matriz cuadrada $A \in M_{n \times n}$ es invertible si y solo si $rango(A) = n$.

### Demostración
$(\implies)$ Supongamos que $A$ es invertible. Entonces para toda columna $B \in M_{n \times 1}$, el sistema $AX = B$ es compatible determinado, pues:
$$
AX = B \Longleftrightarrow X = A^{-1}B \qquad (Sol(S) = \{ A^{-1}B \})
$$
Esto implica (por el teorema de Rouché-Frobenius) que $rango(A) = n$.

De esta forma, concluimos que para las matrices invertibles, cualquier forma escalerizada tiene n escalones, puesto que en caso contrario no sería compatible determinado.

Continuamos con el recíproco:
$(\Longleftarrow)$ Supongamos que $rango(A) = n$. Por Rouché-Frobenius, esto implica que todos los sistemas de la forma $AX = B$ (con $B \in M_{n \times 1}$ cualquiera) es compatible determinado.

Esto es correcto, ya que sabemos que, para cualquier matriz cuadrada de rango n (compatible determinado), su forma escalerizada reducida es la matriz identidad. De esta forma, el sistema es compatible determinado y $B'$ es la solución (es única).
$$
\begin{align}
&\left( \begin{array}{c|c} A & B \end{array} \right) \\
&\downarrow \\
&\left( \begin{array}{c|c} I & B' \end{array} \right)
\end{align}
$$

Sean $X^{1}, X^{2}, \dots, X^{n}$ las (únicas) soluciones de los sistemas
$$
\begin{matrix}
AX^{1} = &I_{n}^{1} = &\begin{pmatrix}
1 \\
0 \\
\dots \\
0
\end{pmatrix} \\
\dots & \dots & \dots \\
AX^{n} = &I_{n}^{n} = &\begin{pmatrix}
0 \\
0 \\
\dots \\
1
\end{pmatrix}
\end{matrix}
$$
Sea
$$
X = \begin{pmatrix}
X^{1} & X^{2} & \dots & X^{n} \\
\dots & \dots & \dots & \dots \\
\dots & \dots & \dots & \dots
\end{pmatrix}
$$
Por construcción, tenemos que
$$
AX = \begin{pmatrix}
AX^{1} & AX^{2} & \dots & AX^{n} \\
\dots & \dots & \dots & \dots \\
\dots & \dots & \dots & \dots
\end{pmatrix} = \begin{pmatrix}
I_{n}^{1} & I_{n}^{2} & \dots & I_{n}^{n} \\
\dots & \dots & \dots & \dots \\
\dots & \dots & \dots & \dots
\end{pmatrix} = \begin{pmatrix}
1 & 0 & \dots & 0 \\
0 & 1 & \dots & 0 \\
\dots & \dots & \dots & \dots \\
0 & 0 & \dots & 1
\end{pmatrix}
$$
Esto demuestra que la inversa existe y es $X$. De hecho, es el mismo método que aplicamos para encontrar la inversa anteriormente.
Es así que una matriz cuadrada es invertible si y solo si su forma escalerizada tiene n escalones (teniendo una única inversa).

Para finalizar con esta sección, realizaremos un ejercicio para determinar el rango de una matriz:
### Ejercicio
Determinar el rango de
$$
A = \begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{pmatrix}
$$
Para determinar el rango de una matriz, tenemos que escalerizarla.
$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & -6 & -12
\end{pmatrix}
\begin{align}
&F_{2} \leftarrow F_{2} - 4F_{1} \\
&F_{3} \leftarrow F_{3} - 7F_{1}
\end{align}
$$
$$
\begin{pmatrix}
1 & 2 & 3 \\
0 & -3 & -6 \\
0 & 0 & 0
\end{pmatrix}
\begin{align}
&F_{3} \leftarrow F_{3} - 2F_{2}
\end{align}
$$
Aquí llegamos a una de las formas escalerizadas de A, y viendo que tenemos 2 escalones en total podemos determinar que, conclusión: $rango(A) = 2$
De esta forma, la matriz no es invertible.

Ya vimos todo lo necesario de inversión de matrices. Pasamos al siguiente tema referente a matrices: matrices elementales.

---
# Matrices elementales
La idea ahora es entender internamente el método de Rouché-Frobenius, el cual funciona gracias a las transformaciones elementales, permitiendo resolver sistemas lineales, matrices inversas, rango, y todos los problemas que hemos afrontado hasta ahora.
Analizaremos la noción de transformación elemental, y veremos que cada una se corresponde con una matriz en particular.

**Objetivo**: mostrar que cada transformación elemental sobre una matriz $A$ de tamaño $m \times n$ se puede ver como un producto (por la izquierda) por cierta matriz $\underbrace{ E }_{ \begin{align} &\text{Matriz elemental} \\ & \text{(o de Frobenius)} \end{align} }$ de tamaño $m \times m$ (cuadrada).

Repasamos los tres tipos de transformaciones elementales.

> [!Transformaciones elementales: tres tipos]
> 1. $T_{\alpha i}$ : multiplicar la fila $i$ por $\alpha \neq 0$
> 2. $T_{i \longleftrightarrow j}$ : intercambiar las filas $i$ y $j$
> 3. $T_{i + \alpha j}$ : sumarle a la fila $i$ la fila $j (\neq i)$ multiplicada por $\alpha$ (puede ser nulo, puesto que simplemente no cambia el sistema)

Seguidamente, estudiaremos una proposición relacionada a las matrices que "funcionan" como transformaciones lineales.
Aclaración: ==las transformaciones lineales solo dependen de las filas==, pues son los índices que se utilizan en las reglas. Por esta razón, las transformaciones elementales dependen de m (cantidad de filas).

## Proposición

> [!Proposición]
> Sea $m, n \geq 1$ (dimensiones de la matriz).
> Para toda transformación elemental T (sobre matrices con m filas).
> 1. Existe una matriz $E \in M_{m \times m}$ tal que $T(A) = E_{T}A$ para toda matriz $A \in M_{m \times n}$
> (Cuando aplicamos una transformación lineal a una matriz $A$, existe una matriz $E$ cuadrada cuyo producto con $A$ es equivalente a la aplicación de la transformación lineal previa).
> 
> 2. Además, la matriz $E_{T}$ asociada a la transformación $T$ está dada por
> $$
> E_{T} = T(I_{m})
> $$
> $E_{T}$ se llama una matriz elemental
> 
> (La matriz $E_{T}$ esta dada por la aplicación de dicha transformación sobre la matriz identidad de tamaño $m \times m$).

A continuación, aplicaremos los tres tipos de transformaciones a la matriz identidad, y verificaremos que todo funciona bien. De esta forma, será una demostración en tres partes (aunque no será completa).

### Tipo 1
$$
T = T_{\alpha i}
$$
$$
E_{\alpha i} := T_{\alpha i}(I_{m}) = \begin{pmatrix}
1 & 0 & \dots & 0 \\
0 & 1 & \dots & 0 \\
\dots & 0 & \alpha & 0 \\
\dots & \dots & \dots & \dots \\
0 & 0 & \dots & 1
\end{pmatrix}
\text{Fila } i
$$
Verificación:
$$
E_{\alpha i} A = T_{\alpha i}(A)
$$
El producto de $E_{\alpha i}$ por cualquier matriz, debe ser equivalente a la aplicación de dicha transformación lineal sobre la matriz correspondiente.
Si desarrollamos el producto, todas las filas de $A$ se mantienen intactas, menos la fila $i$, la cual será multiplicada por $\alpha$.
Ejemplo con la primera fila:
$$
\begin{align}
&\begin{pmatrix}
A
\end{pmatrix} \\

\begin{pmatrix}
1 & 0 & \dots & 0
\end{pmatrix}

&\begin{pmatrix}
A_{1}
\end{pmatrix}
\end{align}
$$
En la fila $i$:
$$
\begin{align}
&\begin{pmatrix}
A
\end{pmatrix} \\

\begin{pmatrix}
0 & \dots & \alpha & \dots & 0
\end{pmatrix}

&\begin{pmatrix}
\alpha A_{i}
\end{pmatrix}
\end{align}
$$==Las matrices elementales son sumamente útiles para descomponer todas las matrices invertibles==.

### Tipo 2
$$
T = T_{i \longleftrightarrow j}
$$
$$
E_{i \longleftrightarrow j} := T_{i \longleftrightarrow j}(I_{m}) = \begin{pmatrix}
1 & 0 & \dots & \dots & 0 \\
\dots & 0 & \dots & 1 & \dots \\
\dots & \dots & \dots & \dots & \dots \\
\dots & 1 & \dots & 0 & \dots \\
0 & 0 & \dots & \dots & 1
\end{pmatrix}
\begin{align}
&\text{Fila } i \\ \\

&\text{Fila } j
\end{align}
$$
Solo intercambiamos las filas $i$ y $j$ de lugar, manteniendo todo el resto.

Verificación:
$$
E_{i \longleftrightarrow j} A = T_{i \longleftrightarrow j} (A)
$$
Si tengo un índice distinto de $i$ y $j$, la fila se mantiene igual (identidad). Sin embargo, en la fila $i$ tendremos los valores de la fila $j$ y en la fila $j$ tendremos los valores de la fila $i$. De esta forma, al desarrollar el producto, obtendremos una matriz cuyas filas son idénticas a $A$, excepto en las filas $i$ y $j$ que estarán intercambiadas.

### Tipo 3
$$
T = T_{i + \alpha j}
$$
$$
E_{i + \alpha j} := T_{i + \alpha j}(I_{m}) = \begin{pmatrix}
1 & 0 & \dots & \dots & 0 \\
\dots & 1 & \dots & \alpha & \dots \\
\dots & \dots & \dots & \dots & \dots \\
\dots & \dots & \dots & 1 & \dots \\
0 & 0 & \dots & \dots & 1
\end{pmatrix}
\begin{align}
&\text{Fila } i \\ \\

&\text{Fila } j
\end{align}
$$
Si en la fila $i$, en la columna $j$, agregamos un $\alpha$, al realizar el producto, obtendremos que la fila $i$ resultante tendrá la suma de los valores de la fila $i$ mas los valores de la fila $j$ multiplicados por $\alpha$.

Verificación:
$$
E_{i + \alpha j} A = T_{i + \alpha j} (A)
$$
De esta forma, manejamos un problema más bien "geométrico", al transformar operaciones determinadas en matrices con características que las diferencian del resto.

### Ejemplo
Sea $E$ la matriz elemental asociada "$F_{3} \leftarrow F_{3} + 4F_{1}$" (es una matriz perteneciente a $M_{3 \times 3}$).
$$
I_{3} = \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix}
$$
$$
E = \begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
4 & 0 & 1
\end{pmatrix}
\begin{align}
&F_{3} \leftarrow F_{3} + 4F_{1}
\end{align}
$$
Ahora, desarrollaremos el producto de esta matriz por otra para ver que sucede.
Sea
$$
A = \begin{pmatrix}
1 & 0 & 2 & 1 \\
2 & -1 & 3 & 6 \\
1 & 4 & 4 & 0
\end{pmatrix}
$$
$$
\begin{align}
&EA = \\ \\

&\begin{pmatrix}
1 & 0 & 2 & 1 \\
2 & -1 & 3 & 6 \\
1 & 4 & 4 & 0
\end{pmatrix} \\

\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
4 & 0 & 1
\end{pmatrix}

&\begin{pmatrix}
1 & 0 & 2 & 1 \\
2 & -1 & 3 & 6 \\
5 & 4 & 12 & 4
\end{pmatrix} \\ \\

&EA = \begin{pmatrix}
1 & 0 & 2 & 1 \\
2 & -1 & 3 & 6 \\
5 & 4 & 12 & 4
\end{pmatrix} \\
\end{align}
$$
Como vemos, las primeras dos filas quedan intactas (puesto que ambas pertenecen a la identidad), mientras que la fila 3 equivale a la fila 3 mas la fila 1 multiplicada por 4. 

