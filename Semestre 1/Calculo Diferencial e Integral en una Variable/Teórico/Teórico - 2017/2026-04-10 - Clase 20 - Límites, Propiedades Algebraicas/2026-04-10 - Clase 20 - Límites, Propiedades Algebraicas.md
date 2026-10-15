# Propiedades algebraicas
Veremos algunas propiedades algebraicas para facilitar las demostraciones y cálculos relacionadas con los límites.

> [!Observación]
> Dados una función $f : I \to \mathbb{R}$, un punto $x_{0} \in \overset{-} I$ y $L \in \mathbb{R}$. Tenemos que:
> $$
> \begin{align}
> \lim_{ x \to x_{0} } f(x) = L &\Longleftrightarrow \lim_{ x \to x_{0} } (f(x) - L) = 0 \\
> &\Longleftrightarrow \lim_{ x \to x_{0} } |f(x) - L| = 0
> \end{align}
> $$

Los tres enunciados anteriores son equivalentes, por lo que se pueden intercambiar.

A continuación lo demostramos (desarrollando lo que implica cada uno de los enunciados):

## Demostración
1. $\forall \epsilon > 0, \exists \delta > 0, \forall x \in E^{*}(x_{0}, \delta) \cap I, |f(x) - L| < \epsilon$
2. $\forall \epsilon > 0, \exists \delta > 0, \forall x \in E^{*}(x_{0}, \delta) \cap I, |(f(x) - L) - 0| < \epsilon$
Como podemos ver $|f(x) - L| = |(f(x) - L) - 0|$, por lo que los enunciados son equivalentes.

3. $\forall \epsilon > 0, \exists \delta > 0, \forall x \in E^{*}(x_{0}, \delta) \cap I, ||f(x) - L| - 0| < \epsilon$
También podemos decir lo mismo de este último enunciado, los valores son idénticos en los tres enunciados.

De esta manera, las tres definiciones son equivalentes, y saber esto nos será útil posteriormente.

---
A continuación, abordamos la suma y la resta:

## Proposición

> [!Proposición]
> Sea $f, g : I \to \mathbb{R}$, y un punto $x_{0} \in \overset{-} I$.
> Si $\lim_{ x \to x_{0} } f(x) = L$ y $\lim_{ x \to x_{0} } g(x) = L'$, entonces
> $$
> \begin{align}
> &\lim_{ x \to x_{0} } (f(x) + g(x)) = L + L' \\
> &\lim_{ x \to x_{0} } (f(x) - g(x)) = L - L'
> \end{align}
> $$

Tenemos que demostrar dos cosas: la suma y la resta. Aquí solo trataremos la suma, pues la resta es análoga.

### Demostración
(Caso de la suma)

Tenemos dos hipótesis, una para $f$ y otra para $g$, lo que nos da dos funciones que para cada $\epsilon$ nos dan un $\delta$ (radio de seguridad).

Por hipótesis, existen dos funciones $\overbrace{ \epsilon \mapsto \delta_{\epsilon} }^{ \text{para } f }$ y $\overbrace{ \epsilon \mapsto \delta'_{\epsilon} }^{ \text{para } g }$ tales que
$$
\left.
\begin{align}
&\forall x \in E^{*}(x_{0}, \delta_{\epsilon}) \cap I, |f(x) - L| < \epsilon &&(*) \\
&\forall x \in E^{*}(x_{0}, \delta'_{\epsilon}) \cap I, |g(x) - L'| < \epsilon &&(*') \\
\end{align}
\right\} \text{para todo } \epsilon > 0
$$

En palabras: "Para la función $f$, yo puedo asociar a cada precisión un radio de seguridad, tal que para todo x en la intersección entre el entorno reducido de centro $x_{0}$ y radio $\delta$ (radio de seguridad) y el dominio de $f$, tenemos que $f(x)$ es igual al límite a menos de $\epsilon$."

Aclarar que manejamos un radio de seguridad para la función f y otro para g, puesto que son funciones diferentes, límites diferentes, no tiene por que manejar el mismo radio de seguridad.

(Ahora, haremos lo mismo para $f(x) + g(x)$)

Se trata de construir $\epsilon \mapsto \delta''_{\epsilon}$ tal que
$$
\forall x \in E^{*}(x_{0}, \delta''_{\epsilon}) \cap I, |(f(x) + g(x)) - (L + L')| < \epsilon
$$

(Tenemos que demostrar esto, llegar al objetivo, partiendo de nuestras hipótesis.)

Como tenemos dos incertitudes de $\epsilon$ (una para $f(x)$ y otra para $g(x)$), realizando la suma de ambas obtendremos una nueva incertitud de $2\epsilon$, por lo que también cambiaremos los $\epsilon$ (a $\frac{\epsilon}{2}$).

Se define $\delta''_{\epsilon} := mín\left( \delta_{\frac{\epsilon}{2}}, \delta'_{\frac{\epsilon}{2}} \right)$ para todo $\epsilon > 0$

Sean $\epsilon > 0$ y $x \in I$ tal que $0 < |x - x_{0}| < \delta''_{\epsilon}$ (es lo mismo que $x \in E^{*}(x_{0}, \delta''_{\epsilon}) \cap I$).

Se observa que (como $0 < |x - x_{0}| < \delta''_{\epsilon}$ se cumple):
- $0 < |x - x_{0}| < \delta_{\frac{\epsilon}{2}}$ (pues $\delta''_{\epsilon} \leq \delta_{\frac{\epsilon}{2}}$)
(Ahora, podemos aplicar el primer punto $(*)$ que desarrollamos anteriormente, referido a $f(x)$, pero ahora con $\frac{\epsilon}{2}$)

Entonces $|f(x) - L| < \frac{\epsilon}{2}$ (por $(*)$)

- $0 < |x - x_{0}| < \delta'_{\frac{\epsilon}{2}}$ (pues $\delta''_{\epsilon} \leq \delta'_{\frac{\epsilon}{2}}$)
Entonces $|g(x) - L'| < \frac{\epsilon}{2}$ (por $(*')$)

(Así, obtuvimos un radio que funciona para $f$ y $g$ a la vez, dando para cada función una aproximación a menos de $\frac{\epsilon}{2}$. Así, cuando sumemos ambas desigualdades, obtendremos una aproximación a menos de $\epsilon$.)

Luego:
$$
\begin{align}
|(f(x) + g(x)) - (L + L')| &= |(f(x) - L) + (g(x) - L')|  \\
&\leq |f(x) - L| + |g(x) - L'| < \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon
\end{align}
$$
Así concluimos la demostración, llegando al resultado esperado.

![[Semestre 1/Calculo Diferencial e Integral en una Variable/Teórico/Teórico - 2017/2026-04-10 - Clase 20 - Límites, Propiedades Algebraicas/Imágenes/1 - Representación de demostración.png]]
Si tomamos el mínimo de ambos $\delta$, sabemos que $L$ es una aproximación a $f(x)$ a menos de $\frac{\epsilon}{2}$ y $L'$ es una aproximación a $g(x)$ a menos de $\frac{\epsilon}{2}$, y cuando sumamos, obtenemos que $L + L'$ es una aproximación de $f(x) + g(x)$ a menos de $\epsilon$.

La idea es encontrar un $\delta$ que cumpla todas las condiciones necesarias para satisfacer el enunciado objetivo. Es por eso que tomamos el más pequeño, siempre podemos reemplazar un radio por otro más pequeño (si una propiedad se cumple para un radio, siempre se cumplirá para un radio más pequeño).

En realidad, realizamos todo este trabajo para cumplir con la demostración oficial, repartiendo los $\epsilon$ por los participantes y desarrollar los $\delta$ en base a estos, en lugar de llegar a la conclusión de que $|f(x) - L| + |g(x) - L'| < \epsilon + \epsilon = 2\epsilon$, que también es correcta, pero no es tan formal.

Ahora que demostramos esta propiedad, podemos estudiar el límite de funciones sumadas, por ejemplo $\sqrt{ x } + x$. No es necesario seguir demostrando la propiedad, puesto que sabemos que es verdadera.
Por esta razón, veremos una serie de teoremas que nos facilitarán las demostraciones y estudio de límites en funciones.

La demostración para la resta de funciones es análoga, simplemente tener en cuenta la siguiente propiedad (propiedad geométrica):

> [!Desigualdad triangular]
> $$
> \begin{align}
> &|a + b| \leq |a| + |b| \\
> &|a - b| \leq |a| + \underbrace{ |-b| }_{ |b| }
> \end{align}
> $$
> En su forma general:
> $$
> |a \pm b| \leq |a| + |b|
> $$

Demostramos que cuando dos funciones tienen límites, podemos sumar los límites y obtengo el límite de la suma. Ídem para la resta.

---
Continuamos con el producto, para lo que utilizaremos varios lemas intermediarios.

## Terminología
> [!Definición]
> Sean $f : \in \mathbb{R}$ y $x_{0} \in \overset{-} I$.
> Se dice que $f$ está <u>acotada en un entorno de</u> $x_{0}$ cuando
> $$
> \begin{align}
> \exists r > 0, \exists M &\geq 0, \forall x \in E(x_{0}, r) \cap I, |f(x)| \leq M \\
> &(>0)
> \end{align}
> $$

Ignorando $r$ y el entorno especificado, es la definición usual de acotada (el valor absoluto está acotado). La ventaja del valor absoluto es que me da a la vez un cota superior e inferior a la función, de esta forma únicamente introducimos $M$ y no es necesario introducir otra variable.

Aclarar que la cota únicamente abarca el entorno de centro $x_{0}$ y radio $r$, fuera de dicho entorno puede hacer cualquier cosa.

Seguidamente, veremos dos lemas que nos serán útiles a posteriori.

---
## Lema
> [!Lema]
> Si $f$ tiene límite (finito) en $x_{0}$, entonces está acotada en un entorno de $x_{0}$

Es decir, la existencia de límite, fuerza la existencia de una cota local.

### Demostración
Consideramos $\epsilon = 1$

Sea $\delta > 0$ tal que $\forall x \in E^{*}(x_{0}, \delta) \cap I, |f(x) - L| < 1$

Se observa que $\forall x \in E^{*}(x_{0}, \delta) \cap I$, tenemos que
$$
\begin{align}
|f(x)| &= |L + (f(x) - L)| \\
&\leq |L| + |f(x) - L| < |L| + 1
\end{align}
$$
Esto nos da una cota para $|f(x)|$ para todo $x \in E^{*}(x_{0}, \delta)$.

Como vemos, aquí casi terminamos, pues para la proposición anterior, podemos tomar $r = \delta$ y $M = |L| + 1$, pero aún nos falta el punto $x_{0}$, pues la proposición maneja un entorno no reducido.
De esta manera, distinguimos dos casos para manejar el caso $x_{0}$:

#### Caso $x_{0} \in I$
Se toman $r := \delta$ y $M := máx(|L| + 1, |f(x_{0})|)$

(Si tomamos un $x$ en el entorno no reducido, hay dos posibilidades: $x \neq x_{0} \implies |f(x)| < máx(|L| + 1, |f(x_{0})|) + 1$, o $x = x_{0} \implies |f(x)| = |f(x_{0})| < máx(|L| + 1, |f(x_{0})|)$.
Al tomar el máximo, estamos seguros de que la cota superior funciona para todos los casos)

#### Caso $x_{0} \not \in I$
Se toman $r := \delta$ y $M = |L| + 1$

(Funciona la desigualdad anterior con normalidad, puesto que da igual si tomamos la intersección con el entorno o con el entorno reducido, $x$ nunca será igual a $x_{0}$, porque $x_{0}$ no pertenece a la intersección).

---
## Propiedad
> [!Propiedad]
> Sean $f,g : I \to \mathbb{R}$ y un punto $x_{0} \in \overset{-} I$.
> 
> Si
> - $f$ está acotada en un entorno de $x_{0}$.
> - $\lim_{ x \to x_{0} } g(x) = 0$
> entonces
> $$
> \lim_{ x \to x_{0} } f(x) g(x) = 0
> $$

Esto dice que el producto de una función acotada al rededor de un punto dado por otra función que tiende a 0 en dicho punto, va a tender a 0 en el punto correspondiente.

Es importante entender que este lema es fundamental.

No vamos a realizar la demostración completa, pero veremos una idea.

### Demostración
$f$ acotada localmente
$$
\longrightarrow \exists r > 0, \exists M > 0, \forall x \in E(x_{0}, r) \cap I, |f(x)| \leq M \qquad \text{(por la terminología anterior)}
$$
$$
\begin{align}
\lim_{ x \to x_{0} } g(x) = 0 \longrightarrow &\epsilon \mapsto \delta_{\epsilon} \qquad \text{para } g \\
&\forall x \in E^{*}(x_{0}, \delta_{\epsilon}) \cap I, |g(x)| < \epsilon
\end{align}
$$

Simplemente tomamos la hipótesis sobre $g(x)$ y la relacionamos con la definición de límite en una función (sabiendo que $g(x)$ tiene límite en $x_{0}$).

Ahora, queremos demostrar lo mismo para el producto $f(x) g(x)$. Para esto, tenemos que definir una nueva función para este producto.

Como sabemos que $f(x)$ no es mayor que $M$, podemos usar $\delta$ para $\frac{\epsilon}{m}$. De esta forma, dividimos a $\epsilon$ en dos partes (ahora que es un producto): $M$ y $\frac{\epsilon}{m}$ tal que $M \cdot \frac{\epsilon}{M} = \epsilon$. Es importante considerar que estos solo funciona en el radio $r$, por lo tanto el valor de $\delta'_{\epsilon}$ no puede superar $r$.

En pocas palabras, tenemos una condición sobre $f$ que solo funciona en un radio $r$, y tenemos una condición sobre $g$ que solo funciona en un radio $\delta_{\frac{\epsilon}{m}}$. Como los radios se superponen, simplemente tenemos que tomar el mínimo para que ambas condiciones funcionen.

Sea $\delta'_{\epsilon} := mín \left( \delta_{\frac{\epsilon}{m}}, r \right)$
$$
\begin{align}
\forall x \in E^{*}(x_{0}, \delta'_{\epsilon}) \cap I, |f(x) g(x)| &= |f(x)| \cdot |g(x)| \\
& < M \cdot \frac{\epsilon}{M} = \epsilon
\end{align}
$$
Concluimos la demostración, por lo que ahora podemos demostrar la propiedad del límite del producto. Esta era una versión parcial que funciona solo en el caso en el que una función esta acotada localmente y la otra tiene límite 0.

La condición de que una de las funciones esté acotada es fundamental. No podemos asegurar nada si esto no está establecido. A continuación, vemos un contraejemplo con una función que no está acotada localmente:

#### Contraejemplo
$(I = R^{+})$
$$
\begin{align}
&f(x) = \frac{1}{x} \qquad \text{(no esta acotada alrededor de 0)} \\
&g(x) = x \underset{x \to 0} \to 0
\end{align}
$$
$$
f(x) g(x) = 1 \cancel{ \underset{x \to 0} \to } 0
$$

---
## Propiedad

> [!Producto]
> Bajo las mismas hipótesis, tengo que:
> 
> Si $\lim_{ x \to x_{0} } f(x) = L$ y $\lim_{ x \to x_{0} } g(x) = L'$, entonces
> $$
> \lim_{ x \to x_{0} } f(x) g(x) = L L'
> $$

Tenemos todos los lemas necesarios para resolver la demostración:

### Demostración
(Demostrar $\lim_{ x \to x_{0} } f(x) g(x) = L L'$ es lo mismo que decir que la diferencia entre ambas cosas tiende a 0, por lo que estudiaremos la diferencia.)

Se observa que
$$
f(x) g(x) - L L' = (f(x) - L) L' + f(x) (g(x) - L')
$$
Si desarrollamos, nos daremos cuenta de la igualdad es verdadera:
$$
(f(x) - L) L' + f(x) (g(x) - L') = \cancel{ f(x)L' } - L L' + f(x)g(x) - \cancel{ f(x)L' } = f(x) g(x) - L L'
$$

Con dicha igualdad, podemos concluir la demostración, ya que:
$$
f(x) g(x) - L L' = \underbrace{ \underbrace{ (f(x) - L) }_{ \to 0 } L' }_{ \to 0 } + \underbrace{ f(x) \underbrace{ (g(x) - L') }_{ \to 0 } }_{ \to 0 }
$$
Como ambas partes tienen a 0 (ya que el valor de $L'$ es acotado y $f(x)$ tiene límite -es localmente acotada por el lema anterior-). Es así que la suma tiende a 0, por lo que el límite de $f(x) g(x)$ tiende a $L L'$.

Algo que podemos confirmar, ==es que todos los polinomios son funciones continuas==, ya que el producto, suma y resta de dos funciones continuas da como resultado una función continua. De esta forma, como los polinomios se construyen a partir de la función identidad por suma y producto, y las funciones continuas, podemos confirmar que todos los polinomios son funciones continuas.

---
Proseguimos a desarrollar la propiedad para el cociente.

## Propiedad

> [!División]
> Sea $f : I \to \mathbb{R}$ tal que:
> - $f(x) \neq 0 \qquad \forall x \in I$
> - $\lim_{ x \to x_{0} } f(x) = L \neq 0$
> 
> Entonces:
> $$
> \lim_{ x \to x_{0} } \frac{1}{f(x)} = \frac{1}{L}
> $$

(Aclaración: la primer condición no implica la segunda, ya que podemos tener una funcion no nula que tenga límite nula (recordemos que el valor de la imagen no determina el valor del limite en un punto correspondiente)).

No lo demostraremos, aunque se usa una idea similar a la del producto. Podemos, en lugar de dividir entre $f(x)$, expresarlo de la siguiente forma:
$$
\frac{1}{f(x)} - \frac{1}{L} = \frac{L - f(x)}{f(x) L}
$$
Podemos desarrollar la igualdad anterior. Además, podemos reconocer que $L - f(x)$ tiende a 0.
$$
= \underbrace{ -\frac{1}{L} \cdot \underbrace{ \underbrace{ \frac{1}{f(x)} }_{ \text{localmente acotado} } \cdot \underbrace{ (f(x) - L) }_{ \begin{align}
\downarrow \\
0
\end{align} } }_{ \begin{align}
\downarrow \\
0
\end{align} } }_{ \begin{align}
\downarrow \\
0
\end{align} }
$$
Lo importante aquí es demostrar que $\frac{1}{f(x)}$ es localmente acotado, llegando a la conclusión de que todo equivale a 0, y demostrando que $\lim_{ x \to x_{0} } \frac{1}{f(x)} = \frac{1}{L}$

Finalizaremos viendo la proposición, consecuencia del cociente:

Si $\lim_{ x \to x_{0} } f(x) = L$ y $\lim_{ x \to x_{0} } g(x) = L' \neq 0$, entonces
$$
\lim_{ x \to x_{0} } \frac{f(x)}{g(x)} = \frac{L}{L'} 
$$
También hay que suponer que $g(x)$ nunca se anula en el intervalo.

Esto se demuestra usando la compuesta del teorema sobre el producto y del teorema sobre $\frac{1}{f(x)}$:
$$
\frac{f(x)}{g(x)} = f(x) \times \frac{1}{g(x)} = L \times \frac{1}{L'} = \frac{L}{L'}
$$
