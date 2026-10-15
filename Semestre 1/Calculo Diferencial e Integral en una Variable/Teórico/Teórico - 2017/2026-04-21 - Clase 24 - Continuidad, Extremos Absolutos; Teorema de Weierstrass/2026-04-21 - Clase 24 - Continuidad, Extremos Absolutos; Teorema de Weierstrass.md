# Límites y continuidad
Durante estas clases estudiaremos los teoremas fundamentales de las funciones continuas, siendo el primero el teorema de los valores intermedios, teniendo dos versiones:
- Teorema de Bolzano: si tengo una función que comienza por debajo del eje x y termina por encima del mismo, si la función es continua, necesariamente tiene que pasar por el eje x. Permite demostrar la existencia de 0 en funciones.
- Teorema de los valores intermedios: consecuencia del anterior (generalización). Se toma una función cualquiera continua, tal que para valores de su dominio $a$ y $b$, con $f(a) < f(b)$, la función necesariamente toma todos los valores $\lambda$ intermedios a $f(a)$ y $f(b)$.

Ahora, veremos un corolario, consecuencia de este teorema:

## Corolario

> [!Corolario]
> Si $f : I \to \mathbb{R}$ es continua y definida en un intervalo $I \subset \mathbb{R}$, entonces su imagen $f(I)$ es un intervalo también.

### Demostración

Se trata de demostrar que:
$$
\forall y_{1}, y_{2} \in f(I), \forall y \in \mathbb{R}, y_{1} < y < y_{2} \implies y \in f(I)
$$
(La frase anterior indica que $f(I)$ es un intervalo, en base a la definición del mismo, por lo que tenemos que demostrarla.)

Sean $y_{1}, y_{2} \in f(I)$ e $y \in \mathbb{R}$ tales que $y_{1} < y < y_{2}$. (Implica que son distintos, por lo que las preimágenes también lo son.)
Existen $x_{1}, x_{2} \in I$ tales que $y_{1} = f(x_{1})$ e $y_{2} = f(x_{2})$.

(No sabemos en que orden se encuentran $x_{1}$ y $x_{2}$, por lo que distinguiremos dos casos.)

Se distinguen dos casos:

1. $x_{1} < x_{2}$
La función $f : [x_{1}, x_{2}] \to \mathbb{R}$ es continua y por hipótesis:
$$
\underbrace{ f(x_{1}) }_{ y_{1} } < y < \underbrace{ f(x_{2}) }_{ y_{2} } \qquad (y \text{ es valor intermedio})
$$
Luego existe $x \in [x_{1}, x_{2}]$ tal que $f(x) = y$ (por el teorema de los valores intermedios).

Por lo tanto:
$$
y = f(x) \in f(I)
$$

2. $x_{2} < x_{1}$
Mismo razonamiento, pero $x_{1}$ y $x_{2}$ se intercambian.

El teorema de los valores intermedios aplica para las funciones definidas en un intervalo cerrado. Sin embargo, el corolario anterior aplica para las funciones definidas en cualquier tipo de intervalo

Lo que queremos establecer es que, en general, la imagen de cualquier tipo de intervalo por una función continua, es otro intervalo.

La idea es que un intervalo de $\mathbb{R}$ es un subconjunto de $\mathbb{R}$ "de una sola pieza" (sin cortar). Si utilizo esto como dominio para una función continuo, necesariamente su imagen tiene que ser "de una sola pieza".

---
A continuación, una aclaración importante:

> [!Observación]
> El tipo de intervalo no se mantiene en general.

Por ejemplo, se puede tener un intervalo abierto, cuya imagen sea cerrada:
![[1 - Observación.png]]
Cualquier otra combinación es posible.

Como vemos, la propiedad "ser un intervalo" se mantiene a través de transformación continua, pero el tipo de intervalo no se mantiene. La única excepción son los intervalos cerrados, y dicha propiedad está dada por un teorema: el Teorema de Weierstrass

**Excepción**: los intervalos cerrados se mantienen:
$$
f([a, b]) = [c, d]
$$

El Teorema de Weierstrass establece que toda función continua definida en un intervalo cerrado tiene mínimo y máximo absoluto, equivalente a decir que su imagen es un intervalo cerrado.

---
# Extremos absolutos

> [!Extremos absolutos]
> Sea $f : I \to \mathbb{R}$ una función cualquiera.
> Se dice que un punto $(x_{0}, f(x_{0}))$ de la gráfica de $f$ es:
> - un mínimo absoluto de $f$ si $f(x_{0}) \leq f(x) \qquad (\forall x \in I)$
> - un máximo absoluto de $f$ si $f(x_{0}) \geq f(x) \qquad (\forall x \in I)$
> - un extremo absoluto si $(x_{0}, f(x_{0}))$ es un mínimo absoluto o un máximo absoluto.
> 
> También se dice que $f$ tiene mínimo/máximo/extremo absoluto en $x_{0} \in I$ cuando el punto $(x_{0}, f(x_{0}))$ es un mínimo/máximo/extremo absoluto de $f$.

De esta forma, podemos decir que el mínimo/máximo/extremo absoluto es un punto con dos coordenadas, o decimos que el mínimo/máximo/extremo absoluto existe en un punto del intervalo (dominio).
La razón es que, si ya conocemos $x_{0}$, podemos calcular su imagen (coordenada y).

Sin embargo, nunca decimos que $x_{0}$ es un mínimo/máximo/extremo absoluto, puesto que se trata de un valor del intervalo, no es una imagen. Dicha noción solo aplica a la noción vertical de la función.

Tampoco está establecida la cantidad de mínimos/máximos/extremos absolutos: pueden haber 0, 1, múltiples, etc.:
![[2 - Extremos absolutos.png]]

Tampoco es una noción que tenga que ver con la continuidad. Por ejemplo, en la función de Dirichlet, la más discontinua que conocemos, todos sus puntos son extremos:
- Todos los valores racionales tienen valor 1, por lo que todos son máximos absolutos.
- Todos los valores irracionales tienen valor 0, por lo que todos son mínimos absolutos.}

Algo interesante es que cada vez que tengo un máximo absoluto, esto establece que el conjunto imagen tiene un máximo. ==De esta forma, el conjunto imagen tiene un máximo, si y solo si la función tiene máximo. Lo mismo aplica para el mínimo==.

---
Tomando en cuenta todo esto, podemos establecer que cuando una función es continua y está definida en un intervalo cerrado, entonces tiene mínimo y máximo.
Antes de demostrar esto, demostraremos que la función está acotada:

## Proposición

> [!Proposición]
> Si $f : [a, b] \to \mathbb{R}$ es continua, entonces $f$ está acotada.

### Demostración
Sea $A := \{ c \in [a, b] : f \text{ está acotada en } [a, c] \}$

(Para demostrar que está acotada en $[a, b]$, vamos a comenzar con los subintervalos por la izquierda. Por eso trabajaremos con $A$, todos los subintervalos que representan una parte izquierda del intervalo.)

**Observación**
$a \in A$, pues $f$ está acotada en $[a, a] = \{ a \}$.

(Estamos seguros de que en el intervalo $[a, a]$ la función está acotada, es un caso trivial. Ahora, queremos avanzar por todo el intervalo, teniendo como objetivo demostrar que $b \in A$.)

Sea $s := sup(A)$. Queremos demostrar que $s = b \in A$.

Desarrollaremos la demostración por partes:
1. Como $f$ es continua en $s$ (sabiendo que es continua en todo punto), está acotada en un entorno de $s$ (pues tiene límite).
Entonces, existen $\delta > 0$ y $M_{s} \geq 0$ tales que
$$
\forall x \in E(x_{0}, \delta) \cap [a, b], |f(x)| \leq M_{s}
$$

2. Como $s = sup(A)$ existe $c \in A$ tal que $s - \delta < c \leq s$
Como $c \in A$, existe $M_{c} \geq 0$ tal que
$$
\forall x \in [a, c], |f(x)| \leq M_{c}
$$ (en base a que $f$ está acotada en $[a, c]$).

(De esta forma, tenemos un punto $s$ y estamos acotados alrededor del mismo. Además, tenemos un punto $c$ a la izquierda de $s$, donde la función está acotada en $[a, c]$, pero establecimos el punto $c$ de tal forma que esté presente en ambos intervalos: $E(x_{0}, \delta) \cap [a, b]$ y $(s - \delta, s]$.)

3. Sea $s' := mín \left( s + \frac{\delta}{2}, b \right)$.
Se observa que
$$
\left.
\begin{align}
&c \in E(x_{0}, \delta) \cap [a, b] \\
&s' \in E(x_{0}, \delta) \cap [a, b]
\end{align}
\right\} [c, s'] \subset E(x_{0}, \delta) \cap [a, b]
$$
![[3 - Representación de demostración.png]]

De esta manera, como $c$ pertenece a ambos intervalos, de forma que podemos unirlos manteniendo la unicidad, y obteniendo una función acotada en la unión de ambos intervalos, que es el intervalo $[a, s']$.

4. Agregando lo anterior:
$$
\left. \forall x \in [a, s'], |f(x)| \leq máx(M_{c}, M_{s}) \space \right\} \implies s' \in A
$$
(Como demostramos que la función está acotada en $[a, s']$, entonces $s'$ pertenece al conjunto $A$.)

5. Como $s' \in A$, tenemos que $s' \leq s = sup(A)$.
Como $s + \frac{\delta}{2} \geq s$ y $b \geq s$, $s' := mín \left( s + \frac{\delta}{2}, b \right) \geq s$

En base a los dos puntos anteriores, concluimos que $s = s'$.

Entonces $s' \neq s + \frac{\delta}{2}$ (puesto que solo se cumple si $\delta = 0$, y sabemos que $\delta > 0$), luego $s' = b = s \in A$, por lo tanto $b \in A$.

6. $b \in A$

De esta forma, concluimos que $b \in A$, por lo que la función $f$ está acotada en $[a, b]$.

---
Ahora, pasaremos a estudiar el Teorema de Weierstrass:

# Teorema de Weierstrass

> [!Teorema de Weierstrass]
> Si $f : [a, b] \to \mathbb{R}$ es continua definida en un intervalo cerrado $[a, b]$, entonces tiene mínimo y máximo.
> Es decir:
> $$
> \exists x_{0}, x_{1} \in [a, b]
> $$
> tales que
> $$
> \forall x \in [a, b], f(x_{0}) \leq f(x) \leq f(x_{1})
> $$

![[4 - Teorema de Weierstrass.png]]
Se trata de un problema geométrico: si logro demostrar la existencia de $x_{1}$, entonces puedo tomar la función inversa y demostrar la existencia de $x_{0}$. Es así que trabajaremos con supremos en lugar de ínfimos

## Demostración (existencia de $x_{1}$)

Como $f$ está acotada (por la proposición anterior) se pueden definir:
- $M := sup(f, [a, b])$
- $g : [a, b] \to \mathbb{R}$
$$
x \mapsto g(x) := sup(f, [a, x])
$$

Representación de $f$ y $g$:
![[5 - Representación de g.png|697]]
(De esta forma, transformamos a $f$ en una función monótona creciente.)

Por construcción:
- $g$ es monótona creciente
- $g(a) = f(a)$
- $g(b) = M \qquad (= sup(f, [a, b]))$

(Ahora, para demostrar que $g$ es monótona creciente, consideraremos todos los puntos que nos da el supremo y tomaremos el último.)

Sea $S := \{ x \in [a, b], g(x) = M \}$ (el conjunto de puntos para los cuales $g$ alcanza su valor máximo).
- $S \neq \emptyset$, pues $b \in S$:  tiene ínfimo: $x_{1} := ínf(S)$

(Ahora, nos queda demostrar que $f(x_{1}) = M$.)

Se observa que:
- Si $x < x_{1}$, entonces $x \not \in S \implies g(x) < M$ (estricto)
- Si $x > x_{1}$, entonces $x > ínf(S)$ y existe $x' \in S$ tal que $x_{1} \leq x' < x$
$g(x) \geq g(x') = M$ (pues es monótona creciente)
$$
\implies g(x) = M, x \in S
$$
Es así que determinamos que para todos los $x < x_{1}, x \not \in S$, mientras que para los $x > x_{1}, x \in S$, pues $g(x) = M$. De esta manera, $S$ es un intervalo que va desde $x_{1}$ a $b$.

Luego:
$$
S = (x_{1}, b] \qquad \text{o} \qquad S = [x_{1}, b]
$$

Queremos demostrar que $f(x_{1}) = M$.
Por el absurdo, se supone que $f(x_{1}) < M$.

(Utilizaremos la continuidad en el punto $x_{1}$.)
![[6 - Representación de demostración por el absurdo.png]]

Sea $\epsilon := \frac{M - f(x_{1})}{2} > 0$.
$$
\exists \delta > 0, \forall x \in E(x_{1}, \delta) \cap [a, b], |f(x) - f(x_{1})| < \epsilon
$$
Lo que implica
$$
f(x) < f(x_{1}) + \epsilon = \frac{f(x_{1}) + M}{2} = M - \epsilon
$$

Concluiremos con una demostración gráfica:

Tomamos un punto $x_{1}^{-}$ que esté dentro del radio de seguridad, siendo menor que $x_{1}$.
$$
x_{1}^{-} := máx (x_{1} - \frac{\delta}{2}, a)
$$
Considerando $x \in [a, x_{1}^{-}]$:
$$
f(x) \leq g(x) \leq g(x_{1}^{-})
$$
Tomamos otro punto $x_{1}^{+}$ definido por simetría dentro del radio de seguridad, mayor que $x_{1}$.
Sabemos que la función es estrictamente menor que $M$ fuera del radio de seguridad, y menor o igual a $M - \epsilon$, lo que nos permite demostrar que:
$$
\begin{align}
g(x_{1}^{+}) &\leq máx(g(x_{1}^{-}), M - \epsilon) \\
&< M
\end{align}
$$
Sin embargo, antes habíamos demostrado que si $x > x_{1}$, entonces $g(x) = M$, por lo que llegamos a una contradicción.
De esta forma, concluimos que $f(x_{1}) = M$ (existe y es máximo).
