# Capítulo 3 - Sucesiones y Series
## Ejercicio 3.10
### Parte 1
Demostrar que si $a_{n} \leq b_{n}, \forall n \in \mathbb{N}$ y ambas tienen límite, entonces $\lim a_{n} \leq \lim b_{n}$. 

Sabemos que ambas sucesiones tienen límite, por lo que:
$$
\forall \epsilon > 0, \exists n_{1} \in \mathbb{N} \text{ tal que } \forall n \geq n_{1}, a_{n} \in E(L_{1}, \epsilon) \qquad (|a_{n} - L_{1}| < \epsilon)
$$
$$
\forall \epsilon > 0, \exists n_{2} \in \mathbb{N} \text{ tal que } \forall n \geq n_{2}, b_{n} \in E(L_{2}, \epsilon) \qquad (|b_{n} - L_{2}| < \epsilon)
$$
Entonces, consideramos $n_{3} = \max\{ n_{1}, n_{2} \}$, verificando que $\forall n \geq n_{3}$: $a_{n} \in E(L_{1}, \epsilon)$ y $b_{n} \in E(L_{2}, \epsilon)$.

Entonces, considerando el índice común $n_{3}$, puede pasar:
- $\exists n \geq n_{3}$ a partir del cual $E(L_{1}, \epsilon) \cap E(L_{2}, \epsilon) = \emptyset$. Aquí podemos considerar que $a_{n} \leq b_{n}, \forall n \in \mathbb{N}$, lo que implicaría que $\forall n \geq n_{3}$, $a_{n} < b_{n}$. En este caso, como ambas sucesiones tienen límite, determinamos que $\lim a_{n} < \lim b_{n}$.
- $E(L_{1}, \epsilon) \cap E(L_{2}, \epsilon) \neq \emptyset, \forall n \geq n_{3}$. En este caso, los entornos nunca son disjuntos. Como esto ocurre para cualquier radio $\epsilon > 0$, necesariamente sus centros tienen que coincidir: $L_{1} = L_{2}$. De esta manera, $\lim a_{n} = \lim b_{n}$.

En conclusión, logramos probar que si $a_{n} \leq b_{n}, \forall n \in \mathbb{N}$ y ambas tienen límite, entonces $\lim a_{n} \leq \lim b_{n}$.

CORRECCIÓN: Se demuestra por absurdo: queremos probar que $a_{n} \leq b_{n}, \forall n \in \mathbb{N}, \lim a_{n} = L_{1}, \lim b_{n} = L_{2} \implies L_{1} \leq L_{2}$.

Suponemos que $L_{1} > L_{2}$:

Como sabemos que ambas sucesiones tienen límite, entonces podemos elegir un $\epsilon$ para probarlo a nuestra conveniencia:
$$
\epsilon = \frac{L_{1} - L_{2}}{2} > 0
$$
Como ambas tienen límite:
- $\forall \epsilon > 0, \exists n_{1} \in \mathbb{N}$ tal que $\forall n \geq n_{1}, a_{n} \in (L_{1} - \epsilon, L_{1} + \epsilon) \implies a_{n} > L_{1} - \epsilon = \frac{L_{1} + L_{2}}{2}$
- $\forall \epsilon > 0, \exists n_{2} \in \mathbb{N}$ tal que $\forall n \geq n_{2}, b_{n} \in (L_{2} - \epsilon, L_{2} + \epsilon) \implies b_{n} < L_{2} + \epsilon = \frac{L_{1} + L_{2}}{2}$

Entonces, consideramos el índice $n_{3} = \max \{ n_{1}, n_{2} \}$, a partir del cual se cumplen ambas condiciones a la vez:
$$
a_{n} > \frac{L_{1} + L_{2}}{2} > b_{n} \implies a_{n} > b_{n}
$$

Sin embargo, esto contradice la hipótesis inicial $a_{n} \leq b_{n}, \forall n \in \mathbb{N}$.

En conclusión, el supuesto $L_{1} > L_{2}$ es falso, por lo que determinamos que $L_{1} \leq L_{2}$

### Parte 2
Hipótesis: sabemos que:
- $a_{n}$ es acotada
- $\lim_{ n \to \infty } b_{n} = 0$

Tesis: queremos probar que:
- $\lim_{ n \to \infty } a_{n} \cdot b_{n} = 0$

Consideremos la definición de sucesión acotada:
$a_{n}$ está acotada $\Longleftrightarrow \exists K \in \mathbb{R}$ tal que $|a_{n}| \leq K, \forall n \in \mathbb{N}$.

Esto significa que absolutamente toda la sucesión es menor que $K$ en valor absoluto, o dicho de otra forma: $-K \leq a_{n} \leq K$.

Si bien no se especifica que la sucesión tenga límite, podemos suponer que tiene como límite a $K$, siendo el valor máximo que podemos considerar.

Entonces, proseguimos a expresar el producto de los límites:
$$
\begin{align}
\lim_{ n \to \infty } a_{n} \cdot b_{n} &= 0 \\
\lim_{ n \to \infty } a_{n} \cdot \lim_{ n \to \infty } b_{n} &= 0 \\
K \cdot 0 &= 0 \\
0 &= 0
\end{align}
$$
Como $K$ es un real, sabemos que el producto de cualquier número real por 0 da como resultado 0. De esta manera, probamos que $\lim_{ n \to \infty } a_{n} \cdot b_{n} = 0$.

DEMOSTRACIÓN INCORRECTA. A CONTINUACIÓN SE REALIZA CORRECTAMENTE:

Hipótesis: sabemos que:
- $a_{n}$ es acotada
- $\lim_{ n \to \infty } b_{n} = 0$

Tesis: queremos probar que:
- $\lim_{ n \to \infty } a_{n} \cdot b_{n} = 0$

Por hipótesis de acotación, sabemos que existe $K \in \mathbb{R}$ tal que
$$
|a_{n}| \leq K \qquad \forall n \in \mathbb{N}
$$

Ahora, consideramos la definición de límite aplicada a la sucesión $a_{n} \cdot b_{n}$ (la cual queremos probar):
$$
\forall \epsilon > 0, \exists n_{0} \in \mathbb{N} \text{ tal que } \forall n \geq n_{0} \text{ se cumple que } |a_{n} \cdot b_{n} - 0| < \epsilon
$$
Lo anterior no está probado, es el objetivo de la demostración. Queremos estudiar el valor absoluto de la tesis para ver que tan cerca de 0 está:
$$
|a_{n} \cdot b_{n} - 0| = |a_{n} \cdot b_{n}| = |a_{n}| \cdot |b_{n}|
$$

Aplicamos la acotación $|a_{n}| \leq K, \forall n \in \mathbb{R}$:
$$
|a_{n}| \cdot |b_{n}| \leq K \cdot |b_{n}|
$$

Por hipótesis, sabemos que $\lim_{ n \to \infty } b_{n} = 0$, lo que quiere decir que $\forall \epsilon > 0, \exists n_{0} \in \mathbb{N} \text{ tal que } \forall n \geq n_{0} \text{ se cumple que } |b_{n}| < \epsilon$

Queremos determinar un valor de $\epsilon$ que nos permita demostrar la tesis. Entonces, dividiremos a la sucesión por $K$ para que sea aún más pequeña:
$$
\epsilon' = \frac{\epsilon}{K} > 0
$$
Entonces, para este $\epsilon'$, existe un $n_{0} \in \mathbb{N}$ tal que si $n \geq n_{0}$, se cumple que $|b_{n}| < \frac{\epsilon}{K}$

Para verificar que funciona, tomamos cualquier índice a partir de $n_{0}$, a partir del cual:
$$
|a_{n} \cdot b_{n}| = |a_{n}| \cdot |b_{n}| \leq K \cdot |b_{n}| < K \cdot \frac{\epsilon}{K} = \epsilon
$$

De esta forma, para cualquier $\epsilon > 0$, logramos encontrar un $n_{0}$ a partir del cual $|a_{n} \cdot b_{n} - 0| < \epsilon$, lo que demuestra por definición de límite de sucesiones que:
$$
\lim_{ n \to \infty } a_{n} \cdot b_{n} = 0 
$$

---
## Ejercicio 3.13
Analicemos que significa que $a_{n}$ sea creciente y $b_{n}$ sea decreciente:
- $a_{n}$ es creciente, entonces verifica que $\forall n \in \mathbb{N}$, $a_{n + 1} \geq a_{n}$.
- $b_{n}$ es decreciente, entonces verifica que $\forall n \in \mathbb{N}$, $a_{n + 1} \leq a_{n}$.

Considerando que $a_{n} \leq b_{n}, \forall n \in \mathbb{N}$ en conjunto con lo anterior, la sucesión $b_{n}$ es superior a $a_{n}$ en todo su recorrido.

De esta forma, la sucesión $b_{n}$ no decrece indefinidamente, sino que lo hace (como máximo) hasta alcanzar una cota determinada por $a_{n}$ (análogo para $a_{n}$). Expresemos dichas cotas como $m = sup \{ a_{n} : n \in \mathbb{N} \}$ y $M = ínf \{ b_{n} : n \in \mathbb{N} \}$. Entonces, podríamos decir que:
- $b_{n} \geq m$
- $a_{n} \leq M$

Esto significa que ambas sucesiones están acotadas, y al ser crecientes/decrecientes, necesariamente tienen límite.

Entonces, podemos denominarlos como $\lim_{ n \to \infty } a_{n} = L$ y $\lim_{ n \to \infty } b_{n} = L'$.

Ya que $b_{n}$ es mayor o igual a $a_{n}$ en todo su recorrido, necesariamente la misma igualdad se mantiene al comparar sus límites, ya que si $L' < L$, a partir de un determinado $n_{0} \in \mathbb{N}$ tendría que cumplirse que $a_{n} > b_{n}, \forall n \geq n_{0}$, y sabemos que esto no es posible por la hipótesis. Entonces, determinamos que $L' \geq L$

Como habíamos mencionado, las sucesiones se encuentran acotadas por dos valores que denominamos $m$ y $M$. Considerando el punto $(iii)$ de la hipótesis, para todo $\epsilon > 0$, existe un $n_{0} \in \mathbb{N}$ tal que verifica $b_{n_{0}} - a_{n_{0}} < \epsilon$. Además, dicha diferencia se haría cada vez menor $\forall n \geq n_{0}$, por la cualidad de creciente/decreciente. Si analizamos la definición de límite aplicada a las sucesiones, llegamos a las igualdades $|b_{n} - L'| < \epsilon$ y $|a_{n} - L| = |L - a_{n}| < \epsilon$. De esta manera, necesariamente tiene que cumplirse que, a partir de $n_{0}$, ambas condiciones se den a la vez:
$$
b_{n_{0}} - a_{n_{0}} < \epsilon \implies \begin{cases}
|b_{n} - L'| < \epsilon \\
|a_{n} - L| = |L - a_{n}| < \epsilon
\end{cases} \space (\forall n \geq n_{0}) \implies L = L'
$$

CORRECCIÓN: Revisar en el chat de Notebook

---
## Ejercicio 3.18
### Parte 1
$$
\begin{align}
\lim_{ n \to \infty } n \cdot [\log(n + 1) - \log(n)] &= 1 \\
\lim_{ n \to \infty } n \cdot \left[ \log\left( \frac{n + 1}{n} \right) \right] &= 1 \\
\lim_{ n \to \infty } n \cdot \left[ \log\left( 1 + \frac{1}{n} \right) \right] &= 1 \\
\lim_{ n \to \infty } n \cdot \left[ \log\left( 1 + 0 \right) \right] &= 1 \\
\lim_{ n \to \infty } n \cdot \log\left( 1 \right) &= 1 \\
\infty \cdot 0 &= 1 \implies \text{Indefinido}
\end{align}
$$
Sustituimos $\log\left( 1 + \frac{1}{n} \right)$ por una sucesión equivalente conocida, como por ejemplo $\frac{1}{n}$:

$$
\begin{align}
\lim_{ n \to \infty } n \cdot \left[ \log \left( 1 + \frac{1}{n} \right) \right] &= \lim_{ n \to \infty } n \cdot \frac{1}{n} \\
&= \lim_{ n \to \infty } \frac{n}{n} \\
&= 1
\end{align}
$$

### Parte 2
$$
\begin{align}
\lim_{ n \to \infty } n^{2} \cdot \sin\left( \frac{1}{n} \right) &= \infty \\
\lim_{ n \to \infty } \infty \cdot \sin\left( 0 \right) &= \infty \\
\lim_{ n \to \infty } \infty \cdot 0 &= \infty \implies \text{Indefinido}
\end{align}
$$
Sustituimos $\sin\left( \frac{1}{n} \right)$ por una función semejante, como $\frac{1}{n}$:
$$
\begin{align}
\lim_{ n \to \infty } n^{2} \cdot \sin\left( \frac{1}{n} \right) &= \lim_{ n \to \infty } n^{2} \cdot \frac{1}{n} \\
&= \lim_{ n \to \infty } \frac{n^{2}}{n} \\
&= \lim_{ n \to \infty } n \\
&= \infty
\end{align}
$$

### Parte 3
$$
\lim_{ n \to \infty } n \cdot \left[ n - \sqrt{ n^{2} - 1 } \right] \overset{?} = \frac{1}{2}
$$
Analizamos el factor $n - \sqrt{ n^{2} - 1 }$ e intentamos simplificarlo multiplicando y dividiendo por el conjugado:
$$
n - \sqrt{ n^{2} - 1 } = \frac{(n - \sqrt{ n^{2} - 1 }) \cdot (n + \sqrt{ n^{2} - 1 })}{n + \sqrt{ n^{2} - 1 }} = \frac{n^{2} - n^{2} + 1}{n + \sqrt{ n^{2} - 1 }} = \frac{1}{n + \sqrt{ n^{2} - 1 }}
$$
En el denominador, cuando $n \to \infty$, el término principal pasa a ser $n^{2}$, por lo tanto:
$$
\sqrt{ n^{2} - 1 } \sim \sqrt{ n^{2} } = n
$$
Entonces, el nuevo factor es $\frac{1}{n + n} = \frac{1}{2n}$

Sustituimos en el límite anterior:
$$
\begin{align}
\lim_{ n \to \infty } n \cdot \left[ n - \sqrt{ n^{2} - 1 } \right] &= \lim_{ n \to \infty } n \cdot \frac{1}{2n} \\
&= \lim_{ n \to \infty } \frac{\cancel{ n }}{2\cancel{ n }} \\
&= \lim_{ n \to \infty } \frac{1}{2} \\
&= \frac{1}{2}
\end{align}
$$
