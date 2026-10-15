# Ejercicios del práctico
## Ejercicio 1
¿Cómo evaluamos cada una de las características mencionadas?
- Monotonía: comparamos los términos $a_{n}$ y $a_{n + 1}$ mediante resta ($a_{n + 1} - a_{n} > 0$?) o división ($\frac{a_{n + 1}}{a_{n}} > 1$?) según el caso.
- Acotación: en base a la definición de la sucesión, evaluar si existe un $K \in \mathbb{R}$ tal que $|a_{n}| \leq K, \forall n \in \mathbb{N}$
- Convergencia: estudiar aplicando la definición de límite, considerando un $\epsilon > 0$ genérico y hallando un $n_{0}$ a partir del cual todos los términos se encuentren en el entorno correspondiente.
### Parte a
$$
a_{n} = 1 + \frac{1}{n}
$$
- Monotonía
$$
\begin{align}
a_{n + 1} - a_{n} &= 1 + \frac{1}{n + 1} - \left( 1 + \frac{1}{n} \right) \\
&= \cancel{ 1 } + \frac{1}{n + 1} - \cancel{ 1 } - \frac{1}{n} \\
&= \frac{1}{n + 1} - \frac{1}{n} \\
&= \frac{n - (n + 1)}{n^{2} + n} \\
&= \frac{\cancel{ n } - \cancel{ n } - 1}{n^{2} + n} \\
&= -\frac{1}{n^{2} + n} < 0
\end{align}
$$
Como $a_{n + 1} - a_{n} < 0$, determinamos que la sucesión es monótona decreciente.

- Acotación
¿Existe $K \in \mathbb{R}$ tal que $|a_{n}| < K, \forall n \in \mathbb{N}$?

Sabemos que $0 < \frac{1}{n} \leq 1$, entonces, si sumamos uno a todos los miembros de la desigualdad, obtenemos:
$$
1 < 1 + \frac{1}{n} \leq 2
$$
Entonces, todos los términos de la sucesión se encuentran atrapados en el intervalo $(1, 2]$, por lo que si elegimos $K = 2$, se cumple que:
$$
|a_{n}| \leq 2, \forall n \in \mathbb{N}
$$

- Convergencia
Sabiendo que la sucesión es monótona decreciente y está acotada, necesariamente converge. Para determinar dicho valor de $L$, primero tenemos que realizar una conjetura:

Analizando la expresión $1 + \frac{1}{n}$ podemos ver que está compuesta por dos términos:
- La sucesión $1$ que converge a $1$.
- La sucesión $\frac{1}{n}$ que converge a $0$.

Entonces, conjeturamos que el límite tiene que ser $L = 1$. Lo probamos con la definición:

Sea $\epsilon > 0$, queremos determinar un $n_{0} \in \mathbb{N}$ en base a $\epsilon$ que cumpla que $\forall n \geq n_{0}, a_{n} \in E(L, \epsilon)$, siendo $L = 1$ el límite correspondiente en caso de existir.

$$
\begin{align}
\left| 1 + \frac{1}{n} - L \right| &< \epsilon \\
\left| \cancel{ 1 } + \frac{1}{n} - \cancel{ 1 } \right| &< \epsilon \\
\left| \frac{1}{n} \right| &< \epsilon \\
\frac{1}{n} &< \epsilon \\
1 &< \epsilon \cdot n \\
\frac{1}{\epsilon} &< n
\end{align}
$$

De esta forma, encontramos un $n_{0} = \frac{1}{\epsilon}$ tal que $\forall n \geq n_{0}$ se cumple que $a_{n} \in E(1, \epsilon)$

En conclusión, la sucesión converge a 1.

### Parte b
$$
a_{n} = 1 + \frac{(-1)^{n}}{n}
$$
- Monotonía
$$
\begin{align}
a_{n + 1} - a_{n} &= 1 + \frac{(-1)^{n + 1}}{n + 1} - \left( 1 + \frac{(-1)^{n}}{n} \right) \\
&= \cancel{ 1 } + \frac{(-1)^{n + 1}}{n + 1} - \cancel{ 1 } - \frac{(-1)^{n}}{n} \\
&= \frac{(-1)^{n + 1}}{n + 1} - \frac{(-1)^{n}}{n} \\
&= \frac{(-1)^{n + 1}}{n + 1} + \frac{(-1)^{n + 1}}{n} \\
&= (-1)^{n + 1} \left( \frac{1}{n + 1} + \frac{1}{n} \right)
\end{align}
$$
La suma $\frac{1}{n + 1} + \frac{1}{n}$ siempre es positiva. Sin embargo, $(-1)^{n + 1}$ va alternando su signo, por lo que la diferencia puede ser positiva o negativa dependiendo del $n$ considerado.

Como no se cumple que la diferencia sea positiva ni negativa de forma continua, determinamos que la sucesión no es monótona creciente ni decreciente.

- Acotación
¿Existe $K \in \mathbb{R}$ tal que $|a_{n}| < K, \forall n \in \mathbb{N}$?

Sabemos que $-1 \leq \frac{(-1)^{n}}{n} < 1$, entonces, si sumamos uno a todos los miembros de la desigualdad, obtenemos:
$$
0 \leq 1 + \frac{(-1)^{n}}{n} < 2
$$
Entonces, todos los términos de la sucesión se encuentran atrapados en el intervalo $[0, 2)$, por lo que si elegimos $K = 2$, se cumple que:
$$
|a_{n}| \leq 2, \forall n \in \mathbb{N}
$$

- Convergencia
Aunque esté acotada, sabemos que la sucesión no es monótona creciente/decreciente, por lo que no podemos asegurar que converja. Antes de poder aplicar la definición, tenemos que realizar una conjetura sobre el posible límite $L$:

Analizando la expresión $1 + \frac{(-1)^{n}}{n}$ podemos ver que está compuesta por dos términos:
- La sucesión $1$ que converge a $1$.
- La sucesión $\frac{(-1)^{n}}{n}$ que converge a $0$.

Entonces, conjeturamos que el límite tiene que ser $L = 1$. Lo probamos con la definición:

Sea $\epsilon > 0$, queremos determinar un $n_{0} \in \mathbb{N}$ en base a $\epsilon$ que cumpla que $\forall n \geq n_{0}, a_{n} \in E(L, \epsilon)$, siendo $L = 1$ el límite correspondiente en caso de existir.

$$
\begin{align}
\left| 1 + \frac{(-1)^{n}}{n} - L \right| &< \epsilon \\
\left| \cancel{ 1 } + \frac{(-1)^{n}}{n} - \cancel{ 1 } \right| &< \epsilon \\
\left| \frac{(-1)^{n}}{n} \right| &< \epsilon \\
\left| (-1)^{n} \right| &< \epsilon \cdot |n| \\
\left| (-1)^{n} \right| &< \epsilon \cdot n \\
\frac{\left| (-1)^{n} \right|}{\epsilon} &< n
\end{align}
$$

De esta forma, encontramos un $n_{0} = \frac{\left| (-1)^{n} \right|}{\epsilon}$ tal que $\forall n \geq n_{0}$ se cumple que $a_{n} \in E(1, \epsilon)$

En conclusión, la sucesión converge a 1.

### Parte c
$$
a_{n} = n + \frac{1}{n}
$$
- Monotonía
$$
\begin{align}
a_{n + 1} - a_{n} &= n + 1 + \frac{1}{n + 1} - \left( n + \frac{1}{n} \right) \\
&= \cancel{ n } + 1 + \frac{1}{n + 1} - \cancel{ n } - \frac{1}{n} \\
&= 1 + \frac{1}{n + 1} - \frac{1}{n} \\
&= 1 + \frac{n - (n + 1)}{n(n + 1)} \\
&= 1 + \frac{\cancel{ n } - \cancel{ n } - 1}{n^{2} + n} \\
&= 1 - \frac{1}{n^{2} + n} > 0
\end{align}
$$
Como $a_{n + 1} - a_{n} > 0$, determinamos que la sucesión es monótona creciente.

- Acotación
¿Existe $K \in \mathbb{R}$ tal que $|a_{n}| < K, \forall n \in \mathbb{N}$?

La pregunta aquí es, ¿Podemos atrapar la expresión $n + \frac{1}{n}$ en una desigualdad que involucre únicamente valores constantes?

Si estudiamos cada término:
- $\frac{1}{n}$ es una sucesión que se podría acotar fácilmente, considerando que converge a 0, es monótona decreciente y acotada, por ejemplo tomando $K = 1$.
- $n$ es una sucesión que toma el valor del natural correspondiente para cada valor de la sucesión, por lo tanto, aumenta a velocidad constante para todos los naturales.

En base al análisis anterior, es imposible acotar la sucesión.

- Convergencia
Aunque sea monótona creciente, sabemos que la sucesión no es acotada, por lo que no tiene límite finito. Igualmente, sigamos el desarrollo realizado en las partes anteriores.

Analizando la expresión $n + \frac{1}{n}$ podemos ver que está compuesta por dos términos:
- La sucesión $\frac{1}{n}$ que converge a $0$.
- La sucesión $n$ que no converge a ningún número real, si no que crece a infinito.

De esta forma, la función crece indefinidamente, tendiendo a infinito:
$$
\lim_{ n \to \infty } n + \frac{1}{n} = +\infty 
$$

### Parte d
$$
a_{n} = \frac{n}{\sqrt{ n^{2} + 1 }}
$$
- Monotonía
$$
\begin{align}
\frac{a_{n + 1}}{a_{n}} &= \frac{\frac{n + 1}{\sqrt{ (n + 1)^{2} + 1 }}}{\frac{n}{\sqrt{ n^{2} + 1 }}} \\
&= \frac{\frac{n + 1}{\sqrt{ n^{2} + 2n + 2 }}}{\frac{n}{\sqrt{ n^{2} + 1 }}} \\
&= \frac{(n + 1)\sqrt{ n^{2} + 1 }}{n\sqrt{ n^{2} + 2n + 2 }} \\
&= \frac{\sqrt{ (n^{2} + 2n + 1)(n^{2} + 1) }}{\sqrt{ n^{4} + 2n^{3} + 2n^{2} }} \\
&= \sqrt{ \frac{(n^{2} + 2n + 1)(n^{2} + 1)}{n^{4} + 2n^{3} + 2n^{2}} } \\
&= \sqrt{ \frac{n^{4} + 2n^{3} + 2n^{2} + 2n + 1}{n^{4} + 2n^{3} + 2n^{2}} } \\
&= \sqrt{ \frac{\cancel{ n^{4} + 2n^{3} + 2n^{2} }}{\cancel{ n^{4} + 2n^{3} + 2n^{2} }} + \frac{2n + 1}{n^{4} + 2n^{3} + 2n^{2}} } \\
&= \sqrt{ 1 + \frac{2n + 1}{n^{4} + 2n^{3} + 2n^{2}} } > 1
\end{align}
$$
Como $\frac{a_{n + 1}}{a_{n}} > 1$, determinamos que la sucesión es monótona creciente.

- Acotación
¿Existe $K \in \mathbb{R}$ tal que $|a_{n}| < K, \forall n \in \mathbb{N}$?

$$
\frac{n}{\sqrt{ n^{2} + 2 }} < \frac{n}{\sqrt{ n^{2} + 1 }} < \frac{n}{\sqrt{ n^{2} }} = \frac{n}{n} = 1
$$
De esta forma, encontramos un $K$ para el cual se cumple que $a_{n} \leq K, \forall n \in \mathbb{N}$.

- Convergencia
Sabiendo que la sucesión es monótona creciente y está acotada, necesariamente converge. Para determinar dicho valor de $L$, primero tenemos que realizar una conjetura:

Analizando la expresión $\frac{n}{\sqrt{ n^{2} + 1 }}$ podemos ver que está compuesta por dos elementos:
- La sucesión $n$ que tiende a $+\infty$.
- La sucesión $\sqrt{ n^{2} + 1 }$ que tiende a $+\infty$. Sin embargo, lo hace un poco más rápido que $n$, ya que $n = \sqrt{ n^{2} } < \sqrt{ n^{2} + 1 }$.

Si desarrollamos su división:
$$
\frac{n}{\sqrt{ n^{2} + 1 }} = \sqrt{ \frac{n^{2}}{n^{2} + 1} } = \sqrt{ \frac{\cancel{ n^{2} }}{\cancel{ n^{2} }\left( 1 + \frac{1}{n^{2}} \right)} } = \sqrt{ \frac{1}{1 + \frac{1}{n^{2}}} } = \frac{1}{\sqrt{ 1 + \frac{1}{n^{2}} }}
$$
Como $\lim_{ n \to \infty } \frac{1}{n^{2}} = 0$:
$$
\lim_{ n \to \infty } \frac{1}{\sqrt{ 1 + \frac{1}{n^{2}} }} = \frac{1}{\sqrt{ 1 }} = \frac{1}{1} = 1
$$


Entonces, conjeturamos que el límite tiene que ser $L = 1$. Lo probamos con la definición:

Sea $\epsilon > 0$, queremos determinar un $n_{0} \in \mathbb{N}$ en base a $\epsilon$ que cumpla que $\forall n \geq n_{0}, a_{n} \in E(L, \epsilon)$, siendo $L = 1$ el límite correspondiente en caso de existir.

$$
\begin{align}
\left| \frac{n}{\sqrt{ n^{2} + 1 }} - L \right| &< \epsilon \\
\left| \frac{n}{\sqrt{ n^{2} + 1 }} - 1 \right| &< \epsilon \\
\left| \frac{1}{\sqrt{ 1 + \frac{1}{n^{2}} }} - 1 \right| &< \epsilon \\
\left| \frac{1}{\sqrt{ 1 + \frac{1}{n^{2}} }} \right| &< \epsilon + 1 \\
\frac{1}{\sqrt{ 1 + \frac{1}{n^{2}} }} &< \epsilon + 1 \\
1 &< (\epsilon + 1)\sqrt{ 1 + \frac{1}{n^{2}} } \\
\frac{1}{(\epsilon + 1)} &< \sqrt{ 1 + \frac{1}{n^{2}} } \\
\frac{1}{\epsilon^{2} + 2\epsilon + 1} &< 1 + \frac{1}{n^{2}} \\
\left| \frac{1}{\epsilon^{2} + 2\epsilon + 1} - 1 \right| &< \frac{1}{n^{2}} \\
\frac{1}{\left| \frac{1}{\epsilon^{2} + 2\epsilon + 1} - 1 \right|} &> n^{2} \\
\sqrt{ \frac{1}{\left| \frac{1}{\epsilon^{2} + 2\epsilon + 1} - 1 \right|} } &> n
\end{align}
$$
ESTE DESARROLLO ES INCORRECTO, A CONTINUACIÓN LA VERSIÓN CORREGIDA:
$$
\begin{align}
\left| \frac{n}{\sqrt{ n^{2} + 1 }} - L \right| &< \epsilon \\
\left| \frac{n}{\sqrt{ n^{2} + 1 }} - 1 \right| &< \epsilon \\
\left| \frac{1}{\sqrt{ 1 + \frac{1}{n^{2}} }} - 1 \right| &< \epsilon \\
1 - \frac{1}{\sqrt{ 1 + \frac{1}{n^{2}} }} &< \epsilon \\
1 - \epsilon &< \frac{1}{\sqrt{ 1 + \frac{1}{n^{2}} }} \\
(1 - \epsilon)^{2} &< \frac{1}{1 + \frac{1}{n^{2}}} \\
1 + \frac{1}{n^{2}} &< \frac{1}{(1 - \epsilon)^{2}} \\
\frac{1}{n^{2}} &< \frac{1}{(1 - \epsilon)^{2}} - 1 = \frac{1 - (1 - \epsilon)^{2}}{(1 - \epsilon)^{2}} = \frac{\epsilon^{2} - 2\epsilon}{(1 - \epsilon)^{2}} = \frac{\epsilon(\epsilon - 2)}{(1 - \epsilon)^{2}} \\
n^{2} &> \frac{(1 - \epsilon)^{2}}{\epsilon(\epsilon - 2)} \\
n &> \frac{1 - \epsilon}{\sqrt{ \epsilon(\epsilon - 2) }}
\end{align}
$$

De esta forma, encontramos un $n_{0} = \frac{1 - \epsilon}{\sqrt{ \epsilon(\epsilon - 2) }}$ tal que $\forall n \geq n_{0}$ se cumple que $a_{n} \in E(1, \epsilon)$

En conclusión, la sucesión converge a 1.

### Parte e
$$
a_{n} = \frac{n^{2}}{2^{n}}
$$
- Monotonía
$$
\begin{align}
\frac{a_{n + 1}}{a_{n}} &= \frac{\frac{(n + 1)^{2}}{2^{n + 1}}}{\frac{n^{2}}{2^{n}}} \\
&= \frac{2^{n}(n + 1)^{2}}{2^{n + 1} \cdot n^{2}} \\
&= \frac{\cancel{ 2^{n} }(n + 1)^{2}}{\cancel{ 2^{n} } \cdot 2 \cdot n^{2}} \\
&= \frac{(n + 1)^{2}}{2 \cdot n^{2}} \\
&= \frac{\sqrt{ (n + 1)^{2} }}{\sqrt{ 2n^{2} }} \\
&= \frac{n + 1}{\sqrt{ 2 }n} \\
&= \frac{\cancel{ n }}{\sqrt{ 2 }\cancel{ n }} + \frac{1}{\sqrt{ 2 }n} \\
&= \frac{1}{\sqrt{ 2 }} + \frac{1}{\sqrt{ 2 }n} < 0
\end{align}
$$
Como $\frac{a_{n + 1}}{a_{n}} > 1$, determinamos que la sucesión es monótona decreciente.

- Convergencia
Sabiendo que la sucesión es monótona decreciente y está acotada, necesariamente converge. Para determinar dicho valor de $L$, primero tenemos que realizar una conjetura:

Analizando la expresión $1 + \frac{1}{n}$ podemos ver que está compuesta por dos elementos:
- La sucesión $n^{2}$ que no converge (tiende a $+\infty$).
- La sucesión $2^{n}$ que no converge (tiende a $+\infty$).

Sin embargo, $2^{n}$ crece más rápidamente que $n^{2}$. Entonces, conjeturamos que el límite tiene que ser $L = 0$. Lo probamos aplicando el teorema del sándwich:

En lugar de $2^{n}$ queremos utilizar una sucesión menor como denominador que nos permita simplificar la expresión. Sabemos que $2^{n}$ crece más rápidamente que cualquier sucesión $n^{\alpha}$, con $\alpha \in \mathbb{N}$. De esta forma, podemos considerar la sucesión $\frac{n^{2}}{n^{3}}$. Además, $\frac{n^{2}}{2^{n}} > 0, \forall n \in \mathbb{N}$. Por lo tanto:
$$
0 < \frac{n^{2}}{2^{n}} \leq \frac{n^{2}}{n^{3}} = \frac{1}{n}
$$
$$
\implies \lim_{ n \to \infty } 0 < \lim_{ n \to \infty } \frac{n^{2}}{2^{n}} \leq \lim_{ n \to \infty } \frac{1}{n} = 0
$$

De esta forma, por el teorema del sándwich logramos probar que la sucesión se encuentra entre dos sucesiones las cuales convergen a 0.

En conclusión, la sucesión converge a 0.

- Acotación
¿Existe $K \in \mathbb{R}$ tal que $|a_{n}| < K, \forall n \in \mathbb{N}$?

Si bien puede ser difícil determinar dicho valor $K$, podemos seguir el siguiente razonamiento lógico:

Se cumple que la sucesión tiene límite $\lim_{ n \to \infty } \frac{n^{2}}{2^{n}} = 0$, por lo tanto, considerando que cualquier sucesión convergente necesariamente está acotada, entonces podemos confirmar que la sucesión $\frac{n^{2}}{2^{n}}$ está acotada.

---
## Ejercicio 2 (anterior)
Sabiendo que $a_{n}$ y $b_{n}$ son sucesiones reales convergentes tal que $\lim_{ n \to \infty } a_{n} = A$ y $\lim_{ n \to \infty } b_{n} = B$, tenemos que probar los enunciados presentados. Para esto, tendremos que aprovechar las diferentes propiedades que posee una sucesión convergente:
- Cumplen con la definición de límite: $\forall \epsilon > 0, \exists n_{0} \in \mathbb{N} \text{ tal que } \forall n \geq n_{0}, |a_{n} - A| < \epsilon$, y el equivalente para $b_{n}$.
- $a_{n}$ y $b_{n}$ están acotadas: $\exists K \in \mathbb{R} \text{ tal que } |a_{n}| \leq K, \forall n \in \mathbb{N}$, y el equivalente para $b_{n}$.

### Parte a
Aplicamos la definición de límite, considerando que $A + B$ es límite de $c_{n} = a_{n} + b_{n}$, buscando encontrar un $n_{0}$ a partir del cual, $\forall n \geq n_{0}, |c_{n} - (A + B)| < \epsilon$:

Consideramos la desigualdad $|a_{n} - A + b_{n} - B| = |a_{n} + b_{n} - A - B| < \epsilon$.

Por desigualdad triangular: $|a_{n} + b_{n} - A - B| < |a_{n} - A| + |b_{n} - B|$. Si logramos probar que $|a_{n} - A| + |b_{n} - B| < \epsilon$, entonces por transitividad, $|a_{n} + b_{n} - A - B| < \epsilon$.

Para esto, analizaremos $|a_{n} - A|$ y $|b_{n} - B|$ por separado, estableciendo un $\epsilon$ adecuado a nuestro beneficio.

Como $a_{n}$ es una sucesión convergente, y $\lim_{ n \to \infty } a_{n} = A$, entonces cumple con la definición de límite. Como se cumple para cualquier $\epsilon > 0$, entonces también se cumple para $\frac{\epsilon}{2}$. Por lo tanto: $\forall \epsilon > 0, \exists n_{1} \in \mathbb{N} \text{ tal que } \forall n \geq n_{1}, |a_{n} - A| < \frac{\epsilon}{2}$.

Análogamente, se cumple para $b_{n}$: $\forall \epsilon > 0, \exists n_{2} \in \mathbb{N} \text{ tal que } \forall n \geq n_{1}, |b_{n} - B| < \frac{\epsilon}{2}$

Ahora, para asegurar que trabajamos en un momento en el que ambas sucesiones se encuentran en los entornos determinados, tomamos $n_{3} = max\{ n_{1}, n_{2} \}$.

De esta forma, podemos asegurar que $c_{n}$ tiene límite:
$$
\forall \epsilon > 0, \exists n_{3} \in \mathbb{N} \text{ tal que } \forall n \geq n_{3}, |a_{n} - A| + |b_{n} - B| < \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon
$$

Ahora, como demostramos que $|a_{n} - A| + |b_{n} - B| < \epsilon$, por transitividad:
$$
|a_{n} + b_{n} - A - B| < |a_{n} - A| + |b_{n} - B| < \epsilon \implies |a_{n} + b_{n} - A - B| < \epsilon
$$

En conclusión:
$$
\lim_{ n \to \infty } c_{n} = \lim_{ n \to \infty } a_{n} + b_{n} = \lim_{ n \to \infty } a_{n} + \lim_{ n \to \infty } b_{n} = A + B
$$

---
## Ejercicio 2
Básicamente, en este ejercicio tenemos que determinar un $n_{0}$ en base a $\epsilon$ a partir del cual se cumple que $\forall n \geq n_{0}, a_{n} \in E(L, \epsilon)$:

### Parte 1
$$
a_{n} = \frac{1}{n}
$$
En base a la forma de la sucesión, consideremos el posible límite $L = 0$:
$$
\begin{align}
|a_{n} - L| &< \epsilon \\
\left| \frac{1}{n} - 0 \right| &< \epsilon \\
\frac{1}{n} &< \epsilon \\
1 &< \epsilon \cdot n \\
\frac{1}{\epsilon} &< n
\end{align}
$$
De esta forma, sabemos que existe $n_{0} > \frac{1}{\epsilon}$ tal que $\forall n \geq n_{0}, \left| \frac{1}{n} - 0 \right| < \epsilon$.

Ahora, determinemos los valores de $n_{0}$ correspondientes a los $\epsilon$ propuestos:
$$
\begin{align}
&\epsilon = 1 \implies \frac{1}{\epsilon} = \frac{1}{1} = 1 \implies n_{0} = 1 + 1 = 2 \\
&\epsilon = 0,1 \implies \frac{1}{\epsilon} = \frac{1}{0,1} = \frac{1}{\frac{1}{10}} = 10 \implies n_{0} = 10 + 1 = 11 \\
&\epsilon = 0,01 \implies \frac{1}{\epsilon} = \frac{1}{0,01} = \frac{1}{\frac{1}{100}} = 100 \implies n_{0} = 100 + 1 = 101
\end{align}
$$

### Parte 2
$$
a_{n} = \frac{n}{n + 1}
$$
En base a la forma de la sucesión, consideremos el posible límite $L = 1$:
$$
\begin{align}
|a_{n} - L| &< \epsilon \\
\left| \frac{n}{n + 1} - 1 \right| &< \epsilon \\
\left| \frac{n - n - 1}{n + 1} \right| &< \epsilon \\
\left| -\frac{1}{n + 1} \right| &< \epsilon \\
\frac{1}{n + 1} &< \epsilon \\
n + 1 &> \frac{1}{\epsilon} \\
n &> \frac{1}{\epsilon} - 1
\end{align}
$$
De esta forma, sabemos que existe $n_{0} > \frac{1}{\epsilon} - 1$ tal que $\forall n \geq n_{0}, \left| \frac{n}{n + 1} - 1 \right| < \epsilon$.

Ahora, determinemos los valores de $n_{0}$ correspondientes a los $\epsilon$ propuestos:
$$
\begin{align}
&\epsilon = 1 \implies \frac{1}{\epsilon} - 1 = \frac{1}{1} - 1 = 0 \implies n_{0} = 0 + 1 = 1 \\
&\epsilon = 0,1 \implies \frac{1}{\epsilon} - 1 = \frac{1}{0,1} - 1 = \frac{1}{\frac{1}{10}} - 1 = 10 - 1 = 9 \implies n_{0} = 9 + 1 = 10 \\
&\epsilon = 0,01 \implies \frac{1}{\epsilon} - 1 = \frac{1}{0,01} - 1 = \frac{1}{\frac{1}{100}} - 1 = 100 - 1 = 99 \implies n_{0} = 99 + 1 = 100
\end{align}
$$
IMPORTANTE: SIEMPRE VERIFICAR QUE ESTEMOS TRABAJANDO CORRECTAMENTE CON EL VALOR ABSOLUTO.

### Parte 3
$$
a_{n} = \frac{(-1)^{n}}{n}
$$
En base a la forma de la sucesión, consideremos el posible límite $L = 0$, ya que:
$$
-\frac{1}{n} \leq \frac{(-1)^{n}}{n} \leq \frac{1}{n} \implies \lim_{ n \to \infty }  -\frac{1}{n} = 0 \leq \lim_{ n \to \infty } \frac{(-1)^{n}}{n} \leq \lim_{ n \to \infty } \frac{1}{n} = 0
$$
$$
\begin{align}
|a_{n} - L| &< \epsilon \\
\left| \frac{(-1)^{n}}{n} - 0 \right| &< \epsilon \\
\left| \frac{(-1)^{n}}{n} \right| &< \epsilon \\
\frac{1^{n}}{n} &< \epsilon \\
\frac{1}{n} &< \epsilon \\
1 &< \epsilon \cdot n \\
\frac{1}{\epsilon} &< n
\end{align}
$$
De esta forma, sabemos que existe $n_{0} > \frac{1}{\epsilon}$ tal que $\forall n \geq n_{0}, \left| \frac{(-1)^{n}}{n} - 0 \right| < \epsilon$.

Ahora, determinemos los valores de $n_{0}$ correspondientes a los $\epsilon$ propuestos:
$$
\begin{align}
&\epsilon = 1 \implies \frac{1}{\epsilon} = \frac{1}{1} = 1 \implies n_{0} = 1 + 1 = 2 \\
&\epsilon = 0,1 \implies \frac{1}{\epsilon} = \frac{1}{0,1} = \frac{1}{\frac{1}{10}} = 10 \implies n_{0} = 10 + 1 = 11 \\
&\epsilon = 0,01 \implies \frac{1}{\epsilon} = \frac{1}{0,01} = \frac{1}{\frac{1}{100}} = 100 \implies n_{0} = 100 + 1 = 101
\end{align}
$$

### Parte 4
$$
a_{n} = \frac{1}{n!}
$$
En base a la forma de la sucesión, consideremos el posible límite $L = 0$:
$$
\begin{align}
|a_{n} - L| &< \epsilon \\
\left| \frac{1}{n!} - 0 \right| &< \epsilon \\
\frac{1}{n!} &< \epsilon \\
1 &< \epsilon \cdot n! \\
\frac{1}{\epsilon} &< n!
\end{align}
$$
De esta forma, sabemos que existe $n_{0}! > \frac{1}{\epsilon}$ tal que $\forall n \geq n_{0}, \left| \frac{1}{n!} - 0 \right| < \epsilon$.
Sin embargo, tenemos que calcular el valor de $n_{0}$ correctamente sin olvidar el factorial.

Ahora, determinemos los valores de $n_{0}$ correspondientes a los $\epsilon$ propuestos:
$$
\begin{align}
&\epsilon = 1 \implies \frac{1}{\epsilon} = \frac{1}{1} = 1 \implies n_{0}! > 1 \implies n_{0} = 2 \\
&\epsilon = 0,1 \implies \frac{1}{\epsilon} = \frac{1}{0,1} = \frac{1}{\frac{1}{10}} = 10 \implies n_{0}! > 10 \implies n_{0} = 4 \\
&\epsilon = 0,01 \implies \frac{1}{\epsilon} = \frac{1}{0,01} = \frac{1}{\frac{1}{100}} = 100 \implies n_{0}! > 100 \implies n_{0} = 5
\end{align}
$$

### Parte 5
$$
a_{n} = \frac{2n}{n^{3} + 1} = \frac{2\cancel{ n }}{\cancel{ n }(n^{2} + 1)} = \frac{2}{n^{2} + 1} = 2 \cdot \frac{1}{n + \frac{1}{n}} \cdot \frac{1}{n}
$$
Ahora, considerando cada uno de los límites anteriores:
$$
\lim_{ n \to \infty } 2 \cdot \frac{1}{n + \frac{1}{n}} \cdot \frac{1}{n} = \lim_{ n \to \infty } 2 \cdot \lim_{ n \to \infty }  \frac{1}{n + \frac{1}{n}} \cdot \lim_{ n \to \infty }  \frac{1}{n} = 2 \cdot 0 \cdot 0 = 0
$$

En base a la forma de la sucesión, consideremos el posible límite $L = 0$:
$$
\begin{align}
|a_{n} - L| &< \epsilon \\
\left| \frac{2n}{n^{3} + 1} - 0 \right| &< \epsilon \\
\frac{2n}{n^{3} + 1} &< \epsilon \\
\frac{2\cancel{ n }}{\cancel{ n }(n^{2} + 1)} &< \epsilon \\
\frac{2}{n^{2} + 1} &< \epsilon \\
\frac{n^{2} + 1}{2} &> \frac{1}{\epsilon} \\
n^{2} + 1 &> \frac{2}{\epsilon} \\
n^{2} &> \frac{2}{\epsilon} - 1 \\
\sqrt{ n^{2} } &> \sqrt{ \frac{2}{\epsilon} - 1 } \\
n &> \sqrt{ \frac{2}{\epsilon} - 1 }
\end{align}
$$
De esta forma, sabemos que existe $n_{0} > \sqrt{ \frac{2}{\epsilon} - 1 }$ tal que $\forall n \geq n_{0}, \left| \frac{2n}{n^{3} + 1} - 0 \right| < \epsilon$.
Las operaciones serán realizadas considerando la desigualdad $n^{2} > \frac{2}{\epsilon} - 1$.

Ahora, determinemos los valores de $n_{0}$ correspondientes a los $\epsilon$ propuestos:
$$
\begin{align}
&\epsilon = 1 \implies \frac{2}{\epsilon} - 1 = \frac{2}{1} - 1 = 2 - 1 = 1 \implies n_{0}^{2} > 1 \implies n_{0} = 2 \\
&\epsilon = 0,1 \implies \frac{2}{\epsilon} - 1 = \frac{2}{0,1} - 1 = \frac{2}{\frac{1}{10}} - 1 = 20 - 1 = 19 \implies n_{0}^{2} > 19 \implies n_{0} = 5 \\
&\epsilon = 0,01 \implies \frac{2}{\epsilon} - 1 = \frac{2}{0,01} - 1 = \frac{2}{\frac{1}{100}} - 1 = 200 - 1 = 199 \implies n_{0}^{2} > 199 \implies n_{0} = 15
\end{align}
$$

---
## Ejercicio 3
### Parte a
$$
a_{n} = \frac{\cos(n)}{n}
$$
Sabemos que la sucesión $a_{n} = \cos(n)$ está acotada: $-1 \leq \cos(n) \leq 1$. Por otra parte, la sucesión $a_{n} = n$ tiende a infinito: $\lim_{ n \to \infty } n = +\infty$. De esta manera, podemos determinar que:
$$
\lim_{ n \to \infty } \frac{-1}{n} \leq \lim_{ n \to \infty } \frac{\cos(n)}{n} \leq \lim_{ n \to \infty } \frac{1}{n}
$$
De esta forma, llegamos a la siguiente conclusión:
$$
\lim_{ n \to \infty } \frac{-1}{n} = \lim_{ n \to \infty } \frac{1}{n} = 0 \implies \lim_{ n \to \infty } \frac{\cos(n)}{n} = 0 
$$

### Parte b
$$
a_{n} = \sqrt{ n + 1 } - \sqrt{ n }
$$
La idea es multiplicar y dividir por el conjugado (estrategia muy utilizada para simplificar problemas con raíces cuadradas):
$$
\sqrt{ n + 1 } - \sqrt{ n } = \frac{(\sqrt{ n + 1 } - \sqrt{ n })(\sqrt{ n + 1 } + \sqrt{ n })}{\sqrt{ n + 1 } + \sqrt{ n }} = \frac{\cancel{ n } + 1 - \cancel{ n }}{\sqrt{ n + 1 } + \sqrt{ n }} = \frac{1}{\sqrt{ n + 1 } + \sqrt{ n }}
$$

Ahora, sabiendo que $\sqrt{ n + 1 } - \sqrt{ n } = \frac{1}{\sqrt{ n + 1 } + \sqrt{ n }}$, la misma igualdad se cumple para los límites:
$$
\lim_{ n \to \infty } \sqrt{ n + 1 } - \sqrt{ n } = \lim_{ n \to \infty } \frac{1}{\sqrt{ n + 1 } + \sqrt{ n }} = \frac{1}{+\infty} = 0
$$

### Parte c
$$
a_{n} = \frac{2n - 5}{n + 3 - 5^{\frac{1}{n}}}
$$
Dividimos toda la expresión por $n$:
$$
\frac{\frac{2n - 5}{n + 3 - 5^{\frac{1}{n}}}}{n} = \frac{\frac{2n - 5}{n}}{\frac{n + 3 - 5^{\frac{1}{n}}}{n}} = \frac{2 - \frac{5}{n}}{1 + \frac{3}{n} - \frac{5^{\frac{1}{n}}}{n}}
$$
Ahora, analizamos cada término por separado:
$$
\begin{align}
\lim_{ n \to \infty } 2 &= 2 \\
\lim_{ n \to \infty } \frac{5}{n} &= 0 \\
\lim_{ n \to \infty } 1 &= 1 \\
\lim_{ n \to \infty } \frac{3}{n} &= 0 \\
\lim_{ n \to \infty } \frac{5^{\frac{1}{n}}}{n} &= \text{?}
\end{align}
$$
$$
\lim_{ n \to \infty } \frac{\exp\left( \log\left( 5 \right) \cdot \frac{1}{n} \right)}{n} = \lim_{ n \to \infty } \frac{e^{\frac{\log(5)}{n}}}{n}
$$
$$
\lim_{ n \to \infty } e^{\frac{\log(5)}{n}} = e^{0} = 1
$$
$$
\implies \lim_{ n \to \infty } \frac{e^{\frac{\log(5)}{n}}}{n} = \lim_{ n \to \infty } \frac{1}{n} = 0
$$

De esta forma:
$$
\lim_{ n \to \infty } \frac{2n - 5}{n + 3 - 5^{\frac{1}{n}}} = \lim_{ n \to \infty } \frac{2 - \frac{5}{n}}{1 + \frac{3}{n} - \frac{5^{\frac{1}{n}}}{n}} = \frac{2 - 0}{1 + 0 - 0} = \frac{2}{1} = 1
$$

### Parte d
$$
a_{n} = \sqrt[n]{ \alpha^{n} + \beta^{n} }, \alpha, \beta \in \mathbb{R}^{+}
$$
Primero, supongamos que $\alpha > \beta$:
$$
\begin{align}
\sqrt[n]{ \alpha^{n} + \beta^{n} } &= (\alpha^{n} + \beta^{n})^{\frac{1}{n}} \\
&= \left( \alpha^{n} \cdot \left( 1 + \frac{\beta^{n}}{\alpha^{n}} \right) \right)^{\frac{1}{n}} \\
&= \alpha^{\frac{n}{n}} \left( 1 + \frac{\beta^{n}}{\alpha^{n}} \right)^{\frac{1}{n}}
\end{align}
$$
Ahora, estudiamos cada factor por separado:
$$
\alpha^{\frac{n}{n}} = \alpha
$$
$$
\begin{align}
\left( 1 + \frac{\beta^{n}}{\alpha^{n}} \right)^{\frac{1}{n}} &= \exp\left( \log\left( 1 + \left( \frac{\beta}{\alpha} \right)^{n} \right)^{\frac{1}{n}} \right) \\
&= \exp\left( \frac{1}{n} \cdot \log\left( 1 + \left( \frac{\beta}{\alpha} \right)^{n} \right) \right) 
\end{align}
$$
$$
\begin{align}
\lim_{ n \to \infty } \frac{1}{n} &= 0 \\
\lim_{ n \to \infty } \left( \frac{\beta}{\alpha} \right)^{n} &= 0 \implies \lim_{ n \to \infty } \log\left( 1 + \left( \frac{\beta}{\alpha} \right)^{n} \right) = \log(1) = 0 \\
\implies \lim_{ n \to \infty } \frac{1}{n} \cdot \log\left( 1 + \left( \frac{\beta}{\alpha} \right)^{n} \right) &= 0 \\
\implies \lim_{ n \to \infty } \exp\left( \frac{1}{n} \cdot \log\left( 1 + \left( \frac{\beta}{\alpha} \right)^{n} \right) \right) &= \exp(0) = 1 
\end{align}
$$

De esta forma, podemos concluir que:
$$
\lim_{ n \to \infty } \sqrt[n]{ \alpha^{n} + \beta^{n} } = \alpha \cdot \exp\left( \frac{1}{n} \cdot \log\left( 1 + \left( \frac{\beta}{\alpha} \right)^{n} \right) \right) = \alpha \qquad (\text{considerando } \alpha > \beta)
$$

Si desarrollamos el mismo camino, considerando $\alpha < \beta$, obtenemos el resultado:
$$
\lim_{ n \to \infty } \sqrt[n]{ \alpha^{n} + \beta^{n} } = \beta \cdot \exp\left( \frac{1}{n} \cdot \log\left( 1 + \left( \frac{\alpha}{\beta} \right)^{n} \right) \right) = \beta \qquad (\text{considerando } \alpha < \beta)
$$

Ahora, ¿Qué sucede en el caso $\alpha = \beta$?

Consideraremos el despeje de $\alpha$ realizado, y volveremos al paso:
$$
\exp\left( \frac{1}{n} \cdot \log\left( 1 + \left( \frac{\beta}{\alpha} \right)^{n} \right) \right)
$$
Aquí, el cociente entre $\alpha$ y $\beta$ es 1:
$$
\begin{align}
\lim_{ n \to \infty } \frac{1}{n} &= 0 \\
\lim_{ n \to \infty } \left( \frac{\beta}{\alpha} \right)^{n} &= 1 \implies \lim_{ n \to \infty } \log\left( 1 + \left( \frac{\beta}{\alpha} \right)^{n} \right) = \log(2) \\
\implies \lim_{ n \to \infty } \frac{1}{n} \cdot \log\left( 1 + \left( \frac{\beta}{\alpha} \right)^{n} \right) &= 0 \\
\implies \lim_{ n \to \infty } \exp\left( \frac{1}{n} \cdot \log\left( 1 + \left( \frac{\beta}{\alpha} \right)^{n} \right) \right) &= \exp(0) = 1 
\end{align}
$$
De esta forma, podemos concluir que:
$$
\lim_{ n \to \infty } \sqrt[n]{ \alpha^{n} + \beta^{n} } = \alpha \cdot \exp\left( \frac{1}{n} \cdot \log\left( 1 + \left( \frac{\beta}{\alpha} \right)^{n} \right) \right) = \alpha = \beta \qquad (\text{considerando } \alpha = \beta)
$$

### Parte e
$$
a_{n} = \sin \left( \frac{1}{n} \right) \cdot \cos(n)
$$
Analicemos cada factor por separado:
$$
\begin{align}
\lim_{ n \to \infty } \sin \left( \frac{1}{n} \right) &= \sin \left( \lim_{ n \to \infty } \frac{1}{n} \right) = \sin(0) = 0 \\
\lim_{ n \to \infty } \cos(n) &= \cos \left( \lim_{ n \to \infty } n \right)
\end{align}
$$
$$
|\cos(n)| \leq 1
$$
Como sabemos el límite de la sucesión $\sin\left( \frac{1}{n} \right)$ es 0 y sabemos que la sucesión $\cos(n)$ está acotada, podemos determinar que:
$$
\lim_{ n \to \infty } \sin \left( \frac{1}{n} \right) \cdot \cos(n) = 0
$$

### Parte f
$$
a_{n} = \frac{n^{\alpha}}{e^{n}}, \alpha \in \mathbb{R}
$$
Tenemos que evaluar tres casos:
- $\alpha = 0$
$$
\lim_{ n \to \infty } \frac{n^{\alpha}}{e^{n}} = \lim_{ n \to \infty } \frac{n^{0}}{e^{n}} = \lim_{ n \to \infty } \frac{1}{e^{n}} = 0
$$
- $\alpha < 0$
$$
\lim_{ n \to \infty } \frac{n^{\alpha}}{e^{n}} = \lim_{ n \to \infty } n^{\alpha} \cdot \frac{1}{e^{n}} = \lim_{ n \to \infty } n^{\alpha} \cdot \lim_{ n \to \infty } \frac{1}{e^{n}}
$$
$$
\lim_{ n \to \infty } n^{\alpha} = \lim_{ n \to \infty } \frac{1}{n^{-\alpha}} = 0
$$
$$
\lim_{ n \to \infty } \frac{1}{e^{n}} = 0
$$
$$
\implies \lim_{ n \to \infty } \frac{n^{\alpha}}{e^{n}} = \lim_{ n \to \infty } n^{\alpha} \cdot \lim_{ n \to \infty } \frac{1}{e^{n}} = 0 \cdot 0 = 0
$$
- $\alpha > 0$
$$
\begin{align}
\lim_{ n \to \infty } \frac{n^{\alpha}}{e^{n}} &= \lim_{ n \to \infty } \exp \left( \log \left( \frac{n^{\alpha}}{e^{n}} \right) \right) \\
&= \lim_{ n \to \infty } \exp \left( \log \left( n^{\alpha} \right) - \log \left( e^{n} \right) \right) \\
&= \lim_{ n \to \infty } \exp \left( \log \left( n^{\alpha} \right) - \log \left( \exp(n) \right) \right) \\
&= \lim_{ n \to \infty } \exp \left( \alpha \cdot \log \left( n \right) - n \right) \\
&= \lim_{ n \to \infty } e^{\alpha \cdot \log \left( n \right) - n} \\
&= \lim_{ n \to \infty } \frac{e^{\alpha \cdot \log \left( n \right)}}{e^{n}}
\end{align}
$$

Aquí, tenemos que comparar los exponentes, y verificar que $\alpha \cdot \log(n) < n$:
$$
\frac{\alpha \cdot \log(n)}{n} = \frac{\alpha \cdot \log(n)}{n}
$$


---
## Ejercicio 4
### Parte a
$$
a_{n} = \frac{1 + (-1)^{n}}{2}
$$
Demostremos que la sucesión no tiene límite:
$$
\begin{align}
|a_{n} - L| &< \epsilon \\
\left| \frac{1 + (-1)^{n}}{2} - L \right| &< \epsilon \\
\left| \frac{1 + (-1)^{n} - 2L}{2} \right| &< \epsilon
\end{align}
$$
Ahora, tenemos que analizar cada caso según si $n$ es par o impar:
- Para $n$ impar: $(-1)^{n} = -1$
$$
\begin{align}
\left| \frac{1 - 1 - 2L}{2} \right| &< \epsilon \\
\left| \frac{-2L}{2} \right| &< \epsilon \\
\left| -L \right| &< \epsilon \\
\left| L \right| &< \epsilon \\
\end{align}
$$
- Para $n$ par: $(-1)^{n} = 1$
$$
\begin{align}
\left| \frac{1 + 1 - 2L}{2} \right| &< \epsilon \\
\left| \frac{2 - 2L}{2} \right| &< \epsilon \\
\left| 1 - L \right| &< \epsilon
\end{align}
$$
En base a la forma de dichas desigualdades, consideramos los puntos 1 y 0, en la siguiente igualdad, la cual utilizaremos para demostrar que la sucesión no tiene límite:
$$
\begin{align}
1 &= |1 - 0| \\
&= |(1 - L) + L| \\
&\leq |1 - L| + |L| \\
&< \epsilon + \epsilon \\
1 &< 2\epsilon \\
\frac{1}{2} &< \epsilon
\end{align}
$$
En base al resultado final, supongamos que la sucesión sí tiene un límite $L$, por lo que la definición de límite debe cumplirse $\forall \epsilon > 0$.
Entonces, si elegimos un $\epsilon \leq \frac{1}{2}$, por ejemplo $\epsilon = \frac{1}{4}$, y aplicamos el desarrollo anterior, llegaríamos a la siguiente desigualdad $\frac{1}{2} < \frac{1}{4}$. También lo podemos pensar como que el valor mínimo para que exista un $n_{0}$ a partir del cual $|a_{n} - L| < \epsilon$ es $\frac{1}{2}$, lo que rompe con lo establecido: $\forall \epsilon > 0$.

Entonces, llegamos a una contradicción matemática absurda, por lo que el supuesto inicial es falso: la sucesión no tiene límite.

Sin embargo, si estudiamos sus subsucesiones, la historia es otra:

Vimos que:
- Para $n$ impar: $(-1)^{n} = -1$
- Para $n$ par: $(-1)^{n} = 1$

De esta forma, podemos distinguir las siguientes subsucesiones:
- $a_{2n} = \frac{1 + (-1)^{2n}}{2}$
Sabemos que $(-1)^{2n} = 1, \forall n \in N$. Por lo tanto:
$$
a_{2n} = \frac{1 + (-1)^{2n}}{2} = \frac{1 + 1}{2} = \frac{2}{2} = 1, \forall n \in \mathbb{N}
$$
Entonces, podemos definir el límite:
$$
\lim_{ n \to \infty } a_{2n} = \lim_{ n \to \infty } \frac{1 + (-1)^{2n}}{2} = \lim_{ n \to \infty } 1 = 1
$$


- $a_{2n + 1} = \frac{1 + (-1)^{2n + 1}}{2}$
Sabemos que $(-1)^{2n + 1} = -1, \forall n \in N$. Por lo tanto:
$$
a_{2n + 1} = \frac{1 + (-1)^{2n + 1}}{2} = \frac{1 - 1}{2} = \frac{0}{2} = 0, \forall n \in \mathbb{N}
$$
Entonces, podemos definir el límite:
$$
\lim_{ n \to \infty } a_{2n + 1} = \lim_{ n \to \infty } \frac{1 + (-1)^{2n + 1}}{2} = \lim_{ n \to \infty } 0 = 0
$$

ACLARACIÓN: SI CONSIDERAMOS SUBSUCESIONES "MULTIPLOS" DE LAS SUBSUCESIONES SELECCIONADAS, EL COMPORTAMIENTO Y LOS LÍMITES SON LOS MISMOS:
- $a_{2n} \sim a_{4n} \sim a_{6n} \dots$
- $a_{2n + 1} \sim a_{4n + 1} \sim a_{6n + 1} \dots$

### Parte b
$$
a_{n} = (-1)^{n}n
$$
Demostremos que la sucesión no tiene límite:
$$
\lim_{ n \to \infty } a_{n} = \lim_{ n \to \infty } (-1)^{n} \cdot n = \lim_{ n \to \infty } (-1)^{n} \cdot \lim_{ n \to \infty } n
$$
Ahora, si estudiamos los límites por separado:
$$
\lim_{ n \to \infty } n = +\infty
$$
$$
\lim_{ n \to \infty } (-1)^{n} = \text{?}
$$
$$
|(-1)^{n} - L| < \epsilon
$$
- Para $n$ impar: $(-1)^{n} = -1$
- Para $n$ par: $(-1)^{n} = 1$

De esta manera, la sucesión oscila infinitamente entre los valores $-1$ y $1$.

Por lo tanto, el producto de ambas funciones no convergerá a ningún valor en particular, ya que, dicho de una forma vulgar, para valores muy grandes de $n$, la función intercalará entre $+\infty$ y $-\infty$ constantemente.

Ahora, podemos analizar sus subsucesiones. Considerando que:
- Para $n$ impar: $(-1)^{n} = -1$
- Para $n$ par: $(-1)^{n} = 1$

Podemos distinguir las siguientes subsucesiones:
- $a_{2n} = (-1)^{2n}2n$
Sabemos que $(-1)^{2n} = 1, \forall n \in N$. Por lo tanto:
$$
a_{2n} = (-1)^{2n}2n = 1 \cdot 2n = 2n, \forall n \in \mathbb{N}
$$
Entonces, podemos definir el límite:
$$
\lim_{ n \to \infty } a_{2n} = \lim_{ n \to \infty } (-1)^{2n}2n = \lim_{ n \to \infty } 2n = +\infty
$$

- $a_{2n + 1} = (-1)^{2n + 1}(2n + 1)$
Sabemos que $(-1)^{2n + 1} = -1, \forall n \in N$. Por lo tanto:
$$
a_{2n + 1} = (-1)^{2n + 1}(2n + 1) = -1 \cdot (2n + 1) = -2n - 1, \forall n \in \mathbb{N}
$$
Entonces, podemos definir el límite:
$$
\lim_{ n \to \infty } a_{2n + 1} = \lim_{ n \to \infty } (-1)^{2n + 1}(2n + 1) = \lim_{ n \to \infty } -2n - 1 = -\lim_{ n \to \infty } 2n - \lim_{ n \to \infty } 1 = -\infty - 1 = -\infty
$$

### Parte c
$$
a_{n} = 3^{\cos(n \pi)}
$$
Primero, analizaremos el exponente para comprender su comportamiento: $\cos(n \pi)$

Sabemos que $\cos(x)$ es una función oscilante. Sin embargo, considerando que el parámetro es la sucesión $n \pi$, la cual está compuesta por múltiplos de $\pi$, el comportamiento del exponente dependerá del valor de $n$:
- $n$ par: $\cos(n \pi) = \cos(0) = 1$
- $n$ impar: $\cos(n \pi) = \cos(\pi) = -1$

De esta manera, la sucesión $a_{n}$ oscilará infinitamente entre dichos valores. Sin embargo, podemos probarlo:
$$
\begin{align}
|a_{n} - L| &< \epsilon \\
\left| 3^{\cos(n \pi)} - L \right| &< \epsilon
\end{align}
$$
Ahora, tenemos que analizar cada caso según si $n$ es par o impar:
- Para $n$ impar: $3^{\cos(n \pi)} = 3^{\cos(\pi)} = 3^{-1} = \frac{1}{3}$
$$
\begin{align}
\left| 3^{-1} - L \right| &< \epsilon \\
\left| \frac{1}{3} - L \right| &< \epsilon \\
\left| L - \frac{1}{3} \right| &< \epsilon
\end{align}
$$
- Para $n$ par: $3^{\cos(n \pi)} = 3^{\cos(0)} = 3^{1} = 3$
$$
\begin{align}
\left| 3^{1} - L \right| &< \epsilon \\
\left| 3 - L \right| &< \epsilon
\end{align}
$$
En base a la forma de dichas desigualdades, consideramos los puntos 3 y 0, en la siguiente igualdad, la cual utilizaremos para demostrar que la sucesión no tiene límite:
$$
\begin{align}
3 &= |3 - \frac{1}{3}| \\
&= \left| (3 - L) + \left( L - \frac{1}{3} \right) \right| \\
&\leq |3 - L| + \left| L - \frac{1}{3} \right| \\
&< \epsilon + \epsilon \\
3 &< 2\epsilon \\
\frac{3}{2} &< \epsilon
\end{align}
$$

En base al resultado final, supongamos que la sucesión sí tiene un límite $L$, por lo que la definición de límite debe cumplirse $\forall \epsilon > 0$.
Entonces, si elegimos un $\epsilon \leq \frac{3}{2}$, por ejemplo $\epsilon = 1$, y aplicamos el desarrollo anterior, llegaríamos a la siguiente desigualdad $\frac{3}{2} < 1$. También lo podemos pensar como que el valor mínimo para que exista un $n_{0}$ a partir del cual $|a_{n} - L| < \epsilon$ es $\frac{3}{2}$, lo que rompe con lo establecido: $\forall \epsilon > 0$.

Entonces, llegamos a una contradicción matemática absurda, por lo que el supuesto inicial es falso: la sucesión no tiene límite.

Igualmente, podemos estudiar sus subsucesiones:

Analizamos cada caso:
- $n$ par: $\cos(n \pi) = \cos(0) = 1$
- $n$ impar: $\cos(n \pi) = \cos(\pi) = -1$

De esta forma, podemos distinguir las siguientes subsucesiones:
- $a_{2n} = 3^{\cos(2n \pi)}$
Sabemos que $\cos(2n \pi) = \cos(0) = 1, \forall n \in N$. Por lo tanto:
$$
a_{2n} = 3^{\cos(2n \pi)} = 3^{\cos(0)} = 3^{1} = 3, \forall n \in \mathbb{N}
$$
Entonces, podemos definir el límite:
$$
\lim_{ n \to \infty } a_{2n} = \lim_{ n \to \infty } 3^{\cos(2n \pi)} = \lim_{ n \to \infty } 3 = 3
$$

- $a_{2n + 1} = 3^{\cos((2n + 1) \pi)}$
Sabemos que $\cos((2n + 1) \pi) = \cos(\pi) = -1, \forall n \in N$. Por lo tanto:
$$
a_{2n} = 3^{\cos((2n + 1) \pi)} = 3^{\cos(\pi)} = 3^{-1} = \frac{1}{3}, \forall n \in \mathbb{N}
$$
Entonces, podemos definir el límite:
$$
\lim_{ n \to \infty } a_{2n} = \lim_{ n \to \infty } 3^{\cos((2n + 1) \pi)} = \lim_{ n \to \infty } \frac{1}{3} = \frac{1}{3}
$$

### Parte d
$$
a_{n} = \frac{n - 1}{n + 1} \cdot \cos\left( \frac{2n \pi}{3} \right)
$$

En este caso, conviene analizar las sucesiones por separado:
$$
\begin{align}
\frac{n - 1}{n + 1} &= \frac{n}{n + 1} - \frac{1}{n + 1} \\
&= \frac{n}{n\left( 1 + \frac{1}{n} \right)} - \frac{1}{n + 1} \\
&= \frac{1}{1 + \frac{1}{n}} - \frac{1}{n + 1}
\end{align}
$$
Ahora, consideramos que:
$$
\begin{align}
\frac{1}{n} > \frac{1}{n + 1} > \frac{1}{n} \cdot \frac{1}{n} &\implies \lim_{ n \to \infty }  \frac{1}{n} > \lim_{ n \to \infty } \frac{1}{n + 1} > \lim_{ n \to \infty } \frac{1}{n} \cdot \lim_{ n \to \infty } \frac{1}{n} \\
&\implies 0 > \lim_{ n \to \infty } \frac{1}{n + 1} > 0 \cdot 0
\end{align}
$$
$$
\implies \lim_{ n \to \infty } \frac{1}{n + 1} = 0
$$
Luego:
$$
\begin{align}
\lim_{ n \to \infty } \frac{1}{1 + \frac{1}{n}} &= \frac{\lim_{ n \to \infty } 1}{\lim_{ n \to \infty } 1 + \frac{1}{n}} \\
&= \frac{\lim_{ n \to \infty } 1}{\lim_{ n \to \infty } 1 + \lim_{ n \to \infty } \frac{1}{n}} \\
&= \frac{1}{1 + 0} \\
&= \frac{1}{1} \\
&= 1
\end{align}
$$

Entonces:
$$
\lim_{ n \to \infty } a_{1_{n}} = \lim_{ n \to \infty }  \frac{n - 1}{n + 1} = \lim_{ n \to \infty } \frac{1}{1 + \frac{1}{n}} - \frac{1}{n + 1} = \lim_{ n \to \infty } \frac{1}{1 + \frac{1}{n}} - \lim_{ n \to \infty } \frac{1}{n + 1} = 1 - 0 = 1
$$

De esta forma, en caso de que la sucesión $\cos\left( \frac{2n \pi}{3} \right)$ converja, podemos determinar el límite. Sin embargo, seguramente no lo haga, ya que $\cos$ es una función oscilante.



---
## Ejercicio 6
En este caso, sabemos que $a_{2n}$, $a_{2n + 1}$ y $a_{3n}$ convergen. El enunciado no establece si convergen a lo mismo o no.

Lo que tenemos que analizar aquí es el comportamiento de las sucesiones establecidas como índices: $2n$, $2n + 1$ y $3n$.

Es interesante ver que elementos comparten:
- $2n = (2, 4, 6, 8, 10, 12, \dots)$
- $2n + 1 = (3, 5, 7, 9, 11, 13, \dots)$
- $3n = (3, 6, 9, 12, 15, 18, \dots)$ (tiene primer elemento de $2n + 1$, tercero de $2n$, cuarto de $2n + 1$, sexto de $2n$, etc.)

Como las tres sucesiones $a_{2n}$, $a_{2n + 1}$ y $a_{3n}$ convergen, entonces verifican que:
- $\forall \epsilon > 0, \exists n_{1} \text{ tal que } \forall n \geq n_{1}, |a_{2n} - L_{1}| < \epsilon$
- $\forall \epsilon > 0, \exists n_{2} \text{ tal que } \forall n \geq n_{2}, |a_{2n + 1} - L_{2}| < \epsilon$
- $\forall \epsilon > 0, \exists n_{3} \text{ tal que } \forall n \geq n_{3}, |a_{3n} - L_{3}| < \epsilon$

A priori no sabemos si $L_{1} = L_{2} = L_{3}$, pero es lo que queremos demostrar para llegar a la conclusión de que, efectivamente, $a_{n}$ es convergente, ya que $2n$ y $2n + 1$ conforman a todos los elementos de $\mathbb{N}$ menos 1 (cosa que no es significativa, ya que el límite se evalúa en $+\infty$). Además, como $3n$ contiene elementos de ambos ($2n$ y $2n + 1$), este será el paso para asegurar que los límites son iguales.

Necesitamos que las tres condiciones se cumplan a la vez, por lo que consideraremos $n_{0} = max\{ n_{1}, n_{2}, n_{3} \}$. De esta forma, sabemos que $|a_{2n} - L_{1}| < \epsilon, |a_{2n + 1} - L_{2}| < \epsilon, |a_{3n} - L_{3}| < \epsilon, \forall n \geq n_{0}$.

Ahora, estando en un entorno en el cual todos los elementos de dichas subsucesiones se encuentra, y sabiendo que $a_{2n}$ y $a_{3n}$ comparten elementos (ya que $2n$ y $3n$ comparten elementos), entonces necesariamente tienen que coincidir en su límite: $L_{1} = L_{3}$. Por el mismo argumento, sabiendo que $a_{2n + 1}$ y $a_{3n}$ comparten elementos, coinciden en su límite: $L_{2} = L_{3}$. Finalmente, por transitividad, los tres límites son iguales:
$$
L_{1} = L_{2} = L_{3} = L
$$

Finalmente, para determinar que $a_{n}$ es convergente y su límite coincide con los anteriores, tenemos que analizar los subíndices anteriores: $2n$ está compuesto por todos los naturales partes, y $2n + 1$ por todos los impares (menos 1). De esta forma, sabemos que tanto la sucesión conformada por todos los naturales pares como la conformada por todos los impares tienen el mismo límite. Por lo tanto, sabemos que la sucesión identidad contiene a los elementos anteriores, y al utilizarla como subíndice, daremos con una sucesión cuyo límite coincide con los anteriores.

En conclusión:
$$
\forall \epsilon > 0, \exists n_{0} \text{ tal que } \forall n \geq n_{0}, |a_{n} - L| < \epsilon
$$

---
## Ejercicio 7
En esta demostración, entra en juego el axioma de completitud de los números reales.

Tenemos un subconjunto $A$ de número reales no vacío y acotado superiormente. Ya que $A$ es
- no vacío
- acotado superiormente

Necesariamente tiene que existir una cota superior que sea menor que el resto: el supremo. Llamemos $L = sup(A)$.

Queremos demostrar que
$(\implies)$
1. $L \geq x, \forall x \in A$.
Por la definición de supremo (la menor de las cotas superiores), $L$ es necesariamente mayor o igual (en caso de que perteneciera al conjunto, siendo también máximo) a todo el resto de elementos del conjunto $A$.

2. Existe $\{ x_{m} \}$ una sucesión de $A$ tal que $\lim_{ m \to +\infty } x_{m} = L$
Esto significa que existe una lista infinita y ordenada de elementos (sucesión) donde todos pertenecen al conjunto $A$, y el límite de dicha sucesión es $L$ (el supremo del conjunto).

Primero que nada, $A$ es un conjunto infinito (ya que si no fuera infinito, no podríamos definir una sucesión en base al mismo, además no se especifica que esté acotado inferiormente, solo superiormente) y acotado (por hipótesis), por lo que tiene al menos un punto de acumulación (por el teorema de Bolzano-Weierstrass).

Como toda sucesión de este estilo contiene únicamente elementos de $A$, entonces todas están acotadas superiormente (ya que el conjunto lo está).

De esta manera, tiene que existir una que sea monótona creciente. Entonces, por teorema, al ser al menos una sucesión monótona creciente y acotada superiormente, entonces tiene límite. Además, como está definida en base a los elementos de $A$, cuyo supremo es $L$, necesariamente el límite de dicha sucesión es $L$:
- Si existe un entorno de $L$ en el conjunto, entonces la sucesión puede aproximarse a $L$ en el infinito.
- Si no existe dicho entorno, pero $L$ está en el conjunto (aislado), entonces existe una sucesión que tome valor $L$ en el infinito.

$(\impliedby)$
Sabemos que $L \geq x, \forall x \in A$. Sin embargo, esto no asegura que $L$ sea supremo, ya que el resto de cotas superiores cumplen la misma condición (sin la posibilidad de ser iguales).

Por esta razón, tenemos que analizar la segunda condición: Existe $\{ x_{m} \}$ una sucesión de $A$ tal que $\lim_{ m \to +\infty } x_{m} = L$

Sabiendo que $L \geq x, \forall x \in A$, y que existe una sucesión conformada por elementos de $A$ que tiene como límite a $L$, existen dos posibilidades:

1. $L$ no pertenece al conjunto: en este caso, para que exista una sucesión que lo tenga como límite, necesariamente se tiene que aproximar a el a menos de $\epsilon$ en $+\infty$ (sin tomarlo como valor). La sucesión sería monótona creciente. Lo importante aquí es que, para que se pueda aproximar infinitamente a $L$, necesariamente tiene que ser supremo, ya que si no lo fuera, existiría una cota superior menor, y dicha cota superior sería el límite en lugar de $L$.
2. $L$ pertenece al conjunto: aquí, $L$ es además máximo, por lo tanto es supremo. Podríamos considerar una sucesión constante $L$, o que tome valor $L$ a $+\infty$.

---
## Ejercicio 8
$(\implies)$
Sabemos que $f$ está acotada, lo que significa que $\exists K \in \mathbb{R}$ tal que $K \geq |f(x)|, \forall x \in \mathbb{R}$.

De esta forma, la sucesión $b_{n} = f(a_{n})$, la cual está conformada por las imágenes de los elementos de $a_{n}$ luego de aplicarles $f$. Por lo tanto:
$$
\begin{align}
&b_{1} = f(a_{1}) \\
&b_{2} = f(a_{2}) \\
&\dots
\end{align}
$$

Como la sucesión $b_{n} = f(a_{n})$ está construida a partir de la función $f$, tratándose de una selección de las imágenes de $f$, entonces necesariamente hereda la misma propiedad: $\exists K \in \mathbb{R}$ tal que $K \geq |f(x)|, \forall x \in \mathbb{R}$.

El valor $K$ puede coincidir o no, dependiendo de $a_{n}$, pero lo importante es que sin importar la sucesión $a_{n}$ tomada, el resultado $b_{n} = f(a_{n})$ siempre está acotado.

$(\impliedby)$
Sabemos que para toda sucesión $a_{n}$, la sucesión $b_{n} = f(a_{n})$ está acotada.

Como $b_{n}$ está acotada, entonces $\exists K \in \mathbb{R}$ tal que $K \geq |b_{n}|, \forall n \in \mathbb{N}$ y para toda sucesión $a_{n}$ (como indica la hipótesis). Esto significa que $K$ es una cota absoluta para todas las variantes posibles de $b_{n}$ considerando diferentes $a_{n}$.

Entonces, como $b_{n}$ está conformado por valores de $f$ (es un subconjunto de las imágenes, pudiendo ser cualquiera), entonces $K$ también es una cota absoluta de $f$.

En conclusión, $f$ está acotada.

---
## Ejercicio 9
- Hipótesis: $a_{n}$ converge a 0.
- Queremos demostrar que: existe $n_{0} \in \mathbb{N}$ tal que $a_{n}^{2} < |a_{n}|$ para todo $n \geq n_{0}$

Queremos llegar a: $|a_{n}^{2} - L| < |a_{n} - L|$, y considerando que $L = 0$: $|a_{n}^{2}| = a_{n}^{2} < |a_{n}|$.

$a_{n}$ converge a 0, lo que significa que
$$
\forall \epsilon > 0, \exists n_{0} \in \mathbb{N} \text{ tal que } \forall n \geq n_{0}, |a_{n} - L| < \epsilon
$$
Sabiendo que $L = 0$:
$$
|a_{n} - L| = |a_{n}| < \epsilon, \forall n \geq n_{0}
$$
Podemos elevar al cuadrado a ambos lados:
$$
|a_{n}^{2}| = a_{n}^{2} < \epsilon^{2}, \forall n \geq n_{0}
$$
Ahora, para probar que existe $n_{0} \in \mathbb{N}$ tal que $a_{n}^{2} < |a_{n}|$ para todo $n \geq n_{0}$, podemos seguir el siguiente razonamiento:

$|a_{n}| < \epsilon, \forall n \geq n_{1}$ y $a_{n}^{2} < \epsilon^{2}, \forall n \geq n_{2}$. Como lo anterior debe ocurrir $\forall \epsilon > 0$, $\exists n_{3} \geq max\{ n_{1}, n_{2} \}$ tal que el $\epsilon$ considerando cumpla $\epsilon < 1$. Por lo tanto, a partir de dicho $n_{3}$ se tiene que cumplir que $|a_{n}| < \epsilon < 1, \forall n \geq n_{3}$ (a partir de $n_{3}$, $|a_{n}|$ se encuentra acotada superiormente por 1, de forma que $|a_{n}| < 1, \forall n \geq n_{3}$), y considerando que $a^{2} < |a|, \forall |a| < 1$, podemos asegurar que $a_{n}^{2} < |a_{n}|, \forall n \geq n_{3}$.

---
## Ejercicio 10
Por hipótesis, sabemos que:
- $a_{n}$ converge a $\alpha \in \mathbb{R}$
- $f : \mathbb{R} \to \mathbb{R}$ es continua en $\alpha$

$a_{n}$ converge a $\alpha \in \mathbb{R}$, por lo que podemos decir que:
- $a_{n}$ es acotada.
- $\forall \epsilon > 0, \exists n_{0} \in \mathbb{N}$ tal que $\forall n \geq n_{0}, |a_{n} - \alpha| < \epsilon$.

Sabiendo esto, podemos afirmar que la sucesión $a_{n}$ se acerca infinitamente a $\alpha$ a menos de $\epsilon$.

Como la función $f$ es continua en $\alpha$, sabemos que
$$
\forall \epsilon > 0, \exists \delta > 0, \forall x \in \mathbb{R}, |x - \alpha| < \delta \implies |f(x) - f(\alpha)| < \epsilon
$$

Ahora, podemos definir la sucesión $b_{n} = f(a_{n})$ y observar si converge a $f(\alpha)$:
¿Se cumple que $\forall \epsilon > 0, \exists n_{0} \in \mathbb{N}$ tal que $\forall n \geq n_{0}, |f(a_{n}) - f(\alpha)| < \epsilon$?
$$
|f(a_{n}) - f(\alpha)| < \epsilon
$$
Para que la condición anterior se cumpla, tenemos que asegurar que el término $a_{n}$ se encuentre en el radio establecido por delta:
$$
\forall \epsilon > 0, \exists \delta > 0, n_{0} \in \mathbb{N}, \forall n \geq n_{0}, |a_{n} - \alpha| < \delta \implies |f(a_{n}) - f(\alpha)| < \epsilon
$$
En este caso, combinamos las dos definiciones para dar lugar a las condiciones necesarias para demostrar que $b_{n}$ converge a $f(\alpha)$. Aquí, $\delta$ juega el papel del $\epsilon$ de la definición de sucesión convergente. Por lo tanto, la condición previa a la implicación se cumple si la sucesión converge.

Sabemos que $|a_{n} - \alpha| < \epsilon$ se cumple $\forall \epsilon > 0$ por hipótesis, por lo que necesariamente $|a_{n} - \alpha| < \delta$ se cumple $\forall \delta > 0$ (aunque basta con que se cumpla para uno). Por lo tanto, se cumplen las condiciones necesarias para que la implicación se verifique:
$$
|f(a_{n}) - f(\alpha)| < \epsilon, \forall \epsilon > 0
$$

De esta forma, llegamos a la condición necesaria que asegura la convergencia de $b_{n}$ a $f(\alpha)$ según la definición de convergencia. Por lo tanto, probamos que $\lim_{ n \to +\infty } b_{n} = f(\alpha)$

ACLARACIÓN: PARA EL PARCIAL, REVISAR TODAS LAS DEMOSTRACIONES CORREGIDAS POR GEMINI NOTEBOOK.







