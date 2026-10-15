Continuamos con las derivadas.
# Derivadas
La clase pasada comenzamos el tema, viendo la noción de derivada y definición formal de derivada en un punto.

> [!Derivada en un punto - Definición]
> $f : I \to \mathbb{R}$ es derivable en un punto $x_{0} \in I$ cuando el cociente $\frac{f(x) - f(x_{0})}{x - x_{0}}$ tiene límite cuando $x \to x_{0}$. Se escribe
> $$
> f'(x_{0}) = \lim_{ x \to x_{0} } \frac{f(x) - f(x_{0})}{x - x_{0}} 
> $$

La función $\frac{f(x) - f(x_{0})}{x - x_{0}}$ es el cociente incremental. Dicha función no está definida en $x_{0}$, pero la noción de límite se extiende sin problemas a esta función, puesto que no importa lo que suceda en el punto (si la función esta definida o no, y si coincide con el límite en dicho punto o no).

También tenemos una definición alternativa:

> [!Observación]
> $$
> f'(x_{0}) = \lim_{ h \to 0 } \frac{f(x_{0} + h) - f(x_{0}) }{h}
> $$
> Siendo $h = x - x_{0}$

También vimos la interpretación gráfica de la derivada, siendo la pendiente de la recta tangente a la función en $x_{0}$:
![[1 - Recta tangente.png]]
$$
R_{0} : y = f(x_{0}) + f'(x_{0})(x - x_{0})
$$

Cuando abordemos el teorema de Taylor, veremos que, al orden 1, establece que la función $f$ se puede aproximar alrededor de $x_{0}$ por su tangente.

---
Ahora, abordaremos algunas propiedades de la derivada:

Nosotros nunca supusimos que la función sea continua para ser derivable. Sin embargo, si una función es derivable en un punto, necesariamente es continua en dicho punto.

## Proposición

> [!Proposición]
> Si $f : I \to \mathbb{R}$ es derivable en el punto $x_{0} \in I$ entonces es continua en $x_{0}$.

**Demostración**

Por hipótesis, tenemos que $\lim_{ x \to x_{0} } \frac{f(x) - f(x_{0})}{x - x_{0}} = f'(x_{0})$

Para demostrar que es continua, multiplicamos por la función $x - x_{0}$.
$$
\underbrace{ f(x) - f(x_{0}) }_{ \underset{ x \to x_{0}} \to 0 } = \underbrace{ \frac{f(x) - f(x_{0})}{x - x_{0}} }_{ \underset{ x \to x_{0}} \to f'(x_{0}) } \times \underbrace{ (x - x_{0}) }_{ \underset{ x \to x_{0}} \to 0 }
$$
Por producto de límites, $f(x) - f(x_{0})$ tiende a 0 cuando $x \to x_{0}$. Esto significa que $f(x) \to f(x_{0})$ cuando $x \to x_{0}$.

Luego:
$$
\lim_{ x \to x_{0} } f(x) = f(x_{0})
$$

Esto demuestra que la función es continua en $x_{0}$.

Es importante entender que el recíproco no se cumple. Que una función sea continua no implica que sea derivable.

> [!Observación]
> La condición de derivabilidad es más exigente que la condición de continuidad.

### Ejemplo 1
$$
f(x) = |x|
$$

![[2 - Función valor absoluto.png]]

Veremos que la función es derivable para todo valor diferente de 0. Fuera de 0, la función es una porción de recta, por lo tanto es derivable. Sin embargo, en 0 presenta un punto anguloso, por lo que no es derivable.

**Demostración**

**Caso: $x_{0} > 0$**
En un entorno de $x_{0}$, tenemos que $f(x) = |x| = x$.
$$
\frac{f(x) - f(x_{0})}{x - x_{0}} = \frac{|x| - |x_{0}|}{x - x_{0}} = \frac{x - x_{0}}{x - x_{0}} = 1 \longrightarrow 1 = f'(x_{0})
$$
Entonces, la función es derivable para $x_{0} > 0$, y tiene derivada 1 (pendiente 1).

**Caso: $x_{0} > 0$**
En un entorno de $x_{0}$, tenemos que $f(x) = |x| = -x$.
$$
\frac{f(x) - f(x_{0})}{x - x_{0}} = \frac{|x| - |x_{0}|}{x - x_{0}} = \frac{-x + x_{0}}{x - x_{0}} = -1 \longrightarrow -1 = f'(x_{0})
$$
Entonces, la función es derivable para $x_{0} < 0$, y tiene derivada -1 (pendiente -1).

**Caso: $x_{0} > 0$**
$$
\frac{f(x) - f(x_{0})}{x - x_{0}} = \frac{|x|}{x} = \begin{cases}
\begin{align}
&1 &&\text{si } x > 0 \\
&-1 &&\text{si } x < 0
\end{align}
\end{cases}
$$
De esta forma, la función no tiene límite en $x \to 0$, puesto que tiende a 1 por la derecha y a -1 por la izquierda.

$f$ no es derivable en el punto $x_{0} = 0$.
No podemos escribir $f'(0)$ en este caso, puesto que no existe el límite correspondiente, no es derivable para $x_{0} = 0$.

De este ejemplo podemos observar lo siguiente:
La función no tiene límite en 0. Sin embargo, tiene límite por la izquierda (-1) y por la derecha (1). Por lo tanto, aunque no sea derivable en 0, si es derivable por la izquierda y derivable por la derecha de 0.

No definiremos dichas nociones (derivada por la izquierda y por derecha), aunque funciona igual que la derivada usual, simplemente se divide en dos.

### Ejemplo 2
Sean $f, g, h : \mathbb{R} \to \mathbb{R}$ definidas por
$$
f(x) = \begin{cases}
\begin{align}
&1 &&\text{si } x \in \mathbb{Q} \\
&-1 &&\text{si } x \not \in \mathbb{Q}
\end{align}
\end{cases}
$$
$$
g(x) = \begin{cases}
\begin{align}
&x &&\text{si } x \in \mathbb{Q} \\
&-x &&\text{si } x \not \in \mathbb{Q}
\end{align}
\end{cases}
$$
$$
h(x) = \begin{cases}
\begin{align}
&x^{2} &&\text{si } x \in \mathbb{Q} \\
&-x^{2} &&\text{si } x \not \in \mathbb{Q}
\end{align}
\end{cases}
$$
Sobre la continuidad de $f$, podemos decir que la misma es discontinua en todos los puntos de $\mathbb{R}$.
- $f$ discontinua en todos los puntos de $\mathbb{R}$.

Sobre la continuidad de $g$, podemos decir que es discontinua en todos los puntos de $\mathbb{R}$, menos en 0, donde es continua (por Sándwich, puesto que como siempre está entre $x$ y $-x$, cuando $x \to 0$, entonces $g(x) \to 0$).
- $g$ es continua en $x_{0} = 0$
- $g$ es discontinua en todos los otros puntos de $\mathbb{R}$.
Sin embargo, ==$g$ no es derivable en $x_{0} = 0$== (no lo demostraremos).

Sobre la continuidad de $h$, podemos decir que es discontinua en todos los puntos de $\mathbb{R}$, menos en 0, donde es continua (mismo argumento que para $g$).
- $h$ es discontinua en todos los otros puntos de $\mathbb{R}$.
- $h$ es continua en $x_{0} = 0$ y derivable.
$$
\frac{h(x) - h(x_{0})}{x - x_{0}} = \frac{h(x)}{x} = \underbrace{ g(x) }_{ \underset{ x \to 0} \to 0 }
$$
En conclusión: $h'(0) = 0$.

De esta forma, definimos una función que es totalmente discontinua con una excepción, donde también es derivable.

---
A continuación, estudiaremos propiedades algebraicas de la derivada.
## Propiedades algebraicas

### Proposición

> [!Proposición]
> Sean $f, g : I \to \mathbb{R}$ y $x_{0} \in I$. Si $f$ y $g$ son derivables en $x_{0}$, entonces:
> $$
> \begin{align}
> &1. &&f + g \text{ es derivable en } x_{0} \text{ y } (f + g)'(x_{0}) = f'(x_{0}) + g'(x_{0}) \\ \\
> 
> &2. &&f - g \text{ es derivable en } x_{0} \text{ y } (f - g)'(x_{0}) = f'(x_{0}) - g'(x_{0}) \\ \\
> 
> &3. &&fg \text{ es derivable en } x_{0} \text{ y } (fg)'(x_{0}) = f'(x_{0})g(x_{0}) + f(x_{0})g'(x_{0})
> \end{align}
> $$
> Además, si $g$ no se anula en un entorno de $x_{0}$, entonces $\frac{f}{g}$ es derivable en $x_{0}$ y
> $$
> \left( \frac{f}{g} \right)'(x_{0}) = \frac{f'(x_{0})g(x_{0}) - f(x_{0})g'(x_{0})}{g^{2}(x_{0})}
> $$

Demostraremos las fórmulas a continuación. No utilizaremos $\epsilon$ ni $\delta$ ya que tenemos los suficientes teoremas y proposiciones para poder prescindir de los mismos.

**Demostración**
1. **Suma**
$$
\frac{f(x) + g(x) - (f(x_{0}) + g(x_{0}))}{x - x_{0}} = \underbrace{ \frac{f(x) - f(x_{0})}{x - x_{0}} }_{ \underset{ x \to x_{0} } \to f'(x_{0}) } + \underbrace{ \frac{g(x) - g(x_{0})}{x - x_{0}} }_{ \underset{ x \to x_{0} } \to g'(x_{0}) }
$$
Por suma de límites:
$$
\lim_{ x \to x_{0} } \frac{f(x) + g(x) - (f(x_{0}) + g(x_{0}))}{x - x_{0}} = f'(x_{0}) + g'(x_{0})
$$

2. **Resta**
Ídem que la suma.

De esta forma, el cociente incremental de la suma de las funciones equivale a la suma de los cocientes incrementales.

3. **Producto**
En este caso, no podemos aplicar la misma técnica:
$$
\frac{f(x)g(x) - f(x_{0})g(x_{0})}{x - x_{0}} \neq \frac{f(x) - f(x_{0})}{x - x_{0}} \times \frac{g(x) - g(x_{0})}{x - x_{0}}
$$
No podemos decir que el cociente incremental del producto es el producto de los cocientes incrementales.

Utilizaremos la misma fórmula usada para demostrar que el límite de un producto es el producto de los límites. Para que la formula funcione es importante que una función tome el $x$ y la otra tome $x_{0}$.
$$
\begin{align}
&= \frac{(f(x) - f(x_{0})) g(x) + f(x_{0}) (g(x) - g(x_{0}))}{x - x_{0}} \\
&= \underbrace{ \frac{f(x) - f(x_{0})}{x - x_{0}} }_{ \underset{ x \to x_{0} } \to f'(x_{0}) } \times \underbrace{ g(x) }_{ \underset{ x \to x_{0} } \to g(x_{0}) } + \underbrace{ f(x_{0}) }_{ = f(x_{0}) } \times \underbrace{ \frac{g(x) - g(x_{0})}{x - x_{0}} }_{ \underset{ x \to x_{0} } \to g'(x_{0}) } \\
&= f'(x_{0}) \times g(x) + f(x_{0}) \times g'(x_{0})
\end{align}
$$
Como vemos, la demostración tiene un paso que requiere cierta creatividad matemática.

4. **Cociente**
$$
\frac{\frac{f(x)}{g(x)} - \frac{f(x_{0})}{g(x_{0})}}{x - x_{0}}
$$
$$
\begin{align}
&= \frac{f(x)\frac{1}{g(x)} - f(x_{0})\frac{1}{g(x_{0})}}{x - x_{0}} \\
&= \frac{(f(x) - f(x_{0})) \frac{1}{g(x)} + f(x_{0}) \left( \frac{1}{g(x)} - \frac{1}{g(x_{0})} \right)}{x - x_{0}} \\
&= \frac{f(x) - f(x_{0})}{x - x_{0}} \times \frac{1}{g(x)} + f(x_{0}) \times \frac{\frac{1}{g(x)} - \frac{1}{g(x_{0})}}{x - x_{0}} \\
&= \frac{f(x) - f(x_{0})}{x - x_{0}} \times  \frac{1}{g(x)} + f(x_{0}) \times \frac{\frac{g(x_{0}) - g(x)}{g(x)g(x_{0})}}{x - x_{0}} \\
&= \frac{f(x) - f(x_{0})}{x - x_{0}} \times  \frac{1}{g(x)} + f(x_{0}) \times \frac{g(x_{0}) - g(x)}{g(x)g(x_{0}) \times (x - x_{0})} \\
&= \underbrace{ \frac{f(x) - f(x_{0})}{x - x_{0}} }_{ \underset{ x \to x_{0} } \to f'(x_{0}) } \times \frac{1}{g(x)} + f(x_{0}) \times \underbrace{ \frac{g(x_{0}) - g(x)}{(x - x_{0})} }_{ \underset{ x \to x_{0} } \to -g'(x_{0}) } \times \frac{1}{g(x)g(x_{0})} \\
&= f'(x_{0}) \times \frac{1}{g(x)} + f(x_{0}) \times (-g'(x_{0})) \times  \frac{1}{g(x)g(x_{0})} \\
&= f'(x_{0}) \times \frac{g(x_{0})}{g^{2}(x_{0})} + f(x_{0}) \times (-g'(x_{0})) \times  \frac{1}{g(x)g(x_{0})} \\
&= f'(x_{0}) \times \underbrace{ \frac{g(x)}{g^{2}(x)} }_{ \underset{ x \to x_{0} } \to \frac{g(x_{0})}{g^{2}(x_{0})} } + f(x_{0}) \times (-g'(x_{0})) \times \underbrace{ \frac{1}{g(x)g(x_{0})} }_{ \underset{ x \to x_{0} } \to \frac{1}{g^{2}(x_{0})} } \\
&= f'(x_{0}) \times \frac{g(x_{0})}{g^{2}(x_{0})} + f(x_{0}) \times (-g'(x_{0})) \times \frac{1}{g^{2}(x_{0})} \\
&= \frac{ f'(x_{0}) \times g(x_{0}) - f(x_{0}) \times g'(x_{0}) }{ g^{2}(x_{0}) }
\end{align}
$$

Esta demostración es un excelente ejemplo de que, para las demostraciones, la creatividad es un factor fundamental. Muchas veces se necesita encontrar la forma correcta de expresar un termino para lograr demostrar una propiedad, fórmula, etc.

Hasta aquí las propiedades algebraicas de la derivada.

---
Cuando abordamos límite, comenzamos estudiando la noción de límite, luego la continuidad en un punto, luego la continuidad en un intervalo. Seguiremos el mismo modelo para la derivabilidad. Ya abordamos la derivabilidad en un punto. Continuaremos estudiando que son las funciones derivables y algunos ejemplos:
## Funciones derivables

> [!Definición - Funciones derivables]
> $f : I \to \mathbb{R}$ es derivable en $I$ cuando es derivable en cada punto de $I$.
> 
> Se define la <u>función derivada</u> $f' : I \to \mathbb{R}$ por
> $$
> f'(x_{0}) := \lim_{ x \to x_{0} } \frac{f(x) - f(x_{0})}{x - x_{0}} \qquad \text{para todo } x_{0} \in I
> $$

Además, las propiedades algebraicas que definimos en un punto, también se extienden a las funciones.

### Proposición

Si $f, g : I \to \mathbb{R}$ son derivables en $I$, entonces
$$
\begin{align}
&1. &&(f + g)' = f' + g' \\
&2. &&(f - g)' = f' - g' \\
&3. &&(\lambda f)' = \lambda f' &&(\lambda \in \mathbb{R}) \\
&4. &&(fg)' = f'g + fg' \\
&5. &&\left( \frac{f}{g} \right)' \frac{f'g - fg'}{g^{2}} &&(\text{si } g(x) \neq 0 \qquad \forall x \in I)
\end{align}
$$

Podemos decir que la derivada es una transformación lineal entre el espacio de las transformación derivables y el espacio de las funciones.

Lo interesante aquí es que el espacio de las funciones derivables es un subespacio vectorial del espacio de las funciones continuas (el cual es un subespacio vectorial de las funciones localmente integrables, siendo un subespacio vectorial del espacio de todas las funciones):

Si una función es derivables, es derivable en todos los puntos, entonces es continua en todos los puntos, entonces es continua.
En conclusión: toda función derivable en un intervalo es continua en dicho intervalo.

Por esta razón, todos los teoremas sobre las funciones continuas también se aplican a las funciones continuas. Sin embargo, la derivada de una función derivable no siempre es continua.


Ahora, derivaremos (calcular la derivada) funciones usuales:

### Ejemplos

#### Ejemplo 1
$$
f(x) = x^{p} \qquad (p \in \mathbb{N})
$$
El caso $p = 1$ es trivial, ya que se trata de la identidad y si operamos utilizando la definición, llegamos a la conclusión de que $f'(x_{0}) = 1$.

Se observa que si $p \geq 1$, tenemos que
$$
x^{p} - x_{0}^{p} = (x - x_{0}) \sum_{k = 0}^{p - 1} x^{k} x_{0}^{p - 1 - k}
$$
$$
\frac{x^{p} - x_{0}^{p}}{x - x_{0}} = \sum_{k = 0}^{p - 1} \underbrace{ x^{k} x_{0}^{p - 1 - k} }_{ \underset{ x \to x_{0} } \to x_{0}^{k} x_{0}^{p - 1 - k} = x_{0}^{p - 1} } \underset{ x \to x_{0} } \longrightarrow p x_{0}^{p - 1}
$$
Esto solo funciona para $p \geq 1$ (también funciona para $p = 0$, pues se anula todo).

La fórmula anterior fue vista en el curso anteriormente, con otras variables:
$$
x^{p} - y^{p} = (x - y) \sum_{k = 0}^{p - 1} x^{k} y^{p - 1 - k}
$$

Continuamos con la función $\sin$.
#### Ejemplo 2
$$
f(x) = \sin x
$$
**Caso: $x_{0} = 0$**
$$
\frac{\sin x - \sin 0}{x - 0} = \frac{\sin x}{x} \underset{ x \to x_{0} } \longrightarrow 1
$$
$$
\sin'(0) = 1
$$
De esta forma, sabemos que para $x = 0$, la función $\sin x$ tiene pendiente 1. De esta manera, la tangente a la función $\sin x$ para $x = 0$ tiene pendiente 1.

Ahora, veremos que gracias a las formulas de trigonometría, se puede extender este resultado a toda función $\sin$.

**Caso: $x \in \mathbb{R}$ cualquiera**
$$
\frac{\sin(x + h) - \sin(x)}{h} = \frac{\sin x \cos h + \cos x \sin h - \sin x}{h}
$$
$$
\begin{align}
&= \underbrace{ \sin x \left( \frac{\cos h - 1}{h} \right) }_{ \underset{ h \to 0 } \to \sin x \times 0 } + \underbrace{ \cos x \frac{\sin h}{h} }_{ \underset{ h \to 0 } \to \cos x \times 1 } \\
&= \sin x \times 0 + \cos x \times 1 = \cos x
\end{align}
$$
$$
\implies \sin' x = \cos x
$$

Haremos lo mismo para la función $\cos$:
$$
f(x) = \cos x
$$
**Caso: $x \in \mathbb{R}$ cualquiera
$$
\frac{\cos(x + h) - \cos(x)}{h} = \frac{\cos x \cos h - \sin x \sin h - \cos x}{h}
$$
$$
\begin{align}
&= \underbrace{ \cos x \left( \frac{\cos h - 1}{h} \right) }_{ \underset{ h \to 0 } \to \cos x \times 0 } - \underbrace{ \sin x \frac{\sin h}{h} }_{ \underset{ h \to 0 } \to \sin x \times 1 } \\
&= \cos x \times 0 - \sin x \times 1
\end{align}
$$
$$
\implies \cos' x = -\sin x
$$

Por último, abordaremos la función $\log$.
#### Ejemplo 3
$$
f : \mathbb{R}^{+} \to \mathbb{R} \qquad f(x) = \log x
$$
**Caso: $x_{0} = 1$**
$$
\frac{\log(x) - \log(1)}{x - 1} = \frac{\log x}{x - 1}
$$Para resolver esto, utilizaremos la siguiente desigualdad, vista durante el capítulo de integrales:
$$
\underbrace{ 1 - \frac{1}{x} }_{ \frac{x - 1}{x} } \leq \log x \leq x - 1
$$
De esta forma, si divido todo entre $x - 1$:
$$
\underbrace{ \frac{1}{x} }_{ \underset{ x \to 1 } \to 1 } \leq \frac{\log x}{x - 1} \leq \underbrace{ 1 }_{ \underset{ x \to 1 } \to 1 }
$$
De esta forma, por Sándwich:
$$
\underbrace{ \frac{\log x}{x - 1} }_{ \underset{ x \to 1 } \to 1 }
$$
Esto demuestra que la función $\log$ es continua, pero además es derivable, al menos para $x_{0} = 1$.

Conclusión:
$$
\log'(1) = 1
$$
La tangente de la función $\log$ en el punto $x = 1$.

Ahora, demostraremos que la función es derivable, cosa que es más sencilla utilizando el teorema fundamental, pero como aún no ha sido abordado, prescindiremos del mismo:

**Caso: $x_{0} \in \mathbb{R}$ fijado**
$$
\frac{\log(x) - \log(x_{0})}{x - x_{0}} = \frac{\log\left(x_{0} \times \frac{x}{x_{0}} \right) - \log(x_{0})}{x - x_{0}} = \frac{\log(x_{0}) + \log \left(\frac{x}{x_{0}} \right) - \log(x_{0})}{x - x_{0}}
$$
$$
= \frac{\cancelto{ 0 }{ \log\left( \frac{x_{0}}{x_{0}} \right) } + \log \left(\frac{x}{x_{0}} \right)}{x - x_{0}} = \frac{\log\left( \frac{x}{x_{0}} \right)}{x - x_{0}} = \frac{1}{x_{0}} \times \frac{\log\left( \frac{x}{x_{0}} \right)}{\frac{x}{x_{0}} - 1} \underbrace{ \longrightarrow }_{ \underset{ x \to 1 } \to 1 } \frac{1}{x_{0}} \times 1
$$
Cuando $x \to x_{0}$, el cociente $\frac{x}{x_{0}}$ tiende a 1. Considerando esto, y tomando como referencia el caso anterior resuelto mediante Sándwich, podemos ver que aquí se nos presenta exactamente el mismo caso, simplemente utilizando como variable a $\frac{x}{x_{0}}$ (por cambio de variable). Entonces:
$$
\underbrace{ \frac{\log \frac{x}{x_{0}}}{\frac{x}{x_{0}} - 1} }_{ \underset{ x \to x_{0} } \to 1 }
$$

Es así que podemos concluir que:
$$
\log'(x) = \frac{1}{x}
$$

Este es un claro ejemplo de como utilizamos los diferentes resultados de límites para llegar al resultado deseado. Puntualmente usamos la compuesta de derivadas: combinamos las funciones $\log$ con $\frac{x}{x_{0}}$, siendo $x_{0}$ una constante.


