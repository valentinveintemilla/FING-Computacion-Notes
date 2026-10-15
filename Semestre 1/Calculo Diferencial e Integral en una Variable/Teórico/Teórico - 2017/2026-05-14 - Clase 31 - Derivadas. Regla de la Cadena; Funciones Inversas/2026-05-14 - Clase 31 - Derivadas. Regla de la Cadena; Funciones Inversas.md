# Derivadas
En la instancia anterior vimos como operar con sumas, restas, producto y cociente de derivadas.

## Proposición

> [!Proposición]
> Si $f, g : I \to \mathbb{R}$ son derivables:
> $$
> \begin{align}
> &(f + g)' = f' + g' \\
> &(f - g)' = f' - g' \\
> &(\lambda f)' = \lambda f' &&(\lambda \in \mathbb{R}) \\
> &(fg)' = f'g + fg' \\
> &\left( \frac{f}{g} \right)' = \frac{f'g - fg'}{g^{2}} &&(\text{si } g(x) \neq 0 \qquad \forall x \in I)
> \end{align}
> $$

En base a las igualdades 1 y 3, podemos determinar que la derivada es una transformación lineal.
Además, el espacio de las funciones derivables es un subespacio vectorial de las funciones continuas, que a su vez es un subespacio vectorial de las funciones integrables, que es un subespacio vectorial de las funciones acotadas o localmente acotadas, que finalmente es un subespacio vectorial del espacio de todas las funciones.

Al ser capaces de reconocer esta jerarquización y considerando en que escalón se encuentra cada uno de los teoremas, lemas, proposiciones y corolarios definidos durante el curso. Esto nos permite ==utilizar los teoremas de un escalón para funciones que se encuentran en escalones inferiores==.

## Ejemplos
$$
\begin{align}
&(x^{n})' = n \times x^{n-1} &&(n \geq 1) \\
&C' = 0 &&(C \in \mathbb{R} \text{ constante}) \\
&\log'(x) = \frac{1}{x} &&(\text{si } x > 0) \\
&\cos'(x) = -\sin(x) \\
&\sin'(x) = \cos(x)
\end{align}
$$
También podemos derivar la función $\tan$:
$$
\tan(x) = \left( \frac{\sin(x)}{\cos(x)} \right)' = \frac{\sin'(x)\cos(x) - \sin(x)\cos'(x)}{\cos ^{2}(x)} = \frac{\cos(x)\cos(x) - \sin(x)(-\sin(x))}{\cos ^{2}(x)}
$$
$$
= \frac{\cos ^{2}(x) + \sin ^{2}(x)}{\cos ^{2}(x)} = \frac{1}{\cos ^{2}(x)}
$$
También se puede calcular sin utilizar Pitágoras ($\cos ^{2}(x) + \sin ^{2}(x)$):
$$
= \frac{\cos ^{2}(x) + \sin ^{2}(x)}{\cos ^{2}(x)} = \frac{\cos ^{2}(x)}{\cos ^{2}(x)} + \frac{\sin ^{2}(x)}{\cos ^{2}(x)} = 1 + \tan ^{2}(x)
$$
De esta forma:
$$
\tan'(x) = \frac{1}{\cos ^{2}(x)} = 1 + \tan ^{2}(x)
$$



> [!Observación - Derivada de polinomios]
> Todos los polinomios son derivables, siguiendo la siguiente forma:
> $$
> f(x) = \sum_{i = 0}^{n} a_{i}x^{i} \qquad (\text{polinomio})
> $$
> $$
> \begin{align}
> f'(x) &= \sum_{i = 1}^{n} a_{i} \times i \space x^{i - 1} \\
> &\sum_{i = 0}^{n - 1} (i + 1) a_{i + 1} \space x^{i}
> \end{align}
> $$
> También podemos ver que la derivada un polinomio es otro polinomio de grado menor por 1 (a excepción de un polinomio constante, grado 0, cuya derivada es 0).

> [!Observación - Derivada de fracciones racionales]
> Las fracciones racionales son derivables cuando son definidas (en los casos en los que el denominador no se anula). Simplemente se aplica la fórmula de cociente vista anteriormente.
> La derivada de una fracción entre dos polinomios siempre es una fracción entre dos polinomios.
> $$
> f(x) = \frac{p(x)}{q(x)}
> $$
> $$
> f'(x) = \frac{p'(x)q(x) - p(x)q'(x)}{q^{2}(x)}
> $$

---

Sin embargo, aún no hemos visto como se deriva una compuesta de dos funciones (composición). Para esto, enunciaremos y demostraremos el siguiente teorema:

## Regla de la cadena (derivación de funciones compuestas)

### Proposición #Proposición

> [!Regla de la cadena]
> Sean $f : I \to \mathbb{R}$ y $g : J \to \mathbb{R}$ tales que:
> - $f, g$ son derivables (en $I, J$)
> - $f(I) \subset J (= dom(g))$
> 
> Entonces la función compuesta $g \circ f : I \to \mathbb{R}$ es derivable en $I$, y para todo $x_{0} \in I$:
> $$
> (g \circ f)'(x_{0}) = g'(f(x_{0})) \times f'(x_{0})
> $$

El truco para memorizar la fórmula consiste en utilizar los intervalos como guía: Como $x_{0} \in I$, entonces $f(x_{0})$ está definido, mientras que no sabemos si $g(x_{0})$ lo está. Por esta razón, en lugar de hacer $g(x_{0})$, tomamos $g'(f(x_{0}))$ que sabemos que esta definido, pues $f(x_{0}) \in J$ para que $g \circ f$ esté definido. Al final, nos quedamos con el producto:
$$
(g \circ f)'(x_{0}) = g'(f(x_{0})) \times f'(x_{0})
$$

A continuación demostramos la fórmula:

#### Demostración
Utilizaremos la intuición física durante la demostración.
$$
\begin{align}
&g = g(y) \\
&y = y(x)
\end{align}
$$De esta forma, podemos derivar $g$ respecto a la variable $x$:
$$
\frac{dg}{dx} = \underbrace{ \frac{dg}{dy} }_{ g' \circ f } \times \underbrace{ \frac{dy}{dx} }_{ f' }
$$
Es así que los físicos utilizan implícitamente la regla de la cadena, y utilizaremos esta intuición para demostrar la fórmula anterior. Como vemos, los físicos siguen utilizando notaciones del siglo $XVIII$ (época de Leibniz).

Esto funciona ya que vimos que una derivada es un límite de un cociente, por lo tanto no podemos hacer lo anterior para las derivadas. Sin embargo, si lo podemos hacer para los cocientes incrementales, y es lo que haremos a continuación.

#### Idea
Comenzamos definiendo el cociente incremental. Queremos conocer el límite cuando $x \to x_{0}$. Por ahora estudiaremos el cociente:
$$
\frac{g(f(x)) - g(f(x_{0}))}{x - x_{0}}
$$
$$
= \frac{g(f(x)) - g(f(x_{0}))}{f(x) - f(x_{0})} \times \frac{f(x) - f(x_{0})}{x - x_{0}}
$$
Ahora, si analizamos cada factor por separado:
$$
\underbrace{ \frac{f(x) - f(x_{0})}{x - x_{0}} }_{ \underset{ x \to x_{0} } \to f'(x_{0}) }
$$
Si observamos $\frac{g(f(x)) - g(f(x_{0}))}{f(x) - f(x_{0})}$, podemos ver que es el cociente incremental de $g$ en el punto $f(x_{0})$ compuesto con $f$:
$$
h(y) = \frac{g(y) - g(f(x_{0}))}{y - f(x_{0})} \underbrace{ \longrightarrow }_{ y \to f(x_{0}) } g'(f(x_{0}))
$$
De esta forma:
$$
\underbrace{ \frac{g(f(x)) - g(f(x_{0}))}{f(x) - f(x_{0})} }_{ h(f(x)) }
$$
Es así que, cuando en $x \to x_{0}$
$$
\underbrace{ h(f(x)) }_{ \underset{ x \to x_{0} } \to g'(f(x_{0})) }
$$
En conclusión:
$$
\underbrace{ \frac{g(f(x)) - g(f(x_{0}))}{f(x) - f(x_{0})} }_{ \underset{ x \to x_{0} } \to g'(f(x_{0})) }
$$
$$
\implies \underbrace{ \frac{g(f(x)) - g(f(x_{0}))}{f(x) - f(x_{0})} }_{ \underset{ x \to x_{0} } \to g'(f(x_{0})) } \times \underbrace{ \frac{f(x) - f(x_{0})}{x - x_{0}} }_{ \underset{ x \to x_{0} } \to f'(x_{0}) } = g'(f(x_{0})) \times f'(x_{0})
$$
Sin embargo, esta no es más que una idea para demostrar la fórmula, ya que contiene un error importante: aunque $x - x_{0}$ no es nulo (puesto que nunca manejamos $x = x_{0}$), en el cociente $\frac{g(f(x)) - g(f(x_{0}))}{f(x) - f(x_{0})}$, el denominador $f(x) - f(x_{0})$ puede anularse si la función es localmente constante.

Ahora, desarrollaremos otra demostración que mantiene las mismas ideas. Habrán muchas cosas que parecen salir "de la nada". La idea será evitar los cocientes para no tener problemas como el mencionado anteriormente:

#### Demostración formal
Sean $h : I \to \mathbb{R}$ y $k : J \to \mathbb{R}$ definidas por
$$
h(x) = \begin{cases}
\begin{align}
&\frac{f(x) - f(x_{0})}{x - x_{0}} &&\text{si } x \neq x_{0} \\
&f'(x_{0}) &&\text{si } x = x_{0}
\end{align}
\end{cases}
$$
$$
k(x) = \begin{cases}
\begin{align}
&\frac{g(y) - g(f(x_{0}))}{y - f(x_{0})} &&\text{si } y \neq f(x_{0}) \\
&g'(f(x_{0})) &&\text{si } y = f(x_{0})
\end{align}
\end{cases}
$$

Sabemos que $\frac{f(x) - f(x_{0})}{x - x_{0}}$ está bien definida en $I$, menos para $x = x_{0}$. Sin embargo, sabemos que tiene límite cuando $x \to x_{0}$, entonces podemos extender la definición de la función poniendo el límite como nuevo valor de la función para $x = x_{0}$. Esto se llama extensión por continuidad.
Por la misma razón, $k$ también es continua.

Por construcción: $h : I \to \mathbb{R}$ y $k : J \to \mathbb{R}$ son continuas en sus respectivos intervalos.

Por construcción:
$$
\begin{align}
&f(x) - f(x_{0}) = (x - x_{0})h(x) &&\forall x \in I &&(1) \\
&g(y) - g(f(x_{0})) = (y - f(x_{0}))k(y) &&\forall x \in I &&(2)
\end{align}
$$
(También se cumple para el caso $x = x_{0}$ y $y = f(x_{0})$, ya que se anulan ambos lados.)

Tenemos que
$$
\begin{align}
g(f(x)) - g(f(x_{0})) &= (f(x) - f(x_{0}))k(f(x)) && (\text{por } 1) \\
&= (x - x_{0})h(x)k(f(x)) && (\text{por } 2)
\end{align}
$$

(Ahora, como apareció $x - x_{0}$ podemos escribir el cociente.)

Luego: $\forall x \neq x_{0}$:
$$
\frac{g(f(x)) - g(f(x_{0}))}{x - x_{0}} = \underbrace{ h(x) }_{ \underset{ x \to x_{0} } \to f'(x_{0}) }\underbrace{ k(f(x)) }_{ \underset{ x \to x_{0} } \to g'(f(x_{0})) }
$$
En conclusión:
$$
\frac{g(f(x)) - g(f(x_{0}))}{x - x_{0}} \underbrace{ \longrightarrow }_{ x \to x_{0} } f'(x_{0}) \times g'(f(x_{0}))
$$
De esta forma, evitamos el problema del cociente utilizando la extensión por continuidad a la hora de definir las funciones.

---
Proseguiremos a tratar las funciones inversas.

## Funciones inversas

### Marco

> [!Marco]
> Sea $f : I \to \mathbb{R}$ continua y estrictamente creciente o decreciente.
> 
> Ya vimos que:
> - la función $f$ es inyectiva y establece una biyección entre $I$ y su imagen $J := f(I)$
> - $J$ es un intervalo (por Bolzano)
> - la función inversa $f^{-1} J \to \mathbb{R}$ es continua.

### Proposición

> [!Proposición]
> Si $f : I \to \mathbb{R}$ es:
> - estrictamente creciente (decreciente) en $I$
> - derivable en $I$
> - su derivada no se anula en $I$: $f'(x) \neq 0$
> 
> Entonces, la función inversa $f^{-1} : J \to \mathbb{R}$ (con $J = f(I)$) es derivable en $J$ y
> $$
> (f^{-1})'(y) = \frac{1}{f'(f^{-1}(y))} \qquad \forall y \in J
> $$

No es necesario memorizar esta formula, ya que se puede deducir a partir de la fórmula de la cadena:
$$
\begin{align}
(\underbrace{ f \circ f^{-1} }_{ \text{Identidad} })'(y) &= f'(f^{-1}(y)) \times (f^{-1})'(u) \\
1 &= f'(f^{-1}(y)) \times (f^{-1})'(u)
\end{align}
$$
$$
\implies (f^{-1})'(u) = \frac{1}{f'(f^{-1}(y))}
$$
Esto lo desarrollamos sabiendo que $f \circ f^{-1} = \text{Identidad}$ en todos los casos, y la derivada de la identidad es 1.

Otro ejemplo de que no es necesario memorizar las formulas, simplemente entender de donde salen y cual es el razonamiento detrás de las mismas.

Esta fórmula se demuestra en base al mismo argumento: la intuición física.

#### Demostración
Sean $y_{0} \in J$ y $x_{0} \in f^{-1}(y_{0}) \in I$.

Sea $h : I \to \mathbb{R}$ definida por
$$
h(x) = \begin{cases}
\begin{align}
&\frac{x - x_{0}}{f(x) - f(x_{0})} &&\text{si } x \neq x_{0} \\
&\frac{1}{(f)'(x_{0})} &&\text{si } x = x_{0}
\end{align}
\end{cases}
$$

Aclaración:

$$
\frac{f(x) - f(x_{0})}{x - x_{0}} \underbrace{ \longrightarrow }_{ x \to x_{0} } f'(x_{0}) \implies \frac{x - x_{0}}{f(x) - f(x_{0})} \underbrace{ \longrightarrow }_{ x \to x_{0} } \frac{1}{f'(x_{0})}
$$

Por construcción: $h : I \to \mathbb{R}$ es continua, entonces $h \circ f^{-1} : J \to \mathbb{R}$ es continua
$$
\forall y \neq f(x_{0}) \qquad f^{-1}(y) \neq x_{0}
$$
$$
\begin{align}
h \circ f^{-1}(y) &= \frac{f^{-1}(y) - \overbrace{ x_{0} }^{ f^{-1}(y_{0}) }}{\underbrace{ f(f^{-1}(y)) }_{ y } - \underbrace{ f(x_{0}) }_{ y_{0} }} \\
&= \frac{f^{-1}(y) - f^{-1}(y_{0})}{y - y_{0}}
\end{align}
$$
De esta forma, llegamos al cociente incremental. Además, como $h$ y $f^{-1}$ son funciones continuas:
$$
h \circ f^{-1}(y) \underbrace{ \longrightarrow }_{ y \to y_{0} } h(f^{-1}(y_{0})) = h(x_{0}) = \frac{1}{f'(x_{0})} = \frac{1}{f'(f^{-1}(y_{0}))}
$$
De esta forma, demostramos que el coeficiente incremental tiene límite, y el límite equivale a $\frac{1}{f'(f^{-1}(y_{0}))}$.

En conclusión:
$$
\frac{1}{f'(f^{-1}(y_{0}))} = (f^{-1})'(y0)
$$

A continuación, veremos un ejemplo de porque no es suficiente decir que la función sea derivable para que su inversa también lo sea. También es necesario que su derivada no se anule.

#### Contraejemplo
$f(x) = x^{3}$ en $\mathbb{R}$ y es estrictamente creciente en $\mathbb{R}$.

Tenemos que
$$
f^{-1}(y) = \sqrt[3]{ y }
$$
$$
f'(x) = 3x^{2} \geq 0
$$
Al tener un punto en el que $f'(x) = 0$ ($x = 0$), la función $f^{-1}(y) = \sqrt[3]{ y }$ no es derivable.

Si observamos la gráfica, podemos ver que $f'(x) = 0$, pero $(f^{-1})'(0) = \text{"} \frac{1}{0} = +\infty \text{"}$. Aquí, la pendiente tiende tangente infinita (vertical).

De esta forma, podemos aplicar el teorema en cualquier intervalo que no contenga a 0: la función $f^{-1}(y) = \sqrt[3]{ y }$ es derivable en cualquier intervalo que no contenga a 0.

Podemos decir que "la pendiente se invierte".

En la próxima clase abordaremos ejemplos.