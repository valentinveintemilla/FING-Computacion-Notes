# Ejercicio 1
Sea $f : \mathbb{R} \to \mathbb{R}$ definido por
$$
f(x) = \begin{cases}
\begin{align}
&42 &&\text{si} &x = 0\\
&x &&\text{si} &x \neq 0
\end{align}
\end{cases}
$$
Como vemos, es la identidad normal, pero en el punto 0 vale 42.
Podemos ver que la función tiene límite en 0: es 0. Igualmente, tiene límite en cualquier otro punto.
De esta forma, verificamos que podemos cambiar la función en una cantidad finita de puntos sin cambiar la propiedad de límite.
Esta demostración es algo más complicada, aunque no hay problema para demostrar la existencia de límite en 0, pues por la definición no se analiza lo que sucede en el punto $x_{0}$. Sin embargo cuando consideramos otro punto, tendremos que reducir el $\delta$ para evitar el valor problemático. De esta manera, hay que distinguir dos casos.

Para solucionar esto, en lugar de tomar $\delta_{\epsilon} := \epsilon$, tomaremos $\delta_{\epsilon} := mín(\epsilon, |x_{0}|)$.

Incluso en la demostración anterior, podríamos haber tomado un valor menor que $\epsilon$, como $\frac{\epsilon}{2}$. En eso consiste el tomar un "radio lo suficientemente pequeño": si encontramos un valor de $\delta$ para el que la demostración es exitosa, también lo será para valores más pequeños de $\delta$.

De esta forma, podemos decir que la función anterior es continua en todos los puntos, salvo en 0. En todos los puntos $x_{0}$, $f(x) = \lim_{ x \to x_{0} } f(x) = x_{0}$, menos en 0.