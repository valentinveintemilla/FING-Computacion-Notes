# Extremos absolutos
La idea era demostrar que si tengo una función continua en un intervalo cerrado, entonces la misma tiene al menos un máximo y mínimo.

Comenzamos por una proposición:

> [!Proposición]
> Si $f : [a, b] \to \mathbb{R}$ es continua definida en un intervalo cerrado $[a, b]$ (con $a < b$) entonces está acotada.

Además, repasaremos el teorema en si:

## Teorema de Weierstrass

> [!Teorema de Weierstrass]
> Si $f : [a, b] \to \mathbb{R}$ es una función continua definida en un intervalo cerrado $[a, b]$, entonces tiene mínimo y máximo.
> Es decir: existen $x_{0}, x_{1} \in [a, b]$ tales que
> $$
> f(x_{0}) \leq f(x) \leq f(x_{1}) \qquad \text{para todo } x \in [a, b]
> $$

También repasaremos la demostración:
(Una vez demostrado el teorema, podemos olvidar la proposición.)
### Demostración

Por la proposición anterior, existe $M := sup(f, [a, b])$ (además de supremo, es máximo).

Se define $g : [a, b] \to \mathbb{R}$ por
$$
g(x) = sup(f, [a, x])
$$
![[1 - Representación de g.png]]

Por la definición, coincide con $f$ en las partes en las que $f$ es creciente. Además, llega un momento en el que su valor no cambia (cuando alcanza el máximo absoluto). Cuando $f$ decrece se queda constante, y cuando $f$ supera al "último máximo", $g$ crece. Además, sabemos que la definición tiene sentido, ya que como la función está acotada en $[a, b]$ también está acotada en cualquier subintervalo $[a, x]$.

- $g$ es monótona creciente
- $g(a) = f(a)$
- $g(b) = M$

Sea $S := \{ x \in [a, b] : g(x) = M \}$
Tenemos que $b \in S$.

Sea $x_{1} := ínf(S)$

(Si bien no sabemos el valor de $x_{1}$, demostraremos que antes de $x_{1}, g(x) < M$, y después de $x_{1}, g(x) = M$.)

- Para todo $x < x_{1}, x \not \in S$, entonces $g(x) < M$.
- Para todo $x > x_{1}$, existe $x' \in S$ tal que $x > x' > x_{1} \qquad (= ínf(S))$.

Sabemos que $g(x') = M$, ya que está en $S$, y como la función es monótona:
$$
g(x) \geq g(x') = M
$$
y como $g(x) \leq M$ se cumple en todos los casos (por definición), entonces
$$
g(x) = M, x \in S
$$
De esta manera, demostramos que para todos los puntos anteriores a $x_{1}, g(x) < M \implies x \not \in S$, y para todos los puntos posteriores a $x_{1}, g(x) = M \implies x \in S$. También se puede demostrar que $x_{1} \in S$, pero no es relevante y no lo utilizaremos en la demostración.

La conclusión importante de todo esto, es que $S$ es un intervalo de la forma
$$
S = (x_{1}, b] \qquad \text{o} \qquad S = [x_{1}, b]
$$

Ahora, analizaremos el caso general: $x_{1} \neq b$, por lo que $S$ es un intervalo con infinitos puntos.
También podríamos determinar casos particulares, como $x_{1} = b$, por lo que $S = [b, b] = \{ b \}$, aunque no lo haremos en este caso.
![[2 - Representación de demostración.png]]

Queremos mostrar que $f(x_{1}) = M$.
Por el absurdo, se supone que $f(x_{1}) < M$.

(Analizaremos los alrededores del punto $x_{1}$, y considerando que $f(x_{1}) < M$, van a haber valores mayores que $x_{1}$ cuya imagen también será menor que $M$. Sin embargo, si analizamos esto con la función $g$, necesariamente habrán valores posteriores a $x_{1}$ para los cuales $g(x) < M$, y ahí es donde está la contradicción, ya que antes determinamos que para todo $x > x_{1}, g(x) = M \implies x \in S$. Para todo esto, aprovecharemos la continuidad en $x_{1}$).

Sea $\epsilon := \frac{M - f(x_{1})}{2} > 0$.
Como $f$ es continua en $x_{1}$, existe $\delta > 0$ tal que $|f(x) - f(x_{1})| < \epsilon$ para todo $x \in E(x_{1}, \delta) \cap [a, b]$

De esta forma, sabemos que la función, nunca supera a $f(x_{1}) + \epsilon = M - \epsilon$. Por eso establecimos dicho $\epsilon$: tenemos un límite que no se supera, y es menor que $M$.
![[3 - Representación de demostración por el absurdo.png]]

Para todo $x \in E(x_{1}, \delta) \cap [a, b]$,
$$
\begin{align}
f(x) < f(x_{1}) + \epsilon &= f(x_{1}) + \frac{M - f(x_{1})}{2} = \frac{M + f(x_{1})}{2} \\
&= M - \epsilon
\end{align}
$$

Se definen
$$
\begin{align}
&x_{1}^{-} = máx \left( x_{1} - \frac{\delta}{2}, a \right) \\
&x_{1}^{+} = mín \left( x_{1} + \frac{\delta}{2}, b \right)
\end{align}
$$

(Nos aseguramos de que $x_{1}^{-}$ y $x_{2}^{+}$ no queden fuera de $[a, b]$.)
(De esta forma, $x_{1}^{-}$ y $x_{1}^{+}$ están en el entorno que nos interesa: $E(x_{1}, \delta) \cap [a, b]$.)

Se observa lo siguiente:
$$
\begin{align}
g(x_{1}^{+}) &= sup(f, [a, x_{1}^{+}]) \\
&= sup(f, [a, x_{1}^{-}] \cup [x_{1}^{-}, x_{1}^{+}]) \\
&= máx(\underbrace{ sup(f, [a, x_{1}^{-}]) }_{ = g(x_{1}^{-}) }, sup(f, [x_{1}^{-}, x_{1}^{+}])) \\
&= máx(g(x_{1}^{-}), \underbrace{ sup(f, [x_{1}^{-}, x_{1}^{+}]) }_{ \leq M - \epsilon }) \\
&\leq máx(g(x_{1}^{-}), M - \epsilon)
\end{align}
$$

Ahora, la idea es demostrar que $g(x_{1}^{+}) < M$, obteniendo una contradicción, pues anteriormente determinamos que $\forall x \in [a, b], x > x_{1}, g(x) = M$.

De esta forma, tenemos que distinguir tres casos posibles considerando la posición de $x_{1}$ en el intervalo $[a, b]$:

1. $a = x_{1} < b$
(El máximo absoluto, $M$, sería alcanzado al comienzo)

Tenemos que: $a = x_{1}^{-} = x_{1} < x_{1}^{+} \leq b$
$$
g(x_{1}^{+}) = sup(f, [a, x_{1}^{+}]) = sup(f, [x_{1}^{-}, x_{1}^{+}]) \leq M - \epsilon
$$
Por otro lado:
$$
x_{1}^{+} > x_{1} \implies g(x_{1}^{+}) = M
$$
Es así que:
$$
\left.
g(x_{1}^{+}) \leq M - \epsilon \text{ y } g(x_{1}^{+}) = M \space
\right\}
\text{ Contradicción}
$$

2. $a < x_{1} = b$
Tenemos que: $a \leq x_{1}^{-} < x_{1} = x_{1}^{+} = b$
$$
g(x_{1}^{+}) \leq máx (\underbrace{ g(x_{1}^{-} }_{ < M }), M - \epsilon) < M
$$
Por otro lado:
$$
\begin{align}
g(x_{1}^{+}) &= g(b) \\
&= M
\end{align}
$$
Nuevamente:
$$
\left.
g(x_{1}^{+}) < M - \epsilon \text{ y } g(x_{1}^{+}) = M \space
\right\}
\text{ Contradicción}
$$

3. $a < x_{1} < b$
Tenemos que: $a \leq x_{1}^{-} < x_{1} < x_{1}^{+} \leq b$
$$
g(x_{1}^{+}) \leq máx (g(x_{1}^{-}), M - \epsilon) < M
$$
Por otro lado:
$$
x_{1}^{+} > x_{1} \implies g(x_{1}^{+}) = M
$$
Nuevamente:
$$
\left.
g(x_{1}^{+}) < M - \epsilon \text{ y } g(x_{1}^{+}) = M \space
\right\}
\text{ Contradicción}
$$

De esta manera, logramos contradecir los tres casos posibles.

Todo este razonamiento fue realizado en base a una idea geométrica absurda, y logramos demostrar su absurdez mediante el uso de propiedades matemáticas. Esta demostración no es trivial, aunque es importante entender de donde surge y cual fue la lógica para desarrollarla.

Para demostrar la existencia de mínimo, podemos tomar la función $-f$ y demostrar que la misma tiene máximo. De esta manera, demostramos indirectamente que $f$ tiene mínimo, concluyendo con la demostración de que:
Si $f : [a, b] \to \mathbb{R}$ es una función continua definida en un intervalo cerrado $[a, b]$, entonces tiene mínimo y máximo.

---
El teorema de Weierstrass tiene una consecuencia, y se expresa en forma de corolario:

> [!Corolario]
> Si $f : [a, b] \to \mathbb{R}$ es una funcion continua definida en un intervalo cerrado $[a, b]$ (con $a < b$),e tnonces la imagen del intervalo $[a, b]$ por $f$ también es un intervalo cerrado:
> $$
> f([a, b]) = [m, M]
> $$
> donde $m := mín (f, [a, b])$ y $M := máx (f, [a, b])$.

---
Ahora, pasaremos a un nuevo tema:

# Funciones inversas

> [!Proposición]
> Sea $f : A \to \mathbb{R}$ una función definida en un subconjunto $A \subset \mathbb{R}$.
> 
> Si $f$ es estrictamente creciente (o decreciente), entonces $f$ es inyectiva y define una biyección entre $A$ y su imagen $B := f(A)$ por la función $f$.
> 
> Además, la función inversa $f^{-1}: B \to A$ también es estrictamente creciente (o decreciente).

(No lo demostraremos. Simplemente tenemos que considerar que tomando dos valores distintos $x_{1}, x_{2} \in A$, entonces $x_{1} < x_{2}$ o $x_{2} < x_{1}$, por lo que $f(x_{1}) \neq f(x_{2})$. Como es posible tomar una función y restringir su codominio a la imagen de la función, la idea es que si tomo una función inyectiva y restrinjo su codominio a la imagen de la función, pasa a ser biyectiva.)

Si añadimos la hipótesis de continuidad, $A$ será un intervalo, y lo mismo para $B$ (tendrá la misma forma). Lo importante aquí es que si la función $f$ es continua, entonces $f^{-1}$ también será continua.

Si $f: I \to \mathbb{R}$ es continua y estrictamente creciente (o decreciente), entonces es inyectiva y define una biyección de $I$ a su imagen $J : f(I)$ (gracias a Bolzano, sabemos que $J$ es un intervalo).

Además, la función inversa $f^{-1} : J \to I$ es estrictamente creciente (o decreciente) y es continua.

De esta manera, una función continua estrictamente creciente (o decreciente) se puede invertir siempre.

![[4 - Funciones inversas.png]]

Teniendo esto, veremos ejemplos, ya que este teorema es muy útil para definir nuevas funciones continuas.

## Ejemplo (raíz n-ésima)

Sea $n \geq 1$. Sea $f : [0, + \infty) \to \underbrace{ [0, + \infty) }_{ f([0, +\infty)) }$ definida por $f(x) = x^{p}$

$f$ es continua y estrictamente creciente. Gracias a estas características, sabiendo lo que pasa al comienzo y al final de la función, podemos intuir lo que pasa en el medio.

Se escribe $\sqrt[n]{ x } := f^{-1}(x)$.

Gracias al teorema, sabemos que dicha función es continua.
$$
\sqrt[n]{ \cdot } [0, + \infty) \to [0, + \infty)
$$

Restringimos el intervalo de entrada a $[0, + \infty)$ para asegurar que la función $f$ sea estrictamente creciente, sin importar si $n$ es par o impar:

**Observación**: cuando $n$ es impar, se puede reemplazar $[0, +\infty)$ por $\mathbb{R}$.

El último ejemplo que veremos es la función $\log$:

## Ejemplo ($\log$)
Sea $f : \mathbb{R}^{+} \to \mathbb{R}$
$$
x \mapsto f(x) = \log(x)
$$
Sabemos que es una función continua y estrictamente creciente, por lo que podemos aplicar el teorema, teniendo que determinar la imagen del mismo, analizando lo que hace en sus extremos.

$f$ es estrictamente creciente y continua:
$$
\lim_{ x \to 0^{+} } \log(x) = - \infty \qquad \text{y} \qquad \lim_{ x \to + \infty } \log(x) = + \infty
$$

Sabemos que la imagen de $f$ es un intervalo que va de $- \infty$ a $+ \infty$. De esta forma, el único intervalo que cumple con estas características es $\mathbb{R}$.

Luego: $\log(\mathbb{R}^{+}) = \mathbb{R}$

Ahora, sabiendo que se puede invertir, podemos definir su inversa:

$$
\exp := \log^{-1} : \mathbb{R} \to \mathbb{R}^{+}
$$

![[5 - Función logaritmo.png]]

Si vemos al logaritmo como una función que transforma a las sumas en productos (tomando en cuenta que $\log(x) + \log(y) = \log(xy)$), la función exponencial transforma a los productos en sumas ($\exp(x) \times \exp(y) = \exp(x + y)$).

Concluiremos con la propiedad fundamental de la exponencial

> [!Propiedad]
> $$
> \exp(0) = 1
> $$
> $$
> \exp(x + y) = \exp(x) \times \exp(y)
> $$
> $$
> \exp(-x) = \frac{1}{\exp(x)}
> $$
> Se define
> $$
> e := \exp(1)
> $$

Esto determina que topológicamente no hay ninguna diferencia esencial entre la suma y el producto.

La próxima clase, continuaremos con la función exponencial.