# 2.1 Axiomas de cuerpo ordenado
## Ejercicio 2.1.1
![[Semestre 1/Calculo Diferencial e Integral en una Variable/Práctico/Práctico 2 - Número real/Imágenes/Ejercicio 2.1.1.png]]
a)
El orden de los números es el siguiente:
$$
0, \space \frac{1}{p}, \space 1, \space \sqrt{ p }, \space p, \space p^{2}
$$
b)
El orden de los números es el siguiente:
$$
0, \space p^{2}, \space p, \space \sqrt{ p }, \space 1, \space \frac{1}{p}
$$

## Ejercicio 2.1.2
![[Semestre 1/Calculo Diferencial e Integral en una Variable/Práctico/Práctico 2 - Número real/Imágenes/Ejercicio 2.1.2.png]]
a)
$$
\begin{align}
&\text{Sea } b < a \text{ para el intervalo } [a,b] \\
&\text{Sea } x\in [a,b] \\
&\text{Como } x \in [a,b] \implies a \leq x \leq b \implies a\leq b \\
&\text{Sin embargo, } b < a \text{, por lo que se contradice la condición } a \leq b \\
&\text{Por esta razón, no existe un } x \text{ que satisfaga la condición establecida, lo que implica que } [a,b]=\emptyset \\ \\

&\text{Si existiera } x \in [a,b] \implies a\leq x \land x \leq b \\
&\text{Por transitividad, } a \leq b \\
&\text{Esto contradice la hipótesis } b < a \\
&\text{Al suponer que existe un } x \text{ llegamos a una contradicción, entonces concluimos que no existe tal } x \text{, por lo tanto } [a,b] = \emptyset \\
\end{align}
$$
b)
$$
\begin{align}
&\text{Sean dos intervalos cerrados } A=[a,b] (a \leq b) \text{ y } B=[c,d] (c \leq d)\text{, tales que } x\in A, y \in B \implies ínf(A) \leq x \leq sup(A) \leq ínf(B) \leq y \leq sup(B). \\
&\text{Existen dos posibilidades:} \\
&\text{1. Los intervalos no tienen elementos en común } (sup(A) < ínf(B) \implies A \cap B = \emptyset) \text{. En este caso la intersección es un intervalo cerrado, ya que anteriormente demostramos que el conjunto vacío es un intervalo cerrado.} \\
&\text{2. Los intervalos tienen elementos en común } (b \geq c \implies A \cap B \neq \emptyset) \text{. Vamos a desarrollar este caso:} \\ \\

&\text{En este caso, sucede que el elemento b (supremo y máximo de A), es mayor o igual a c (ínfimo y mínimo de B). Expresado matemáticamente: } sup(A) \geq sup(B) \\
&\text{Como vemos, los conjuntos A y B se superponen en una sección delimitada por } sup(A) \text{ y } ínf(B). \\
&\text{Siguiendo el razonamiento, la intersección de A y B está dada por esta superposición, de forma que: } A \cap B = [sup(A), ínf(B)] \\ \\

&\text{En conclusión, partiendo de dos intervalos cerrados cualesquiera, la intersección de los mismos siempre será otro intervalo cerrado.}
\end{align}
$$
La resolución anterior no es genérica, puesto que solo funciona para dos intervalos, estando uno después del otro. A continuación, una demostración general:
$$
\begin{align}
&\text{Sean } A=[a,b] \text{ y } B=[c,d] \\
&\text{Por definición de intersección: } x \in A \cap B \Longleftrightarrow x \in A \land x \in B \\
&\text{Entonces, } x \in A \cap B \Longleftrightarrow a \leq x \leq b \land c \leq x \leq d \\ \\

&\text{Reagrupamos en base a los conceptos de máximo y mínimo: } \\
&(a \leq x \land c \leq x) \implies máx(a,c) \leq x \\
&(x \leq b \land x \leq d) \implies x \leq mín(b,d) \\ \\

&\text{De esta forma, } x \in A \cap B \Longleftrightarrow máx(a,c) \leq x \leq mín(b,d) \\
&\text{La desigualdad anterior define el conjunto cerrado } [máx(a,c), mín(b,d)] \text{, que por definición es un intervalo cerrado, y si el máximo resula mayor al mínimo, es un conjunto vacío, el cual también es cerrado}
\end{align}
$$
## Ejercicio 2.1.3
![[Semestre 1/Calculo Diferencial e Integral en una Variable/Práctico/Práctico 2 - Número real/Imágenes/Ejercicio 2.1.3.png]]
a)
$$
\begin{align}
&x^{2}-2x>3 \\
&x^{2}-2x-3=0 \\
&a=1,b=-2,c=-3 \\ \\
&\text{Aplicamos Bhaskara} \\
&x=\frac{2\pm \sqrt{ (-2)^{2}-4\times1\times(-3) }}{2\times_{1}} \\
&=\frac{2\pm \sqrt{ 4+12 }}{2} \\
&=\frac{2\pm \sqrt{ 16 }}{2} \\
&=\frac{2\pm 4}{2} \\
&\implies \\
&x_{1}=\frac{2 + 4}{2}=\frac{6}{2}=3 \\
&x_{2}=\frac{2 - 4}{2}=\frac{-2}{2}=-1
\end{align}
$$
Como 3 y -1 son raíces de $x^{2}-2x-3$, entonces podemos determinar que:
$$
\begin{align}
&x^{2}-2x-3>0, \forall x \in \mathbb{R}, x < -1 \oplus x > 3
\end{align}
$$
d)
$$
\begin{align}
&\frac{2-x}{1+x} \leq \frac{1+x}{2-x} \\
&\frac{2-x}{1+x} - \frac{1+x}{2-x} \leq 0 \\
&\frac{2-x}{1+x} - \frac{1+x}{2-x} \leq 0 \\ \\
&\text{Importante: } x\neq-1 \land x \neq 2 \\ \\
&\frac{(2-x)^{2} - (1+x)^{2}}{(1+x)(2-x)} \leq 0 \\
&\frac{4 -2x -2x + x^{2} - (1+x+x+x^{2})}{(1+x)(2-x)} \leq 0 \\
&\frac{4 -4x + \not x^{2} - 1 -x -x - \not x^{2})}{(1+x)(2-x)} \leq 0 \\
&\frac{3 -6x}{(1+x)(2-x)} \leq 0
\end{align}
$$
No desarrollamos el divisor, puesto que nos sirve tenerlo factorizado para estudiar su signo:
![[Semestre 1/Calculo Diferencial e Integral en una Variable/Práctico/Práctico 2 - Número real/Imágenes/Resolución de ejercicio 2.1.3d.png]]
$$
Sol(d): (- \infty, -1) \cup \left[ \frac{1}{2}, 2 \right)
$$

g)
$$
\begin{align}
&\sqrt{ x+4 } < x - 1 \\ \\

&\text{Necesariamente } x+4 \geq 0 \implies x \geq -4 \\ \\

&x+4 < (x - 1)^{2} \\
&x+4 - (x-1)^{2} < 0 \\
&x+4 - (x^{2} - 2x + 1) < 0 \\
&x+4 - x^{2} + 2x - 1 < 0 \\
&- x^{2} + 3x + 3 < 0 \\ \\

&a=-1, b=3, c=3 \\
&x=\frac{-3 \pm \sqrt{ 3^{2} - 4 \times (-1) \times 3 }}{2 \times (-1)} \\
&x=\frac{-3 \pm \sqrt{ 9 + 12 }}{-2} \\
&x=\frac{-3 \pm \sqrt{ 21 }}{-2} \\
&\text{Esto nos deja dos raíces:} \\ \\

&x_{1}=\frac{-3 + \sqrt{ 21 }}{-2} = \frac{3 - \sqrt{ 21 }}{2} \\
&x_{2}=\frac{-3 - \sqrt{ 21 }}{-2} = \frac{3 + \sqrt{ 21 }}{2} \\ \\

&\implies - x^{2} + 3x + 3 < 0, \forall x < \frac{3 - \sqrt{ 21 }}{2} \oplus \forall \\
&x > \frac{3 + \sqrt{ 21 }}{2}, \text{ puesto que el coeficiente principal es negativo } (-x^{2}) \\
&\text{Sin embargo, como habíamos establecido anteriormente, } x \geq -4 \implies x > \frac{3 + \sqrt{ 21 }}{2} \\
&Sol(g)= \left(\frac{3 + \sqrt{ 21 }}{2}, + \infty \right)
\end{align}
$$

i)
$$
\begin{align}
&|2x-5| < |3x+4| \\
&2x-5=0 \implies x = \frac{5}{2} \Longleftrightarrow \text{Signo - si } x < \frac{5}{2} \text{, Signo + si } x > \frac{5}{2} \\
&3x+4=0 \implies x=-\frac{4}{3} \Longleftrightarrow \text{Signo - si } x < -\frac{4}{3} \text{, Signo + si } x > -\frac{4}{3} \\ \\

&\text{Sin embargo, como valor absoluto se aplica a ambas funciones, mientras x sea diferente a la raíz, la imagen será positiva siempre} \\

&\text{La desigualdad anterior se puede resolver siguiendo la siguiente lógica: } \\ \\
&|2x-5| < |3x+4| \implies (2x-5)^{2} < (3x+4)^{2} \\
&=4x^{2}-10x-10x+25 \leq 9x^{2} + 12x + 12x + 16 \\
&=4x^{2}-20x+25 \leq 9x^{2} + 24x + 16 \\
&=4x^{2}-20x+25 - 9x^{2} - 24x - 16 \leq 0 \\
&=-5x^{2}-44x+9 \leq 0 \\
&a=-5, b=-44, c=9 \\
 \\
&x=\frac{44\pm \sqrt{ (-44)^{2} - 4 \times (-5) \times 9 }}{2 \times (-5)} \\
&x=\frac{44\pm \sqrt{ 1936 + 180 }}{-10} \\
&x=\frac{44\pm \sqrt{ 2116 }}{-10} \\
&x=\frac{44\pm 46}{-10} \\
&\text{Esto nos lleva a dos raíces:} \\
&x_{1}=\frac{44 + 46}{-10} = \frac{90}{-10} = -9 \\
&x_{2}=\frac{44 - 46}{-10} = \frac{-2}{-10} = \frac{1}{5} \\
 \\
&\text{Como el coeficiente de } x^{2} \text{ es negativo, la gráfica está "hacia abajo". De esta forma, las imágenes serán negativas para valores menores que } -9 \text{ y mayores que } \frac{1}{5} \\
&Sol(i)=(- \infty, -9) \cup \left( \frac{1}{5}, + \infty \right)
\end{align}
$$

l)
$$
\begin{align}
&\sqrt{ x + n }-\sqrt{ x } > 1 \text{ con } n \in \mathbb{N} \\ \\

&x \geq 0 \text{ ya que en caso contrario } \sqrt{ x } \text{ no se puede resolver para } x \in \mathbb{R} \\ \\

&=\sqrt{ x + n } > 1 + \sqrt{ x } \\
&=(\sqrt{ x + n })^{2} > (1 + \sqrt{ x })^{2} \\
&=x + n > 1 + \sqrt{ x } + \sqrt{ x } + (\sqrt{ x })^{2} \\
&=\not x + n > 1 + 2\sqrt{ x } + \not x \\
&=n > 1 + 2\sqrt{ x } \\
&=n - 1 > 2\sqrt{ x } \\
&=\frac{n - 1}{2} > \sqrt{ x } \\
&=\left( \frac{n - 1}{2} \right)^{2} > x \\ \\

&x < \left( \frac{n - 1}{2} \right)^{2} \\ \\

&x \geq 0 \land x < \left( \frac{n - 1}{2} \right)^{2} \implies 0 \leq x < \left( \frac{n - 1}{2} \right)^{2} \\
&Sol(l)= \left[ 0, \left( \frac{n - 1}{2} \right)^{2} \right)
\end{align}
$$

## Ejercicio 2.1.4
$$
\begin{align}
&\text{Sean a, b dos números reales tales que } 0 < a < b \text{, demostrar que } a<H<G<A<b \\
&\text{Sabemos que } a<b \text{. Vamos a proseguir demostrando el orden del resto de valores.} \\ \\

&\text{Comenzamos por A: Demostrar que } a < A < b \\
&a < A \implies a < \frac{a+b}{2} \\
&\implies a = \frac{a + a}{2} < \frac{a+b}{2} \Longleftrightarrow a < b \\
&A < b \implies \frac{a+b}{2} < b \\
&\implies \frac{a+b}{2} < b = \frac{b+b}{2} \Longleftrightarrow a < b \\
&\text{Demostramos correctamente que } a < A < b \text{. Proseguimos con G} \\ \\

&\text{Demostrar que } a < G < A \\
&a < G \implies a < \sqrt{ ab } \\
&\implies a^{2} = aa < ab \Longleftrightarrow a < b \\
&G < A \implies \sqrt{ ab } < \frac{a+b}{2} \\
&\implies ab < \left( \frac{a+b}{2} \right)^{2} = \frac{(a+b)(a+b)}{4} = \frac{a^{2}+2ab+b^{2}}{4}  \\
&\implies 4ab < 4\frac{a^{2}+2ab+b^{2}}{4} = a^{2}+2ab+b^{2} \\
&\implies 2ab < a^{2}+b^{2} \\
&\implies 0 < a^{2}+b^{2} - 2ab = (a-b)^{2} \Longleftrightarrow a \neq b \\
&\text{Demostramos correctamente que } a < G < A \text{. Proseguimos con H} \\ \\

&\text{Demostrar que } a < H < G \\
&a < H \implies a < \frac{2}{\frac{1}{a}+\frac{1}{b}} = \frac{2}{\frac{b+a}{ab}} = \frac{2ab}{b+a} \\
&\implies a(b+a) = ab+a^{2} = ab+aa < 2ab = ab + ab \\
&\implies aa < ab \Longleftrightarrow a < b \\
&H < G \implies \frac{2}{\frac{1}{a}+\frac{1}{b}} = \frac{2}{\frac{b+a}{ab}} = \frac{2ab}{b+a} < \sqrt{ ab } \\
&\implies \left( \frac{2ab}{b+a} \right)^{2} = \frac{(2ab)^{2}}{(b+a)^{2}} = \frac{4a^{2}b^{2}}{b^{2}+2ab+a^{2}} < ab \\
&\implies 4a^{2}b^{2} < ab(b^{2}+2ab+a^{2}) = ab^{3}+2a^{2}b^{2}+a^{3}b \\
&\implies 2a^{2}b^{2} < ab^{3}+a^{3}b = ab(b^{2} + a^{2}) \\
&\implies \frac{2a^{2}b^{2}}{ab} = 2ab < b^{2} + a^{2} \\
&\implies 0 < b^{2} + a^{2} - 2ab = (b-a)^{2} \Longleftrightarrow a \neq b \\ \\

&\text{En conclusión, logramos demostrar que, con las especificaciones dadas, se cumple que } a < H < G < A < b
\end{align}
$$

## Ejercicio 2.1.5
![[Semestre 1/Calculo Diferencial e Integral en una Variable/Práctico/Práctico 2 - Número real/Imágenes/Resolución de ejercicio 2.1.5.png]]

# 2.2 Funciones reales
## Ejercicio 2.2.1
![[Semestre 1/Calculo Diferencial e Integral en una Variable/Práctico/Práctico 2 - Número real/Imágenes/Ejercicio 2.2.1.png]]
![[Semestre 1/Calculo Diferencial e Integral en una Variable/Práctico/Práctico 2 - Número real/Imágenes/Resolución de ejercicio 2.2.1.png]]

## Ejercicio 2.2.2
$$
\begin{align}
&f(x)=|x| \\
&g(x)=signo(x) \\ \\

&a. f \circ f = f \\
&f \circ f = f(f(x)) = f(|x|) = ||x|| = |x| \\ \\

&b. g \circ g = g \\
&g \circ g = g(g(x)) = g(signo(x)) \\ \\

&signo(x)\begin{cases}
-1 \text{ si } x < 0 \\
0 \text{ si } x = 0 \\
1 \text{ si } x > 0 \\
\end{cases} \\
&\implies g(signo(x)) = signo(x) \\ \\

&c. g \circ f = f \circ g \\
&g \circ f = g(f(x)) = g(|x|) = signo(|x|) \\
&g \circ f\begin{cases}
1 \text{ si } x < 0 \\
0 \text{ si } x = 0 \\
1 \text{ si } x > 0 \\
\end{cases} \\ \\

&f \circ g = f(g(x)) = f(signo(x)) = |signo(x)| \\
&f \circ g\begin{cases}
1 \text{ si } x < 0 \\
0 \text{ si } x = 0 \\
1 \text{ si } x > 0 \\
\end{cases} \\ \\

&\text{De esta manera, demostramos que } g \circ f = f \circ g
\end{align}
$$

## Ejercicio 2.2.3
![[Semestre 1/Calculo Diferencial e Integral en una Variable/Práctico/Práctico 2 - Número real/Imágenes/Ejercicio 2.2.3.png]]
a) $$f|_{[a,b]}, a=-3, b=3 \implies f|_{[-3,3]}=[-0.54, 3.55]$$
IMPORTANTE: Fijarse en los picos de la función. La respuesta es el rango de imágenes en ese intervalo puntual, para eso hay que ver el punto mayor y menor en y en dicho intervalo.
b) $$f|_{[a,b]}, a=-3, b=-2 \implies f|_{[-3,-2]}=[-0.54, -0.31]$$
c) $$f|_{[a,b]}, a=-3, b=0 \implies f|_{[-3,0]}=[-0.54, 2]$$
d) $$f|_{[a,b]}, a=0, b=2 \implies f|_{[0,2]}=[2, 3.55]$$
Mismo caso que en la parte a. El pico máximo de y en el intervalo $[0,2]$ no se corresponde con f(2).

## Ejercicio 2.2.5
a) Es estrictamente monótona creciente, ya que para cualquier valor de x, la imagen es $x-5$, de forma que dados dos elementos $x_{1},x_{2} \in \mathbb{R}, f(x_{1}) = f(x_{2}) \implies x_{1} = x_{2}$ y si $x_{1} < x_{2} \implies f(x_{1}) < f(x_{2})$.

b) Es estrictamente monótona decreciente, ya que para cualquier valor de x, la imagen es $-2x$, de forma que dados dos elementos $x_{1},x_{2} \in \mathbb{R}, f(x_{1}) = f(x_{2}) \implies x_{1} = x_{2}$ y si $x_{1} < x_{2} \implies f(x_{1}) > f(x_{2})$.

c) Es no monótona, ya que para cualquier valor de x, la imagen es $|x|$. De esta forma, podemos dar dos contraejemplos sobre la monotonía de la función:
- No es creciente, pues $-1 < 0$ pero $f(-1) = 1 > f(0) = 0$ (orden "invertido").
- No es decreciente, pues $0 < 1$ pero $f(0) = 0 < f(1) = 1$ (orden "normal").

d) Es no monótona, ya que para cualquier valor de x, la imagen es $x^{2}$. De esta forma, podemos dar dos contraejemplos sobre la monotonía de la función:
- No es creciente, pues $-1 < 0$ pero $f(-1) = 1 > f(0) = 0$ (orden "invertido").
- No es decreciente, pues $0 < 1$ pero $f(0) = 0 < f(1) = 1$ (orden "normal").

e) Es estrictamente monótona creciente, ya que para cualquier valor de x, la imagen es $x^{3}$, de forma que dados dos elementos $x_{1},x_{2} \in \mathbb{R}, f(x_{1}) = f(x_{2}) \implies x_{1} = x_{2}$ y si $x_{1} < x_{2} \implies f(x_{1}) < f(x_{2})$.

## Ejercicio 2.2.8
Fórmula a aplicar: $$
\begin{align}
&|f(x) − f(y)| ≤ K|x − y| \\
&\left| \frac{f(x) − f(y)}{x-y} \right| \leq K
\end{align}
$$
Lo que haremos es:
1. Aplicar la fórmula de la función f como parámetros de la fórmula anterior (x e y), para llegar a el valor de K.
2. Buscar un par x, y que formen parte del dominio (teniendo imagen en el codominio), y calcular sus imágenes.
3. Sustituir dicho par en la fórmula especificada.
a) 
$$
\begin{align}
&\frac{|3x - 3y|}{|x-y|} \leq K \\ \\

&f(0) = 3\times 0 + 7 = 7 \\
&f(1) = 3\times 1 + 7 = 10 \\ \\

&\left| \frac{7-10}{0-1} \right| \leq K \\
&\left| \frac{-3}{-1} \right| \leq K \\
&3 \leq K \\ \\

&\text{Probaremos con otros dos valores, esta vez más distantes} \\
&f(-10) = 3\times -10 + 7 = -23 \\
&f(200) = 3\times 200 + 7 = 607 \\ \\

&\left| \frac{-23-607}{-10-200} \right| \leq K \\
&\left| \frac{-630}{-210} \right| \leq K \\ \\
&\left| \frac{-3}{-1} \right| \leq K \\
&3 \leq K \\ \\

&\text{Llegamos a la desigualdad } 3 \leq K \text{, de tal forma que la funcion es lipschitziana, puesto que } \exists K \in \mathbb{R}, 3 \leq K \text{, pudiendo K ser cualquier valor mayor o igual a 3}
\end{align}
$$
c)
$$
\begin{align}
&\frac{|x^{2} - y^{2}|}{|x-y|} \leq K \\ \\

&f(0) = 0^{2} = 0 \\
&f(2) = 2^{2} = 4 \\ \\

&\left| \frac{0-4}{0-2} \right| \leq K \\
&\left| \frac{-4}{-2} \right| \leq K \\
&2 \leq K \\ \\

&\text{Probaremos con otros dos valores, esta vez más distantes} \\
&f(10) = (10)^{2} = 100 \\
&f(100) = 100^{2} = 10000 \\ \\

&\left| \frac{100-10000}{10-100} \right| \leq K \\
&\left| \frac{-9900}{-90} \right| \leq K \\ \\
&\left| \frac{-110}{-1} \right| \leq K \\
&110 \leq K \\ \\

&\text{Como vemos, obtuvimos desigualdades diferentes a medida que modificabamos los púntos utilizados. Igualmente, como } f(x) = x^{2} \text{, podemos concluir en que la función no es lipschitziana, ya que } \not \exists K \in \mathbb{R}, x, y \in [0, + \infty] \text{ tal que } |f(x) − f(y)| ≤ K|x − y| \text{. Esto sucedem ya que la función es creciente de forma exponencial.}
\end{align}
$$
Una forma mejor de determinarlo es, a partir de la fórmula para determinar si una función es lipschitziana, y una ecuación de función puntual, llegar a una demostración formal o enunciado, el cual establezca si la función es o no lipschitziana. Por ejemplo, para los ejercicios a y b:
$$
\begin{align}
&\text{Ejercicio a:} \\
&\left| \frac{f(x) − f(y)}{x-y} \right| = \left| \frac{3x + 7 − 3y - 7}{x-y} \right| = \left| \frac{3x − 3y}{x-y} \right| = \frac{3|x − y|}{|x-y|} = 3 \\
 \\
&\text{Ejercicio c:} \\
&\left| \frac{f(x) − f(y)}{x-y} \right| = \left| \frac{x^{2} - y^{2}}{x-y} \right| = \left| \frac{(x-y)(x+y)}{x-y} \right| = |x+y| \\
 \\
&\text{Ejercicio b (ejemplo no resuelto):} \\
&\left| \frac{f(x) − f(y)}{x-y} \right| = \left| \frac{\sqrt{ x } - \sqrt{ y }}{x-y} \right| = \left| \frac{(\sqrt{ x } - \sqrt{ y })^{2}}{(x-y)^{2}} \right| = \left| \frac{x -2\sqrt{ xy } + y}{x^{2}-2xy+y^{2}} \right| \\
&\text{En este caso, la función tampoco será lipschitziana, puesto que tiene a infinito cuando x tiende a 0, de modo que no existe un valor K que cumpla con la desigualdad establecida.}
\end{align}
$$

# 2.3 Axioma de completitud

## Ejercicio 2.3.1
![[Resolución de ejercicio 2.3.1.png]]

## Ejercicio 2.3.2
a)
El coseno de un número está entre -1 y 1 (de forma que el conjunto será $\{ -1,0,1 \}$).  Según el circulo trigonométrico, consideramos al coseno como la coordenada x del punto de la circunferencia que intercepta el radio cuando tenemos $\frac{n\pi}{2}$ radianes de apertura.
De esta forma, el coseno siempre será 1 cuando el punto de intersección entre el radio y la circunferencia sea (0, 1), y será -1 cuando dicho punto sea (0, -1). Estos son los valores extremos, que además de ser ínfimo y supremo, también son mínimo y máximo.
$$
\begin{align}
&\cos\left( \frac{n\pi}{2} \right): \\
&\text{Si } n \in \{ 1, 5, 9,\dots \} \implies \cos\left( \frac{n\pi}{2} \right) = 1 \\
&\text{Si } n \in \{ 3, 7, 11,\dots \} \implies \cos\left( \frac{n\pi}{2} \right) = -1 \\
&\text{En otro caso: } -1 < \cos\left( \frac{n\pi}{2} \right) = 0
\end{align}
$$
De esta forma, determinamos que el supremo y máximo (puesto que forma parte del conjunto) es 1, mientas que el ínfimo y mínimo (puesto que forma parte del conjunto) es -1.

c)
Para resolver este conjunto, tomaremos como referencia el círculo trigonométrico.
![[Resolución de ejercicio 2.3.2c.png]]

Podemos determinar que:
$$
\begin{cases}
\cos(\theta) > \sin(\theta) \text{ si } \theta \in \cup_{k \in \mathbb{Z}} \left( \left[ 2k\pi, \frac{1}{4}\pi + 2k\pi \right) \cup (\frac{5}{4}\pi + 2k\pi, 2\pi + 2k\pi] \right) \\
\cos(\theta) = \sin(\theta) \text{ si } \theta \in \left\{ \frac{1}{4}\pi + k\pi, k \in \mathbb{Z} \right\} \\
\cos(\theta) < \sin(\theta) \text{ si } \theta \in \cup_{k \in \mathbb{Z}} \left( \frac{1}{4}\pi + 2k\pi, \frac{5}{4}\pi + 2k\pi \right) \\
\end{cases}
$$
De esta forma, como queremos encontrar la solución para el caso $\cos(\theta) < \sin(0)$, obtendremos una unión de conjuntos, como lo indica la fórmula 3. Considerando además que $\theta \in [0,10]$, el resultado será un conjunto finito.
$$
\begin{align}
&\{ \theta \in [0,10] : cos(\theta) < sin(\theta) \}  \\
&=\left( \frac{1}{4}\pi, \frac{5}{4}\pi \right) \cup \left( \frac{9}{4}\pi, 10 \right] \qquad \text{(Finalizado en 10, ya que } \frac{13}{4}\pi > 10 \text{).}
\end{align}
$$
De esta manera, el ínfimo del conjunto especificado es $\frac{1}{4}\pi$ y el supremo es 10. 10 también es máximo, puesto que forma parte del conjunto, pero $\frac{1}{4}\pi$ no es mínimo, puesto que no forma parte del mismo (ya que para $\frac{1}{4}\pi, \cos(\theta) = \sin(\theta)$).

e)
Para el conjunto definido en este caso, el resultado es el siguiente:
$$
\{ x \in \mathbb{R} : x^{2} \leq 3 \} = [- \sqrt{ 3 }, \sqrt{ 3 }]
$$
De esta forma, el ínfimo del conjunto establecido es $- \sqrt{ 3 }$, mientras que el supremo es $\sqrt{ 3 }$. En este caso, tanto el ínfimo como el supremo se encuentran dentro del conjunto, por lo que también son mínimo y máximo.

g)
$$
\left\{  x \in R : \frac{3x + 1}{x-2} \leq 0  \right\}
$$
Para responder a la pregunta, analizaremos el signo de cada función:
En el caso de $3x+1$, es:
- Negativo, para $x < -\frac{1}{3}$
- Neutro, para $x = -\frac{1}{3}$
- Positivo, para $x > -\frac{1}{3}$

En el caso de $x-2$, es:
- Negativo, para $x < 2$
- Neutro, para $x = 2$
- Positivo, para $x > 2$

Si combinamos ambas funciones, obtenemos que el signo es:
- Positivo, para $x < -\frac{1}{3}$
- Neutro, para $x = -\frac{1}{3}$
- Negativo, para $-\frac{1}{3} < x < 2$
- No existe, para $x = 2$
- Positivo, para $x > 2$

De esta forma, como el caso que nos interesa es $\frac{3x + 1}{x-2} \leq 0$, únicamente nos centraremos en que el signo es negativo para $-\frac{1}{3} < x < 2$:
$$
\left\{  x \in R : \frac{3x + 1}{x-2} \leq 0  \right\} = \left( -\frac{1}{3}, 2 \right)
$$
En este caso particular, tenemos que $-\frac{1}{3}$ es el ínfimo y $2$ es el supremo del conjunto resultado. Sin embargo, como ninguno de los dos forma parte del conjunto (ya que es abierto), no tiene mínimo ni máximo.

i)
$$
[0,1] \setminus \mathbb{Q}
$$
El conjunto resultado contendrá todos los elementos que se encuentran en $[0,1]$ que no se encuentran en los racionales. De esta forma, $[0,1] \setminus \mathbb{Q}$ contiene todos los irracionales comprendidos entre 0 y 1. De esta forma, el mismo será cerrado, de forma que su ínfimo y supremo también serán mínimo y máximo.

## Ejercicio 2.3.3
a)
Sea $A \subset B$ y B es acotado,  demostrar que $ínf(B) \leq ínf(A) \leq sup(A) \leq sup(B)$

Partimos de que A es subconjunto de B.
Como B es acotado $\implies$ A es acotado $\implies$ A tiene cota superior e inferior.
Como A tiene cota superior e inferior, entonces $\exists x,y \in \mathbb{R} \text{ tal que } \forall a \in A, x \leq a \leq y$
Al tener cota superior e inferior, podemos decir que existe un valor de las cotas superiores que es menor que el resto (al que llamaremos supremo), y existe un valor de las cotas inferiores que es mayor que el resto (al que llamaremos ínfimo).

Es así que:
$$
\begin{align}
\exists! ínf(A) \text{ tal que } ínf(A) \leq a, \forall a \in A \\
\exists! sup(A) \text{ tal que } a \leq sup(A), \forall a \in A \\
\end{align}
$$
Volviendo al comienzo, como B es acotado, B también tiene cota superior e inferior, por lo que también podemos definir su ínfimo y supremo:
$$
\begin{align}
\exists! ínf(B) \text{ tal que } ínf(B) \leq b, \forall b \in B \\
\exists! sup(B) \text{ tal que } b \leq sup(B), \forall b \in B \\
\end{align}
$$
Además, como A es un subconjunto de B:
$$
\begin{align}
&\exists b \in B, \forall a \in A \text{ tal que } b \leq a \text{ (existe al menos un elemento en B que es cota inferior de A) } \\
&\exists b \in B, \forall a \in A \text{ tal que } a \leq b \text{ (existe al menos un elemento en B que es cota superior de A) }
\end{align}
$$
Las proposiciones anteriores también incluyen al supremo e ínfimo de A.
Por esta razón, podemos deducir que:
$$
\begin{align}
&\exists b \in B, \forall a \in A \text{ tal que } b \leq a \implies b \leq ínf(A) \\
&\exists b \in B, \forall a \in A \text{ tal que } a \leq b \implies sup(A) \leq b \\
\end{align}
$$
En conclusión, podemos establecer con seguridad que:
$$
ínf(B) \leq ínf(A) \leq sup(A) \leq sup(B)
$$

## Ejercicio 2.3.7
Para demostrar que $xn > y \implies n > \frac{y}{x}$
$x, y \in \mathbb{R}, x > 0 \implies \frac{y}{x} \in \mathbb{R}, \text{ cuyo signo está dado por y (ya que x es siempre positivo)}$
La idea es demostrar que existe al menos un natural que es mayor que $\frac{y}{x}$.

Esto lo podemos demostrar por absurdo, considerando que $\mathbb{N}$ tiene supremo (está acotado superiormente).
De esta forma:
$$
\exists z \in \mathbb{R}, \forall n \in \mathbb{N}, n \leq z \text{ (z es cota superior de } \mathbb{N} \text{)}
$$
Como $\mathbb{N}$ no es vacío, hay un elemento de $\mathbb{N}$ que es mayor o igual al resto (su supremo):
Sea $s := sup(\mathbb{N})$

Aproximamos el supremo a un natural utilizando $\epsilon$:
Tomando
$$
\begin{align}
&\epsilon = 1, \exists n \in \mathbb{N} \\
&s - 1 < n \leq s \\
&\implies s < n + 1 \in \mathbb{N}
\end{align}
$$
Como vemos, al operar en la desigualdad, encontramos que existe un valor $n + 1 \in \mathbb{N}$ mayor que el supremo $s := sup(\mathbb{N})$. De esta forma, demostramos que el conjunto de los naturales no tiene supremo, por lo que siempre encontraremos un valor que cumpla que $n > \frac{y}{x} \implies nx > y, \forall x,y \in \mathbb{R}, x > 0$.

## Ejercicio 2.3.8
La opción a es la correcta, puesto que el conjunto $A = \{ \frac{m}{n} : 0 < m < n, m, n \in \mathbb{N} \}$ está acotado superiormente, teniendo supremo, pero no tiene máximo. Esto se debe a que como el elemento está compuesto por todas las fracciones cuyo numerador se encuentre entre entre 0 y n, y n sea mayor que 2 (no puede ser 1, ya que tendría que ser igual a m). De esta forma, ninguna de las fracciones representará a un número mayor o igual que 1, por lo que podemos decir que 1 es cota superior del conjunto, y además es supremo del mismo, puesto que a medida que aumentamos el valor m y n, manteniendo que $m = n-1$, nos vamos a acercando a 1.
Sin embargo, esto no significa que 1 sea máximo de dicho conjunto, puesto que no forma parte del mismo (ninguna de las fracciones formuladas será equivalente a 1, pues el numerados siempre será menor que el denominador, siendo ambos positivos).

# 2.4 Funciones reales y axioma de completitud
## Ejercicio 2.4.1
![[Resolución de ejercicio 2.4.1.png]]

## Ejercicio 2.4.2
Importante: las funciones f(x) y g(x) pueden tener supremo en diferente lugar (para diferente valor de x). De esta forma, la suma individual de dichos supremos será mayor que el supremo de la suma de ambas funciones.

Como sabemos, la suma de las funciones $f(x): \mathbb{R} \to \mathbb{R}$ y $g(x): \mathbb{R} \to \mathbb{R}$ da como resultado una nueva función $(f + g)(x): \mathbb{R} \to \mathbb{R}$, tal que $(f + g)(x) = f(x) + g(x), \forall x \in \mathbb{R}$.
Consideremos el caso en el que el supremo de f(x) y g(x) coinciden (ambas tienen su supremo en el mismo valor de x). En este caso, tomemos $x \in [a,b] \implies (f + g)(x) = f(x) + g(x)$. Como vemos, si f(x) y g(x) tienen su supremo en el mismo x, entonces se cumple que $(f + g)(x) = f(x) + g(x)$.
Sin embargo, esto puede no ser así, de modo que el supremo de f(x) y el supremo de g(x) no coincidan en su valor x. En este caso, la suma de ambos supremos será mayor que el supremo de la suma de las funciones, ya que este último no será el resultado de sumar ambos supremos individuales, siendo menor siempre que no coincidan.

Más formalmente:
Sea $s \in [a,b] \text{ tal que } f(s) = sup\{ f(x): x \in [a,b] \} \text{ y } g(s) = sup\{ g(x): x \in [a,b] \}$
Como $f(x) + g(x) = (f + g)(x), \forall x \in [a,b] \implies f(s) + g(s) = (f + g)(s) = sup\{ (f + g)(x): x \in [a,b] \} \text{ (siendo un caso particular)}$
Sin embargo, puede darse que $s_{1},s_{2} \in [a,b] \text{ tal que } f(s_{1}) = sup\{ f(x): x \in [a,b] \} \text{ y } g(s_{2}) = sup\{ g(x): x \in [a,b] \} \text{, con } s_{1} \neq s_{2}$
En este caso, como ya establecimos antes, $f(x) + g(x) = (f + g)(x), \forall x \in [a,b] \implies f(s_{1}) + g(s_{2}) \neq sup\{ (f + g)(x): x \in [a,b] \} \text{, ya que } s_{1} \neq s_{2}$
De esta forma, $sup\{ (f + g)(x): x \in [a,b] \} < sup\{ f(x): x \in [a,b] \} + sup\{ g(x): x \in [a,b] \}$

En conclusión, en todos los casos se cumple que $sup\{ (f + g)(x): x \in [a,b] \} \leq sup\{ f(x): x \in [a,b] \} + sup\{ g(x): x \in [a,b] \}$

La prueba de que $ínf\{ (f + g)(x): x \in [a,b] \} \geq ínf\{ f(x): x \in [a,b] \} + ínf\{ g(x): x \in [a,b] \}$:

Sea $i \in [a,b] \text{ tal que } f(i) = ínf\{ f(x): x \in [a,b] \} \text{ y } g(i) = ínf\{ g(x): x \in [a,b] \}$
Como $f(x) + g(x) = (f + g)(x), \forall x \in [a,b] \implies f(i) + g(i) = (f + g)(i) = ínf\{ (f + g)(x): x \in [a,b] \} \text{ (siendo un caso particular)}$
Sin embargo, puede darse que $i_{1},i_{2} \in [a,b] \text{ tal que } f(i_{1}) = ínf\{ f(x): x \in [a,b] \} \text{ y } g(i_{2}) = ínf\{ g(x): x \in [a,b] \} \text{, con } i_{1} \neq i_{2}$
En este caso, como ya establecimos antes, $f(x) + g(x) = (f + g)(x), \forall x \in [a,b] \implies f(i_{1}) + g(i_{2}) \neq ínf\{ (f + g)(x): x \in [a,b] \} \text{, ya que } i_{1} \neq i_{2}$
De esta forma, $ínf\{ (f + g)(x): x \in [a,b] \} > ínf\{ f(x): x \in [a,b] \} + ínf\{ g(x): x \in [a,b] \}$

En conclusión, en todos los casos $ínf\{ (f + g)(x): x \in [a,b] \} \geq ínf\{ f(x): x \in [a,b] \} + ínf\{ g(x): x \in [a,b] \}$

CORRECCIÓN MÁS FORMAL:

Sea $x \in [a,b]$ cualquier valor del intervalo. Por definición de supremo, sabemos que:
$$
\begin{align}
&f(x) \leq sup \{ f(x): x \in [a,b] \} \\
&g(x) \leq sup \{ g(x): x \in [a,b] \}
\end{align}
$$
Si sumamos ambas desigualdades (ya que se cumplen para el mismo x):
$$
(f + g)(x) = f(x) + g(x) \leq sup \{ f(x): x \in [a,b] \} + sup \{ g(x): x \in [a,b] \}
$$
La última expresión es una constante. Como la desigualdad se cumple para todo $x \in [a,b]$, significa que el número $sup \{ f(x): x \in [a,b] \} + sup \{ g(x): x \in [a,b] \}$ es una cota superior del conjunto $\{ (f + g)(x) : x \in [a,b] \}$.

Por definición, el supremo de $(f + g)$ es la menor de las cotas superiores. Por lo tanto:
$$
sup \{ (f + g)(x) : x \in \mathbb{R} \} \leq sup \{ f(x): x \in [a,b] \} + sup \{ g(x): x \in [a,b] \}
$$

El razonamiento para el ínfimo es análogo:

Sea $x \in [a,b]$ cualquier valor del intervalo. Por definición de ínfimo, sabemos que:
$$
\begin{align}
&f(x) \geq ínf \{ f(x): x \in [a,b] \} \\
&g(x) \geq ínf \{ g(x): x \in [a,b] \}
\end{align}
$$
Si sumamos ambas desigualdades (ya que se cumplen para el mismo x):
$$
(f + g)(x) = f(x) + g(x) \geq ínf \{ f(x): x \in [a,b] \} + ínf \{ g(x): x \in [a,b] \}
$$
La última expresión es una constante. Como la desigualdad se cumple para todo $x \in [a,b]$, significa que el número $ínf \{ f(x): x \in [a,b] \} + ínf \{ g(x): x \in [a,b] \}$ es una cota inferior del conjunto $\{ (f + g)(x) : x \in [a,b] \}$.

Por definición, el ínfimo de $(f + g)$ es la mayor de las cotas inferiores. Por lo tanto:
$$
ínf \{ (f + g)(x) : x \in \mathbb{R} \} \geq ínf \{ f(x): x \in [a,b] \} + ínf \{ g(x): x \in [a,b] \}
$$

Ejemplos de funciones que cumplen las desigualdades estrictas:
Tomaremos las funciones $f,g : [0, 10] \to \mathbb{R}$
$$
\begin{align} \\
&f(x) = x^{2} \\
&g(x) = -x \\
 \\
&\implies (f + g)(x) = x^{2} - x
\end{align}
$$
De esta forma, tenemos que:
$$
\begin{align}
&\text{Supremos: } \\

&sup \{ f(x) : x \in [0, 10] \} = 100 \text{ (para x = 10)} \\
&sup \{ g(x) : x \in [0, 10] \} = 0 \text{ (para x = 0)} \\
 \\
&\text{Ínfimos: } \\

&ínf \{ f(x) : x \in [0, 10] \} = 0 \text{ (para x = 0)} \\
&ínf \{ g(x) : x \in [0, 10] \} = -10 \text{ (para x = 10)} \\
 \\
&\implies \\
&sup \{ (f + g)(x) : x \in [0, 10] \} = 90 \text{ (para x = 10)} < sup \{ f(x) : x \in [0, 10] \} + sup \{ g(x) : x \in [0, 10] \} \\
&ínf \{ (f + g)(x) : x \in [0, 10] \} = -\frac{1}{4} \text{ (para x = } \frac{1}{2} \text{)} > ínf \{ f(x) : x \in [0, 10] \} + ínf \{ g(x) : x \in [0, 10] \}
\end{align}
$$
Aclaración: el ínfimo de $(f + g)(x)$ se calcula usando la fórmula del vértice:
$$
x_{v} = \frac{-b}{2a} = \frac{-(-1)}{2(1)} = \frac{1}{2}
$$
Con esto, sabemos que valor de x es el vértice de la parábola, de forma que tendrá el menor y.
$$
(f + g)\left( \frac{1}{2} \right) = \left( \frac{1}{2} \right)^{2} - \frac{1}{2} = \frac{1}{4} - \frac{1}{2} = -\frac{1}{4}
$$

Ejemplo de una función que cumple la especificación:
$$
\begin{align}
&f(x)\begin{cases}
x \text{ si } 0 \leq x < 1 \\
0 \text{ si } x = 1 \\
\end{cases} \\ \\

&\mathrm{Im}(f) = [0, 1) \\
&sup(\mathrm{Im}(f)) = 1
\end{align}
$$
En este caso, el supremo es 1, y es superior a todas las demás imágenes (ningún elemento tiene imagen 0, todos tienen imagen menor).

Otro ejemplo:
$$
\begin{align}
&f(x)\begin{cases}
x \text{ si } -1 \leq x < 0 \\
-1 \text{ si } x = 0 \\
-x \text{ si } 0 < x \leq 1 \\
\end{cases} \\ \\

&\mathrm{Im}(f) = [-1, 0) \\
&sup(\mathrm{Im}(f)) = 0
\end{align}
$$

# 2.5 Complementarios
# Ejercicio 2.5.4
Sean A, B ⊂ R acotados y no vacíos, y tal que A \ B es no vacío.

a) Probar que $sup(A \setminus B) \leq sup(A)$.

Referente al $sup(a) \text{ y } sup(A \setminus B)$, pueden darse dos casos:
1. $sup(A) \in B \implies sup(A) \not \in A \setminus B \implies \forall x \in A \setminus B, x < sup(A) \Longleftrightarrow sup(A \setminus B) < sup(A)$
2. $sup(A) \not \in B \implies sup(A) \in A \setminus B \implies \forall x \in A \setminus B, x \leq sup(A) \Longleftrightarrow sup(A \setminus B) = sup(A)$

En conclusión: $sup(A \setminus B) \leq sup(A)$

Una demostración mejor:
Por definición de resta de conjuntos, $A \setminus B = \{ x \in \mathbb{R} : x \in A \land x \not \in B \}$
Esto implica directamente que $A \setminus B \subseteq A$
Como $A \setminus B \subseteq A$ son conjuntos acotados superiores, entonces $sup(A \setminus B) \leq sup(A)$

Sea $x \in A \setminus B \implies x \leq sup(A \setminus B)$.
Como $x \in A \setminus B \implies x \in A \land x \not \in B$.
Si $x \in A \implies x \leq sup(A)$

b) Probar que si $sup(B) < sup(A) \implies sup(A \setminus B) = sup(A)$.

Por definición de resta de conjuntos, $A \setminus B = \{ x \in \mathbb{R} : x \in A \land x \not \in B \}$
Si $sup(B) < sup(A) \implies \forall x \in B, x < sup(A) \implies sup(A) \not \in B \Longleftrightarrow sup(A) \in A \setminus B$
Además $\forall x \in A \setminus B, x \in A \Longleftrightarrow A \setminus B \subseteq A$
En conclusión, como $sup(A) \in A \setminus B \land A \setminus B \subseteq A \Longleftrightarrow sup(A \setminus B) = sup(A)$


c) De un ejemplo donde $sup(B) = sup(A) \land sup(A \setminus B) < sup(A)$.
$$
\begin{align}
&A = [1, 10] \\
&B = [5, 10] \\
 \\
& A \setminus B = [1, 5) \\
 \\
&\implies sup(A \setminus B) = 5 < sup(A) = 10
\end{align}
$$

d) De un ejemplo donde $sup(B) = sup(A) \land sup(A \setminus B) = sup(A)$.
$$
\begin{align}
&A = [1, 10] \\
&B = [5, 10) \\
 \\
& A \setminus B = [1, 5) \cup \{ 10 \} \\
 \\
&\implies sup(A \setminus B) = 10 = sup(A) = 10
\end{align}
$$
