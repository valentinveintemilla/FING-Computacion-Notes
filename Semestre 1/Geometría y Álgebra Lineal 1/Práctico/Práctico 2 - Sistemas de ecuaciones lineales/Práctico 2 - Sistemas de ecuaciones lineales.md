# Sistemas lineales
## Ejercicio 1
![[Semestre 1/Geometría y Álgebra Lineal 1/Práctico/Práctico 2 - Sistemas de ecuaciones lineales/Imágenes/Ejercicio 1.png]]
a)
$$
(a){\begin{cases}
-x+y-z=-1 \\
4x+2y-z=5 \\
x+z=2
\end{cases}}
$$
$F_{2} \leftarrow F_{2} + F_{3}$
$$
(a){\begin{cases}
-x+y-z=-1 \\
5x+2y=7 \\
x+z=2
\end{cases}}
$$
$F_{1} \leftarrow 2F_{1} - F_{2}$
$$
(a){\begin{cases}
-7x-2z=-9 \\
5x+2y=7 \\
x+z=2
\end{cases}}
$$
$F_{1} \leftarrow F_{1} + 2F_{3}$
$$
(a){\begin{cases}
-5x=-5 \\
5x+2y=7 \\
x+z=2
\end{cases}}
$$
$F_{1} \leftarrow \frac{F_{1}}{-5}$
$$
(a){\begin{cases}
x=1 \\
5x+2y=7 \\
x+z=2
\end{cases}}
$$
$F_{2} \leftarrow F_{2}-5F_{1}$
$F_{3} \leftarrow F_{3}-F_{1}$
$$
(a){\begin{cases}
x=1 \\
2y=2 \\
z=1
\end{cases}}
$$
$F_{2} \leftarrow \frac{F_{2}}{2}$
$$
(a){\begin{cases}
x=1 \\
y=1 \\
z=1
\end{cases}}
$$
$Sol(a)={(1,1,1)}$

A partir de ahora, voy a utilizar matrices para facilitar la representación.

c)
$$
(c){\begin{cases}
x-y+5z=-2 \\
2x+y+4z=2 \\
2x+4y-2z=10
\end{cases}}
$$
Matriz del sistema:
$$
\begin{pmatrix}
1 & -1 & 5 \\
2 & 1 & 4 \\
2 & 4 & -2
\end{pmatrix}
$$
Matriz ampliada:
$$
\left(
\begin{array}{ccc|c}
1 & -1 & 5 & -2 \\
2 & 1 & 4 & 2 \\
2 & 4 & -2 & 10
\end{array}
\right)
$$
Comenzamos a operar:
$$
\left(
\begin{array}{ccc|c}
3 & 0 & 9 & 0 \\
2 & 1 & 4 & 2 \\
-6 & 0 & -18 & 2
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + F_{2} \\
&F_{3} \leftarrow F_{3} - 4F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 0 & 0 & 2 \\
2 & 1 & 4 & 2 \\
-6 & 0 & -18 & 2
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow 2F_{1} + F_{3}
\end{align}
$$
Obtuvimos una igualdad sin sentido, en este caso en la fila uno, donde se declara 0=2, por lo que podemos detenernos en el planteamiento del problema y concluir que el sistema es incompatible.
$Sol(c)=\emptyset$

f)
$$
(f){\begin{cases}
x+2y-2z=1 \\
2x+2y-z=6 \\
3x+4y-3z=5
\end{cases}}
$$
Matriz del sistema:
$$
\begin{pmatrix}
1 & 2 & -2 \\
2 & 2 & -1 \\
3 & 4 & -3
\end{pmatrix}
$$
Matriz ampliada:
$$
\left(
\begin{array}{ccc|c}
1 & 2 & -2 & 1 \\
2 & 2 & -1 & 6 \\
3 & 4 & -3 & 5
\end{array}
\right)
$$
Comenzamos a operar:
$$
\left(
\begin{array}{ccc|c}
-1 & 0 & -1 & -5 \\
2 & 2 & -1 & 6 \\
-1 & 0 & -1 & -7
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2} \\
&F_{3} \leftarrow F_{3} - 2F_{2}
\end{align}
$$
Obtuvimos dos ecuaciones similares, pero con diferente resultado: $F_{1}$ y $F_{3}$.
Podemos restar ambos resultados, verificando que el sistema no tiene solución:
$$
\left(
\begin{array}{ccc|c}
0 & 0 & 0 & 2 \\
2 & 2 & -1 & 6 \\
-1 & 0 & -1 & -7
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{3}
\end{align}
$$
Llegamos a la incoherencia 0=2. Por esta razón, podemos decir que ambas funciones representadas gráficamente son paralelas, por lo que no tienen ningún elemento en común. De esta manera, podemos concluir que el conjunto solución es vacío, por lo que el sistema es incompatible.
$Sol(c)=\emptyset$

## Ejercicio 2
![[Semestre 1/Geometría y Álgebra Lineal 1/Práctico/Práctico 2 - Sistemas de ecuaciones lineales/Imágenes/Ejercicio 2.png]]a)
$$
(a){\begin{cases}
2w+y+z=6 \\
y-2z=-3 \\
x+2y-z=-2 \\
-2w+2x+y+3z=0
\end{cases}}
$$
Verificamos el orden los términos de las ecuaciones, de tal forma que las incógnitas queden en el mismo orden en todas las ecuaciones.
En forma de matriz ampliada:
$$
\left(
\begin{array}{cccc|c}
2 & 0 & 1 & 1 & 6 \\
0 & 0 & 1 & -2 & -3 \\
0 & 1 & 2 & -1 & -2 \\
-2 & 2 & 1 & 3 & 0
\end{array}
\right)
$$
Simplemente cambiamos de lugar $F_{2}$ y $F_{3}$.
Comenzamos a operar:
$$
\left(
\begin{array}{cccc|c}
2 & 0 & 1 & 1 & 6 \\
0 & 1 & 1 & 1 & 1 \\
0 & 0 & 1 & -2 & -3 \\
-2 & 2 & 1 & 3 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - F_{3}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
2 & 0 & 1 & 1 & 6 \\
0 & 1 & 1 & 1 & 1 \\
0 & 0 & 1 & -2 & -3 \\
0 & 2 & 2 & 4 & 6
\end{array}
\right)
\begin{align}
&F_{4} \leftarrow F_{4} + F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
2 & 0 & 1 & 1 & 6 \\
0 & 1 & 1 & 1 & 1 \\
0 & 0 & 1 & -2 & -3 \\
0 & 0 & 0 & 2 & 4
\end{array}
\right)
\begin{align}
&F_{4} \leftarrow F_{4} - 2F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
2 & 0 & 1 & 1 & 6 \\
0 & 1 & 1 & 1 & 1 \\
0 & 0 & 1 & 0 & 1 \\
0 & 0 & 0 & 1 & 2
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} + F_{4} \\
&F_{4} \leftarrow \frac{F_{4}}{2}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
2 & 0 & 1 & 1 & 6 \\
0 & 1 & 0 & 0 & -2 \\
0 & 0 & 1 & 0 & 1 \\
0 & 0 & 0 & 1 & 2
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - F_{3} \\
&F_{2} \leftarrow F_{2} - F_{4}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 0 & \frac{3}{2} \\
0 & 1 & 0 & 0 & -2 \\
0 & 0 & 1 & 0 & 1 \\
0 & 0 & 0 & 1 & 2
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{3} \\
&F_{1} \leftarrow F_{1} - F_{4} \\
&F_{1} \leftarrow \frac{F_{1}}{2}
\end{align}
$$
Llegamos a la conclusión de que el sistema es compatible determinado, siendo la solución del mismo $(\frac{3}{2}, -2, 1, 2)$.
$Sol(a)={(\frac{3}{2}, -2, 1, 2)}$

c)
$$
(c){\begin{cases}
w+2x+z=5 \\
-w+y=-1 \\
-w+3x-z=0 \\
w+4x+y+2z=9
\end{cases}}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 2 & 0 & 1 & 5 \\
-1 & 0 & 1 & 0 & -1 \\
-1 & 3 & 0 & -1 & 0 \\
1 & 4 & 1 & 2 & 9
\end{array}
\right)
$$
$$
\left(
\begin{array}{cccc|c}
0 & 2 & 1 & 1 & 4 \\
-1 & 0 & 1 & 0 & -1 \\
-1 & 3 & 0 & -1 & 0 \\
1 & 0 & -1 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + F_{2} \\
&F_{4} \leftarrow F_{4} - 2F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
0 & 2 & 1 & 1 & 4 \\
-1 & 0 & 1 & 0 & -1 \\
0 & 1 & 0 & 0 & 1 \\
1 & 0 & -1 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{2} \\
&F_{3} \leftarrow F_{3} + F_{1} \\
&F_{3} \leftarrow \frac{F_{3}}{5}
\end{align}
$$
Como podemos ver, las filas $F_{2}$ y $F_{4}$ son opuestas, por lo que al sumarlas, obtenemos una fila de ceros.
$$
\left(
\begin{array}{cccc|c}
0 & 2 & 1 & 1 & 4 \\
-1 & 0 & 1 & 0 & -1 \\
0 & 1 & 0 & 0 & 1 \\
0 & 0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{4} \leftarrow F_{4} + F_{2} \\
\end{align}
$$
Al tener una fila de ceros $(0=0)$ y ninguna contradicción, confirmamos que es un sistema compatible indeterminado.
Llegados a este punto, comenzaremos a operar sustituyendo, para expresar los valores en función de una variable (en este caso, utilizaremos z), ya que tenemos una fila nula ($F_{2}$ y $F_{4}$ se anulan, quedando $0=0$).
$$
\begin{align}
&F_{3}=x=1 \\
&F_{2} \text{ o } F_{4}=-w+y=-1 \implies w=y+1 \\
&F_{1}=2x+y+z=2+y+z=4 \implies y=4-2-z=2-z \\
&\text{Sustituyo y en la ecuación de w: }w=(2-z)+1=3-z \\
&\text{En conclusión, el conjunto solución es el siguiente: } Sol(c)={(3-\alpha, 1, 2-\alpha, \alpha):\alpha \in \mathbb{R}}
\end{align}
$$

## Ejercicio 3
![[Semestre 1/Geometría y Álgebra Lineal 1/Práctico/Práctico 2 - Sistemas de ecuaciones lineales/Imágenes/Ejercicio 3.png]]

a)
$$
(a){\begin{cases}
x + 2y − z = 0 \\
−x − 2y + z = 1
\end{cases}}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 2 & -1 & 0 \\
−1 & -2 & 1 & 1
\end{array}
\right)
$$
$$
\begin{align}
F_{1}+F_{2} = (x+2y-z) + (-x-2y+z) = 0 + 1 \\
=\not x-\not x+ \not 2y- \not 2y- \not z+ \not z=1 \\
0=1
\end{align}
$$
Como vemos, llegamos a una igualdad errónea, puesto que $0 \neq 1$. Por esta razón, podemos confirmar que se trata de un sistema incompatible, puesto que no hay valores de x, y, y z que funcionen para $x + 2y − z = 0$ y $−x − 2y + z = 1$ al mismo tiempo.

c)
$$
(c){\begin{cases}
w + x − y = 0 \\
2w + 3x − z = 0 \\
2w + x − 4y + z = 0
\end{cases}}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 1 & -1 & 0 & 0 \\
2 & 3 & 0 & -1 & 0 \\
2 & 1 & -4 & 1 & 0
\end{array}
\right)
$$
$$
\left(
\begin{array}{cccc|c}
1 & 1 & -1 & 0 & 0 \\
0 & 1 & 2 & -1 & 0 \\
0 & -1 & -2 & 1 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - 2F_{1} \\
&F_{3} \leftarrow F_{3} - 2F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 1 & -1 & 0 & 0 \\
0 & 1 & 2 & -1 & 0 \\
0 & 0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} + F_{2} \
\end{align}
$$
Como vemos, logramos anular una ecuación, haciendo que para 4 incógnitas queden solo 2 ecuaciones. De esta manera, confirmamos que es un sistema compatible indeterminado. A continuación, definimos las soluciones del mismo, tomando como referencia dos variables:
$$
\begin{align}
F_{1}=w+x-y=0 \\
\implies w = -x+y \\
F_{2}=x+2y-z=0 \\
\implies z = x+2y
\end{align}
$$
x e y son las variables que tomamos como "elementos de $\mathbb{R}$".
$Sol(c)={(\beta-\alpha,\alpha,\beta,\alpha+2\beta):\alpha, \beta \in \mathbb{R}}$

d)
$$
(d){\begin{cases}
x − y + z = 2 \\
4x − 2y − z = 2 \\
x + y + 5z = 2 \\
−x − y − z = 2
\end{cases}}
$$
$$
\left(
\begin{array}{ccc|c}
1 & -1 & 1 & 2 \\
4 & -2 & -1 & 2 \\
1 & 1 & 5 & 2 \\
-1 & -1 & -1 & 2
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
0 & -2 & 0 & 4 \\
4 & -2 & -1 & 2 \\
0 & 0 & 4 & 4 \\
-1 & -1 & -1 & 2
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + F_{4} \\
&F_{3} \leftarrow F_{3} + F_{4}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 1 & 0 & -2 \\
4 & -2 & -1 & 2 \\
0 & 0 & 1 & 1 \\
-1 & -1 & -1 & 2
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{F_{1}}{-2} \\
&F_{3} \leftarrow \frac{F_{3}}{4}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 1 & 0 & -2 \\
4 & 0 & -1 & -2 \\
0 & 0 & 1 & 1 \\
-1 & -1 & -1 & 2
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} + 2F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 1 & 0 & -2 \\
4 & 0 & 0 & -1 \\
0 & 0 & 1 & 1 \\
-1 & -1 & -1 & 2
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} + F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 1 & 0 & -2 \\
1 & 0 & 0 & -\frac{1}{4} \\
0 & 0 & 1 & 1 \\
-1 & -1 & -1 & 2
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow \frac{F_{2}}{4}
\end{align}
$$
Reordenamos las ecuaciones para ver la escalerización más claramente:
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & -\frac{1}{4} \\
0 & 1 & 0 & -2 \\
0 & 0 & 1 & 1 \\
-1 & -1 & -1 & 2
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow \frac{F_{2}}{4}
\end{align}
$$
Para verificar, finalmente sumamos las tres ecuaciones, y dicho resultado lo sumamos a $F_{4}$.
$$
\begin{align}
&x+y+z=-\frac{1}{4}-2+1=-\frac{5}{4} \\
&-x-y-z=2 \\
&x+y+z-x-y-z=-\frac{5}{4}+2 \\
&0=\frac{3}{4}?
\end{align}
$$
Como vemos, el sistema es incompatible, puesto que llegamos a una incoherencia con $F_{4}$.
$Sol(d)=\emptyset$

## Ejercicio 4
![[Semestre 1/Geometría y Álgebra Lineal 1/Práctico/Práctico 2 - Sistemas de ecuaciones lineales/Imágenes/Ejercicio 4.png]]
a)
$$
(a){\begin{cases}
z_{1} − z_{2} = i \\
(1 − i)z_{1} + (1 + i)z_{2} = 1
\end{cases}}
$$
Si $z_{1} - z_{2} = i \implies \mathrm{Re}(z_{1})=\mathrm{Re}(z_{2}) \land \mathrm{Im}(z_{1})-\mathrm{Im}(z_{2})=1$
$$
\begin{align} \\
&z_{1}=a+bi \\
&z_{2}=a+ci \\
&\implies z_{1} − z_{2} = i \\
&\Longleftrightarrow (a+bi) − (a+ci) = i \\ 
&(a-a)+(b-c)i=i \implies b-c=1 \\ \\

&(1 − i)z_{1} + (1 + i)z_{2} = 1 \\
&z_{1}-z_{1}i+z_{2}+z_{2}i=1 \\
&z_{1}i=(a+bi)i=ai+bi^{2}=ai-b \\
&\implies z_{2}i=ai-c \\ \\

&z_{1}-z_{1}i+z_{2}+z_{2}i=1 \\
&(a+bi)-(ai-b)+(a+ci)+(ai-c)=1 \\
&a+bi-ai+b+a+ci+ai-c=1 \\
&(a+b+a-c)+(b-a+c+a)i=1 \\
&(2a+b-c)+(b+c)i=1 \\
&b-c=1 \implies (2a+b-c)+(b+c)i=(2a+1)+(b+c)i=1 \\
&(2a+1)+(b+c)i=1 \implies \mathrm{Im}((2a+1)+(b+c)i)=0 \implies b+c=0 \\ \\
  
\end{align}
$$
Pasamos a desarrollar un nuevo sistema intermedio, para encontrar los valores de b y c en base a las ecuaciones $b-c=1$ y $b+c=0$
$$
\begin{cases}
b-c = 1 \\
b+c = 0
\end{cases}
$$
$$
\left(
\begin{array}{cc|c}
1 & -1 & 1 \\
1 & 1 & 0 \\
\end{array}
\right)
$$
$$
\left(
\begin{array}{cc|c}
1 & -1 & 1 \\
2 & 0 & 1 \\
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} + F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cc|c}
1 & -1 & 1 \\
1 & 0 & \frac{1}{2} \\
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow \frac{F_{2}}{2}
\end{align}
$$
$$
\left(
\begin{array}{cc|c}
0 & -1 & \frac{1}{2} \\
1 & 0 & \frac{1}{2} \\
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1}-F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cc|c}
0 & 1 & -\frac{1}{2} \\
1 & 0 & \frac{1}{2} \\
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} \times -1
\end{align}
$$
En conclusión, $b=\frac{1}{2}$ y $c=-\frac{1}{2}$.
$$
\begin{align}
&(2a+1)+(b+c)i=1 \land b=\frac{1}{2} \land c=-\frac{1}{2} \\
&\implies (2a+1)+\left( \frac{1}{2}-\frac{1}{2} \right)i=1 \\
&\implies (2a+1)+0i=1 \\
&\implies 2a+1=1 \\
\end{align}
$$
Ahora, simplemente nos falta despejar a y tendremos los valores de $z_{1}$ y $z_{2}$.
$$
\begin{align}
&2a+1=1 \\
&2a=1-1=0 \\
&a=\frac{0}{2}=0 \\
&a=0
\end{align}
$$
Logramos despejar la variable a, obteniendo $a=0$.
En definitiva, las variables son $a=0$, $b=\frac{1}{2}$ y $c=-\frac{1}{2}$.
De esta manera:
$$
\begin{align}
z_{1}=a+bi=0+\frac{1}{2}i=\frac{1}{2}i \\
z_{2}=a+ci=0-\frac{1}{2}i=-\frac{1}{2}i
\end{align}
$$

c)
$$
(c){\begin{cases}
2iz_{1} + (4 − 2i)z_{2} + 4z_{3} = 6 − 4i \\
2z_{1} + (−2 − 4i)z_{2} + (1 − 2i)z_{3} = 1 − i \\
(1 + i)z_{1} + (1 − 3i)z_{2} + (3 + i)z_{3} = 3 − 2i
\end{cases}}
$$
Esto nos da lugar a las siguientes formulas (tomando a los números complejos $z_{1}$, $z_{2}$ y $z_{3}$ como $a+bi$, $c+di$, $e+fi$):
$$
\begin{align}
&(c){\begin{cases}
2i(a+bi) + (4 − 2i)(c+di) + 4(e+fi) = 6 − 4i \\
2(a+bi) + (−2 − 4i)(c+di) + (1 − 2i)(e+fi) = 1 − i \\
(1 + i)(a+bi) + (1 − 3i)(c+di) + (3 + i)(e+fi) = 3 − 2i
\end{cases}} \\ \\

&\text{Ecuación 1} \\
&2i(a+bi) + (4 − 2i)(c+di) + 4(e+fi) = 6 − 4i \\
&2ai+2bi^{2} + 4c+4di-2ci-2di^{2} + 4e+4fi = 6 − 4i \\
&2ai-2b + 4c+4di-2ci+2d + 4e+4fi = 6 − 4i \\
&(-2b+4c+2d+4e) + (2a+4d-2c+4f)i = 6 − 4i \\
&\implies \mathrm{Re}((-2b+4c+2d+4e) + (2a+4d-2c+4f)i)=6=-2b+4c+2d+4e \\
&\land \mathrm{Im}((-2b+4c+2d+4e) + (2a+4d-2c+4f)i)=-4=2a+4d-2c+4f \\ \\

&\text{Ecuación 2} \\
&2(a+bi) + (−2 − 4i)(c+di) + (1 − 2i)(e+fi) = 1 − i \\
&2a+2bi - 2c-2di-4ci-4di^{2} + e+fi-2ei-2fi^{2} = 1 − i \\
&2a+2bi - 2c-2di-4ci+4d + e+fi-2ei+2f = 1 − i \\
&(2a-2c+4d+e+2f) + (2b-2d-4c+f-2e)i = 1 − i \\
&\implies \mathrm{Re}((2a-2c+4d+e+2f) + (2b-2d-4c+f-2e)i)=1=2a-2c+4d+e+2f \\
&\land \mathrm{Im}((2a-2c+4d+e+2f) + (2b-2d-4c+f-2e)i)=-1=2b-2d-4c+f-2e \\ \\

&\text{Ecuación 3} \\
&(1 + i)(a+bi) + (1 − 3i)(c+di) + (3 + i)(e+fi) = 3 − 2i \\
&a+bi+ai+bi^{2} + c+di-3ci-3di^{2} + 3e+3fi+ei+fi^{2} = 3 − 2i \\
&a+bi+ai-b + c+di-3ci+3d + 3e+3fi+ei-f = 3 − 2i \\
&(a-b+c+3d+3e-f) + (b+a+d-3c+3f+e)i = 3 − 2i \\
&\implies \mathrm{Re}((a-b+c+3d+3e-f) + (b+a+d-3c+3f+e)i)=3=a-b+c+3d+3e-f \\
&\land \mathrm{Im}((a-b+c+3d+3e-f) + (b+a+d-3c+3f+e)i)=-2=b+a+d-3c+3f+e \\ \\
&\end{align}
$$Si bien este es un método válido, formando un sistema con seis ecuaciones y seis incógnitas en total, es preferible proseguir con el método tradicional, al menos se manejan menos variables (únicamente 3, y no 2 por cada número complejo):
$$
\left(
\begin{array}{ccc|c}
2i & (4 − 2i) & 4 & 6 − 4i \\
2 & (−2 − 4i) & (1 − 2i) & 1 − i \\
(1 + i) & (1 − 3i) & (3 + i) & 3 − 2i
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
i & (2 − 1i) & 2 & 3 − 2i \\
2 & (−2 − 4i) & (1 − 2i) & 1 − i \\
(1 + i) & (1 − 3i) & (3 + i) & 3 − 2i
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{F_{1}}{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
-1 & (1 + 2i) & (-1 - i) & 0 \\
2 & (−2 − 4i) & (1 − 2i) & 1 − i \\
(1 + i) & (1 − 3i) & (3 + i) & 3 − 2i
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1}-F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
-2 & (2 + 4i) & (-2 - 2i) & 0 \\
2 & (−2 − 4i) & (1 − 2i) & 1 − i \\
(1 + i) & (1 − 3i) & (3 + i) & 3 − 2i
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow 2F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 0 & (-1 - 4i) & 1 − i \\
2 & (−2 − 4i) & (1 − 2i) & 1 − i \\
(1 + i) & (1 − 3i) & (3 + i) & 3 − 2i
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1}+F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 0 & 1 & \frac{1 − i}{-1 - 4i} \\
2 & (−2 − 4i) & (1 − 2i) & 1 − i \\
(1 + i) & (1 − 3i) & (3 + i) & 3 − 2i
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{F_{1}}{-1 - 4i}
\end{align}
$$
Resolvemos la división:
$$
\begin{align}
&\frac{1 − i}{-1 - 4i} \\
&= \frac{(1 − i)(-1+4i)}{(-1 - 4i)(-1+4i)} \\
&= \frac{-1+4i+i-4i^{2}}{1-4i+4i-16i^{2}} \\
&= \frac{(-1+4)+(4+1)i}{(1+16)+(-4+4)i} \\
&= \frac{(-1+4)+(4+1)i}{(1+16)+(-4+4)i} \\
&= \frac{3+5i}{17+(-\not4+\not4)i} \\
&= \frac{3}{17} + \frac{5}{17}i
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 0 & 1 & \frac{3}{17} + \frac{5}{17}i \\
2 & (−2 − 4i) & (1 − 2i) & 1 − i \\
(1 + i) & (1 − 3i) & (3 + i) & 3 − 2i
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{F_{1}}{-1 - 4i}
\end{align}
$$
A continuación, desarrollaremos un sistema $2 \times 2$, incluyendo las ecuaciones $F_{2}$ y $F_{3}$. Sin embargo, primero debemos calcular el valor de las variables que tienen a $z_{3}$ como incógnita, pues ya descubrimos su valor:
$$
\begin{align}
&F_{2} = 2z_{1} + (−2 − 4i)z_{2} + (1 − 2i)z_{3} = 1 − i \\
&= 2z_{1} + (−2 − 4i)z_{2} + (1 − 2i)\left( \frac{3}{17} + \frac{5}{17}i \right) = 1 − i \\
&= 2z_{1} + (−2 − 4i)z_{2} + \frac{3}{17}+\frac{5}{17}i-\frac{6}{17}i-\frac{10}{17}i^{2} = 1 − i \\
&= 2z_{1} + (−2 − 4i)z_{2} + \frac{3}{17}+\frac{5}{17}i-\frac{6}{17}i+\frac{10}{17} = 1 − i \\
&= 2z_{1} + (−2 − 4i)z_{2} + \frac{13}{17}-\frac{1}{17}i = 1 − i \\
&= 2z_{1} + (−2 − 4i)z_{2} = 1 − i -\frac{13}{17}+\frac{1}{17}i \\
&= 2z_{1} + (−2 − 4i)z_{2} = (1-\frac{13}{17}) + (-1+\frac{1}{17})i \\
&= 2z_{1} + (−2 − 4i)z_{2} = \frac{4}{17} -\frac{16}{17}i \\ \\ \\

&F_{3} = (1 + i)z_{1} + (1 − 3i)z_{2} + (3 + i)z_{3} = 3 − 2i \\
&= (1 + i)z_{1} + (1 − 3i)z_{2} + (3 + i)\left( \frac{3}{17} + \frac{5}{17}i \right) = 3 − 2i \\
&= (1 + i)z_{1} + (1 − 3i)z_{2} + \frac{9}{17}+\frac{15}{17}i+\frac{3}{17}i+\frac{5}{17}i^{2} = 3 − 2i \\
&= (1 + i)z_{1} + (1 − 3i)z_{2} + \frac{9}{17}+\frac{15}{17}i+\frac{3}{17}i-\frac{5}{17} = 3 − 2i \\
&= (1 + i)z_{1} + (1 − 3i)z_{2} + \frac{4}{17}+\frac{18}{17}i = 3 − 2i \\
&= (1 + i)z_{1} + (1 − 3i)z_{2} = 3 − 2i - \frac{4}{17} - \frac{18}{17}i \\
&= (1 + i)z_{1} + (1 − 3i)z_{2} = (3-\frac{4}{17}) + (-2 - \frac{18}{17})i \\
&= (1 + i)z_{1} + (1 − 3i)z_{2} = \frac{47}{17} - \frac{52}{17}i
\end{align}
$$
$$
(c){\begin{cases}
2z_{1} + (−2 − 4i)z_{2} = \frac{4}{17} + -\frac{16}{17}i \\
(1 + i)z_{1} + (1 − 3i)z_{2} = \frac{47}{17} - \frac{52}{17}i
\end{cases}}
$$
$$
\left(
\begin{array}{cc|c}
2 & (−2 − 4i) & \frac{4}{17} -\frac{16}{17}i \\
(1 + i) & (1 − 3i) & \frac{47}{17} - \frac{52}{17}i
\end{array}
\right)
$$
$$
\left(
\begin{array}{cc|c}
(-2-2i) & (-2+6i) & -\frac{20}{17} +\frac{12}{17}i \\
(1 + i) & (1 − 3i) & \frac{47}{17} - \frac{52}{17}i
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} \times (-1-i)
\end{align}
$$
$$
\left(
\begin{array}{cc|c}
0 & 0 & \frac{74}{17} - \frac{92}{17}i \\
(1 + i) & (1 − 3i) & \frac{47}{17} - \frac{52}{17}i
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + 2F_{2}
\end{align}
$$
Como vemos, conseguimos anular una ecuación, pero obteniendo un resultado incoherente $0=\frac{74}{17}-\frac{92}{17}i$. De esta manera, podemos concluir en que el sistema es incompatible.
$Sol(c)=\emptyset$

## Ejercicio 5
![[Ejercicio 5.png]]
a)
$$
\left(
\begin{array}{ccccc}
1 & -3 & 0 & -1 & 0 \\
0 & 1 & 0 & 0 & -4 \\
1 & 0 & 0 & 1 & 9
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccccc}
1 & -3 & 0 & -1 & 0 \\
0 & 1 & 0 & 0 & -4 \\
0 & 3 & 0 & 2 & 9
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccccc}
1 & -3 & 0 & -1 & 0 \\
0 & 1 & 0 & 0 & -4 \\
0 & 0 & 0 & 2 & 21
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - 3F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccccc}
1 & -3 & 0 & -1 & 0 \\
0 & 1 & 0 & 0 & -4 \\
0 & 0 & 0 & 1 & \frac{21}{2}
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow \frac{F_{3}}{2}
\end{align}
$$
$$
\left(
\begin{array}{ccccc}
1 & 0 & 0 & -1 & -12 \\
0 & 1 & 0 & 0 & -4 \\
0 & 0 & 0 & 1 & \frac{21}{2}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + 3F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccccc}
1 & 0 & 0 & 0 & -\frac{3}{2} \\
0 & 1 & 0 & 0 & -4 \\
0 & 0 & 0 & 1 & \frac{21}{2}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + F_{3}
\end{align}
$$
$$
{\begin{cases}
a -\frac{3}{2}e = 0 \\
b -4e = 0 \\
d + \frac{21}{2}e = 0
\end{cases}}
$$
$$
{\begin{cases}
a = \frac{3}{2}e \\
b = 4e \\
c = \beta \\
d = -\frac{21}{2}e \\
e = \alpha
\end{cases}}
$$
$$
Sol(a) = \left\{  \left( \frac{3}{2}\alpha, 4\alpha, \beta, -\frac{21}{2}\alpha, \alpha \right): \alpha, \beta \in \mathbb{R}  \right\}
$$
Como vector:
$$
Sol(a) = \left\{ 
\left( 0,0,0,0,0 \right)
+ \alpha\left( \frac{3}{2},4,0,-\frac{21}{2},1 \right)
+ \beta\left( 0,0,1,0,0 \right)
: \alpha, \beta \in \mathbb{R}  \right\}
$$
b)
$$
\left(
\begin{array}{ccccc}
1 & 0 & -5 & 0 & -8 \\
0 & 1 & 4 & -1 & 0 \\
0 & 0 & 0 & 0 & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccccc}
1 & 0 & -5 & 0 & 0 \\
0 & 1 & 4 & -1 & 0 \\
0 & 0 & 0 & 0 & 1
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + 8F_{3}
\end{align}
$$
$$
{\begin{cases}
a - 5c = 0 \\
b + 4c - d = 0 \\
e = 0
\end{cases}}
$$
$$
{\begin{cases}
a = 5c \\
b = -4c + d \\
c = \alpha \\
d = \beta \\
e = 0
\end{cases}}
$$
$$
Sol(b) = \left\{  \left( 5\alpha,-4\alpha+\beta,\alpha,\beta,0 \right): \alpha, \beta \in \mathbb{R}  \right\}
$$
Como vector:
$$
Sol(b) = \left\{ 
\left( 0,0,0,0,0 \right)
+ \alpha\left( 5,-4,1,0,0 \right)
+ \beta\left( 0,1,0,1,0 \right)
: \alpha, \beta \in \mathbb{R}  \right\}
$$
c)
$$
\left(
\begin{array}{ccccc}
1 & -5 & 4 & 0 & 0 \\
0 & 1 & 0 & 1 & 0 \\
0 & 0 & 3 & 0 & 0 \\
0 & 0 & 0 & 1 & 2
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccccc}
1 & 0 & 4 & 5 & 0 \\
0 & 1 & 0 & 1 & 0 \\
0 & 0 & 1 & 0 & 0 \\
0 & 0 & 0 & 1 & 2
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow \frac{F_{3}}{3}
\end{align}
$$
$$
\left(
\begin{array}{ccccc}
1 & 0 & 4 & 5 & 0 \\
0 & 1 & 0 & 1 & 0 \\
0 & 0 & 1 & 0 & 0 \\
0 & 0 & 0 & 1 & 2
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + 5F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccccc}
1 & 0 & 0 & 5 & 0 \\
0 & 1 & 0 & 1 & 0 \\
0 & 0 & 1 & 0 & 0 \\
0 & 0 & 0 & 1 & 2
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - 4F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccccc}
1 & 0 & 0 & 0 & -10 \\
0 & 1 & 0 & 0 & -2 \\
0 & 0 & 1 & 0 & 0 \\
0 & 0 & 0 & 1 & 2
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - 5F_{4} \\
&F_{2} \leftarrow F_{2} - F_{4}
\end{align}
$$
$$
{\begin{cases}
a - 10e = 0 \\
b - 2e = 0 \\
c = 0 \\
d + 2e = 0
\end{cases}}
$$
$$
{\begin{cases}
a = 10e \\
b = 2e \\
c = 0 \\
d = -2e \\
e = \alpha
\end{cases}}
$$
$$
Sol(c) = \left\{  \left( 10\alpha, 2\alpha, 0, -2\alpha, \alpha \right): \alpha \in \mathbb{R}  \right\}
$$
Como vector:
$$
Sol(c) = \left\{ 
\left( 0,0,0,0,0 \right)
+ \alpha\left( 10, 2, 0, -2, 1 \right)
: \alpha \in \mathbb{R}  \right\}
$$

## Ejercicio 6
![[Semestre 1/Geometría y Álgebra Lineal 1/Práctico/Práctico 2 - Sistemas de ecuaciones lineales/Imágenes/Ejercicio 6.png]]
a)
$$
(a){\begin{cases}
x + y = 2 \\
x + \lambda y = 4 
\end{cases}}
$$
Lo importante aquí es intentar que no queden operaciones de tipo $\frac{a}{\lambda}, \forall a \in \mathbb{R}$, ya que si esto ocurre, hay que distinguir casos (que pasa si $\lambda$ es 0, por ejemplo).
$$
\left(
\begin{array}{cc|c}
1 & 1 & 2 \\
1 & \lambda & 4
\end{array}
\right)
$$
$$
\left(
\begin{array}{cc|c}
1 & 1 & 2 \\
0 & \lambda-1 & 2
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - F_{1}
\end{align}
$$
Ahora, tenemos dos casos posibles para lambda:
1. $\lambda=1$
$$
\left(
\begin{array}{cc|c}
1 & 1 & 2 \\
0 & 0 & 2
\end{array}
\right)
\begin{align}
&\implies \text{Incompatible} \\
&Sol(a) \text{ (si } \lambda = 1) = \text{Incompatible}
\end{align}
$$
2. $\lambda \neq 1$
$$
\begin{align}
&y(\lambda-1)=2 \\
&y=\frac{2}{\lambda-1} \\
&\implies \text{(en la primer ecuación)} \\
&x+\frac{2}{\lambda-1}=2 \\
&x=2-\frac{2}{\lambda-1} \\
&Sol(a) \text{ (si } \lambda \neq 1) = \text{Compatible determinado}
\end{align}
$$

d)
$$
(d){\begin{cases}
x + y − z = 2 \\
x + 2y + z = 3 \\
x + y + (λ − 5)z = λ
\end{cases}}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & -1 & 2 \\
1 & 2 & 1 & 3 \\
1 & 1 & (λ − 5) & λ
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & -1 & 2 \\
1 & 2 & 1 & 3 \\
0 & 0 & λ − 4 & λ-2
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{1}
\end{align}
$$
Ahora, nos quedan dos casos posibles para $\lambda$:
1. $\lambda=4$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & -1 & 2 \\
1 & 2 & 1 & 3 \\
0 & 0 & 0 & 2
\end{array}
\right)
\begin{align}
&\implies \text{Incompatible} \\
&Sol(a) \text{ (si } \lambda = 4) = \text{Incompatible}
\end{align}
$$
2. $\lambda \neq 4$
$$
\begin{align}
&z(\lambda-4)=\lambda-2 \\
&z=\frac{\lambda-2}{\lambda-4} \\

\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & -1 & 2 \\
1 & 2 & 1 & 3 \\
0 & 0 & 1 & \frac{\lambda-2}{\lambda-4}
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 0 & 2 + \frac{\lambda-2}{\lambda-4} \\
1 & 2 & 0 & 3 - \frac{\lambda-2}{\lambda-4} \\
0 & 0 & 1 & \frac{\lambda-2}{\lambda-4}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + F_{3} \\
&F_{2} \leftarrow F_{2} - F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 0 & 2 + \frac{\lambda-2}{\lambda-4} \\
0 & 1 & 0 & 1 - \frac{\lambda-2}{\lambda-4} \\
0 & 0 & 1 & \frac{\lambda-2}{\lambda-4}
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - F_{1}
\end{align}
$$
$$
\begin{align}
&y=1-\frac{\lambda-2}{\lambda-4} \\
&=\frac{\lambda-4}{\lambda-4}-\frac{\lambda-2}{\lambda-4} \\
&=\frac{\lambda-4}{\lambda-4}+\frac{-(\lambda-2)}{\lambda-4} \\
&=\frac{\lambda-4-(\lambda-2)}{\lambda-4} \\
&=\frac{\not \lambda-4- \not \lambda+2}{\lambda-4} \\
&=\frac{-4 + 2}{\lambda-4} \\
&=\frac{-2}{\lambda-4}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 0 & 2 + \frac{\lambda-2}{\lambda-4} \\
0 & 1 & 0 & \frac{-2}{\lambda-4} \\
0 & 0 & 1 & \frac{\lambda-2}{\lambda-4}
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & 2 + \frac{\lambda-2}{\lambda-4} - \frac{-2}{\lambda-4} \\
0 & 1 & 0 & \frac{-2}{\lambda-4} \\
0 & 0 & 1 & \frac{\lambda-2}{\lambda-4}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2}
\end{align}
$$
$$
\begin{align}
&x=2 + \frac{\lambda-2}{\lambda-4} - \frac{-2}{\lambda-4} \\
&=2 + \frac{\lambda-2}{\lambda-4} + \frac{2}{\lambda-4} \\
&=2 + \frac{\lambda- \not 2+ \not 2}{\lambda-4} \\
&=2 + \frac{\lambda}{\lambda-4} \\
&=\frac{2(\lambda-4)}{\lambda-4} + \frac{\lambda}{\lambda-4} \\
&=\frac{2(\lambda-4)+\lambda}{\lambda-4} \\
&=\frac{2\lambda-8+\lambda}{\lambda-4} \\
&=\frac{3\lambda-8}{\lambda-4}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & \frac{3\lambda-8}{\lambda-4} \\
0 & 1 & 0 & \frac{-2}{\lambda-4} \\
0 & 0 & 1 & \frac{\lambda-2}{\lambda-4}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2}
\end{align}
$$
$$Sol(a) \text{ (si } \lambda \neq 4) = \text{Compatible determinado}$$
## Ejercicio 7
![[Ejercicio 7.png]]
a)
$$
(a){\begin{cases}
x + y + z = \alpha \\
x + y + \beta z = 1 
\end{cases}}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & \alpha \\
1 & 1 & \beta & 1
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & \alpha \\
0 & 0 & \beta-1 & 1-\alpha
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - F_{1}
\end{align}
$$
Ahora, tenemos dos casos posibles para $\beta$:
1. $\beta=1$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & \alpha \\
0 & 0 & 0 & 1-\alpha
\end{array}
\right)
$$
	1. $\alpha=1$
El resultado de $1-\alpha = 0$, por lo tanto podemos proseguir:
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 1 \\
0 & 0 & 0 & 0
\end{array}
\right)
$$
Como vemos, anulamos $F_{2}$, de forma que únicamente nos queda una ecuación efectiva: $x+y+z=1$.
De esta manera, concluimos en que el sistema es Compatible Indeterminado, pero ahora con dos parámetros libres ($\alpha$ y $\beta$ ya no forman parte).
	2. $\alpha != 1$
El resultado de $1-\alpha \neq 0$, de forma que:
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & \alpha \\
0 & 0 & 0 & 1-\alpha
\end{array}
\right)
\begin{align}
\implies &\text{Sistema Incompatible} \\
&Sol(a) \text{ (si } \beta = 1 \land \alpha = 1) = \emptyset
\end{align}
$$
2. $\beta \neq 1$
$$
\begin{align}
&z(\beta-1)=1-\alpha \\
&z=\frac{1-\alpha}{\beta-1} \\
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & \alpha \\
0 & 0 & 1 & \frac{1-\alpha}{\beta-1}
\end{array}
\right)
$$
Como tenemos un sistema con 2 ecuaciones efectivas y tres incógnitas, el sistema es Compatible indeterminado. Hay infinitas soluciones que dependerán de un parámetro, pudiendo dejar a x o y como variable libre.

Este razonamiento se basa en el Teorema de Rouché-Frobenius, el cual se basa en el concepto de "grados de libertad":
Yo tengo un sistema con n incógnitas, representando la cantidad de dimensiones que puedo manejar (siendo n en este caso), y r el rango de la matriz (número de ecuaciones efectivas o filas no nulas luego de escalerizar). Teniendo en cuenta que el sistema sea consistente (no hayan incoherencias o igualdades incorrectas), podemos confirmar que:
1. Si r = n: el sistema es Compatible Determinado (única solución).
2. Si r < n: el sistema es Compatible Indeterminado (infinitas soluciones).

b)
$$
(b){\begin{cases}
\alpha x + 2y + 3z = 4 \\
4x + 5y + \beta z = 3 \\
14x + 16y + 3 \beta z = 0
\end{cases}}
$$
$$
\left(
\begin{array}{ccc|c}
\alpha & 2 & 3 & 4 \\
4 & 5 & \beta & 3 \\
14 & 16 & 3 \beta & 0
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
4 & 5 & \beta & 3 \\
\alpha & 2 & 3 & 4 \\
14 & 16 & 3 \beta & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftrightarrow F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
4 & 5 & \beta & 3 \\
0 & \frac{8-5\alpha}{4} & \frac{12-\alpha \beta}{4} & \frac{16-3\alpha}{4} \\
0 & -\frac{6}{4} & -\frac{2}{4} \beta & -\frac{42}{4}
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - \frac{\alpha}{4}F_{1} \\
&F_{3} \leftarrow F_{3} - \frac{14}{4}F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
4 & 5 & \beta & 3 \\
0 & 8-5\alpha & 12-\alpha \beta & 16-3\alpha \\
0 & -6 & -2 \beta & -42
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow 4F_{2} \\
&F_{3} \leftarrow 4F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
4 & 5 & \beta & 3 \\
0 & 8-5\alpha & 12-\alpha \beta & 16-3\alpha \\
0 & 3 & \beta & 21
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow \frac{F_{2}}{-2} \\
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
4 & 5 & \beta & 3 \\
0 & 3 & \beta & 21 \\
0 & 8-5\alpha & 12-\alpha \beta & 16-3\alpha
\end{array}
\right)
\begin{align}
&F_{2} \leftrightarrow F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
4 & 5 & \beta & 3 \\
0 & 3 & \beta & 21 \\
0 & 0 & 12-\alpha \beta & 16-3\alpha
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - \frac{8-5\alpha}{3}F_{2}
\end{align}
$$
Realizamos la operación a continuación:
$$
\begin{align}
&12-\alpha \beta - \left( \beta \times \frac{8-5\alpha}{3} \right) \\
&=12-\alpha \beta - \left(\frac{\beta(8-5\alpha)}{3} \right) \\
&=12-\alpha \beta - \frac{8\beta-5\alpha \beta}{3} \\
&=12-\alpha \beta - \frac{8\beta}{3}+\frac{5\alpha \beta}{3} \\
&=12-\frac{3\alpha \beta}{3} - \frac{8\beta}{3}+\frac{5\alpha \beta}{3} \\
&=12+\frac{2\alpha \beta}{3} - \frac{8\beta}{3} \\
&=12+\frac{2\alpha \beta-8\beta}{3} \\ \\

&\text{Término independiente} \\
&16-3\alpha-21\frac{8-5\alpha}{3} \\
&=16-3\alpha-\frac{168-105\alpha}{3} \\
&=16-3\alpha+\frac{-168+105\alpha}{3} \\
&=16-3\alpha-56+35\alpha \\
&=-40+32\alpha
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
4 & 5 & \beta & 3 \\
0 & 3 & \beta & 21 \\
0 & 0 & 12+\frac{2}{3}\alpha \beta- \frac{8}{3}\beta & -40+32\alpha
\end{array}
\right)
\begin{align}

\end{align}
$$
$$
12+\frac{2}{3}\alpha \beta - \frac{8}{3} \beta = 0
$$
Ahora, despejaremos el valor de $\beta$ en la expresión anterior:
$$
\begin{align}
&12+\frac{2}{3}\alpha \beta - \frac{8}{3} \beta = 0 \\
&\frac{2}{3}\alpha \beta - \frac{8}{3} \beta = -12 \\
&\frac{\beta}{3}(2\alpha-8)=-12 \\
&\beta(2\alpha-8)=-36 \\
&\implies \beta = -\frac{36}{2\alpha-8} \\
&= -\frac{18}{\alpha-4}
\end{align}
$$
Aquí ya tenemos la primer ramificación de casos:
1. $\alpha = 4$
$$
\begin{align}
&12+\frac{\beta}{3}(-8+2\alpha) \\
&=12+\frac{\beta}{3}(-8+8) \\
&=12+\frac{\beta}{3} \times 0 \\
&=12+0 \\
&=12 \\
\end{align}
$$
$\implies$ El sistema es Compatible Determinado para todo $\beta \in \mathbb{R}$, ya que $12 \neq 0$, quedando la tercer ecuación "fija" (o al menos su coeficiente), ya que no depende de ninguna otra variable como $\alpha$ o $\beta$.
$$
\left(
\begin{array}{ccc|c}
4 & 5 & \beta & 3 \\
0 & 3 & \beta & 21 \\
0 & 0 & 1 & \frac{22}{3}
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow \frac{F_{3}}{12}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
4 & 5 & 0 & 3 - \frac{22}{3}\beta \\
0 & 3 & 0 & 21 - \frac{22}{3}\beta \\
0 & 0 & 1 & \frac{22}{3}
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2}-\beta F_{3} \\
&F_{1} \leftarrow F_{1}-\beta F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
4 & 5 & 0 & 3 - \frac{22}{3}\beta \\
0 & 1 & 0 & 7 - \frac{22}{9}\beta \\
0 & 0 & 1 & \frac{22}{3}
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow \frac{F_{2}}{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
4 & 0 & 0 & -32 - \frac{44}{9}\beta \\
0 & 1 & 0 & 7 - \frac{22}{9}\beta \\
0 & 0 & 1 & \frac{22}{3}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1}-5F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & -8 + \frac{11}{9}\beta \\
0 & 1 & 0 & 7 - \frac{22}{9}\beta \\
0 & 0 & 1 & \frac{22}{3}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{F_{1}}{4}
\end{align}
$$
De esta forma, obtuvimos los valores de x, y y z, cuando $\alpha = 4$.
$Sol(b) \text{ (si } \alpha = 4) = {\left(  -8+\frac{11}{9}\beta, 7-\frac{22}{9}\beta, \frac{22}{3} \right)}$

Proseguimos con el resto de casos:
2. $\alpha \neq 4$
Aquí tenemos dos casos diferentes:
	1. $\beta \neq -\frac{18}{\alpha-4}$
Como no tenemos valores fijos para $\alpha$ ni para $\beta$, entonces tenemos que proseguir despejando z de la tercer fila:
$$
\begin{align}
&z\left( 12+\frac{2}{3}\alpha \beta- \frac{8}{3}\beta \right) = -40+32\alpha \\
&z=\frac{-40+32\alpha}{12+\frac{2}{3}\alpha \beta- \frac{8}{3}\beta} \\
&z=\frac{3(-40+32\alpha)}{3\left( 12+\frac{2}{3}\alpha \beta- \frac{8}{3}\beta \right)} \\
&z=\frac{-120+96\alpha}{36+ 2\alpha \beta- 8\beta} \\
&z=\frac{\frac{-120+96\alpha}{2}}{\frac{36+ 2\alpha \beta- 8\beta}{2}} \\
&z=\frac{-60+48\alpha}{18+ \alpha \beta- 4\beta} \\
&z=\frac{12(4\alpha-5)}{18+ \beta(\alpha- 4)}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
4 & 5 & \beta & 3 \\
0 & 3 & \beta & 21 \\
0 & 0 & 1 & \frac{12(4\alpha-5)}{18+ \beta(\alpha- 4)}
\end{array}
\right)
\begin{align}

\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
4 & 5 & 0 & \frac{54+ 3\beta(\alpha- 4)}{18+ \beta(\alpha- 4)} - \frac{12\beta(4\alpha-5)}{18+ \beta(\alpha- 4)} \\
0 & 3 & 0 & \frac{378+ 21\beta(\alpha- 4)}{18+ \beta(\alpha- 4)} - \frac{12\beta(4\alpha-5)}{18+ \beta(\alpha- 4)} \\
0 & 0 & 1 & \frac{12(4\alpha-5)}{18+ \beta(\alpha- 4)}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - \beta F_{3} \\
&F_{2} \leftarrow F_{2} - \beta F_{3}
\end{align}
$$
$$
\begin{align}
&\text{Para la fila 1:} \\
&\frac{54+ 3\beta(\alpha- 4)}{18+ \beta(\alpha- 4)} - \frac{12(4\alpha-5)}{18+ \beta(\alpha- 4)} \\
&=\frac{54+ 3\beta(\alpha- 4)-12\beta(4\alpha-5)}{18+ \beta(\alpha- 4)} \\
&=\frac{54+ 3\beta\alpha - 12\beta - 48\beta \alpha + 60\beta}{18+ \beta(\alpha- 4)} \\
&=\frac{54 -45\beta\alpha + 48\beta}{18+ \beta(\alpha- 4)} \\
&=\frac{54 +3\beta(16 - 15\alpha)}{18+ \beta(\alpha- 4)} \\ \\

&\text{Para la fila 2:} \\
&\frac{378+ 21\beta(\alpha- 4)}{18+ \beta(\alpha- 4)} - \frac{12\beta(4\alpha-5)}{18+ \beta(\alpha- 4)} \\
&=\frac{378+ 21\beta(\alpha- 4)-12\beta(4\alpha-5)}{18+ \beta(\alpha- 4)} \\
&=\frac{378+ 21\beta\alpha - 84\beta - 48\beta \alpha + 60\beta}{18+ \beta(\alpha- 4)} \\
&=\frac{378 -27\beta\alpha - 24\beta}{18+ \beta(\alpha- 4)} \\
&=\frac{378 -3\beta(8 + 9\alpha)}{18+ \beta(\alpha- 4)}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
4 & 5 & 0 & \frac{54 +3\beta(16 - 15\alpha)}{18+ \beta(\alpha- 4)} \\
0 & 3 & 0 & \frac{378 -3\beta(8 + 9\alpha)}{18+ \beta(\alpha- 4)} \\
0 & 0 & 1 & \frac{12(4\alpha-5)}{18+ \beta(\alpha- 4)}
\end{array}
\right)
\begin{align}

\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
4 & 5 & 0 & \frac{54 +3\beta(16 - 15\alpha)}{18+ \beta(\alpha- 4)} \\
0 & 1 & 0 & \frac{126 -\beta(8 + 9\alpha)}{18+ \beta(\alpha- 4)} \\
0 & 0 & 1 & \frac{12(4\alpha-5)}{18+ \beta(\alpha- 4)}
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow \frac{F_{2}}{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
4 & 5 & 0 & \frac{54 +3\beta(16 - 15\alpha)}{18+ \beta(\alpha- 4)} \\
0 & 1 & 0 & \frac{126 -\beta(8 + 9\alpha)}{18+ \beta(\alpha- 4)} \\
0 & 0 & 1 & \frac{12(4\alpha-5)}{18+ \beta(\alpha- 4)}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - 5F_{2}
\end{align}
$$
$$
\begin{align}
&\frac{54 +3\beta(16 - 15\alpha)}{18+ \beta(\alpha- 4)} - 5\left( \frac{126 -\beta(8 + 9\alpha)}{18+ \beta(\alpha- 4)} \right) \\
&=\frac{54 +3\beta(16 - 15\alpha)}{18+ \beta(\alpha- 4)} - \frac{630 -5\beta(8 + 9\alpha)}{18+ \beta(\alpha- 4)} \\
&=\frac{54 +3\beta(16 - 15\alpha)-630 +5\beta(8 + 9\alpha)}{18+ \beta(\alpha- 4)} \\
&=\frac{54 +48\beta - 45\alpha \beta-630 + 40\beta + 45\alpha \beta}{18+ \beta(\alpha- 4)} \\
&=\frac{54-630 +48\beta+40\beta - 45\alpha \beta + 45\alpha \beta}{18+ \beta(\alpha- 4)} \\
&=\frac{-576 +88\beta}{18+ \beta(\alpha- 4)}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
4 & 0 & 0 & \frac{-576 +88\beta}{18+ \beta(\alpha- 4)} \\
0 & 1 & 0 & \frac{126 -\beta(8 + 9\alpha)}{18+ \beta(\alpha- 4)} \\
0 & 0 & 1 & \frac{12(4\alpha-5)}{18+ \beta(\alpha- 4)}
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
4 & 0 & 0 & \frac{-576 +88\beta}{18+ \beta(\alpha- 4)} \\
0 & 1 & 0 & \frac{126 -\beta(8 + 9\alpha)}{18+ \beta(\alpha- 4)} \\
0 & 0 & 1 & \frac{12(4\alpha-5)}{18+ \beta(\alpha- 4)}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{F_{1}}{4}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & \frac{-144 +22\beta}{18+ \beta(\alpha- 4)} \\
0 & 1 & 0 & \frac{126 -\beta(8 + 9\alpha)}{18+ \beta(\alpha- 4)} \\
0 & 0 & 1 & \frac{12(4\alpha-5)}{18+ \beta(\alpha- 4)}
\end{array}
\right)
\begin{align}
\end{align}
$$
$\implies$ El sistema es Compatible Determinado
$Sol(b) \text{ (si } \alpha \neq 4 \land \beta \neq -\frac{18}{\alpha-4}) = {(\frac{-144 +22\beta}{18+ \beta(\alpha- 4)}, \frac{126 -\beta(8 + 9\alpha)}{18+ \beta(\alpha- 4)}, \frac{12(4\alpha-5)}{18+ \beta(\alpha- 4)})}$
	2. $\beta = -\frac{18}{\alpha-4}$
Este es el caso donde el coeficiente de z se vuelve cero, por lo tanto:
$$
\left(
\begin{array}{ccc|c}
4 & 5 & \beta & 3 \\
0 & 3 & \beta & 2 \\
0 & 0 & 0 & -40+32\alpha
\end{array}
\right)
\begin{align}

\end{align}
$$
El sistema es incompatible en caso de que $-40 + 32\alpha \neq 0$ y compatible indeterminado si $-40 + 32\alpha = 0$.
$$
\begin{align}
&-40+32\alpha = 0 \\
&32\alpha = 40 \\
&\alpha=\frac{40}{32} \\
&\alpha=\frac{5}{4}
\end{align}
$$
De esta forma, nos vuelven a quedar dos casos:
		1.$\alpha = \frac{5}{4}$
Aquí el sistema es Compatible Indeterminado, ya que logramos anular una ecuación, tomando como referencia Rouché-Frobenius, en base al rango de la matriz.
$\implies$ El sistema es Compatible Indeterminado
		2.$\alpha \neq \frac{5}{4}$
En este caso, el sistema es Incompatible, puesto que llegamos a una incoherencia.
$\implies$ El sistema es Incompatible

Entonces, tenemos un total de 4 casos diferentes
1. $\alpha = 4 \rightarrow Sol(b) \text{ (si } \alpha = 4) = {\left(  -8+\frac{11}{9}\beta, 7-\frac{22}{9}\beta, \frac{22}{3} \right)}$
2. $\alpha \neq 4 \land \beta \neq -\frac{18}{\alpha-4} \rightarrow Sol(b) \text{ (si } \alpha \neq 4 \land \beta \neq -\frac{18}{\alpha-4}) = {(\frac{-144 +22\beta}{18+ \beta(\alpha- 4)}, \frac{126 -\beta(8 + 9\alpha)}{18+ \beta(\alpha- 4)}, \frac{12(4\alpha-5)}{18+ \beta(\alpha- 4)})}$
3. $\beta = -\frac{18}{\alpha-4} \land \alpha = \frac{5}{4} \rightarrow \text{Compatible Indeterminado}$
4. $\beta = -\frac{18}{\alpha-4} \land \alpha \neq \frac{5}{4} \rightarrow \text{Incompatible}$

## Ejercicio 8
a)Probar que si $(\alpha_{1},\alpha_{2},\dots,\alpha_{n})$ es solución entonces $(c\alpha_{1}, c\alpha_{2},\dots, c\alpha_{n})$ también es solución $\forall c \in \mathbb{R}$.

Sea A un sistema lineal homogéneo, entonces todos sus términos independientes son nulos.
Esto aplica para cualquier forma de la matriz de dicho sistema, incluso sea escalerizada, o escalerizada reducida.
De esta forma, la matriz sigue la forma
$$
\left(
\begin{array}{cccc|c}
a_{1,1} & a_{1,2} & \dots & a_{1,n} & 0 \\
a_{2,1} & a_{2,2} & \dots & a_{2,n} & 0 \\
\dots \\
a_{m,1} & a_{m,2} & \dots & a_{m,n} & 0 \\
\end{array}
\right)
\begin{align}

\end{align}
$$
o simplemente
$$
\left(
\begin{array}{cccc}
a_{1,1} & a_{1,2} & \dots & a_{1,n} \\
a_{2,1} & a_{2,2} & \dots & a_{2,n} \\
\dots \\
a_{m,1} & a_{m,2} & \dots & a_{m,n} \\
\end{array}
\right)
\begin{align}

\end{align}
$$
Por esta misma razón, sabemos que el sistema es compatible, pues sabemos que tiene al menos una solución trivial: $(0,0,\dots,0)$.
En este caso, si tomamos un elemento $c \in \mathbb{R}$, sin importar el valor de c, el producto con la solución trivial también es solución, aunque no tiene mucho sentido destacarlo, puesto que se trata de exactamente la misma solución (cualquier elemento multiplicado por 0 es 0).

Lo interesante aquí es demostrar que sucede en el caso de las soluciones no triviales:

Supongamos que A tiene soluciones no triviales, entonces:
- Al menos una incógnita de A es parámetro, que pueden tomar cualquier valor de $\mathbb{R}$ y el resto de incógnitas se expresan en función de dichos parámetros.
- La solución del sistema se expresa como un vector de n dimensiones, el cual depende de p parámetros.

De esta manera, cada uno de las dimensiones de dicho vector (incógnitas) puede incluir las siguientes partes:
- Parámetros y/o múltiplos de los mismos (opcional).
- Término independiente (opcional, únicamente si también hay parámetros).
Esto implica que multiplicar una solución del sistema por cualquier real será equivalente a simplemente multiplicar los parámetros correspondientes por dicho valor, y utilizar su resultado para calcular otra solución del sistema. De esta forma, si $(\alpha_{1},\alpha_{2},\dots,\alpha_{n})$ es solución entonces $(c\alpha_{1}, c\alpha_{2},\dots, c\alpha_{n})$ también es solución $\forall c \in \mathbb{R}$.

A continuación, una demostración matemática:
A es un sistema homogéneo con solución no trivial, entonces cada componente de la solución puede ser:
- 0.
- Parámetros y/o múltiplos de los mismos + un posible termino independiente.
$(\alpha_{1},\alpha_{2},\dots,\alpha_{n})$ es solución de A, entonces cada $\alpha_{i}, i \in [1..n]$ pertenece a uno de los grupos anteriores.
$\forall \alpha_{i}, i \in [1..n], \alpha_{i} = a \times b, a,b \in \mathbb{R}$
Para los componentes de la solución que dependan de un parámetro real, el componente puede tomar como valor cualquier número real, puesto que la suma, resta, producto y cociente son cerradas para $\mathbb{R}$.
Como vemos, podemos expresar a cualquier numero real, como el producto de otros dos números reales.
De esta forma:
$\implies (\alpha_{i} \times c) \in \mathbb{R}$
$\implies (\alpha_{1},\alpha_{2},\dots,\alpha_{n}) \text{ es solución de A } \Longleftrightarrow (c\alpha_{1},c\alpha_{2},\dots,c\alpha_{n}) \forall c \in \mathbb{R} \text{ es solución de A }$

Para demostrarlo correctamente, tenemos que hacer lo siguiente:
$$
\begin{align}
&\text{Sea la i-ésima ecuación del sistema:} \\
&a_{i,1}x_{1} + a_{i,2}x_{2} + \dots + a_{i,n}x_{n} = 0 \\ \\

&\text{Si } (\alpha_{1},\alpha_{2},\dots,\alpha_{n}) \text{ es solución, significa que: } \\
&\sum_{j=1}^{n} a_{i,j}\alpha_{j} = 0 \\ \\

&\text{Ahora probamos con el vector } (c\alpha_{1},c\alpha_{2},\dots,c\alpha_{n}): \\
&\sum_{j=1}^{n} a_{i,j} (c\alpha_{j}) = 0 \\ \\

&\text{Por la propiedad distributiva y asociativa del producto en } \mathbb{R} \text{, podemos extraer la constante } c: \\
&c\left( \sum_{j=1}^{n} a_{i,j} \alpha_{j} \right) = 0 \\ \\

&\text{Como sabemos que la suma original es igual a 0 (porque el vector original era solución):} \\
&c \cdot (0) = 0 \\ \\

&\text{Esto demuestra que el nuevo vector también satisface todas las ecuaciones del sistema para cualquier } c \in \mathbb{R}
\end{align}
$$


# Sistemas lineales con restricciones enteras
## Ejercicio 10
$$
{\begin{cases}
4l + 2h + 6g + 8k = 32 \\
3l + 1h + 3g + 6k = 22 \\
5l + 5h + 15g + 10k = 50
\end{cases}}
$$
$$
\left(
\begin{array}{cccc|c}
4 & 2 & 6 & 8 & 32 \\
3 & 1 & 3 & 6 & 22 \\
5 & 5 & 15 & 10 & 50
\end{array}
\right)
\begin{align}

\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
2 & 1 & 3 & 4 & 16 \\
3 & 1 & 3 & 6 & 22 \\
1 & 1 & 3 & 2 & 10
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{F_{1}}{2} \\
&F_{3} \leftarrow \frac{F_{3}}{5}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
2 & 1 & 3 & 4 & 16 \\
0 & -1 & -3 & 0 & -4 \\
0 & 1 & 3 & 0 & 4
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow 2F_{2} - 3F_{1} \\
&F_{3} \leftarrow 2F_{3} - F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
2 & 1 & 3 & 4 & 16 \\
0 & 1 & 3 & 0 & 4 \\
0 & -1 & -3 & 0 & -4
\end{array}
\right)
\begin{align}
&F_{2} \leftrightarrow F_{3} 
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
2 & 1 & 3 & 4 & 16 \\
0 & 1 & 3 & 0 & 4 \\
0 & 0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} + F_{2} 
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
2 & 0 & 0 & 4 & 12 \\
0 & 1 & 3 & 0 & 4 \\
0 & 0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2} 
\end{align}
$$
$$
\left(
\begin{array}{cccc|c}
1 & 0 & 0 & 2 & 6 \\
0 & 1 & 3 & 0 & 4 \\
0 & 0 & 0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{F_{1}}{2} 
\end{align}
$$
$$
{\begin{cases}
l + 2k = 6 \\
h + 3g = 4
\end{cases}}
$$
$$
{\begin{cases}
l = 6 - 2k \\
h = 4 - 3g \\
g = \alpha \\
k = \beta
\end{cases}}
$$
$$
Sol(a) = \left\{  \left( 6-2\beta, 4-3\alpha, \alpha, \beta \right): \alpha, \beta \in \mathbb{Z}^{+}, \alpha \leq 1, \beta \leq 2 \right\}
$$
Como vector:
$$
Sol(a) = \left\{ 
\left( 6,4,0,0 \right)
+ \alpha\left( 0, -3, 1, 0 \right)
+ \beta\left( -2, 0, 0, 1 \right)
: \alpha, \beta \in \mathbb{Z}^{+}, \alpha \leq 1, \beta \leq 2  \right\}
$$
De esta forma, tenemos las siguientes soluciones para el sistema planteado:
$$
\begin{align}
&\text{1. } (6-2 \times 1, 4-3 \times 1, 1, 1) = (6-2, 4-3, 1, 1) = (4, 1, 1, 1) \qquad (\alpha = 1, \beta = 1) \\
&\text{1. } (6-2 \times 2, 4-3 \times 1, 1, 2) = (6-4, 4-3, 1, 2) = (2, 1, 1, 2)
\qquad (\alpha = 1, \beta = 2) \end{align}
$$
En conclusión, necesitamos repartir las piezas de sushi entre
1. 4 tablas Lagrange, 1 tabla Hausdorff, 1 tabla Gauss y 1 tabla Kolmogorov.
2. 2 tablas Lagrange, 1 tabla Hausdorff, 1 tabla Gauss y 2 tablas Kolmogorov.

# Geometría
## Ejercicio 11
Comenzamos con la función $f(x) = a_{1}x + b_{1}$:
$$
{\begin{cases}
-2a_{1} + b_{1} = 4 \\
-a_{1} + b_{1} = 3 \\
a_{1} + b_{1} = 1
\end{cases}}
$$
$$
\left(
\begin{array}{cc|c}
-2 & 1 & 4 \\
-1 & 1 & 3 \\
1 & 1 & 1
\end{array}
\right)
\begin{align}

\end{align}
$$
$$
\left(
\begin{array}{cc|c}
-2 & 1 & 4 \\
0 & 1 & 2 \\
0 & 3 & 6
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow 2F_{2} - F_{1} \\
&F_{3} \leftarrow 2F_{3} + F_{1}
\end{align}
$$
$$
\left(
\begin{array}{cc|c}
-2 & 0 & 2 \\
0 & 1 & 2 \\
0 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2} \\
&F_{3} \leftarrow F_{3} - 3F_{2}
\end{align}
$$
$$
\left(
\begin{array}{cc|c}
1 & 0 & -1 \\
0 & 1 & 2
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow -2F_{1}
\end{align}
$$
De esta forma, en la función $f(x) = a_{1}x + b_{1}$ determinamos que $a_{1}=-1$ y $b_{1} = 2$. En conclusión, $f(x) = -x + 2$.

Continuamos con la función $g(x) = a_{2}x^{3} + b_{2}x^{2} + c_{2}x$:
$$
{\begin{cases}
(-2)^{3}a_{2} + (-2)^{2}b_{2} + -2c_{2} = 4 \\
(-1)^{3}a_{2} + (-1)^{2}b_{2} + -c_{2} = 3 \\
1^{3}a_{2} + 1^{2}b_{2} + c_{2} = 1
\end{cases}}
$$
$$
{\begin{cases}
-8a_{2} + 4b_{2} + -2c_{2} = 4 \\
-a_{2} + b_{2} + -c_{2} = 3 \\
a_{2} + b_{2} + c_{2} = 1
\end{cases}}
$$
$$
\left(
\begin{array}{ccc|c}
-8 & 4 & -2 & 4 \\
-1 & 1 & -1 & 3 \\
1 & 1 & 1 & 1
\end{array}
\right)
\begin{align}

\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
-8 & 4 & -2 & 4 \\
0 & 2 & 0 & 4 \\
0 & 12 & 6 & 12
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} + F_{3} \\
&F_{3} \leftarrow 8F_{3} + F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
-8 & 4 & -2 & 4 \\
0 & 2 & 0 & 4 \\
0 & 0 & 6 & -12
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - 6F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
-8 & 4 & -2 & 4 \\
0 & 1 & 0 & 2 \\
0 & 0 & 1 & -2
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow \frac{F_{3}}{2} \\
&F_{3} \leftarrow \frac{F_{3}}{6}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
-8 & 0 & -2 & -4 \\
0 & 1 & 0 & 2 \\
0 & 0 & 1 & -2
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - 4F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
-8 & 0 & 0 & -8 \\
0 & 1 & 0 & 2 \\
0 & 0 & 1 & -2
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} + 2F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & 1 \\
0 & 1 & 0 & 2 \\
0 & 0 & 1 & -2
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow \frac{F_{1}}{-8}
\end{align}
$$
De esta forma, en la función $g(x) = a_{2}x^{3} + b_{2}x^{2} + c_{2}x$ determinamos que $a_{2}=1$, $b_{2} = 2$ y $c_{2} = -2$. En conclusión, $g(x) = x^{3} + 2x^{2} - 2x$.