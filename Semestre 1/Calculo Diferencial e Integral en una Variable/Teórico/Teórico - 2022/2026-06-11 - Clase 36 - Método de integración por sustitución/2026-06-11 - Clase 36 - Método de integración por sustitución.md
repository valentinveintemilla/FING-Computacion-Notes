# Método de integración por sustitución

En esta ocasión, abordaremos un nuevo método de integración: Integración por sustitución (o cambio de variable).

Es el otro método de integración importante, aparte de la integración por partes.

En el caso de la integración por partes era una consecuencia de la regla de Leibniz para la derivada del producto de dos funciones, la integración por sustitución es una consecuencia de la regla de la cadena (funciones compuestas).

## Fórmula de integración por sustitución

El contexto es el mismo de siempre: $f$ es una función continua, $g$ es una función derivable (con derivada continua).

La fórmula es la siguiente:

> [!Fórmula de integración por sustitución]
> $$
> \int f(g(x)) \cdot g'(x) \space dx = F(g(x)) + c
> $$
> donde $F$ es una primitiva de $f$ (es decir $F' = f$).

Podemos enunciar una versión definida de la fórmula de integración por sustitución, la cual indica como calcular la integral de la función mencionada en un intervalo dado:

> [!Fórmula de integración por sustitución (versión definida)]
> $$
> \int_{a}^{b} f(g(x)) \cdot g'(x) \space dx \underset{\text{por Barrow}} = F(g(x)) |_{a}^{b} = F(g(b)) - F(g(a)) = \left. F(x) \right|_{g(a)}^{g(b)} = \int_{g(a)}^{g(b)} f(x) \space dx
> $$
> En definitiva:
> $$
> \int_{a}^{b} f(g(x)) \cdot g'(x) \space dx = \int_{g(a)}^{g(b)} f(x) \space dx
> $$

Lo que hicimos fue aprovechar la notación $f(x)_{a}^{b}$ para simplificar la expresión, y llegar a una expresión aún más sencilla que la inicial.

En definitiva, lo importante es visualizar que $F$ es una primitiva de $f$, lo que quiere decir que $(F(g(x)))' = F'(g(x)) \cdot g'(x) = f(g(x)) \cdot g'(x)$.

Este mismo razonamiento es el que nos lleva a fórmulas para la integral definida como la vista previamente.

Ahora, veremos una serie de ejemplos (comenzando por la versión definida):

### Ejemplos
#### Ejemplo 1
$$
\int_{0}^{\frac{\pi}{2}} \sin ^{2}(x) \cdot \cos(x) \space dx
$$
Lo primero es reconocer la forma de la función que estamos integrando cuando podemos usar la fórmula de integración por sustitución.
$$
(\sin(x))^{2} \cdot \cos(x)
$$
Si estudiamos la función, reconocemos que tiene la forma:
$$
(\sin(x))^{2} \cdot \cos(x) = f(g(x)) \cdot g'(x)
$$
donde
$$
\begin{align}
&f = x^{2} \\
&g = \sin(x) \implies g' = \cos(x)
\end{align}
$$

De esta forma, podemos ver que existe una $g$, la cual aparece una vez compuesta (con $x^{2}$), y luego derivada, pasando a ser $\cos(x)$. Esta función $g$ es $\sin(x)$.

Ahora que sabemos cual es la fórmula, si queremos estudiar una integral definida (como es el caso), simplemente lo expresamos en base a la fórmula anterior (versión definida):
$$
\int_{0}^{\frac{\pi}{2}} \sin ^{2}(x) \cdot \cos(x) \space dx = \int_{\sin(0)}^{\sin\left( \frac{\pi}{2} \right)} x^{2} \space dx
$$
De esta forma, comenzamos queriendo calcular la integral $\int_{0}^{\frac{\pi}{2}} \sin ^{2}(x) \cdot \cos(x) \space dx$, y tomando como referencia la expresión $\int_{a}^{b} f(g(x)) \cdot g'(x) \space dx = \int_{g(a)}^{g(b)} f(x) \space dx$, así como analizando cuidadosamente la función que se estaba integrando para entender la equivalencia y quienes serían $f$ y $g$, primitivizando $f$, logramos reducir el problema a calcular la integral $\int_{\sin(0)}^{\sin\left( \frac{\pi}{2} \right)} x^{2} \space dx$, la cual es una función bien conocida.

Ahora, determinamos una integral en la que simplemente tenemos que encontrar una primitiva de $f$, en este caso $x^{2}$, aplicando Barrow para concluir:
$$
\int_{0}^{\frac{\pi}{2}} \sin ^{2}(x) \cdot \cos(x) \space dx = \int_{\sin(0)}^{\sin\left( \frac{\pi}{2} \right)} x^{2} \space dx \underset{\text{por Barrow}} = \left. \frac{x^{3}}{3} \right|_{\sin(0)}^{\sin\left( \frac{\pi}{2} \right)} = \frac{1^{3}}{3} - \frac{0^{3}}{3} = \frac{1}{3}
$$

Lo principal al aplicar este método es reconocer que la función que queremos integrar tiene la forma adecuada. En este caso, estudiando la expresión, notamos que $\sin ^{2}(x) = (\sin(x))^{2}$, lo que es una función compuesta:
$$
x \overset{g} \mapsto \sin(x) \overset{f} \mapsto (\sin(x)^{2})
$$
De esta forma, la primer modificación que se le aplica a $x$ es la función $g$, mientras que el segundo cambio, aplicado sobre el primero, es la función $f$. Básicamente es la composición de dos funciones, siendo el resultado $f(g(x))$.

En conclusión, al tener una integral de una función, cuya forma se puede estudiar como $f(g(x)) \cdot g'(x)$, el problema se reduce a reconocer cuales son las funciones $f$, $g$ y $g'$ (lo mejor es realizar un diagrama para no perderse) y encontrar una primitiva de $f$, a la cual denotamos $F$ (para poder aplicar Barrow y calcular el valor de la integral).

También podríamos haberlo resuelto de esta forma (en base a la versión no definida):
$$
\int \sin ^{2}(x) \cdot \cos(x) \space dx
$$
$$
\begin{align}
&f = x^{2} \implies F(x) = \frac{x^{3}}{3} \text{ es una primitiva de } f \\
&g = \sin(x)
\end{align}
$$
De esta forma:
$$
\int \sin ^{2}(x) \cdot \cos(x) \space dx = \frac{(\sin(x))^{3}}{3} + c
$$
Podemos comprobarlo, derivando $F(g(x))$:
$$
\left( \frac{(\sin(x))^{3}}{3} \right)' = \frac{\cancel{ 3 } \cdot (\sin(x))^{2} \cdot \cos(x)}{\cancel{ 3 }} = (\sin(x))^{2} \cdot \cos(x)
$$
Así, confirmamos que el resultado es correcto.

Este tipo de problemas también se puede resolver tomando un enfoque nemotécnico.
$$
\int (\sin(x))^{2} \cdot \cos(x) \space dx
$$
Primero, reconocemos la función $g$. Aquí, $g = \sin(x)$, puesto que aparece $g' = \cos(x) = (\sin(x))'$ (básicamente buscamos que haya una función y su derivada, $g$ y $g'$). Entonces, realizaremos un cambio de variable, denotando $u = g = \sin(x)$ y su derivada $du = g' = \cos(x) \space dx$. Este es un tema más bien notacional y formal, pero si efectivamente identificamos correctamente a las funciones, cuando sustituyamos ambas por su nueva denominación, vamos a haber simplificado sumamente el problema inicial:
$$
\int (\underbrace{ \sin(x) }_{ g })^{2} \cdot \underbrace{ \cos(x) }_{ g' } \space dx \underset{\begin{align}
&u = \sin(x) \\
&du = \cos(x) \space dx
\end{align}} = \int \underbrace{ u^{2} }_{ f(u) } du = \underbrace{ \frac{u^{3}}{3} }_{ F(u) } + c = \underbrace{ \frac{(\sin(x))^{3}}{3}}_{ F(g(x)) } + c
$$
En este caso $f(u) = u^{2}$, pasando de la expresión $\int (\sin(x))^{2} \cdot \cos(x) \space dx$, a una muchísimo más simple $\int u^{2} du$, que únicamente tiene una función $u^{2}$ (puesto que su derivada, al ser notada como $du$ pasa a ser simplemente un símbolo, el diferencial, la hicimos desaparecer).

Ahora, concluimos buscando una primitiva de la nueva función que estamos integrando $u^{2}$, y luego procedemos a deshacer el cambio de variable: volver a cambiar $u$ por lo que era originalmente. En este caso, sustituir $u$ por $\sin(x)$ nuevamente.

Así, llegamos al mismo resultado.

Realizamos los mismos pasos desarrollados previamente, pero con un enfoque un poco más "abstracto" y "simbólico".

Continuaremos utilizando esta misma técnica, el enfoque del cambio de variable.

#### Ejemplo 2
$$
\int \sin(x^{3}) \cdot x^{2} \space dx
$$
Aquí tenemos una composición:
$$
x \mapsto x^{3} \mapsto \sin(x^{3})
$$
De esta forma, podríamos notar
$$
\begin{align}
&g = x^{3} \implies g' = 3x^{2} \\
&f = \sin(x)
\end{align}
$$
Ahora, proseguimos realizando cambio de variable:
$$
\int \sin(x^{3}) \cdot x^{2} \space dx \underset{\begin{align}
u = x^{3} \\
du = 3x^{2}
\end{align}} = ?
$$
El problema es que no es exactamente lo que tenemos. Por esta razón, modificamos la expresión para hacer aparecer el 3 que necesitamos (pasando las constantes fuera de la integral y cancelándose, lo que asegura que las expresiones son equivalente):
$$
\frac{1}{3} \int \underbrace{ \sin(x^{3}) }_{ f(g(x)) } \cdot \underbrace{ 3x^{2} }_{ g'(x) } \space dx \underset{\begin{align}
&u = x^{3} \\
&du = 3x^{2} \space dx
\end{align}} = \frac{1}{3} \int \underbrace{ \sin(u) }_{ f(u) } \space du = \frac{1}{3} \cdot (\underbrace{ -\cos(u) }_{ F(u) }) + c = \frac{1}{3} \cdot (-\cos(x^{3})) + c
$$
Si derivamos:
$$
\left( \frac{(-\cos(x^{3})) + c}{3} \right)' = \frac{\sin(x^{3}) \cdot \cancel{ 3 }x^{2}}{\cancel{ 3 }} = \sin(x^{3}) \cdot x^{2}
$$
Comprobamos que el resultado obtenido es correcto.

#### Ejemplo 3
$$
\int \sqrt{ 2x + 1 } \space dx
$$
Ya podemos ver que conviene reconocer esta forma, si sabemos primitivizar $f$.
En este caso, parece que:
$$
\begin{align}
&g(x) = 2x + 1 \implies g'(x) = 2 \\
&f(x) = \sqrt{ x }
\end{align}
$$
Siendo $f$ una función que sabemos primitivizar.
$$
\int \sqrt{ 2x + 1 } \space dx \underset{\begin{align}
u = 2x + 1 \\
du = 2 \space dx
\end{align}} = ?
$$
Nuevamente, no es exactamente lo que tenemos, por lo que es necesario modificar la expresión para poder utilizar las variables definidas:
$$
\frac{1}{2} \int 2\sqrt{ 2x + 1 } \space dx \underset{\begin{align}
u = 2x + 1 \\
du = 2 \space dx
\end{align}} = \frac{1}{2} \int \sqrt{ u } \space du
$$
Conocemos dicha primitiva, ya que podemos tomar como referencia la primitiva de $u^{\alpha}$:
$$
\int u^{\alpha} \space du = \frac{u^{\alpha + 1}}{\alpha + 1} + c \qquad \alpha \neq -1
$$
En el caso $\alpha = -1$, $\int u^{\alpha} \space du = \int \frac{1}{u} \space u = \log(u)$

Dicho esto, proseguimos:
$$
\frac{1}{2} \int 2\sqrt{ 2x + 1 } \space dx \underset{\begin{align}
u = 2x + 1 \\
du = 2 \space dx
\end{align}} = \frac{1}{2} \int \sqrt{ u } \space du = \frac{1}{2} \int \underbrace{ u^{\frac{1}{2}} }_{ f(u) } \space du = \frac{1}{2} \cdot \underbrace{ \frac{u^{\frac{3}{2}}}{\frac{3}{2}} }_{ F(u) } + c = \frac{1}{2} \cdot \underbrace{ \frac{(2x + 1)^{\frac{3}{2}}}{\frac{3}{2}} }_{ F(g(x)) } + c
$$

#### Ejemplo 4
$$
\int \tan(x) \space dx = \int \frac{\sin(x)}{\cos(x)} \space dx = \int \frac{1}{\cos(x)} \cdot \sin(x) \space dx
$$
Al expresarlo como un cociente, empieza a tomar una forma que invita a aplicar el método de integración por sustitución, ya que tenemos dos funciones, $\sin(x)$ y $\cos(x)$, que podríamos decir que una es la derivada de la otra (en cualquier sentido, solo diferenciándose por un signo). Podemos agregar el signo faltante fuera de la integral para compensar, y tener la forma "ideal" para trabajar.
$$
\int \frac{1}{\cos(x)} \cdot \sin(x) \space dx = -\int \frac{1}{\cos(x)} \cdot (-\sin(x)) \space dx \underbrace{ = }_{ \begin{align}
u = \cos(x) \\
du = -\sin(x) \space dx
\end{align} } -\int \frac{1}{u} \space du
$$
$\int \frac{1}{u} \space du$ también se puede notar como $\int \frac{du}{u}$, aunque es exactamente lo mismo, no cambia la expresión ni su significado.

Ya conocemos una primitiva de $\frac{1}{u}$: $\log(u)$
$$
-\int \frac{1}{u} \space du = -\log(u) + C
$$
Queda deshacer el cambio de variable:
$$
-\log(u) + C = -\log(\cos(x)) + C
$$
En conclusión:
$$
\int \tan(x) \space dx = -\log(\cos(x)) + C
$$

Antes de pasar al último ejemplo, veremos otro punto de vista del método:
#### Otro punto de vista: composición con la función inversa
Hasta ahora, hemos seguido el siguiente proceso: reconocemos la forma $f(g(x)) \cdot g'(x)$, y reducimos el problema a encontrar una primitiva de $f$:
$$
\int f(g(x)) \cdot g'(x) \space dx = F(g(x)) + C
$$
con $F' = f$.

Sin embargo, hay casos en los que aplicamos la fórmula al revés:
Supongamos que tenemos una igualdad como $\int f(g(x)) \cdot g'(x) \space dx = F(g(x)) + C$, en la que además $g(x)$ es invertible. En este caso, podríamos desarrollar lo siguiente:
$$
\left( \int f(g(x)) \cdot g'(x) \space dx \right) \circ g^{-1}(x) = (F(g(x)) + C) \circ g^{-1}(x) = F(x) + C = \int f(x) \space dx
$$
donde $F' = f$ ($F$ es una primitiva de $f$).

De esta manera, si tomamos una primitiva de la integral y la componemos con $g^{-1}(x)$, obtendremos una primitiva de $f$ (calculando la integral).

Entonces, el procedimiento que puede ser conveniente en casos puntuales es:
- Sustituir $x$ por una función.
- Multiplicar por la derivada de dicha función.
- Hallar una primitiva de dicha función (integral).
- Componer el resultado con la función inversa de la función agregada.

Ahora, lo estudiaremos con un ejemplo, viendo que no es tan distinto de lo que hacíamos anteriormente, simplemente a la inversa.

#### Ejemplo 5
$$
\int \sqrt{ 1 - u^{2} } \space du
$$
Lo que haremos es aplicar el cambio de variable al revés. Anteriormente, sustituíamos una función por una variable. Ahora, sustituiremos nuestra variable $u$ por una función $g(x)$ (por eso le pusimos $u$, para que sea un poco más intuitivo).
$$
\int \sqrt{ 1 - u^{2} } \space du \underbrace{ = }_{ \begin{align}
&u = \sin(x) \\
&du = \cos(x) \space dx
\end{align} } \int \sqrt{ 1 - \sin ^{2}(x) } \cdot \cos(x) \space dx
$$
Ahora, podemos aplicar igualdades trigonométricas: $\sqrt{ 1 - \sin ^{2}(x) } = \cos(x)$:
$$
\int \sqrt{ 1 - \sin ^{2}(x) } \cdot \cos(x) \space dx = \int \cos(x) \cdot \cos(x) \space dx
$$
Podemos calcular la primitiva de $\cos ^{2}(x)$ aplicando partes:
$$
\begin{align}
\int \cos ^{2}(x) \space dx &= \int 1 - \sin ^{2}(x) \space dx \\
&= \int 1 \space dx - \int \sin ^{2}(x) \space dx \\
&= x - \int \sin ^{2}(x) \space dx \\
&= x - \left(\sin(x) (-\cos(x)) - \int \cos(x) (-\cos(x)) \space dx \right) \\
&= x - \left(\sin(x) (-\cos(x)) + \int \cos ^{2}(x) \space dx \right) \\
&= x - \sin(x) (-\cos(x)) - \int \cos ^{2}(x) \space dx \\
\int \cos ^{2}(x) \space dx + \int \cos ^{2}(x) \space dx &= x - \sin(x) (-\cos(x)) \\
2\int \cos ^{2}(x) \space dx &= x - \sin(x) (-\cos(x)) \\
2\int \cos ^{2}(x) \space dx &= x + \sin(x) \cos(x) \\
\int \cos ^{2}(x) \space dx &= \frac{x + \sin(x) \cos(x)}{2} + C
\end{align}
$$
Concluimos el cálculo:
$$
\int \cos(x) \cdot \cos(x) \space dx = \frac{x + \sin(x) \cos(x)}{2} + C
$$
Ahora, tenemos que realizar el cambio de variable a la inversa. Como hicimos aparecer una función, no se trata solo de sustituir la función por la variable nuevamente. También tenemos que determinar el valor de $x$ (ya que aparece en el resultado):
$$
\begin{align}
&u = \sin(x) \implies x = \arcsin(u) \\
&du = \cos(x) \space dx
\end{align}
$$
Despejamos pasando el seno como la función inversa aplicada a lo que está del otro lado.

De esta manera:
$$
\frac{x + \sin(x) \cos(x)}{2} + C = \frac{\arcsin(u) + \sin(\arcsin(u)) \cos(\arcsin(u))}{2} + C
$$

¿Cuál es el sentido de seguir un método tan enrevesado?
Puesto que en principio no sabíamos calcular una primitiva de $\sqrt{ 1 - u^{2} }$, y al agregar $g(x)$ y $g'(x)$, logramos llegar a un resultado. Ahora, desglosamos cada uno de los componentes que vimos durante este proceso:
$$
\begin{align}
\int \overbrace{ \sqrt{ 1 - u^{2} } }^{ f(x) } \space du &= \int \overbrace{ \sqrt{ 1 - \sin ^{2}(x) } }^{ f(g(x)) \cdot g'(x) \cdot \cos(x) \space dx } \\
&= \overbrace{ \frac{x + \sin(x) \cos(x)}{2} + C }^{ \int f(g(x)) \cdot g'(x) \space dx \text{ (primitiva)} } \\
&= \overbrace{ \frac{\arcsin(u) + \sin(\arcsin(u)) \cos(\arcsin(u))}{2} + C }^{ (\int f(g(x)) \cdot g'(x) \space dx) \space \circ g^{-1}(x) }
\end{align}
$$

Esta integral en particular es importante, ya que:

Si consideramos un circulo de radio uno, el medio círculo de radio uno se puede estudiar como la función $f(x) = \sqrt{ 1 - x^{2} }$. De esta forma, el área de dicha función es:
$$
\int_{-1}^{1} \sqrt{ 1 - x^{2} } \space dx
$$
Conociendo la primitiva de dicha función, podemos calcular el valor de la integral, y los cálculos no serán tan complejos, ya que los extremos son valores en los que las funciones trigonométricas son conocidas:
$$
\begin{align}
\int_{-1}^{1} \sqrt{ 1 - x^{2} } \space dx &= \frac{\arcsin(1) + \sin(\arcsin(1)) \cos(\arcsin(1))}{2} - \frac{\arcsin(-1) + \sin(\arcsin(-1)) \cos(\arcsin(-1))}{2} \\
&= \frac{\frac{\pi}{2} + \sin\left( \frac{\pi}{2} \right) \cos\left( \frac{\pi}{2} \right)}{2} - \frac{-\frac{\pi}{2} + \sin\left( -\frac{\pi}{2} \right) \cos\left( -\frac{\pi}{2} \right)}{2} \\
&= \frac{\frac{\pi}{2} + \cancel{ 1 \cdot 0 }}{2} - \frac{-\frac{\pi}{2} + \cancel{ (-1) \cdot 0 }}{2} \\
&= \frac{\frac{\pi}{2}}{2} - \frac{-\frac{\pi}{2}}{2} \\
&= \frac{\frac{\pi}{2}}{2} + \frac{\frac{\pi}{2}}{2} \\
&= \frac{\pi}{2}
\end{align}
$$
De esta forma, el área de medio círculo de radio 1 es $\frac{\pi}{2}$, por lo que el área del círculo completo es $\pi = 1^{2} \cdot \pi$, siendo 1 el radio.

Para concluir con la clase:
La fórmula de integración por sustitución es:
$$
\int f(g(x)) \cdot g'(x) \space dx = F(g(x)) + C
$$
con $F' = f$.

Y en general, es aplicable a la mayoría de los casos. En ciertos casos que envuelven funciones trigonométricas, uno aplica el método inverso, realizando la sustitución por una función e incluyendo la composición por la función inversa, pero son casos excepcionales. La gran mayoría se resuelve por el método regular.

En la próxima clase abordaremos el método de integración con fracciones simples, finalizando el tema de métodos de integración.