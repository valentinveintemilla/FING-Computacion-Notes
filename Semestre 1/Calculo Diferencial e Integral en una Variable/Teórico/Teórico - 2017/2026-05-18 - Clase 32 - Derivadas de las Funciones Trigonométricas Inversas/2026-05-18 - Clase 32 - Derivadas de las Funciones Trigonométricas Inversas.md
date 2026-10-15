# Derivadas
Durante la clase pasada, abordamos la derivación de funciones inversas.

## Funciones inversas

> [!Proposición]
> Sea $f : I : \mathbb{R}$ una función tal que:
> - $f$ es estrictamente creciente o decreciente en I
> - $f$ es derivable en $I$
> - $f'(x) \neq 0 \qquad \forall x \in I$
> 
> La función inversa $f^{-1} : J \to \mathbb{R}$ (donde $J = f(I)$) es derivable en $J$ y:
> $$
> (f^{-1})'(y) = \frac{1}{f'(f^{-1}(y))}
> $$

Al ser estrictamente creciente o decreciente, sabemos que es inyectiva, por lo que define una biyección entre el intervalo $I$ y su imagen. Además, como es derivable en $I$, es continua en $I$, por lo que sabemos que la imagen del intervalo $I$ también es un intervalo (por Bolzano), y esto implica que la función inversa también es continua.

### Ejemplos

#### Ejemplo 1
Comenzaremos estudiando la función exponencial.

Sea $f(x) = \log(x)$ en $\mathbb{R}^{+} = (0 + \infty)$.
- Ya vimos que $\log$ es estrictamente creciente en $\mathbb{R}^{+}$ y define una biyección entre $\mathbb{R}^{+}$ y $\mathbb{R}$ cuya inversa es la función exponencial $\exp : \mathbb{R} \to \mathbb{R}^{+}$. También sabemos que es continua, puesto que $\log$ es continua.
- Además:
$$
\log'(x) = \frac{1}{x} > 0 \qquad \forall x \in \mathbb{R}^{+}
$$
Entonces, la función $\exp = \log ^{-1} : \mathbb{R} \to \mathbb{R}^{+}$ es derivable y:
$$
\exp'(x) = (\log ^{-1})'(x) = \frac{1}{\log'(\exp(x))} = \frac{1}{\frac{1}{\exp x}} = \exp x
$$ De esta forma, la derivada de $\exp x$ es $\exp x$.

Este es el ejemplo de base, pudiendo explorar otros a partir de este.

A continuación, abordaremos la derivada de la potencia generalizada (tomando como referencia la derivada anterior).

> [!Observación]
> Dado $\alpha \in \mathbb{R}$. se define 
> $$
> f(x) = x^{\alpha} = e^{\alpha \log x} \qquad (\text{si } x > 0)
> $$
> Entonces:
> $$
> \begin{align}
> (x^{\alpha})' &= \exp'(\alpha \log x) \times (\alpha \log x)' = \exp(\alpha \log x) \times \frac{\alpha}{x} \\
> &= x^{\alpha} \times \frac{\alpha}{x} = \alpha \times x^{\alpha} \times x^{-1} = \alpha x^{\alpha - 1} \qquad (\text{si } x > 0)
> \end{align}
> $$

De esta forma, obtuvimos la misma fórmula que habíamos determinado anteriormente, pero en base a la función exponencial (siempre y cuando $x > 0$). Este nuevo resultado se generaliza al caso en el que la potencia no es un entero.

Podemos ver que, gracias a esto podemos derivar la raíz cuadrada, raíz n-ésima (generalización).
Para hacerlo tenemos dos estrategias:
1. Observar que la raíz n-ésima es la inversa de la función $x^{n}$ y aplicar la fórmula de funciones inversas.
2. Considerar que la raíz n-ésima es equivalente a $x^{\frac{1}{n}}$.

Ambos métodos llevan a la misma fórmula.


$$
f(x) = \sqrt[n]{ x } = x^{\frac{1}{n}} \qquad (\text{si } x > 0)
$$
$$
f'(x) = \frac{1}{n} x^{\frac{1}{n} - 1} = \frac{1}{n} x^{\frac{1 - n}{n}} = \frac{1}{n(\sqrt[n]{ x })^{n - 1}}
$$

Caso particular $n = 2$:
$$
f(x) = \sqrt{ x } = x^{\frac{1}{2}}
$$
$$
f'(x) = \frac{1}{2} x^{-\frac{1}{2}} = \frac{1}{2\sqrt{ x }}
$$
Todo esto funciona $\forall x > 0$.
No funciona para el caso $x = 0$, ya que en el punto 0, la función raíz n-ésima no es derivable, ya que tiene pendiente infinita.

En el caso en el que $n$ es impar, la raíz n-ésima está definida en todo $\mathbb{R}$. En este caso, se puede demostrar que es derivable en todo $\mathbb{R}$ salvo en 0, y es la misma fórmula.

También se puede observar en la fórmula, si $x = 0$:
$$
\frac{1}{n(\sqrt[n]{ x })^{n - 1}} = \frac{1}{n(\sqrt[n]{ 0 })^{n - 1}} = \frac{1}{0}
$$

La única formula necesaria es:
$$
f'(x) = \frac{1}{n} x^{\frac{1}{n} - 1}
$$

Como vemos, todas estas derivadas surgen del teorema de las funciones inversas. Ahora, pasaremos a estudiar las funciones inversas de las funciones trigonométricas: $\arcsin, \arccos, \arctan$.
#### Ejemplo 1
Sabemos que la función seno es oscilante (no es creciente ni decreciente). Por lo tanto, consideraremos un trozo de dicha función en el cual sea creciente o decreciente. Analizando el gráfico y comportamiento de la función, estudiaremos el trozo que se encuentra en el intervalo $\left[ -\frac{\pi}{2}, \frac{\pi}{2} \right]$, donde es estrictamente creciente.
También se puede considerar otro intervalo con el mismo comportamiento, o en el cual sea estrictamente decreciente.

Sea $f(x) = \sin(x)$ en $I = \left[ -\frac{\pi}{2}, \frac{\pi}{2} \right]$

$f$ es estrictamente creciente en $I = \left[ -\frac{\pi}{2}, \frac{\pi}{2} \right]$, entonces define una biyección entre $I$ y su imagen $f(I) = [-1, 1]$.

Sea $\arcsin := f^{-1} : [-1, 1] \to \left[ -\frac{\pi}{2}, \frac{\pi}{2} \right]$
$\arcsin$ es continua en $[-1, 1]$.

![[1 - Función arcsen.png]]

(Ya que la función $\sin$ tiene pendiente 0 en $-\frac{\pi}{2}$ y $\frac{\pi}{2}$, la función $\arcsin$ tiene pendiente infinita en $-1$ y $1$. Por esta razón, la función no es derivable en dichos puntos, por lo que los excluiremos del intervalo analizado. Para realizar un trato equivalente en la función $\sin$, excluimos los extremos del intervalo, aunque la función $\sin$ es derivable).

**Función seno**
$$
\forall x \in \left( -\frac{\pi}{2}, \frac{\pi}{2} \right), f'(x) = \cos(x) > 0 \qquad \text{(derivada de seno)}
$$

**Función arcoseno**
$$
\forall x \in \left( -1, 1 \right), \arcsin'(x) = \frac{1}{\sin'(\arcsin x)} \qquad \text{(derivada de arcoseno)}
$$
(En base a la fórmula de la derivada de una función inversa.)
$$
= \frac{1}{\cos(\arcsin x)}
$$
Sabemos que $\cos ^{2}x = 1 - \sin ^{2}x$. Sin embargo, como sabemos que $\cos > 0$ en el intervalo considerado, podemos considerar $\cos x = \sqrt{ 1 - \sin ^{2} x }$
$$
= \frac{1}{\sqrt{ 1 - \sin ^{2}(\arcsin x) }}
$$
Como $\arcsin$ aplicado a $\sin$ corresponde a la identidad (puesto que equivale a $f \circ f^{-1} = f(f^{-1}(x))$), y considerando que $\sin ^{2}(\alpha) = (\sin \alpha)^{2}$:
$$
= \frac{1}{\sqrt{ 1 - x^{2} }} \qquad \forall x \in (-1, 1)
$$
La idea es ser capaz de entender de donde salen dichas formulas, con tal de poder desarrollar rápidamente dichos razonamientos cuando necesitamos utilizarlas (y así evitar depender de la memoria).

También podemos darnos cuenta a la hora de analizar la fórmula cual es la causa de que la función $\arcsin$ no sea derivable para $x = \pm 1$.

Pasamos a estudiar la función $\arccos$:
#### Ejemplo 3
$$
f(x) = \cos x \text{ en } I = [0, \pi]
$$
$f$ es estrictamente decreciente en $I = [0, \pi]$ y define una biyección entre $I$ y $f(I) = [-1, 1]$ cuya función inversa se escribe
$$
\arccos := f^{-1} : [-1, 1] \to [0, \pi]
$$
![[2 - Función arccos.png]]

$\arccos$ es estrictamente decreciente y continua en $[-1, 1]$.
(Igual que al caso anterior, como tenemos un problema de pendientes infinitos, tenemos que restringir el intervalo.)

Solo es derivable en $(-1, 1)$

**Función arco coseno**
$$
\arccos'(x) = \frac{1}{\cos'(\arccos x)}
$$
$$
= - \frac{1}{\sin(\arccos x)}
$$
Aquí también podemos aprovechar la fórmula $\sin ^{2}x = 1 - \cos ^{2}x$, puesto que como $\sin x > 0$ en el intervalo establecido, podemos considerar $\sin x = \sqrt{ 1 - \cos ^{2} x }$
$$
= - \frac{1}{\sqrt{ 1 - \cos ^{2}(\arccos x) }}
$$
Como en el caso anterior, $\arccos$ aplicado a $\cos$ corresponde a la identidad (puesto que equivale a $f \circ f^{-1} = f(f^{-1}(x))$), y considerando que $\cos ^{2}(\alpha) = (\cos \alpha)^{2}$:
$$
= - \frac{1}{\sqrt{ 1 - x^{2} }}
$$

En conclusión, podemos deducir que si sumamos $\arcsin$ y $\arccos$, obtenemos una función cuya derivada es nula (puesto que si sumamos las derivadas obtenemos 0). Por esta razón, la suma de ambas es una función constante: $\arcsin x + \arccos x = \frac{\pi}{2}$. Es algo que se puede prever en base al comportamiento de $\sin$ y $\cos$ y su relación con $\frac{\pi}{2}$.

Son funciones sumamente útiles para calcular valores de $\sin$ y $\cos$ fácilmente (utilizando las fórmulas de las derivadas).

Continuamos estudiando la última función trigonométrica inversa, $\arctan$:
#### Ejemplo 4
$$
f(x) = \tan x \text{ en } \left( -\frac{\pi}{2}, \frac{\pi}{2} \right)
$$
Sea
$$
\arctan := f^{-1} : \mathbb{R} \to \left( -\frac{\pi}{2}, \frac{\pi}{2} \right)
$$

![[3 - Función arctan.png]]

No seguiremos dando especificaciones como las que venimos dando, ya muchas se intuyen de la representación (la función es estrictamente creciente, $\tan ^{2}(\alpha) = (\tan \alpha)^{2}$, entre otras cosas).

Tenemos que $f'(x) = 1 + \tan ^{2}(x) > 1$
(Siempre es positiva, ya que el cuadrado de un numero real nunca será menor que 0.)

Luego:
$$
\arctan'(x) = \frac{1}{\tan'(\arctan x)} = \frac{1}{1 + \tan ^{2}(\arctan x)} = \frac{1}{1 + x^{2}}
$$

La función $\arctan$ es quizás la función trigonométrica inversa más importante, fundamental históricamente hablando: es la función que nos permitió calcular el número $\pi$.

Primeramente, sus propiedades se deducen por inversa de las propiedades de $\tan$.

$$
\tan\left( \frac{\pi}{4} \right) = 1 \implies \arctan(1) = \frac{\pi}{4}
$$
De esta forma, si se calcular $\arctan$, se calcular $\pi$

Considerando las series (tema que aún no hemos abordado, pero consiste en una sumatoria infinita), tenemos una forma de determinar $\pi$:
$$
\arctan(x) = \sum_{n = 0}^{\infty} \frac{(-1)^{n}}{2n + 1} x^{2n + 1} \qquad x \in [-1, 1]
$$
Entonces:
$$
\frac{\pi}{4} = \sum_{n = 0}^{\infty} \frac{(-1)^{n}}{2n + 1} = 1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + \frac{1}{9} - \dots
$$
Sin embargo, este método es sumamente ineficiente.

Existen formas de acelerar la convergencia de la serie:

> [!Recordatorio]
> $$
> \tan(\alpha + \beta) = \frac{\overbrace{ \tan(\alpha) }^{ x } + \overbrace{ \tan(\beta) }^{ y }}{1 - \underbrace{ \tan(\alpha) \tan (\beta) }_{ xy }}
> $$

La fórmula anterior se puede transformar en una formula similar para $\arctan$:
$$
\arctan x + \arctan y = \arctan\left( \frac{x + y}{1 - xy} \right)
$$

Ahora, el truco consiste en encontrar valores de $x$ e $y$ para los cuales $\frac{x + y}{1 - xy} = 1$, por ejemplo:
$$
\arctan \frac{1}{2} + \arctan \frac{1}{3} = \arctan \left( \frac{\frac{1}{2} + \frac{1}{3}}{1 - \frac{1}{2} \times \frac{1}{3}} \right) = \arctan \left( \frac{\frac{5}{6}}{\frac{5}{6}} \right) = \frac{\pi}{4}
$$
Entonces:
$$
\frac{\pi}{4} = \arctan \frac{1}{2} + \arctan \frac{1}{3}
$$
(Ahora, podemos usar la serie anterior 2 veces: para $\frac{1}{2}$ y para $\frac{1}{3}$.)
$$
= \sum_{n = 0}^{\infty} \frac{(-1)^{n}}{(2n + 1) 2^{n}} + \sum_{n = 0}^{\infty} \frac{(-1)^{n}}{(2n + 1) 3^{n}}
$$
Es así que con este método se obtienen dígitos de $\pi$ más rápidamente a medida que indagamos en la serie.

Hasta ahora, la fórmula más sencilla y efectiva que conocemos para calcular $\pi$ es:
$$
\frac{\pi}{4} = 4 \arctan \frac{1}{5} - \arctan \frac{1}{239}
$$
Entonces:
$$
= 4 \sum_{n = 0}^{\infty} \frac{(-1)^{n}}{(2n + 1) 5^{n}} - \sum_{n = 0}^{\infty} \frac{(-1)^{n}}{(2n + 1) 239^{n}}
$$
Históricamente fue determinada por John Machin, logrando calcular los 100 primeros dígitos de $\pi$ a mano y con una precisión exacta (teniendo errores posteriormente).

La serie definida será demostrada con desarrollo de Taylor.

En la próxima clase, abordaremos el tema "extremos relativos".