# 1 - Teorema fundamental
Durante toda esta sección, deberemos tener en cuenta muchas propiedades y conceptos básicos. A continuación se listan algunos de estos:

> [!Teorema fundamental]
> Sea $f : [a, b] \to \mathbb{R}$ integrable, y $F : [a, b] \to \mathbb{R}$ definida por
> $$
> F(x) = \int_{a}^{x} f(t) \space dt
> $$
> Entonces, si $f$ es continua en $x_{0}$, $F$ es derivable en $x_{0}$ y
> $$
> F'(x_{0}) = f(x_{0})
> $$

> [!Primitiva - Definición]
> Dada $f : I \to \mathbb{R}$, decimos que $F : I \to \mathbb{R}$ es una primitiva de $f$ si
> $$
> F'(x) = f(x) \qquad \forall x \in I
> $$

> [!Teorema]
> Sea $\alpha, \beta : [c, d] \to [a, b]$ derivables,, y $f : [a, b] \to \mathbb{R}$ continua, entonces
> $$
> G(x) = \int_{\alpha(x)}^{\beta(x)} f(t) \space dt
> $$
> es derivable, y
> $$
> G'(x) = f(\beta(x)) \beta'(x) - f(\alpha(x)) \alpha'(x)
> $$
> (en base a la regla de la cadena).

> [!Regla de Barrow]
> Sea $f$ continua y $F$ primitiva de $f$:
> $$
> \int_{a}^{b} f(t) \space dt = F(b) - F(a)
> $$

## Ejercicio 7.1.1
Una parte por fila.

Para resolver este ejercicio, tenemos que tomar como referencia lo que dice el teorema fundamental: Si tenemos una función definida como el área bajo una función:
$$
f(x) = \int_{a}^{x} g(t) \space dt
$$
Entonces, la derivada de esa función es simplemente la función del integrando evaluada en el límite superior:
$$
f'(x) = g(x)
$$

### Parte a)
$$
f(x) = \int_{1}^{x} \sqrt{ t^{2} - t + 1 } \space dt
$$
$$
\implies f'(x) = \sqrt{ x^{2} - x + 1 }
$$
No es necesario aplicar el segundo teorema, ya que los extremos de la integral no son funciones (únicamente el extremo superior, pero igualmente se trata de la función $x$, por lo que al aplicar la regla de la cadena, obtenemos 1 y nos queda el término anterior, cancelándose el otro término al anularse).

### Parte c)
$$
f(x) = \int_{\cos(x)}^{3} \sqrt{ t^{2} - t + 1 } \space dt
$$
En este caso, es conveniente aplicar el segundo teorema para resolver el ejercicio correctamente:
$$
\begin{align}
\implies f'(x) &= \cancel{ \sqrt{ 3^{2} - 3 + 1 } \cdot (3)' } - \sqrt{ (\cos(x))^{2} - \cos(x) + 1 } \cdot (\cos(x))' \\
&= \sin(x) \sqrt{ (\cos(x))^{2} - \cos(x) + 1 }
\end{align}
$$
En conclusión:
$$
f'(x) = \sin(x) \sqrt{ (\cos(x))^{2} - \cos(x) + 1 }
$$

### Parte e)
$$
f(x) = \int_{e^{x}}^{2} \frac{t^{7}}{1 + t^{4}} \space dt
$$
$$
\begin{align}
\implies f'(x) &= \cancel{ \frac{2^{7}}{1 + 2^{4}} \cdot (2)' } - \frac{(e^{x})^{7}}{1 + (e^{x})^{4}} \cdot (e^{x})' \\
&= -e^{x}\frac{(e^{x})^{7}}{1 + (e^{x})^{4}} \\
&= -e^{x}\frac{e^{7x}}{1 + e^{4x}} \\
&= -\frac{e^{8x}}{1 + e^{4x}}
\end{align}
$$
En conclusión:
$$
f'(x) = -\frac{e^{8x}}{1 + e^{4x}}
$$

### Parte h)
$$
f(x) = \int_{\sqrt{ x^{2} + 1 }}^{3x} \frac{\sin(t)}{3 + e^{t}} \space dt
$$
$$
\begin{align}
\implies f'(x) &= \frac{\sin(3x)}{3 + e^{3x}} \cdot (3x)' - \frac{\sin(\sqrt{ x^{2} + 1 })}{3 + e^{\sqrt{ x^{2} + 1 }}} \cdot (\sqrt{ x^{2} + 1 })' \\
&= \frac{3\sin(3x)}{3 + e^{3x}} - \frac{\sin(\sqrt{ x^{2} + 1 })}{3 + e^{\sqrt{ x^{2} + 1 }}} \cdot \frac{1}{2\sqrt{ x^{2} + 1 }} \cdot (x^{2} + 1)' \\
&= \frac{3\sin(3x)}{3 + e^{3x}} - \frac{\sin(\sqrt{ x^{2} + 1 })}{3 + e^{\sqrt{ x^{2} + 1 }}} \cdot \frac{1}{\cancel{ 2 }\sqrt{ x^{2} + 1 }} \cdot \cancel{ 2 }x \\
&= \frac{3\sin(3x)}{3 + e^{3x}} - \frac{\sin(\sqrt{ x^{2} + 1 })}{3 + e^{\sqrt{ x^{2} + 1 }}} \cdot \frac{x}{\sqrt{ x^{2} + 1 }} \\
&= \frac{3\sin(3x)}{3 + e^{3x}} - \frac{x\sin(\sqrt{ x^{2} + 1 })}{\sqrt{ x^{2} + 1 } (3 + e^{\sqrt{ x^{2} + 1 }})}
\end{align}
$$
En conclusión:
$$
f'(x) = \frac{3\sin(3x)}{3 + e^{3x}} - \frac{x\sin(\sqrt{ x^{2} + 1 })}{\sqrt{ x^{2} + 1 } (3 + e^{\sqrt{ x^{2} + 1 }})}
$$

---
## Ejercicio 7.1.4
Una parte por fila.

### Parte b)
$$
\int_{x}^{1} f(t) \space dt = \cos ^{2}(x) + C
$$
Haremos el desarrollo a la inversa:
$$
\begin{align}
(\cos ^{2}(x) + C)' &= \cancel{ f(1) \cdot (1)' } - f(x) \cdot (x)' \\
2\cos(x) \cdot (\cos(x))' &= -f(x) \cdot 1 \\
2\cos(x) \cdot (-\sin(x)) &= -f(x) \\
-2\cos(x) \sin(x) &= -f(x) \\
2\cos(x) \sin(x) &= f(x)
\end{align}
$$
Para hallar el valor de $c$, evaluamos el valor de $x = 1$, ya que de esta forma se anula la integral y facilita los cálculos:
$$
\begin{align}
\int_{x}^{1} f(t) \space dt = \cos ^{2}(x) + C \implies \int_{1}^{1} f(t) \space dt &= \cos ^{2}(1) + C \\
0 &= \cos ^{2}(1) + C \\
-\cos ^{2}(1) &= c
\end{align}
$$

En conclusión:
$$
\begin{align}
&f(x) = 2\cos(x) \sin(x) \\
&c = -\cos ^{2}(1)
\end{align}
$$

### Parte c)
$$
\int_{x}^{1} f(t) \space dt = \sqrt{ x^{4} + 1 } + C
$$
Haremos el desarrollo a la inversa:
$$
\begin{align}
(\sqrt{ x^{4} + 1 } + C)' &= \cancel{ f(1) \cdot (1)' } - f(x) \cdot (x)' \\
\frac{1}{2\sqrt{ x^{4} + 1 }} \cdot (x^{4} + 1)' &= -f(x) \cdot 1 \\
\frac{1}{2\sqrt{ x^{4} + 1 }} \cdot 4x^{3} &= -f(x) \\
\frac{2x^{3}}{\sqrt{ x^{4} + 1 }} &= -f(x) \\
-\frac{2x^{3}}{\sqrt{ x^{4} + 1 }} &= f(x)
\end{align}
$$
Para hallar el valor de $c$, evaluamos el valor de $x = 1$, ya que de esta forma se anula la integral y facilita los cálculos:
$$
\begin{align}
\int_{x}^{1} f(t) \space dt = \sqrt{ x^{4} + 1 } + C \implies \int_{1}^{1} f(t) \space dt &= \sqrt{ 1^{4} + 1 } + C \\
0 &= \sqrt{ 2 } + C \\
-\sqrt{ 2 } &= c
\end{align}
$$

En conclusión:
$$
\begin{align}
&f(x) = 2\sin(x) \cos(x) \\
&c = -\sqrt{ 2 }
\end{align}
$$

### Parte f)
$$
\int_{c}^{x} f(t) \space dt = \sin ^{2}(x) + 1
$$
Haremos el desarrollo a la inversa:
$$
\begin{align}
(\sin ^{2}(x) + 1)' &= f(x) \cdot (x)' - \cancel{ f(c) \cdot (c)' } \\
2\sin(x) \cdot (\sin(x))' &= f(x) \cdot 1 \\
2\sin(x) \cdot \cos(x) &= f(x) \\
2\sin(x) \cos(x) &= f(x)
\end{align}
$$
Para hallar el valor de $c$, evaluamos el valor de $x = c$, ya que de esta forma se anula la integral y facilita los cálculos:
$$
\begin{align}
\int_{c}^{x} f(t) \space dt = \sin ^{2}(x) + 1 \implies \int_{c}^{c} f(t) \space dt &= \sin ^{2}(c) + 1 \\
0 &= \sin ^{2}(c) + 1 \\
\sin ^{2}(c) &= -1
\end{align}
$$
Sin embargo, no existe un numero real $c$ tal que $\sin ^{2}(c) = -1$, puesto que $\sin ^{2}(x) \in [0, 1], \forall x \in \mathbb{R}$.

En conclusión:
$$
\begin{align}
&f(x) = 2\sin(x) \cos(x) \\
&\text{No existe un } c \in \mathbb{R} \text{ tal que } \sin ^{2}(c) = -1
\end{align}
$$




---
## Ejercicio 7.1.5
Una parte por fila.

### Parte a)
$$
\int_{1}^{\cos(x)} f(t) \space dt = 2 \sin ^{2}(x)
$$
Haremos un desarrollo similar al ejercicio anterior. Como se cumple la igualdad anterior, se tiene que cumplir que
$$
\begin{align}
(2 \sin ^{2}(x))' &= f(\cos(x)) \cdot (\cos(x))' - \cancel{ f(1) \cdot (1)' } \\
2 (\sin ^{2}(x))' &= f(\cos(x)) \cdot (-\sin(x)) \\
2 \cdot 2 \sin(x) \cdot (\sin(x))' &= -f(\cos(x)) \cdot \sin(x) \\
4 \cancel{ \sin(x) } \cdot \cos(x) &= -f(\cos(x)) \cdot \cancel{ \sin(x) } \\
4 \cos(x) &= -f(\cos(x)) \\
-4 \cos(x) &= f(\cos(x)) \implies f(x) = -4x
\end{align}
$$

En conclusión:
$$
f(x) = -4x \text{ tal que } \int_{1}^{\cos(x)} -4t \space dt = 2 \sin ^{2}(x)
$$

Para confirmar la resolución, podemos aplicar la regla de Barrow:
$$
\int_{a}^{b} f(t) \space dt = F(b) - F(a)
$$
$$
\begin{align}
\int_{1}^{\cos(x)} -4t \space dt &= -2t^{2} |_{1}^{\cos(x)} \\
&= -2\cos ^{2}(x) - (-2 \cdot 1^{2}) \\
&=  -2\cos ^{2}(x) + 2
\end{align}
$$
Sabiendo que $\cos ^{2}(x) = 1 - \sin ^{2}(x)$
$$
\begin{align}
-2\cos ^{2}(x) + 2 &= -2(1 - \sin ^{2}(x)) + 2 \\
&= \cancel{ -2 } + 2\sin ^{2}(x) + \cancel{ 2 } \\
&= 2\sin ^{2}(x)
\end{align}
$$
Así, confirmamos que la resolución fue correcta.

### Parte d)
$$
\int_{0}^{x^{2}} f(t) \space dt = x^{2} \cos(x)
$$
Haremos un desarrollo similar al ejercicio anterior. Como se cumple la igualdad anterior, se tiene que cumplir que
$$
\begin{align}
(x^{2} \cos(x))' &= f(x^{2}) \cdot (x^{2})' - \cancel{ f(0) \cdot (0)' } \\
2x \cos(x) + x^{2} (-\sin(x)) &= f(x^{2}) \cdot 2x \\
2x \cos(x) - x^{2} \sin(x) &= 2xf(x^{2}) \\
x(2 \cos(x) - x \sin(x)) &= 2xf(x^{2}) \\
\frac{x(2 \cos(x) - x \sin(x))}{2x} &= f(x^{2}) \\
\frac{2 \cos(x) - x \sin(x)}{2} &= f(x^{2}) \implies f(x) = \frac{2 \cos(\sqrt{ x }) - \sqrt{ x } \sin(\sqrt{ x })}{2}
\end{align}
$$

En conclusión:
$$
f(x) = \frac{2 \cos(\sqrt{ x }) - \sqrt{ x } \sin(\sqrt{ x })}{2} \text{ tal que } \int_{0}^{x^{2}} \frac{2 \cos(\sqrt{ t }) - \sqrt{ t } \sin(\sqrt{ t })}{2} \space dt = x^{2} \cos(x)
$$

Aclaración: Podemos ver el último paso para hallar $f(x)$, como una sustitución lógica $t = x^{2}$, lo que implica que $x = \sqrt{ t }$.

---
## Ejercicio 7.1.7
$$
F(x) = \frac{1}{2} \int_{1}^{x^{2}} e^{\frac{-t^{2}}{2}} \space dx
$$
Tenemos que determinar el valor de $(F^{-1}(x))'$ evaluada en $x = 0$.

Ahora, tendremos que considerar la regla para derivar funciones inversas:

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

Primero que nada, recordemos que la función inversa intercambio el dominio y el recorrido. De esta forma:
$$
f(x) = y \implies f^{-1}(y) = x
$$
Entonces:
$$
F^{-1}(0) = x \implies F(x) = 0
$$
Tenemos que encontrar un valor de $x$ para el cual $F(x) = 0$.
Conociendo la definición de $F$, tenemos que igualar los extremos de la integral. De esta manera, consideraremos $x = \pm1$:
$$
\begin{align}
F(1) &= \frac{1}{2} \int_{1}^{1^{2}} e^{\frac{-t^{2}}{2}} \space dx \\
&= \frac{1}{2} \cdot 0 \\
&= 0
\end{align}
$$
Entonces:
$$
F^{-1}(0) = 1
$$
Ahora, simplemente tenemos que determinar la derivada de $F$:
$$
\begin{align}
F'(x) &= \left( \frac{1}{2} \int_{1}^{x^{2}} e^{\frac{-t^{2}}{2}} \space dx \right)' \\
&= \frac{1}{2} \left( \int_{1}^{x^{2}} e^{\frac{-t^{2}}{2}} \space dx \right)' \\
&= \frac{1}{2} \left(e^{\frac{-(x^{2})^{2}}{2}} \cdot (x^{2})' - \cancel{ e^{\frac{-1^{2}}{2}} \cdot (1)' } \right) \\
&= \frac{1}{2} e^{\frac{-(x^{2})^{2}}{2}} \cdot \cancel{ 2 }x \\
&= e^{\frac{-x^{4}}{2}} \cdot x \\
&= xe^{\frac{-x^{4}}{2}}
\end{align}
$$
Ahora, podemos aplicar la regla enunciada al principio:
$$
\begin{align}
(f^{-1})'(y) = \frac{1}{f'(f^{-1}(y))} \implies (F^{-1})'(0) &= \frac{1}{1 \cdot e^{\frac{-1^{4}}{2}}} \\
&= \frac{1}{e^{-\frac{1}{2}}} \\
&= \frac{1}{\frac{1}{\sqrt{ e }}} \\
&= \sqrt{ e }
\end{align}
$$
En conclusión, la derivada de la función $F^{-1}$ en 0 vale $\sqrt{ e }$:
$$
(F^{-1})'(0) = \sqrt{ e }
$$


---
## Ejercicio 7.1.9

### Parte a)
$$
\int_{a}^{x} f(t) \space dt + \int_{f(a)}^{f(x)} f^{-1}(t) \space dt - x f(x) + af(a) = 0 \qquad \forall x \in [a, b]
$$
Como el ejercicio se trata de demostrar que la expresión es igual a 0 para todo $x$, podemos demostrar que su derivada es 0 (siendo una función constante), y luego verificar que el valor de la constante es es 0 evaluando en un punto (la función es la constante 0).

Para esto, definamos una función auxiliar $G$:
$$
G(x) = \int_{a}^{x} f(t) \space dt + \int_{f(a)}^{f(x)} f^{-1}(t) \space dt - x f(x) + a f(a)
$$
Ahora, queremos confirmar que $G'(x) = 0$ para todo $x \in [a, b]$:
$$
G'(x) = 0 \implies \left( \int_{a}^{x} f(t) \space dt + \int_{f(a)}^{f(x)} f^{-1}(t) \space dt - x f(x) + a f(a) \right)' = 0
$$
Derivamos parte por parte:
$$
\left( \int_{a}^{x} f(t) \space dt  \right)' = f(x)
$$
$$
\begin{align}
\left( \int_{f(a)}^{f(x)} f^{-1}(t) \space dt  \right)' &= \overbrace{ f^{-1}(f(x)) }^{ =x } \cdot (f(x))' - \cancel{ \overbrace{ f^{-1}(f(a)) }^{ = a } \cdot (f(a))' } \\
&= xf'(x)
\end{align}
$$
$$
\begin{align}
\left( x f(x)  \right)' &= (x)' f(x) + x f'(x) \\
&= f(x) + x f'(x)
\end{align}
$$
$$
\begin{align}
\left( a f(a)  \right)' &= \cancel{ (a)' f(a) } + \cancel{ a (f(a))' } \\
&= 0
\end{align}
$$
De esta forma:
$$
\begin{align}
G'(x) = f(x) + x f'(x) - (f(x) + x f'(x)) &= 0 \\
\cancel{ f(x) } + x f'(x) - \cancel{ f(x) } - x f'(x) &= 0 \\
\cancel{ x f'(x) } - \cancel{ x f'(x) } &= 0 \\
0 &= 0
\end{align}
$$
Finalmente, determinamos que la derivada de la función $G$ es 0, por lo que la función es constante durante todo su intervalo.

Ahora, tenemos que determinar la imagen para cualquiera de los valores del intervalo $[a, b]$. En este caso, utilizaremos $x = a$ para anular las integrales:
$$
\begin{align}
\cancel{ \int_{a}^{a} f(t) \space dt } + \cancel{ \int_{f(a)}^{f(a)} f^{-1}(t) \space dt } - a f(a) + a f(a) &= 0 \\
\cancel{ -a f(a) } + \cancel{ a f(a) } &= 0 \\
0 &= 0
\end{align}
$$
En conclusión, probamos que el enunciado
$$
\int_{a}^{x} f(t) \space dt + \int_{f(a)}^{f(x)} f^{-1}(t) \space dt - x f(x) + af(a) = 0 \qquad \forall x \in [a, b]
$$
es verdadero.

### Parte b)
Tenemos que calcular
$$
\int_{1}^{2} \log(t) \space dt
$$
en base al resultado anterior.

Primero que nada, denotamos $f(x) = \log(x)$, tal que
$$
f^{-1}(x) = e^{x}
$$
De esta manera, y tomando como referencia la expresión anterior:
$$
\int_{1}^{x} \log(t) \space dt + \int_{\log(1)}^{\log(x)} e^{t} \space dt - x \log(x) + \log(1) = 0 \qquad \forall x \in [1, 2]
$$
Sabemos que $\log(1) = 0$:
$$
\int_{1}^{x} \log(t) \space dt + \int_{0}^{\log(x)} e^{t} \space dt - x \log(x) = 0
$$
Ahora, conocemos una primitiva de $e^{x}$: $e^{x}$, ya que $(e^{x})' = e^{x}$. Por lo tanto, sabemos que $e^{x} = \int_{a}^{x} e^{t} \space dt$. Sustituyendo en los valores anteriores y aplicando Barrow:
$$
\begin{align}
\int_{0}^{\log(x)} e^{t} \space dt &= e^{\log(x)} - e^{0} \\
&= e^{\log(x)} - 1
\end{align}
$$
De esta forma:
$$
\int_{1}^{x} \log(t) \space dt + e^{\log(x)} - 1 - x \log(x) = 0
$$
Ahora, despejamos la integral:
$$
\int_{1}^{x} \log(t) \space dt = -e^{\log(x)} + 1 + x \log(x)
$$
Nos queda sustituir $x = 2$. En conclusión:
$$
\int_{1}^{2} \log(t) \space dt = 2 \log(2) - e^{\log(2)} + 1
$$
Sabiendo que $e^{\log(x)} = x$, ya que son funciones inversas:
$$
\begin{align}
\int_{1}^{2} \log(t) \space dt &= 2 \log(2) - 2 + 1 \\
&= 2 \log(2) - 1
\end{align}
$$

---
## Ejercicio 7.1.12
Nuevamente, consideramos para un ejercicio la fórmula para derivar funciones inversas:
$$
(f^{-1})'(x) = \frac{1}{f'(f^{-1}(x))}
$$
De esta forma, podemos determinar las derivadas de las inversas trigonométricas:

$$
\begin{align}
\tan'(x) &= \left( \frac{\sin(x)}{\cos(x)} \right)' \\
&= \frac{\sin'(x)\cos(x) - \sin(x) \cos'(x)}{\cos ^{2}(x)} \\
&= \frac{\cos ^{2}(x) + \sin ^{2}(x)}{\cos ^{2}(x)} \\
&= \frac{1}{\cos ^{2}(x)}
\end{align}
$$
$$
\begin{align}
&\arcsin'(x) = \frac{1}{\cos(\arcsin(x))} = \frac{1}{\sqrt{ 1 - \sin ^{2}(\arcsin(x)) }} = \frac{1}{\sqrt{ 1 - x^{2} }} \\
&\arccos'(x) = -\frac{1}{\sin(\arccos(x))} = -\frac{1}{\sqrt{ 1 - \cos ^{2}(\arccos(x)) }} = -\frac{1}{\sqrt{ 1 - x^{2} }} \\
&\arctan'(x) = \frac{1}{\frac{1}{\cos ^{2}(\arctan(x))}} = \cos ^{2}(\arctan(x)) = \frac{1}{1 + \tan ^{2}(\arctan(x))} = \frac{1}{1 + x^{2}}
\end{align}
$$

### Parte a)
$$
\int_{a}^{b} \frac{1}{1 + x^{2}} \space dx
$$
$$
\frac{1}{1 + x^{2}} = \arctan'(x) = (\tan ^{-1})'(x)
$$
De esta forma, sabemos que $\arctan'(x) = (\tan ^{-1})'(x)$ es una primitiva de $\frac{1}{1 + x^{2}}$. Por lo tanto, podemos asegurar que:
$$
\begin{align}
\int_{a}^{b} \frac{1}{1 + x^{2}} \space dx &= \arctan(x) |_{a}^{b} \\
&= \arctan(b) - \arctan(a)
\end{align}
$$

En conclusión:
$$
\int_{a}^{b} \frac{1}{1 + x^{2}} \space dx = \arctan(b) - \arctan(a) = \tan ^{-1}(b) - \tan ^{-1}(a)
$$

### Parte b)
$$
\int_{a}^{b} \frac{1}{\sqrt{ 1 - x^{2} }} \space dx, \qquad a, b \in [-1, 1]
$$
$$
\frac{1}{\sqrt{ 1 - x^{2} }} = \arcsin'(x) = (\sin ^{-1})'(x)
$$
De esta forma, sabemos que $\arcsin'(x) = (\sin ^{-1})'(x)$ es una primitiva de $\frac{1}{\sqrt{ 1 - x^{2} }}$. Por lo tanto, podemos asegurar que:
$$
\begin{align}
\int_{a}^{b} \frac{1}{\sqrt{ 1 - x^{2} }} \space dx &= \arcsin(x) |_{a}^{b} \\
&= \arcsin(b) - \arcsin(a)
\end{align}
$$

En conclusión:
$$
\int_{a}^{b} \frac{1}{\sqrt{ 1 - x^{2} }} \space dx = \arcsin(b) - \arcsin(a) = \sin ^{-1}(b) - \sin ^{-1}(a)
$$

### Parte c)
$$
\int_{a}^{b} -\frac{1}{\sqrt{ 1 - x^{2} }} \space dx, \qquad a, b \in [-1, 1]
$$
$$
-\frac{1}{\sqrt{ 1 - x^{2} }} = \arccos'(x) = (\cos ^{-1})'(x)
$$
De esta forma, sabemos que $\arccos'(x) = (\cos ^{-1})'(x)$ es una primitiva de $-\frac{1}{\sqrt{ 1 - x^{2} }}$. Por lo tanto, podemos asegurar que:
$$
\begin{align}
\int_{a}^{b} -\frac{1}{\sqrt{ 1 - x^{2} }} \space dx &= \arccos(x) |_{a}^{b} \\
&= \arccos(b) - \arccos(a)
\end{align}
$$

En conclusión:
$$
\int_{a}^{b} -\frac{1}{\sqrt{ 1 - x^{2} }} \space dx = \arccos(b) - \arccos(a) = \cos ^{-1}(b) - \cos ^{-1}(a)
$$



---
## Ejercicio 7.1.13
### Parte a)
Tenemos que calcular
$$
\int_{-1}^{2} f(x) \space dx
$$
y
$$
\int_{-2}^{2} f(x) \space dx
$$
Sabiendo que $F$ es una primitiva de $f$ ($F' = f$), tenemos que utilizar $F$ y las imágenes de los puntos de interés para calcular las integrales determinadas

Al ser $F$ una primitiva, podemos tomar el enfoque de la regla de Barrow:
$$
\begin{align}
\int_{-1}^{2} f(x) \space dx &= F(x) |_{-1}^{2} \\
&= F(2) - F(-1) \\
&= 128 - (-7) \\
&= 128 + 7 \\
&= 135
\end{align}
$$
$$
\begin{align}
\int_{-2}^{2} f(x) \space dx &= F(x) |_{-2}^{2} \\
&= F(2) - F(-2) \\
&= 128 - 16 \\
&= 112
\end{align}
$$
En conclusión:
$$
\begin{align}
&\int_{-1}^{2} f(x) \space dx = 135 \\
&\int_{-2}^{2} f(x) \space dx = 112
\end{align}
$$

### Parte b)
El área de la región limitada por el gráfico de la función $f$ y el eje $Ox$ en el intervalo $[-2, 2]$ es diferente de la integral calculada anteriormente ($\int_{-2}^{2} f(x) \space dx$), ya que se solicita un área más bien geométrica (considerar todo valores positivos).

Si analizamos la gráfica de $f$, vemos que tiene una parte negativa en $[-2, -1]$ y una positiva en $[-1, 2]$. Por lo tanto, calcularemos dichas integrales por separado (tomando el valor absoluto de cada una) y las sumaremos.
$$
\begin{align}
\int_{-2}^{-1} f(x) \space dx &= F(x) |_{-2}^{-1} \\
&= F(-1) - F(-2) \\
&= -7 - 16 \\
&= -25
\end{align}
$$
$$
\int_{-1}^{2} f(x) \space dx = 135
$$
$$
\implies \left| \int_{-2}^{-1} f(x) \space dx \right| + \left| \int_{-1}^{2} f(x) \space dx \right| = |-25| + |135| = 25 + 135 = 160
$$
En conclusión, área de la región limitada por el gráfico de la función $f$ y el eje $Ox$ en el intervalo $[-2, 2]$ es 160.

### Parte c)
Para determinar la ecuación de la recta tangente al gráfico de $F$ en el punto $(1, 25)$, tenemos que determinar la pendiente de la recta, a la cual denotaremos $m$. Sabiendo que pasa por el punto $(1, 25)$, podemos desarrollar la siguiente ecuación:
$$
\begin{align}
y - y_{1} &= m(x - x_{1}) \\
y - 25 &= m(x - 1) \\
y - 25 &= mx - m \\
y &= mx - m + 25
\end{align}
$$
Ahora, calculamos $m$:
Sabemos que, como $F$ es primitiva de $f$, entonces $F' = f$. Por lo tanto:
$$
F'(1) = f(1) = 48
$$
De esta manera, la derivada en el punto $(1, 25)$ es 48. Ahora, simplemente sustituimos $m = 48$:
$$
\begin{align}
y &= mx - m + 25 \\
&= 48x - 48 + 25 \\
&= 48x - 23
\end{align}
$$
En conclusión, la ecuación de la recta tangente al gráfico de $F$ en el punto $(1, 25)$ es:
$$
y = 48x - 23
$$


---
## Ejercicio 7.1.14
Una parte por fila.

Básicamente, tenemos que aplicar la regla de Barrow para calcular las integrales propuestas:

> [!Regla de Barrow]
> Sea $f$ continua y $F$ primitiva de $f$:
> $$
> \int_{a}^{b} f(t) \space dt = F(b) - F(a)
> $$

### Parte c)
$$
\int_{1}^{2} x^{5} - 4x^{3} + x \space dx
$$
Simplemente, tenemos que encontrar una primitiva de $x^{5} - 4x^{3} + x$, esto quiere decir, una función $F$, tal que:
$$
F'(x) = x^{5} - 4x^{3} + x
$$

Al tratarse de polinomios, se trata de un caso simple, puesto que tenemos que aumentar el grado de cada término en 1 y dividir entre el grado de cada término:
$$
\begin{align}
F(x) &= \frac{x^{6}}{6} - \frac{4x^{4}}{4} + \frac{x^{2}}{2} \\
&= \frac{x^{6}}{6} - x^{4} + \frac{x^{2}}{2}
\end{align}
$$
Para verificar, podemos derivar la función:
$$
\begin{align}
F'(x) &= \left( \frac{x^{6}}{6} - x^{4} + \frac{x^{2}}{2} \right)' \\
&= \frac{6(x^{6})' - \cancel{ (6)'x^{6} }}{36} - 4x^{3} + \frac{2(x^{2})' - \cancel{ (2)'x^{2} }}{4} \\
&= \frac{\cancel{ 36 }x^{5}}{\cancel{ 36 }} - 4x^{3} + \frac{\cancel{ 4 }x}{\cancel{ 4 }} \\
&= x^{5} - 4x^{3} + x
\end{align}
$$
Así, verificamos que efectivamente, $F$ es una primitiva de $x^{5} - 4x^{3} + x$.

Ahora, desarrollamos los cálculos aplicando Barrow:
$$
\begin{align}
\int_{1}^{2} x^{5} - 4x^{3} + x \space dx &= \left. \frac{x^{6}}{6} - x^{4} + \frac{x^{2}}{2} \right|_{1}^{2} \\
&= \frac{2^{6}}{6} - 2^{4} + \frac{2^{2}}{2} - \left( \frac{1^{6}}{6} - 1^{4} + \frac{1^{2}}{2} \right) \\
&= \frac{64}{6} - 16 + \frac{4}{2} - \left( \frac{1}{6} - 1 + \frac{1}{2} \right) \\
&= \frac{64}{6} - \frac{96}{6} + \frac{12}{6} - \left( \frac{1}{6} - \frac{6}{6} + \frac{3}{6} \right) \\
&= -\frac{20}{6} - \left( -\frac{2}{6} \right) \\
&= -\frac{20}{6} + \frac{2}{6} \\
&= -\frac{18}{6} \\
&= -3
\end{align}
$$
En conclusión:
$$
\int_{1}^{2} x^{5} - 4x^{3} + x \space dx = -3
$$

### Parte d)
$$
\int_{1}^{4} 3\sqrt{ x } + \sqrt[5]{ x } \space dx
$$
Es más sencillo abordar el problema en forma de potencia:
$$
\int_{1}^{4} 3\sqrt{ x } + \sqrt[5]{ x } \space dx = \int_{1}^{4} 3x^{\frac{1}{2}} + x^{\frac{1}{5}} \space dx
$$
De esta forma:
$$
\begin{align}
&F'(x) = 3x^{\frac{1}{2}} \\
&G'(x) = x^{\frac{1}{5}}
\end{align}
$$
Sabiendo que se trata de monomios, y cuando derivamos un polinomio su grado se reduce en 1:
$$
\begin{align}
\left( x^{\frac{3}{2}} \right)' &= \frac{3}{2}x^{\frac{1}{2}} \\
\implies \left( 2x^{\frac{3}{2}} \right)' &= \cancel{ (2)'x^{\frac{1}{2}} } + 2\left( x^{\frac{3}{2}} \right)' \\
&= \cancel{ 2 } \cdot \frac{3}{\cancel{ 2 }}x^{\frac{1}{2}} \\
&= 3x^{\frac{1}{2}} \\
&= 3\sqrt{ x }
\end{align}
$$
$$
\begin{align}
\left( x^{\frac{3}{2}} \right)' &= \frac{3}{2}x^{\frac{1}{2}} \\
\implies \left( 2x^{\frac{3}{2}} \right)' &= \cancel{ (2)'x^{\frac{1}{2}} } + 2\left( x^{\frac{3}{2}} \right)' \\
&= \cancel{ 2 } \cdot \frac{3}{\cancel{ 2 }}x^{\frac{1}{2}} \\
&= 3x^{\frac{1}{2}} \\
&= 3\sqrt{ x }
\end{align}
$$

$$
\begin{align}
\left( x^{\frac{6}{5}} \right)' &= \frac{6}{5}x^{\frac{1}{5}} \\
\implies \left( \frac{5}{6}x^{\frac{6}{5}} \right)' &= \cancel{ \left( \frac{5}{6} \right)'x^{\frac{6}{5}} } + \frac{5}{6}\left( x^{\frac{6}{5}} \right)' \\
&= \cancel{ \frac{5}{6} } \cdot \cancel{ \frac{6}{5} }x^{\frac{1}{5}} \\
&= x^{\frac{1}{5}} \\
&= \sqrt[5]{ x }
\end{align}
$$

De esta forma:
$$
\begin{align}
&F(x) = 2x^{\frac{3}{2}}  \\
&G(x) = \frac{5}{6}x^{\frac{6}{5}}
\end{align}
$$
Entonces, sabemos que una primitiva de $3\sqrt{ x } + \sqrt[5]{ x }$ es $F(x) + G(x) = 2x^{\frac{3}{2}} + x^{\frac{6}{5}}$.

Ahora, aplicamos Barrow para calcular la integral:
$$
\begin{align}
\int_{1}^{4} 3\sqrt{ x } + \sqrt[5]{ x } \space dx &= \left. 2x^{\frac{3}{2}} + \frac{5}{6}x^{\frac{6}{5}} \right|_{1}^{4} \\
&= \left( 2 \cdot 4^{\frac{3}{2}} + \frac{5}{6} \cdot 4^{\frac{6}{5}} \right) - \left( 2 \cdot 1^{\frac{3}{2}} + \frac{5}{6} \cdot 1^{\frac{6}{5}} \right) \\
&= \left( 2 \cdot 4\sqrt{ 4 } + \frac{5}{6} \cdot 4\sqrt[5]{ 4 } \right) - \left( 2 + \frac{5}{6} \right) \\
&= 8\sqrt{ 4 } + \frac{20}{6}\sqrt[5]{ 4 } - \frac{17}{6} \\
&= 16 + \frac{10}{3}\sqrt[5]{ 4 } - \frac{17}{6} \\
&= \frac{96}{6} + \frac{10}{3}\sqrt[5]{ 4 } - \frac{17}{6} \\
&= \frac{79}{6} + \frac{10}{3}\sqrt[5]{ 4 }
\end{align}
$$
En conclusión:
$$
\int_{1}^{4} 3\sqrt{ x } + \sqrt[5]{ x } \space dx = \frac{79}{6} + \frac{10}{3}\sqrt[5]{ 4 }
$$

### Parte h)
$$
\int_{0}^{1} \sin(\pi x) \space dx
$$
Una función que derivada da $\sin(x)$ es $-\cos(x)$. Sin embargo, también tenemos que considerar el parámetro pasado a la función, ya que:
$$
\begin{align}
(-\cos(\pi x)) &= -\cos'(\pi x) \cdot (\pi x)' \\
&= \sin(\pi x) \cdot \pi \\
&= \pi \sin(\pi x)
\end{align}
$$
De esta forma, podemos dividir entre $\pi$:
$$
\begin{align}
\left( -\frac{\cos(\pi x)}{\pi} \right)' &= -\frac{\pi (\cos(\pi x))' - \cancel{ (\pi)' \cos(\pi x) }}{\pi^{2}} \\
&= -\frac{\pi (-\sin(\pi x)) \cdot (\pi x)'}{\pi^{2}} \\
&= -\frac{\pi (-\sin(\pi x)) \cdot \pi}{\pi^{2}} \\
&= -\frac{\cancel{ \pi^{2} } (-\sin(\pi x))}{\cancel{ \pi^{2} }} \\
&= -(-\sin(\pi x)) \\
&= \sin(\pi x)
\end{align}
$$
De esta manera, confirmamos que $-\frac{\cos(\pi x)}{\pi}$ es una primitiva de $\sin(\pi x)$.

Ahora, podemos utilizarla, junto con Barrow para calcular la integral anterior:
$$
\begin{align}
\int_{0}^{1} \sin(\pi x) \space dx &= \left. -\frac{\cos(\pi x)}{\pi} \right|_{0}^{1} \\
&= -\frac{\cos(\pi \cdot 1)}{\pi} + \frac{\cos(\pi \cdot 0)}{\pi} \\
&= -\frac{\cos(\pi)}{\pi} + \frac{\cos(0)}{\pi} \\
&= -\frac{-1}{\pi} + \frac{1}{\pi} \\
&= \frac{1}{\pi} + \frac{1}{\pi} \\
&= \frac{1 + 1}{\pi} \\
&= \frac{2}{\pi}
\end{align}
$$
En conclusión:
$$
\int_{0}^{1} \sin(\pi x) \space dx = \frac{2}{\pi}
$$

---
## Ejercicio 7.1.15
Partes a hasta d, y una parte por fila de la parte e.

Primero que nada, es importante considerar que $f : [a, b] \to \mathbb{R}$ es una función positiva, o sea que $f(x) > 0, \forall x \in [a, b]$, y derivable, por lo que $f'(x)$ está definido $\forall x \in [a, b]$.
### Parte a)
$$
\int_{a}^{b} 2 f'(t) f(t) \space dt = f^{2}(b) - f^{2}(a)
$$
Primero que nada, estudiemos la integral:
$$
\int_{a}^{b} 2 f'(t) f(t) \space dt
$$
Para calcular la misma, tenemos que hallar una función $F$ primitiva de $2 f'(x) f(x)$, lo que quiere decir que $F' = f$. Viendo que hay un cociente dos, y el producto de $f$ y su derivada, podemos probar con la siguiente función:
$$
F(x) = f^{2}(x)
$$
De esta forma:
$$
\begin{align}
F'(x) &= (f^{2}(x))' \\
&= 2 f(x) \cdot (f(x))' \\
&= 2 f(x) f'(x)
\end{align}
$$
Entonces, confirmamos que $f^{2}(x)$ es primitiva de $2 f'(x) f(x)$.

Ahora, aplicamos Barrow para determinar la ecuación que nos permite calcular la integral en el intervalo dado:
$$
\begin{align}
\int_{a}^{b} 2 f'(t) f(t) \space dt &= f^{2}(x) |_{a}^{b} \\
&= f^{2}(b) - f^{2}(a)
\end{align}
$$

De esta forma, demostramos que
$$
\int_{a}^{b} 2 f'(t) f(t) \space dt = f^{2}(b) - f^{2}(a)
$$
ya que $f^{2}(x)$ es primitiva de $2 f'(x) f(x)$.

$$
\int_{a}^{b} n f'(t) f^{n - 1}(t) \space dt = f^{n}(b) - f^{n}(a)
$$
Similar al caso anterior, tomaremos el mismo enfoque: hallar una función $F$ primitiva de $n f'(x) f^{n - 1}(x)$. Probaremos con una función con la misma forma, aunque generalizada:
$$
F(x) = f^{n}(x)
$$
De esta forma:
$$
\begin{align}
F'(x) &= (f^{n}(x))' \\
&= n f^{n - 1}(x) \cdot (f(x))' \\
&= n f^{n - 1}(x) f'(x)
\end{align}
$$
Confirmamos que $f^{n}(x)$ es primitiva de $n f^{n - 1}(x) f'(x)$.

Nuevamente aplicamos Barrow para expresar el valor de la integral dada en base a la función primitiva:
$$
\begin{align}
\int_{a}^{b} n f'(t) f^{n - 1}(t) \space dt &= f^{n}(x) |_{a}^{b} \\
&= f^{n}(b) - f^{n}(a)
\end{align}
$$

De esta forma, demostramos que
$$
\int_{a}^{b} n f'(t) f^{n - 1}(t) \space dt = f^{n}(b) - f^{n}(a)
$$
ya que $f^{n}(x)$ es primitiva de $n f'(x) f^{n - 1}(x)$.

### Parte b)
$$
\int_{a}^{b} \frac{f'(t)}{f(t)} \space dt = \log(f(b)) - \log(f(a))
$$
Primero que nada, estudiemos la integral:
$$
\int_{a}^{b} 2 f'(t) f(t) \space dt
$$
En todas las partes de este ejercicio, tenemos que hallar una función $F$ primitiva de la función interior de la integral, por lo que dejaremos de especificar dicho paso. Simplemente nos enfocaremos a encontrar una primitiva (una función $F = \int_{a}^{b} f(t) \space dt$ tal que $F' = f$):

Buscamos una primitiva:
$$
F'(x) = \frac{f'(x)}{f(x)} \implies F(x) = \log(f(x))
$$
De esta manera:
$$
\begin{align}
F'(x) &= \left( \log(f(x)) \right)' \\
&= \frac{1}{f(x)} \cdot f'(x) \\
&= \frac{f'(x)}{f(x)}
\end{align}
$$
Confirmamos que, efectivamente, $F$ es una primitiva de $\frac{f'(x)}{f(x)}$.

Ahora, aplicamos Barrow para determinar el valor de la integral:
$$
\begin{align}
\int_{a}^{b} \frac{f'(t)}{f(t)} \space dt &= \left. \log(f(x)) \right|_{a}^{b} \\
&= \log(f(b)) - \log(f(a))
\end{align}
$$

De esta forma, demostramos que
$$
\int_{a}^{b} \frac{f'(t)}{f(t)} \space dt = \log(f(b)) - \log(f(a))
$$
ya que $\log(f(x))$ es primitiva de $\frac{f'(x)}{f(x)}$.

### Parte c)
$$
\int_{a}^{b} \frac{f'(t)}{2\sqrt{ f(t) }} \space dt = \sqrt{ f(b) } - \sqrt{ f(a) }
$$
Comenzamos estudiando la integral:
$$
\int_{a}^{b} \frac{f'(t)}{2\sqrt{ f(t) }} \space dt
$$
Buscamos una función $F$ primitiva de $\frac{f'(x)}{2\sqrt{ f(x) }}$:
$$
F'(x) = \frac{f'(x)}{2\sqrt{ f(x) }} \implies F(x) = \sqrt{ f(x) }
$$
De esta manera:
$$
\begin{align}
F'(x) &= \left( \sqrt{ f(x) } \right)' \\
&= \frac{1}{2\sqrt{ f(x) }} \cdot f'(x) \\
&= \frac{f'(x)}{2\sqrt{ f(x) }}
\end{align}
$$
Confirmamos que, efectivamente, $F$ es una primitiva de $\frac{f'(x)}{2\sqrt{ f(x) }}$.

Ahora, aplicamos Barrow para determinar el valor de la integral:
$$
\begin{align}
\int_{a}^{b} \frac{f'(t)}{2\sqrt{ f(t) }} \space dt &= \left. \sqrt{ f(x) } \right|_{a}^{b} \\
&= \sqrt{ f(b) } - \sqrt{ f(a) }
\end{align}
$$

De esta forma, demostramos que
$$
\int_{a}^{b} \frac{f'(t)}{2\sqrt{ f(t) }} \space dt = \sqrt{ f(b) } - \sqrt{ f(a) }
$$
ya que $\sqrt{ f(x) }$ es primitiva de $\frac{f'(x)}{2\sqrt{ f(x) }}$.

### Parte d)
$$
\int_{a}^{b} f'(t) e^{f(t)} \space dt = e^{f(b)} - e^{f(a)}
$$
Comenzamos estudiando la integral:
$$
\int_{a}^{b} f'(t) e^{f(t)} \space dt
$$
Buscamos una función $F$ primitiva de $f'(x) e^{f(x)}$:
$$
F'(x) = f'(x) e^{f(x)} \implies F(x) = e^{f(x)}
$$
De esta manera:
$$
\begin{align}
F'(x) &= \left( e^{f(x)} \right)' \\
&= e^{f(x)} \cdot f'(x) \\
&= f'(x) e^{f(x)}
\end{align}
$$
Confirmamos que, efectivamente, $F$ es una primitiva de $f'(x) e^{f(x)}$.

Ahora, aplicamos Barrow para determinar el valor de la integral:
$$
\begin{align}
\int_{a}^{b} f'(t) e^{f(t)} \space dt &= \left. e^{f(x)} \right|_{a}^{b} \\
&= e^{f(b)} - e^{f(a)}
\end{align}
$$

De esta forma, demostramos que
$$
\int_{a}^{b} f'(t) e^{f(t)} \space dt = e^{f(b)} - e^{f(a)}
$$
ya que $e^{f(x)}$ es primitiva de $f'(x) e^{f(x)}$.

### Parte e)
En este ejercicio, tenemos que calcular las integrales propuestas considerando las primitivas generalizadas demostradas en las partes anteriores.
#### Parte a)
$$
\int \sin ^{6}(x) \cos(x) \space dx
$$
Buscamos una primitiva de $\sin ^{6}(x) \cos(x)$. Podemos ver que la función tiene la forma $f^{6}(x) f'(x)$, por lo que podemos considerar la función $F(x) = \frac{f^{7}(x)}{7} = \frac{\sin ^{7}(x)}{7}$:
$$
\begin{align}
F'(x) &= \left( \frac{\sin ^{7}(x)}{7} \right)' \\
&= \frac{\cancel{ 7 } \sin ^{6}(x) \cdot \sin'(x)}{\cancel{ 7 }} \\
&= \sin ^{6}(x) \cdot \cos(x) \\
&= \sin ^{6}(x) \cos(x)
\end{align}
$$
Confirmamos que $F$ es primitiva de $\sin ^{6}(x) \cos(x)$.

Proseguimos a calcular la integral. En conclusión:
$$
\int \sin ^{6}(x) \cos(x) \space dx = \frac{\sin ^{7}(x)}{7} + C
$$

Aclaración: más que calcular la integral, la notación $\int f(x) \space dx = F(x)$ simplemente indica que $F$ es una primitiva de $f$. Por lo tanto, podemos leer a $\int f(x) \space dx$ como "primitiva de $f$".

#### Parte e)
$$
\int \tan(x) \space dx
$$
En este caso, conviene reescribir la integral, considerando la igualdad $\tan(x) = \frac{\sin(x)}{\cos(x)}$:
$$
\int \tan(x) \space dx = \int \frac{\sin(x)}{\cos(x)} \space dx
$$

Buscamos una primitiva de $\frac{\sin(x)}{\cos(x)}$. Podemos ver que la función tiene la forma $-\frac{f'(x)}{f(x)}$, por lo que podemos considerar la función $F(x) = -\log(f(x)) = -\log(\cos(x))$:
$$
\begin{align}
F'(x) &= \left( -\log(\cos(x)) \right)' \\
&= -\frac{1}{\cos(x)} \cdot \cos'(x) \\
&= -\frac{1}{\cos(x)} \cdot (-\sin(x)) \\
&= \cancel{ - }\frac{\cancel{ - }\sin(x)}{\cos(x)} \\
&= \frac{\sin(x)}{\cos(x)}
\end{align}
$$
Confirmamos que $F$ es primitiva de $\frac{\sin(x)}{\cos(x)} = \tan(x)$.

Proseguimos a calcular la integral. En conclusión:
$$
\int \tan(x) \space dx = \int \frac{\sin(x)}{\cos(x)} \space dx = -\log(\cos(x)) + C
$$

#### Parte h)
$$
\int \frac{x^{2}}{\sqrt{ x^{3} - 1 }} \space dx
$$

Buscamos una primitiva de $\frac{x^{2}}{\sqrt{ x^{3} - 1 }}$. Podemos ver que la función tiene la forma $\frac{f'(x)}{2\sqrt{ f(x) }}$, por lo que podemos considerar la función $F(x) = \sqrt{ f(x) } = \sqrt{ x^{3} - 1 }$:
$$
\begin{align}
F'(x) &= \left( \sqrt{ x^{3} - 1 } \right)' \\
&= \frac{1}{2\sqrt{ x^{3} - 1 }} \cdot (x^{3} - 1)' \\
&= \frac{1}{2\sqrt{ x^{3} - 1 }} \cdot 3x^{2} \\
&= \frac{3}{2}\frac{x^{2}}{\sqrt{ x^{3} - 1 }}
\end{align}
$$
Como vemos, hace falta multiplicar todo por $\frac{2}{3}$ para llegar a la función presentada:
$$
\begin{align}
F'(x) &= \left( \frac{2}{3} \sqrt{ x^{3} - 1 } \right)' \\
&= \cancel{ \left( \frac{2}{3} \right)' \sqrt{ x^{3} - 1 } } + \frac{2}{3} (\sqrt{ x^{3} - 1 })' \\
&= \frac{2}{3} \cdot \frac{1}{2\sqrt{ x^{3} - 1 }} \cdot (x^{3} - 1)' \\
&= \frac{2}{3} \cdot \frac{1}{2\sqrt{ x^{3} - 1 }} \cdot 3x^{2} \\
&= \cancel{ \frac{2}{3} } \cdot \cancel{ \frac{3}{2} } \frac{x^{2}}{\sqrt{ x^{3} - 1 }} \\
&= \frac{x^{2}}{\sqrt{ x^{3} - 1 }}
\end{align}
$$
De esta forma, nos quedamos con la primitiva $F(x) = \frac{2}{3} \sqrt{ x^{3} - 1 }$, confirmando que $F$ es primitiva de $\frac{x^{2}}{\sqrt{ x^{3} - 1 }}$.

Proseguimos a calcular la integral. En conclusión:
$$
\int \frac{x^{2}}{\sqrt{ x^{3} - 1 }} \space dx = \frac{2}{3} \sqrt{ x^{3} - 1 } + C
$$

#### Parte l)
$$
\int \frac{e^{\sqrt{ x }}}{\sqrt{ x }} \space dx
$$

Buscamos una primitiva de $\frac{e^{\sqrt{ x }}}{\sqrt{ x }}$. Podemos ver que la función tiene la forma $f'(x) e^{f(x)}$, por lo que podemos considerar la función $F(x) = 2e^{f(x)} = 2e^{\sqrt{ x }}$:
$$
\begin{align}
F'(x) &= \left( 2e^{\sqrt{ x }} \right)' \\
&= \cancel{ (2)' e^{\sqrt{ x }} } + 2 (e^{\sqrt{ x }})' \\
&= 2e^{\sqrt{ x }} \cdot (\sqrt{ x })' \\
&= 2e^{\sqrt{ x }} \cdot \frac{1}{2\sqrt{ x }} \cdot (x)' \\
&= 2e^{\sqrt{ x }} \cdot \frac{1}{2\sqrt{ x }} \\
&= \frac{\cancel{ 2 }e^{\sqrt{ x }}}{\cancel{ 2 }\sqrt{ x }} \\
&= \frac{e^{\sqrt{ x }}}{\sqrt{ x }}
\end{align}
$$

Confirmamos que $F$ es primitiva de $\frac{e^{\sqrt{ x }}}{\sqrt{ x }}$.

Proseguimos a calcular la integral. En conclusión:
$$
\int \frac{e^{\sqrt{ x }}}{\sqrt{ x }} \space dx = 2e^{\sqrt{ x }} + C
$$

---
# 2 - Métodos de integración
## Ejercicio 7.2.1
Una parte por fila.

En este ejercicio, tenemos que aplicar el método de integración por pártes, técnica basada en la regla de Leibniz (integral del producto de dos funciones):
$$
(f(x)g(x))' = f'(x)g(x) + f(x)g'(x)
$$
De esta forma, $f \cdot g$ es una primitiva de $f'g + fg'$.

Por ejemplo, para calcular la siguiente integral:
$$
\int_{a}^{b} f'(x) \cdot g(x) + f(x) \cdot g'(x) \space dx = f(b) \cdot g(b) - f(a) \cdot g(a) = f(x) \cdot g(x) |_{a}^{b}
$$
Esta sería la fórmula base, aunque normalmente se expresa y utiliza de la siguiente forma:
$$
\int_{a}^{b} f'(x) \cdot g(x) \space dx = f(x) \cdot g(x) |_{a}^{b} - \int_{a}^{b} f(x) \cdot g'(x) \space dx
$$
La fórmula es sumamente útil, ya que muchas veces podemos identificar que la función se trata de un producto (o lo podemos expresar como tal), y aunque no sepamos integrar $f'(x) \cdot g(x)$, sabemos integrar $f(x) \cdot g'(x)$ (reduciendo el problema de una integral que no sabemos calcular a una que si).

### Parte a)
$$
\int x \sin(x) \space dx
$$
Consideraremos la siguiente combinación:
$$
\left[
\begin{align}
&f(x) = x &&f'(x) = 1 \\
&g'(x) = \sin(x) &&g(x) = -\cos(x)
\end{align}
\right]
$$
$$
\begin{align}
\int x \sin(x) \space dx &= x (-\cos(x)) - \int 1 \cdot (-\cos(x)) \space dx \\
&= -x \cos(x) + \int \cos(x) \space dx \\
&= -x \cos(x) + \sin(x) \\
&= \sin(x) - x \cos(x)
\end{align}
$$

En conclusión:
$$
\int x \sin(x) \space dx = \sin(x) - x \cos(x) + C
$$

### Parte e)
$$
\int \cos ^{2}(x) \space dx = \int \cos(x) \cos(x) \space dx
$$
Consideraremos la siguiente combinación:
$$
\left[
\begin{align}
&f(x) = \cos(x) &&f'(x) = -\sin(x) \\
&g'(x) = \cos(x) &&g(x) = \sin(x)
\end{align}
\right]
$$
$$
\begin{align}
\int \cos(x) \cos(x) \space dx &= \cos(x) \sin(x) - \int (-\sin(x)) \sin(x) \space dx \\
&= \cos(x) \sin(x) + \int \sin(x) \sin(x) \space dx \\
&= \cos(x) \sin(x) + \int \sin ^{2}(x) \space dx \\
&= \cos(x) \sin(x) + \int 1 - \cos ^{2}(x) \space dx \\
&= \cos(x) \sin(x) + \int 1 \space dx - \int \cos ^{2}(x) \space dx
\end{align}
$$
Ahora, proseguimos a pasar el último término para el lado izquierdo de la equación, ya que es igual que la integral inicial:
$$
\begin{align}
\int \cos(x) \cos(x) \space dx &= \cos(x) \sin(x) + \int 1 \space dx - \int \cos ^{2}(x) \space dx \\
\int \cos ^{2}(x) \space dx + \int \cos ^{2}(x) \space dx &= \cos(x) \sin(x) + \int 1 \space dx \\
2 \int \cos ^{2}(x) \space dx &= \cos(x) \sin(x) + \int 1 \space dx \\
2 \int \cos ^{2}(x) \space dx &= \cos(x) \sin(x) + x \\
\int \cos ^{2}(x) \space dx &= \frac{\cos(x) \sin(x) + x}{2}
\end{align}
$$

En conclusión:
$$
\int \cos ^{2}(x) \space dx = \frac{\cos(x) \sin(x) + x}{2} + C
$$

### Parte f)
$$
\int \log(x) \space dx
$$
En este caso, no parece haber otro factor, por lo que haremos aparecer el factor 1:
$$
\int \log(x) \space dx = \int 1 \cdot \log(x) \space dx
$$
Consideraremos la siguiente combinación:
$$
\left[
\begin{align}
&f(x) = \log(x) &&f'(x) = \frac{1}{x} \\
&g'(x) = 1 &&g(x) = x
\end{align}
\right]
$$
$$
\begin{align}
\int 1 \cdot \log(x) \space dx &= \log(x) \cdot x - \int \frac{1}{x} \cdot x \space dx \\
&= \log(x) \cdot x - \int 1 \space dx \\
&= \log(x) \cdot x - x \\
&= x\left( \log(x) - 1 \right)
\end{align}
$$

En conclusión:
$$
\int \log(x) \space dx = x\left( \log(x) - 1 \right) + C
$$

### Parte i)
$$
\int \cos(x) e^{2x} \space dx
$$
Consideraremos la siguiente combinación:
$$
\left[
\begin{align}
&f(x) = \cos(x) &&f'(x) = -\sin(x) \\
&g'(x) = e^{2x} &&g(x) = \frac{e^{2x}}{2}
\end{align}
\right]
$$
$$
\begin{align}
\int \cos(x) e^{2x} \space dx &= \cos(x) \frac{e^{2x}}{2} - \int (-\sin(x)) \frac{e^{2x}}{2} \space dx \\
&= \cos(x) \frac{e^{2x}}{2} + \int \sin(x) \frac{e^{2x}}{2} \space dx \\
&= \cos(x) \frac{e^{2x}}{2} + \frac{1}{2} \int \sin(x) e^{2x} \space dx
\end{align}
$$
$$
\int \sin(x) e^{2x} \space dx
$$
$$
\left[
\begin{align}
&f(x) = e^{2x} &&f'(x) = 2e^{2x} \\
&g'(x) = \sin(x) &&g(x) = -\cos(x)
\end{align}
\right]
$$
$$
\begin{align}
\int \sin(x) e^{2x} \space dx &= -(\cos(x)) e^{2x} - \int (-\cos(x)) 2e^{2x} \space dx \\
&= -\cos(x) e^{2x} + \int \cos(x) 2e^{2x} \space dx \\
&= -\cos(x) e^{2x} + 2\int \cos(x) e^{2x} \space dx
\end{align}
$$
$$
\begin{align}
\implies \int \cos(x) e^{2x} \space dx &= \cos(x) \frac{e^{2x}}{2} + \left( -\cos(x) e^{2x} + 2\int \cos(x) e^{2x} \space dx \right) \\
\int \cos(x) e^{2x} \space dx &= \cos(x) \frac{e^{2x}}{2} -\cos(x) e^{2x} + 2\int \cos(x) e^{2x} \space dx \\
\int \cos(x) e^{2x} \space dx &= -\cos(x) \frac{e^{2x}}{2} + 2\int \cos(x) e^{2x} \space dx \\
\int \cos(x) e^{2x} \space dx - 2\int \cos(x) e^{2x} \space dx &= -\cos(x) \frac{e^{2x}}{2} \\
-\int \cos(x) e^{2x} \space dx &= -\cos(x) \frac{e^{2x}}{2} \\
\int \cos(x) e^{2x} \space dx &= \cos(x) \frac{e^{2x}}{2} \\
\int \cos(x) e^{2x} \space dx &= \frac{\cos(x) e^{2x}}{2}
\end{align}
$$

En conclusión:
$$
\int \cos(x) e^{2x} \space dx = \frac{\cos(x) e^{2x}}{2} + C
$$
ACLARACIÓN: Para resolver integrales aplicando el método de integración por partes, es importante ser consistente: si decidimos integrar la exponencial en el primer paso, debemos integrarla también en el segundo. Hacer lo contario nos llevaría a un bucle en el que siempre volvemos a la integral inicial.

CORRECCIÓN:
Volvemos a la segunda combinación:
$$
\int \sin(x) e^{2x} \space dx
$$
$$
\left[
\begin{align}
&f(x) = \sin(x) &&f'(x) = \cos(x) \\
&g'(x) = e^{2x} &&g(x) = \frac{e^{2x}}{2}
\end{align}
\right]
$$
De esta manera:
$$
\begin{align}
\int \sin(x) e^{2x} \space dx &= \sin(x) \frac{e^{2x}}{2} - \int \cos(x) \frac{e^{2x}}{2} \space dx \\
&= \sin(x) \frac{e^{2x}}{2} - \frac{1}{2}\int \cos(x) e^{2x} \space dx
\end{align}
$$
Ahora, sustituimos en la igualdad principal:
$$
\begin{align}
\implies \int \cos(x) e^{2x} \space dx &= \cos(x) \frac{e^{2x}}{2} + \frac{1}{2} \left( \sin(x) \frac{e^{2x}}{2} - \frac{1}{2}\int \cos(x) e^{2x} \space dx \right) \\
\int \cos(x) e^{2x} \space dx &= \cos(x) \frac{e^{2x}}{2} + \sin(x) \frac{e^{2x}}{4} - \frac{1}{4}\int \cos(x) e^{2x} \space dx \\
\int \cos(x) e^{2x} \space dx &= \frac{\cos(x) e^{2x}}{2} + \frac{\sin(x) e^{2x}}{4} - \frac{1}{4}\int \cos(x) e^{2x} \space dx \\
\int \cos(x) e^{2x} \space dx &= \frac{2 \cos(x) e^{2x} + \sin(x) e^{2x}}{4} - \frac{1}{4}\int \cos(x) e^{2x} \space dx \\
\int \cos(x) e^{2x} \space dx + \frac{1}{4}\int \cos(x) e^{2x} \space dx &= \frac{2 \cos(x) e^{2x} + \sin(x) e^{2x}}{4} \\
\frac{5}{4} \int \cos(x) e^{2x} \space dx &= \frac{2 \cos(x) e^{2x} + \sin(x) e^{2x}}{4} \\
\int \cos(x) e^{2x} \space dx &= \frac{4}{5} \frac{2 \cos(x) e^{2x} + \sin(x) e^{2x}}{4} \\
\int \cos(x) e^{2x} \space dx &= \frac{8 \cos(x) e^{2x} + 4\sin(x) e^{2x}}{20} \\
\int \cos(x) e^{2x} \space dx &= \frac{2 \cos(x) e^{2x} + \sin(x) e^{2x}}{5} \\
\int \cos(x) e^{2x} \space dx &= \frac{e^{2x}(2 \cos(x) + \sin(x))}{5}
\end{align}
$$
En conclusión:
$$
\int \cos(x) e^{2x} \space dx = \frac{e^{2x}(2 \cos(x) + \sin(x))}{5} + c
$$

---
## Ejercicio 7.2.2
Una parte por fila.

En este caso, tenemos que utilizar la técnica de integración por sustitución, cuya fórmula es la siguiente:

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

### Parte b)
$$
\int \frac{e^{x}}{1 + e^{2x}} \space dx
$$
Ahora, analicemos cuidadosamente la función, para entender donde se da la composición:

La función $g$ es $e^{x}$ en este caso, por lo que
$$
g(x) = e^{x} \implies g'(x) = e^{x}
$$
Si analizamos cuidadosamente y expresamos como un producto, podemos ver que tenemos la forma ideal para aplicar la sustitución. En este caso:
$$
f(x) = \frac{1}{1 + x^{2}}
$$
Ahora, realizaremos la sustitución:
$$
\int \frac{e^{x}}{1 + e^{2x}} \space dx = \int \frac{1}{1 + e^{2x}} \cdot e^{x} \space dx \underbrace{ = }_{ \begin{align}
&u = e^{x} \\
&du = e^{x} \space dx
\end{align} } \int \frac{1}{1 + u^{2}} \space du
$$
Ahora, si estudiamos la forma de la función $f(u) = \frac{1}{1 + u^{2}}$, podemos ver que la misma se corresponde con $\arctan'(u)$. Por lo tanto, $\arctan(u)$ es una primitiva de $f(u)$:
$$
\int \frac{1}{1 + u^{2}} \space du = \arctan(u)
$$
Ahora, deshacemos la sustitución:
$$
\arctan(u) = \arctan(e^{x})
$$

En conclusión:
$$
\int \frac{e^{x}}{1 + e^{2x}} \space dx = \arctan(e^{x}) + C
$$

Básicamente, el proceso es el siguiente:
1. Primero, reconocemos la función $g$, la función que se pasa por parámetro a la compuesta, o en caso de no ver tal cosa, básicamente buscamos que haya una función y su derivada, $g(x)$ y $g'(x)$.
2. Entonces, realizaremos un cambio de variable, denotando $u = g(x)$ y su derivada $du = g'(x) \space dx$. Este es un tema más bien notacional y formal, pero si efectivamente identificamos correctamente a las funciones, cuando sustituyamos ambas por su nueva denominación, vamos a haber simplificado sumamente el problema inicial.
3. Ahora, obtuvimos una integral de la forma: $\int f(u) \space du$.
4. Tenemos que encontrar una función $F$ primitiva de la función $f$, para deshacernos de la integral: $\int f(u) \space du = F(u) + C$.
5. Finalmente, deshacemos el cambio de variable: $F(u) + C = F(g(x)) + C$.
6. En caso de tener una integral definida en $[a, b]$ (con extremos marcados), podemos cambiar los limites de integración de $[a, b]$ a $[g(a), g(b)]$.
En resumidas cuentas:
$$
\int f(g(x)) \cdot g'(x) \space dx \underset{\begin{align}
&u = g(x) \\
&du = g'(x) \space dx
\end{align}} = \int f(u) du = F(u) + C = F(g(x)) + C
$$
En caso de que esté definida, y ya hayamos determinado $F$:
$$
F(g(x)) + C |_{a}^{b} = F(g(b)) + C - F(g(a)) - C = \left. F(x) + C \right|_{g(a)}^{g(b)} = \int_{g(a)}^{g(b)} f(x) \space dx
$$

ACLARACIÓN: De una integral, únicamente se pueden extraer constantes. No es válido extraer términos o factores que incluyan variables como $x$.

### Parte d)
$$
\int \frac{x^{2}}{\sqrt{ x^{3} - 1 }} \space dx
$$
Como vemos, tenemos la función $\frac{x^{2}}{\sqrt{ x^{3} - 1 }} = \frac{1}{\sqrt{ x^{3} - 1 }} \cdot x^{2}$. Claramente está definida como el producto de dos funciones. Aquí consideraremos $g(x) = x^{3}$ Sin embargo, para asegurar que el segundo factor sea la derivada de $g$, sabiendo que $(x^{3})' = 3x^{2}$, tenemos que multiplicarlo por 3. Por lo tanto, para no modificar el valor de la integral, dividiremos todo entre 3:
$$
\int \frac{x^{2}}{\sqrt{ x^{3} - 1 }} \space dx = \frac{1}{3} \int \frac{1}{\sqrt{ x^{3} - 1 }} \cdot 3x^{2}
$$
Ahora, podemos aplicar el método:
$$
\frac{1}{3} \int \frac{1}{\sqrt{ x^{3} - 1 }} \space dx \cdot 3x^{2} \underbrace{ = }_{ \begin{align}
&u = x^{3} \\
&du = 3x^{2} \space dx
\end{align} } \frac{1}{3} \int \frac{1}{\sqrt{ u - 1 }} \space du
$$
Ahora, se trata de encontrar una función $F(u)$ primitiva de $\frac{1}{\sqrt{ u - 1 }}$. Sabiendo que $(\sqrt{ x })' = \frac{1}{2\sqrt{ x }}$, podemos considerar la función $F(u) = 2\sqrt{ u - 1 }$.

Finalmente, determinamos la integral y deshacemos el cambio de variable:
$$
\frac{1}{3} \int \frac{1}{\sqrt{ u - 1 }} \space du = \frac{2\sqrt{ u - 1 }}{3} = \frac{2\sqrt{ x^{3} - 1 }}{3}
$$

En conclusión:
$$
\int \frac{x^{2}}{\sqrt{ x^{3} - 1 }} \space dx = \frac{2\sqrt{ x^{3} - 1 }}{3} + C
$$

### Parte h)
$$
\int x\sqrt{ 1 + x^{2} } \space dx
$$
Consideraremos $g(x) = x^{2}$. Sin embargo, para asegurar que el segundo factor sea la derivada de $g$, sabiendo que $(x^{2})' = 2x$, tenemos que multiplicarlo por 2. Por lo tanto, para no modificar el valor de la integral, dividiremos todo entre 2:
$$
\int x\sqrt{ 1 + x^{2} } \space dx = \frac{1}{2} \int 2x\sqrt{ 1 + x^{2} } \space dx
$$
Ahora, podemos aplicar el método:
$$
\frac{1}{2} \int 2x\sqrt{ 1 + x^{2} } \space dx \underbrace{ = }_{ \begin{align}
&u = x^{2} \\
&du = 2x \space dx
\end{align} } \frac{1}{2} \int \sqrt{ 1 + u } \space du
$$
Ahora, se trata de encontrar una función $F(u)$ primitiva de $\sqrt{ 1 + u }$. Sabiendo que $\left( x^{\frac{3}{2}} \right)' = \frac{3}{2}x^{\frac{1}{2}} = \frac{3\sqrt{ x }}{2}$, podemos considerar la función $F(u) = \frac{2}{3}(1 + u)^{\frac{3}{2}}$, ya que:
$$
\begin{align}
F'(u) &= \left( \frac{2}{3}(1 + u)^{\frac{3}{2}} \right)' \\
&= \frac{2}{3}\left( (1 + u)^{\frac{3}{2}} \right)' \\
&= \cancel{ \frac{2}{3} } \cdot \cancel{ \frac{3}{2} }(1 + u)^{\frac{1}{2}} \\
&= (1 + u)^{\frac{1}{2}} \\
&= \sqrt{ 1 + u }
\end{align}
$$

Finalmente, determinamos la integral y deshacemos el cambio de variable:
$$
\frac{1}{2} \int \sqrt{ 1 + u } \space du = \frac{1}{2} \cdot \frac{2}{3}(1 + u)^{\frac{3}{2}} = \frac{2}{6} (1 + u)^{\frac{3}{2}} = \frac{(1 + u)^{\frac{3}{2}}}{3}
$$

En conclusión:
$$
\int x\sqrt{ 1 + x^{2} } \space dx = \frac{(1 + u)^{\frac{3}{2}}}{3} + C
$$

### Parte k)
$$
\int \frac{1}{\cos(x)} \space dx
$$
En este caso, manipularemos un poco la expresión para llevarla a la forma que queremos:
$$
\int \frac{1}{\cos(x)} \space dx = \int \frac{\cos(x)}{\cos ^{2}(x)} \space dx = \int \frac{\cos(x)}{1 - \sin ^{2}(x)} \space dx = \int \frac{1}{1 - \sin ^{2}(x)} \cdot \cos(x) \space dx
$$
Consideraremos $g(x) = \sin(x)$, tal que $g'(x) = \cos(x)$. Ahora, desarrollamos la sustitución:
$$
\int \frac{1}{1 - \sin ^{2}(x)} \cdot \cos(x) \space dx \underbrace{ = }_{ \begin{align}
&u = \sin(x) \\
&du = \cos(x) \space dx
\end{align} } = \int \frac{1}{1 - u^{2}} \space du
$$

### Parte m)
$$
\int \frac{\log(\log(x))}{x \log(x)} \space dx
$$
En este caso, simplemente lo expresamos como un producto:
$$
\int \frac{\log(\log(x))}{x \log(x)} \space dx = \int \frac{1}{x \log(x)} \cdot \log(\log(x)) \space dx
$$
Si desarrollamos la derivada de uno de los factores:
$$
\begin{align}
(\log(\log(x)))' &= \frac{1}{\log(x)} \cdot (\log(x))' \\
&= \frac{1}{\log(x)} \cdot \frac{1}{x} \\
&= \frac{1}{x \log(x)}
\end{align}
$$
De esta forma, la integral tiene la forma:
$$
\int \frac{1}{x \log(x)} \cdot \log(\log(x)) \space dx = \int f'(g(x)) \cdot f(g(x)) \space dx
$$

Quizás, podamos tomar el siguiente enfoque:
$$
\int \frac{\log(\log(x))}{x \log(x)} \space dx = \int \frac{\log(\log(x))}{\log(x)} \cdot \frac{1}{x} \space dx
$$
Ahora, tenemos una función de la forma:
$$
\int \frac{\log(\log(x))}{\log(x)} \cdot \frac{1}{x} \space dx = \int \frac{\log(g(x))}{g(x)} \cdot g'(x) \space dx
$$
Procedemos a realizar el cambio de variable:
$$
\int \frac{\log(\log(x))}{\log(x)} \cdot \frac{1}{x} \space dx \underbrace{ = }_{ \begin{align}
&u = \log(x) \\
&du = \frac{1}{x} \space dx
\end{align} } \int \frac{\log(u)}{u} \space du
$$
Ahora, simplemente tenemos que encontrar una primitiva de $\frac{\log(u)}{u}$. En caso de no conocer ninguna, podemos volver a aplicar sustitución:
$$
\int \frac{\log(u)}{u} \space du = \int \log(u) \cdot \frac{1}{u} \space du \underbrace{ = }_{ \begin{align}
&v = \log(u) \\
&dv = \frac{1}{u} \space du
\end{align} } \int v \space dv
$$
Ahora buscamos una primitiva de $v$. Como se trata de una simple variable, es una función bien conocida, por lo que ya sabemos una de sus primitivas: $\frac{v^{2}}{2}$.

De esta manera, nos queda simplemente deshacer los cambios de variable:
$$
\int v \space dv = \frac{v^{2}}{2} = \frac{\log(u)^{2}}{2} = \frac{\log(\log(x))^{2}}{2}
$$

En conclusión:
$$
\int \frac{\log(\log(x))}{x \log(x)} \space dx = \frac{\log(\log(x))^{2}}{2} + C
$$

En realidad, podríamos haber tomado el primer enfoque, y habría sido necesario realizar cambio de variable una sola vez:
$$
\int \frac{1}{x \log(x)} \cdot \log(\log(x)) \space dx = \int f'(g(x)) \cdot f(g(x)) \space dx
$$
Entonces, realizamos el cambio de variable:
$$
\int \frac{1}{x \log(x)} \cdot \log(\log(x)) \space dx \underbrace{ = }_{ \begin{align}
&u = \log(\log(x)) \\
&dv = \frac{1}{x \log(x)} \space dx
\end{align} } \int u \space du
$$
Buscamos una primitiva de $u$. Consideraremos $\frac{u^{2}}{2}$. Luego, deshacemos el cambio de variable:
$$
\int u \space du = \frac{u^{2}}{2} = \frac{\log(\log(x))^{2}}{2}
$$

En definitiva, llegamos a la misma conclusión:
$$
\int \frac{\log(\log(x))}{x \log(x)} \space dx = \frac{\log(\log(x))^{2}}{2} + C
$$

### Parte n)
$$
\int \log(\cos(x)) \tan(x) \space dx
$$
Reescribamos la integral:
$$
\int \log(\cos(x)) \tan(x) \space dx = \int \log(\cos(x)) \cdot \frac{\sin(x)}{\cos(x)} \space dx = \int \frac{\log(\cos(x)) \sin(x)}{\cos(x)} \space dx
$$
Como vemos, tenemos las funciones trigonométricas $\sin(x)$ y $\cos(x)$. Sabiendo que $\cos'(x) = -\sin(x)$, consideramos $g(x) = \cos(x)$ y $g'(x) = -\sin(x)$:
$$
\int \frac{\log(\cos(x)) \sin(x)}{\cos(x)} \space dx = -\int \frac{\log(\cos(x))}{\cos(x)} \cdot (-\sin(x)) \space dx \underbrace{ = }_{ \begin{align}
&u = \cos(x) \\
&du = -\sin(x) \space dx
\end{align} } -\int \frac{\log(u)}{u} \space du
$$
Ahora, realizamos una segunda sustitución:
$$
-\int \frac{\log(u)}{u} \space du = -\int \log(u) \cdot \frac{1}{u} \space du \underbrace{ = }_{ \begin{align}
&v = \log(u) \\
&dv = \frac{1}{u} \space du
\end{align} } -\int v \space dv
$$
Sabiendo que una primitiva de $v$ es $\frac{v^{2}}{2}$:
$$
-\int v \space dv = -\frac{v^{2}}{2}
$$
Finalmente, deshacemos los cambios de variable:
$$
-\frac{v^{2}}{2} = -\frac{\log(u)^{2}}{2} = -\frac{\log(\cos(x))^{2}}{2}
$$

En conclusión:
$$
\int \log(\cos(x)) \tan(x) \space dx = -\frac{\log(\cos(x))^{2}}{2} + C
$$

---
## Ejercicio 7.2.3
Una parte por fila.

El método de fracciones simples se divide en tres partes principales:

1. Reducción al caso grado (numerador) < grado (denominador)
Partimos de un cociente cualquiera, y lo expresamos como $$
   \frac{f(x)}{g(x)} = Q(x) + \frac{R(x)}{g(x)}
   $$
siendo $Q(x), R(x), g(x)$ polinomios, pero con la particular de que el grado de $R(x)$ es menor que el grado de $g(x)$: $gr(R(x)) < gr(g(x))$.
   
En caso de que $gr(f(x)) < gr(g(x))$, este paso no se realiza.

2. Descomposición en fracciones simples
Este es el paso más importante.

Teniendo $\frac{f(x)}{g(x)}$ con $gr(f(x)) < gr(g(x))$, descompondremos la expresión como una suma de funciones racionales más simples, las cuales sabremos integrar:
$$
\frac{f(x)}{g(x)} = \frac{P_{1}(x)}{Q_{1}(x)} + \frac{P_{2}(x)}{Q_{2}(x)} + \dots + \frac{P_{n}(x)}{Q_{n}(x)}
$$

3. Integrar
$$
\int \frac{f(x)}{g(x)} \space dx = \int \frac{P_{1}(x)}{Q_{1}(x)} \space dx + \int \frac{P_{2}(x)}{Q_{2}(x)} \space dx + \dots + \int \frac{P_{n}(x)}{Q_{n}(x)} \space dx
$$

Básicamente, el procedimiento sería el siguiente:
1. Expresar el cociente de tal forma que cumpla la condición $gr(f) < gr(g)$ (mediante división de polinomios).
2. Teniendo la nueva expresión, buscamos las raíces del denominador y lo expresamos como un producto.
3. Expresamos el cociente como $n$ términos sumados con numeradores desconocidos, siendo $n$ la cantidad de factores en los que expresamos $g(x)$.
4. Hacemos denominador común con todos los términos e igualamos los coeficientes del polinomio numerador original con los numeradores desconocidos. Una alternativa es aplicar el método de la tapadita.
5. Resolvemos el sistema para hallar los valores de dichos numeradores.
6. Hallamos las primitivas de los nuevos términos, que ahora consisten en funciones más sencillas que sabemos integrar.

### Parte a)
$$
\int \frac{x}{(x + 1)(x + 2)(x + 3)} \space dx
$$
Desarrollamos la descomposición en fracciones simples
$$
\frac{x}{(x + 1)(x + 2)(x + 3)} = \frac{A}{x + 1} + \frac{B}{x + 2} + \frac{C}{x + 3}
$$
Desarrollamos factor común y luego resolvemos el sistema:
$$
\begin{align}
\frac{A}{x + 1} + \frac{B}{x + 2} + \frac{C}{x + 3} &= \frac{A(x + 2) + B(x + 1)}{(x + 1)(x + 2)} + \frac{C}{x + 3} \\
&= \frac{(A(x + 2) + B(x + 1))(x + 3) + C(x + 1)(x + 2)}{(x + 1)(x + 2)(x + 3)}
\end{align}
$$
$$
\begin{align}
(A(x + 2) + B(x + 1))(x + 3) + C(x + 1)(x + 2) &= (Ax + 2A + Bx + B)(x + 3) + C(x^{2} + 3x + 2) \\
&= Ax^{2} + 2Ax + Bx^{2} + Bx + 3Ax + 6A + 3Bx + 3B + Cx^{2} + 3Cx + 2C \\
&= Ax^{2} + 5Ax + Bx^{2} + 4Bx + 6A + 3B + Cx^{2} + 3Cx + 2C \\
&= (A + B + C)x^{2} + (5A + 4B + 3C)x + (6A + 3B + 2C)
\end{align}
$$
Sabiendo que $(A + B + C)x^{2} + (5A + 4B + 3C)x + (6A + 3B + 2C) = x$:
$$
\begin{cases}
A + B + C = 0 \\
5A + 4B + 3C = 1 \\
6A + 3B + 2C = 0
\end{cases}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 0 \\
5 & 4 & 3 & 1 \\
6 & 3 & 2 & 0
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 0 \\
2 & 1 & 0 & 1 \\
4 & 1 & 0 & 0
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - 3F_{1} \\
&F_{3} \leftarrow F_{3} - 2F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 0 \\
2 & 1 & 0 & 1 \\
2 & 0 & 0 & -1
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 0 \\
2 & 1 & 0 & 1 \\
1 & 0 & 0 & -\frac{1}{2}
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow \frac{1}{2}F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 1 & 1 & \frac{1}{2} \\
0 & 1 & 0 & 2 \\
1 & 0 & 0 & -\frac{1}{2}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{3} \\
&F_{2} \leftarrow F_{2} - 2F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 0 & 1 & -\frac{3}{2} \\
0 & 1 & 0 & 2 \\
1 & 0 & 0 & -\frac{1}{2}
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2}
\end{align}
$$
Reordenamos la matriz:
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & -\frac{1}{2} \\
0 & 1 & 0 & 2 \\
0 & 0 & 1 & -\frac{3}{2}
\end{array}
\right)
$$
De esta manera, determinamos que
$$
\begin{align}
&A = -\frac{1}{2} \\
&B = 2 \\
&C = -\frac{3}{2}
\end{align}
$$
Entonces:
$$
\begin{align}
\frac{x}{(x + 1)(x + 2)(x + 3)} &= \frac{A}{x + 1} + \frac{B}{x + 2} + \frac{C}{x + 3} \\
&= -\frac{\frac{1}{2}}{x + 1} + \frac{2}{x + 2} - \frac{\frac{3}{2}}{x + 3}
\end{align}
$$
De esta manera, podemos determinar la integral de la función:
$$
\begin{align}
\int \frac{x}{(x + 1)(x + 2)(x + 3)} \space dx &= \int -\frac{\frac{1}{2}}{x + 1} + \frac{2}{x + 2} - \frac{\frac{3}{2}}{x + 3} \space dx \\
&= -\frac{1}{2}\int \frac{1}{x + 1} \space dx + 2\int \frac{1}{x + 2} \space dx - \frac{3}{2}\int \frac{1}{x + 3} \space dx
\end{align}
$$
$$
\begin{align}
&-\frac{1}{2}\int \frac{1}{x + 1} \space dx = -\frac{1}{2}\log(|x + 1|) + C \\
&2\int \frac{1}{x + 2} \space dx = 2\log(|x + 2|) + C \\
&\frac{3}{2}\int \frac{1}{x + 3} \space dx = \frac{3}{2}\log(|x + 3|) + C
\end{align}
$$

En conclusión:
$$
\int \frac{x}{(x + 1)(x + 2)(x + 3)} \space dx = -\frac{1}{2}\log(|x + 1|) + 2\log(|x + 2|) - \frac{3}{2}\log(|x + 3|) + C
$$

### Parte d)
$$
\int \frac{6x^{3}}{x^{3} - 6x^{2} + 11x - 6} \space dx
$$
En este caso, es necesario reducir el grado del numerador.

Al desarrollar la división de polinomios, obtuvimos como cociente 6 y resto $36x^{2} - 66x + 36$.
De esta manera, podemos expresar al polinomio numerador como el producto del denominador y el cociente, mas el resto:
$$
6x^{3} = 6(x^{3} - 6x^{2} + 11x - 6) + 36x^{2} - 66x + 36
$$
Entonces:
$$
\begin{align}
\frac{6x^{3}}{x^{3} - 6x^{2} + 11x - 6} &= \frac{6(x^{3} - 6x^{2} + 11x - 6) + 36x^{2} - 66x + 36}{x^{3} - 6x^{2} + 11x - 6} \\
&= 6 + \frac{36x^{2} - 66x + 36}{x^{3} - 6x^{2} + 11x - 6}
\end{align}
$$

Desarrollamos la descomposición en fracciones simples. Para esto, tenemos que encontrar raíces del denominador $x^{3} - 6x^{2} + 11x - 6$. Analizando su estructura, podemos ver que $x = 1$ (ya que la suma de todos los coeficientes es 0). Entonces $x^{3} - 6x^{2} + 11x - 6 = (x - 1)(x^{2} - 5x + 6)$.

Ahora, buscamos las raíces de $x^{2} - 5x + 6$ mediante Bhaskara:
$$
\begin{align}
&a = 1 \\
&b = -5 \\
&c = 6
\end{align}
$$
$$
\begin{align}
x &= \frac{5 \pm \sqrt{ (-5)^{2} - 4 \cdot 1 \cdot 6 }}{2 \cdot 1} \\
&= \frac{5 \pm \sqrt{ 25 - 24 }}{2} \\
&= \frac{5 \pm \sqrt{ 1 }}{2} \\
&= \frac{5 \pm 1}{2}
\end{align}
$$
$$
\begin{align}
\implies &x_{1} = \frac{5 + 1}{2} = \frac{6}{2} = 3 \\
&x_{2} = \frac{5 - 1}{2} = \frac{4}{2} = 2
\end{align}
$$
De esta forma, tenemos otras dos raíces para el conjunto: $x = 3$ y $x = 2$:
$$
(x - 1)(x^{2} - 5x + 6) = (x - 1)(x - 2)(x - 3)
$$
Entonces:
$$
6 + \frac{36x^{2} - 66x + 36}{x^{3} - 6x^{2} + 11x - 6} = 6 + \frac{36x^{2} - 66x + 36}{(x - 1)(x - 2)(x - 3)} = 6 + \frac{A}{x - 1} + \frac{B}{x - 2} + \frac{C}{x - 3}
$$

Desarrollamos factor común y luego resolvemos el sistema:
$$
\begin{align}
\frac{A}{x - 1} + \frac{B}{x - 2} + \frac{C}{x - 3} &= \frac{A(x - 2) + B(x - 1)}{(x - 1)(x - 2)} + \frac{C}{x - 3} \\
&= \frac{(A(x - 2) + B(x - 1))(x - 3) + C(x - 1)(x - 2)}{(x - 1)(x - 2)(x - 3)}
\end{align}
$$
$$
\begin{align}
(A(x - 2) + B(x - 1))(x - 3) + C(x - 1)(x - 2) &= (Ax - 2A + Bx - B)(x - 3) + C(x^{2} - 3x + 2) \\
&= Ax^{2} - 2Ax + Bx^{2} - Bx - 3Ax + 6A - 3Bx + 3B + Cx^{2} - 3Cx + 2C \\
&= Ax^{2} - 5Ax + Bx^{2} - 4Bx + 6A + 3B + Cx^{2} - 3Cx + 2C \\
&= (A + B + C)x^{2} + (-5A - 4B - 3C)x + (6A + 3B + 2C)
\end{align}
$$
Sabiendo que $(A + B + C)x^{2} + (-5A - 4B - 3C)x + (6A + 3B + 2C) = 36x^{2} - 66x + 36$:
$$
\begin{cases}
A + B + C = 36 \\
-5A - 4B - 3C = -66 \\
6A + 3B + 2C = 36
\end{cases}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 36 \\
-5 & -4 & -3 & -66 \\
6 & 3 & 2 & 36
\end{array}
\right)
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 36 \\
5 & 4 & 3 & 66 \\
6 & 3 & 2 & 36
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow -F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 36 \\
2 & 1 & 0 & -42 \\
4 & 1 & 0 & -36
\end{array}
\right)
\begin{align}
&F_{2} \leftarrow F_{2} - 3F_{1} \\
&F_{3} \leftarrow F_{3} - 2F_{1}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 36 \\
2 & 1 & 0 & -42 \\
2 & 0 & 0 & 6
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow F_{3} - F_{2}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
1 & 1 & 1 & 36 \\
2 & 1 & 0 & -42 \\
1 & 0 & 0 & 3
\end{array}
\right)
\begin{align}
&F_{3} \leftarrow \frac{1}{2}F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 1 & 1 & 33 \\
0 & 1 & 0 & -48 \\
1 & 0 & 0 & 3
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{3} \\
&F_{2} \leftarrow F_{2} - 2F_{3}
\end{align}
$$
$$
\left(
\begin{array}{ccc|c}
0 & 0 & 1 & 81 \\
0 & 1 & 0 & -48 \\
1 & 0 & 0 & 3
\end{array}
\right)
\begin{align}
&F_{1} \leftarrow F_{1} - F_{2}
\end{align}
$$
Reordenamos la matriz:
$$
\left(
\begin{array}{ccc|c}
1 & 0 & 0 & 3 \\
0 & 1 & 0 & -48 \\
0 & 0 & 1 & 81
\end{array}
\right)
$$
De esta manera, determinamos que
$$
\begin{align}
&A = 3 \\
&B = -48 \\
&C = 81
\end{align}
$$
Entonces:
$$
\begin{align}
\frac{6x^{3}}{x^{3} - 6x^{2} + 11x - 6} &= 6 + \frac{A}{x - 1} + \frac{B}{x - 2} + \frac{C}{x - 3} \\
&= 6 + \frac{3}{x - 1} - \frac{48}{x - 2} + \frac{81}{x - 3}
\end{align}
$$
De esta manera, podemos determinar la integral de la función:
$$
\begin{align}
\int \frac{6x^{3}}{x^{3} - 6x^{2} + 11x - 6} \space dx &= \int 6 + \frac{3}{x - 1} - \frac{48}{x - 2} + \frac{81}{x - 3} \space dx \\
&= 6\int 1 \space dx + 3\int \frac{1}{x - 1} \space dx - 48\int \frac{1}{x - 2} \space dx + 81\int \frac{1}{x - 3} \space dx
\end{align}
$$
$$
\begin{align}
&6\int 1 \space dx = 6x + C \\
&3\int \frac{1}{x - 1} \space dx = 3\log(|x - 1|) + C \\
&48\int \frac{1}{x - 2} \space dx = 48\log(|x - 2|) + C \\
&81\int \frac{1}{x - 3} \space dx = 81\log(|x - 3|) + C
\end{align}
$$

En conclusión:
$$
\int \frac{6x^{3}}{x^{3} - 6x^{2} + 11x - 6} \space dx \space dx = 6x + 3\log(|x - 1|) - 48\log(|x - 2|) + 81\log(|x - 3|) + C
$$

### Parte f)
$$
\int \frac{4x - 3}{3x^{2} + 3x + 2} \space dx
$$
Desarrollamos la descomposición en fracciones simples. Para esto, tenemos que encontrar raíces del denominador $3x^{2} + 3x + 2$. Para esto utilizaremos Bhaskara:
$$
\begin{align}
&a = 3 \\
&b = 3 \\
&c = 2
\end{align}
$$
$$
\begin{align}
x &= \frac{-3 \pm \sqrt{ 3^{2} - 4 \cdot 3 \cdot 2 }}{2 \cdot 3} \\
&= \frac{-3 \pm \sqrt{ 9 - 24 }}{6} \\
&= \frac{-3 \pm \sqrt{ -15 }}{6}
\end{align}
$$
Como vemos, el discriminante es negativo, lo que indica que el polinomio no tiene raíces reales.

Entonces, tenemos que aplicar el método de completar cuadrados (llevar a la función a la forma de la derivada de arco tangente $\frac{x}{x^{2} + 1}$):

Ahora, lo que tenemos que hacer es intentar separar el cociente en dos términos: uno que se resuelva por sustitución y otro por completar cuadrados.

Además, para el término que se resolverá por sustitución, tenemos que considerar la derivada del denominador:
$$
(3x^{2} + 3x + 2)' = 6x + 3
$$
Conviene expresar el numerador de tal forma que aparezca dicho término:
$$
\begin{align}
4x - 3 &= A(6x + 3) + B \\
&= 6Ax + 3A + B
\end{align}
$$
$$
\begin{cases}
6A = 4 \implies A = \frac{4}{6} = \frac{2}{3} \\
3A + B = -3 \implies 2 + B = -3 \implies B = -5
\end{cases}
$$
$$
\implies 4x - 3 = \frac{2}{3}(6x + 3) - 5
$$

Entonces:
$$
\begin{align}
\int \frac{4x - 3}{3x^{2} + 3x + 2} \space dx &= \int \frac{\frac{2}{3}(6x + 3) - 5}{3x^{2} + 3x + 2} \space dx \\
&= \int \frac{\frac{2}{3}(6x + 3)}{3x^{2} + 3x + 2} - \frac{5}{3x^{2} + 3x + 2} \space dx \\
&= \int \frac{\frac{2}{3}(6x + 3)}{3x^{2} + 3x + 2} \space dx - \int \frac{5}{3x^{2} + 3x + 2} \space dx \\
&= \frac{2}{3}\int \frac{6x + 3}{3x^{2} + 3x + 2} \space dx - 5\int \frac{1}{3x^{2} + 3x + 2} \space dx
\end{align}
$$

El primer término se resuelve mediante sustitución:
$$
\int \frac{6x + 3}{3x^{2} + 3x + 2} \space dx \underbrace{ = }_{ \begin{align}
&u = 3x^{2} + 3x + 2 \\
&du = 6x + 3 \space dx
\end{align} } \int \frac{du}{u} = \log(u) + C \underbrace{ = }_{ DCV } \log(|3x^{2} + 3x + 2|) + C
$$

Ahora, estudiamos el segundo término:

Necesitamos completar el cuadrado: No podemos escribir la función $3x^{2} + 3x + 2$ como el cuadrado de otro polinomio. Sin embargo, podemos escribirlo como el cuadrado de un polinomio mas un resto:
$$
3x^{2} + 3x + 2 = 3\left( x^{2} + x + \frac{2}{3} \right) = 3 \left( x + \frac{1}{2} \right)^{2} + \frac{5}{4}
$$
ya que $\left( x + \frac{1}{2} \right)^{2} = x^{2} + x + \frac{1}{4}$.

De esta manera:
$$
\begin{align}
\int \frac{1}{3x^{2} + 3x + 2} \space dx &= \int \frac{1}{3 \left( x + \frac{1}{2} \right)^{2} + \frac{5}{4}} \space dx \\
&= \frac{1}{3}\int \frac{1}{\left( x + \frac{1}{2} \right)^{2} + \frac{5}{12}} \space dx \\
&\underbrace{ = }_{ \begin{aligned}
&u = x + \frac{1}{2} \\
&du = dx
\end{aligned} } \frac{1}{3}\int \frac{du}{u^{2} + \frac{5}{12}} \\
&= \frac{1}{3}\int \frac{du}{u^{2} + \left( \frac{\sqrt{ 5 }}{\sqrt{ 12 }} \right)^{2}} \\
&= \frac{1}{3}\int \frac{du}{\left( \frac{\sqrt{ 5 }}{\sqrt{ 12 }} \right)^{2}\left( \frac{u^{2}}{\left( \frac{\sqrt{ 5 }}{\sqrt{ 12 }} \right)^{2}} + 1 \right)} \\
&= \frac{1}{3\left( \frac{\sqrt{ 5 }}{\sqrt{ 12 }} \right)^{2}}\int \frac{du}{\frac{u^{2}}{\left( \frac{\sqrt{ 5 }}{\sqrt{ 12 }} \right)^{2}} + 1} \\
&= \frac{1}{3\left( \frac{\sqrt{ 5 }}{\sqrt{ 12 }} \right)^{2}}\int \frac{du}{\left( \frac{u}{\frac{\sqrt{ 5 }}{\sqrt{ 12 }}} \right)^{2} + 1} \\
&= \frac{\cancel{ \frac{\sqrt{ 5 }}{\sqrt{ 12 }} }}{3\left( \frac{\sqrt{ 5 }}{\sqrt{ 12 }} \right)\cancel{ ^{2} }}\int \frac{\frac{du}{\frac{\sqrt{ 5 }}{\sqrt{ 12 }}}}{\left( \frac{u}{\frac{\sqrt{ 5 }}{\sqrt{ 12 }}} \right)^{2} + 1} \\
&= \frac{\sqrt{ 12 }}{3 \sqrt{ 5 }}\int \frac{\frac{du}{\frac{\sqrt{ 5 }}{\sqrt{ 12 }}}}{\left( \frac{u}{\frac{\sqrt{ 5 }}{\sqrt{ 12 }}} \right)^{2} + 1} \\
&= \frac{\sqrt{ 12 }}{3 \sqrt{ 5 }} \arctan\left( \frac{\sqrt{ 12 }}{\sqrt{ 5 }}u \right) + C \\
&\underbrace{ = }_{ DCV } \frac{\sqrt{ 12 }}{3 \sqrt{ 5 }} \arctan\left( \frac{\sqrt{ 12 }}{\sqrt{ 5 }}\left( x + \frac{1}{2} \right) \right) + C \\
&= \frac{\sqrt{ 12 }}{3 \sqrt{ 5 }} \arctan\left( \frac{\sqrt{ 12 }x + \sqrt{ 3 }}{\sqrt{ 5 }} \right) + C
\end{align}
$$

Ahora, sustituimos los valores obtenidos:
$$
\begin{align}
\int \frac{4x - 3}{3x^{2} + 3x + 2} \space dx &= \frac{2}{3}\int \frac{6x + 3}{3x^{2} + 3x + 2} \space dx - 5\int \frac{1}{3x^{2} + 3x + 2} \space dx \\
&= \frac{2}{3}\log(|3x^{2} + 3x + 2|) - 5 \cdot \frac{\sqrt{ 12 }}{3 \sqrt{ 5 }} \arctan\left( \frac{\sqrt{ 12 }x + \sqrt{ 3 }}{\sqrt{ 5 }} \right) + C \\
&= \frac{2}{3}\log(|3x^{2} + 3x + 2|) - \frac{5\sqrt{ 12 }}{3 \sqrt{ 5 }} \arctan\left( \frac{\sqrt{ 12 }x + \sqrt{ 3 }}{\sqrt{ 5 }} \right) + C
\end{align}
$$

En conclusión:
$$
\int \frac{4x - 3}{3x^{2} + 3x + 2} \space dx = \frac{2}{3}\log(|3x^{2} + 3x + 2|) - \frac{5\sqrt{ 12 }}{3 \sqrt{ 5 }} \arctan\left( \frac{\sqrt{ 12 }x + \sqrt{ 3 }}{\sqrt{ 5 }} \right) + C
$$

### Parte i)
$$
\int \frac{1}{(x^{2} + 1)(x^{2} + 2)} \space dx
$$
Desarrollamos la descomposición en fracciones simples. Si estudiamos los factores del denominador, podemos ver que ninguno de los dos tiene raíces reales, por lo que tendremos que aplicar el mismo método visto en la parte f.

$$
\begin{align}
\frac{1}{(x^{2} + 1)(x^{2} + 2)} &= \frac{Ax + B}{x^{2} + 1} + \frac{Cx + D}{x^{2} + 2} \\
&= \frac{(Ax + B)(x^{2} + 2) + (Cx + D)(x^{2} + 1)}{(x^{2} + 1)(x^{2} + 2)} \\
&= \frac{Ax^{3} + 2Ax + Bx^{2} + 2B + Cx^{3} + Cx + Dx^{2} + D}{(x^{2} + 1)(x^{2} + 2)} \\
&= \frac{(A + C)x^{3} + (B + D)x^{2} + (2A + C)x + (2B + D)}{(x^{2} + 1)(x^{2} + 2)}
\end{align}
$$
$$
\begin{cases}
A + C = 0 \\
B + D = 0 \\
2A + C = 0 \\
2B + D = 1
\end{cases}
$$
$$
\begin{align}
&A + C = 0 \land 2A + C = 0 \implies 2A + C - (A + C) = 2A + C - A - C = 0 \implies A = 0 \\
&A + C = 0 \implies C = 0 \\
&B + D = 0 \land 2B + D = 1 \implies 2B + D - (B + D) = 2B + D - B - D = 1 \implies B = 1 \\
&B + D = 0 \implies D = -1
\end{align}
$$
$$
\implies \frac{1}{(x^{2} + 1)(x^{2} + 2)} = \frac{Ax + B}{x^{2} + 1} + \frac{Cx + D}{x^{2} + 2} = \frac{1}{x^{2} + 1} - \frac{1}{x^{2} + 2}
$$

De esta manera:
$$
\int \frac{1}{(x^{2} + 1)(x^{2} + 2)} \space dx = \int \frac{1}{x^{2} + 1} - \frac{1}{x^{2} + 2} \space dx = \int \frac{1}{x^{2} + 1} \space dx - \int \frac{1}{x^{2} + 2} \space dx
$$
$$
\int \frac{1}{x^{2} + 1} \space dx = \arctan(x) + C \\
$$
$$
\begin{align}
\int \frac{1}{x^{2} + 2} \space dx &= \int \frac{1}{x^{2} + (\sqrt{ 2 })^{2}} \space dx \\
&= \int \frac{1}{(\sqrt{ 2 })^{2}\left( \frac{x^{2}}{(\sqrt{ 2 })^{2}} + 1 \right)} \space dx \\
&= \int \frac{1}{(\sqrt{ 2 })^{2}\left( \left( \frac{x}{\sqrt{ 2 }} \right)^{2} + 1 \right)} \space dx \\
&= \int \frac{1}{(\sqrt{ 2 })^{2}\left( \left( \frac{x}{\sqrt{ 2 }} \right)^{2} + 1 \right)} \space dx \\
&= \frac{1}{(\sqrt{ 2 })^{2}} \int \frac{1}{\left( \frac{x}{\sqrt{ 2 }} \right)^{2} + 1} \space dx \\
&= \frac{\cancel{ \sqrt{ 2 } }}{(\sqrt{ 2 })\cancel{ ^{2} }} \int \frac{\frac{1}{\sqrt{ 2 }}}{\left( \frac{x}{\sqrt{ 2 }} \right)^{2} + 1} \space dx \\
&= \frac{1}{\sqrt{ 2 }} \int \frac{\frac{1}{\sqrt{ 2 }}}{\left( \frac{x}{\sqrt{ 2 }} \right)^{2} + 1} \space dx \\
&\underbrace{ = }_{ \begin{aligned}
&u = \frac{x}{\sqrt{ 2 }} \\
&du = dx
\end{aligned} } \frac{1}{\sqrt{ 2 }} \int \frac{du}{u^{2} + 1} \\
&= \frac{1}{\sqrt{ 2 }} \arctan(u) + C \\
&\underbrace{ = }_{ DCV } \frac{1}{\sqrt{ 2 }} \arctan \left( \frac{x}{\sqrt{ 2 }} \right) + C
\end{align}
$$

Ahora, sustituimos los valores obtenidos:
$$
\begin{align}
\int \frac{1}{(x^{2} + 1)(x^{2} + 2)} \space dx &= \int \frac{1}{x^{2} + 1} \space dx - \int \frac{1}{x^{2} + 2} \space dx \\
&= \arctan(x) - \frac{1}{\sqrt{ 2 }} \arctan \left( \frac{x}{\sqrt{ 2 }} \right) + C
\end{align}
$$

En conclusión:
$$
\int \frac{1}{(x^{2} + 1)(x^{2} + 2)} \space dx = \arctan(x) - \frac{1}{\sqrt{ 2 }} \arctan \left( \frac{x}{\sqrt{ 2 }} \right) + C
$$

---
## Ejercicio 7.2.4
### Parte a)
$$
\int x \sqrt{ 3x + 10 } \space dx
$$
Aplicamos sustitución:

$$
\begin{align}
&u = 3x + 10 \\
&du = (3x + 10)' \space dx = 3 \space dx \implies \frac{1}{3} \space du = dx
\end{align}
$$
Esto también nos permite despejar la $x$ suelta:
$$
\begin{align}
u &= 3x + 10 \\
u - 10 &= 3x \\
\frac{u - 10}{3} &= x
\end{align}
$$

$$
\begin{align}
\int x \sqrt{ 3x + 10 } \space dx &\underbrace{ = }_{ \begin{aligned}
&u = 3x + 10 \\
&du = 3 \space dx \implies dx = \frac{1}{3} du
\end{aligned} } \int \left( \frac{u - 10}{3} \right) \cdot \sqrt{ u } \cdot \frac{1}{3} \space du \\
&= \int \frac{\sqrt{ u } (u - 10)}{9} \space du \\
&= \int \frac{u^{\frac{1}{2}} (u - 10)}{9}\space du \\
&= \int \frac{u^{\frac{3}{2}} - 10u^{\frac{1}{2}}}{9} \space du \\
&= \frac{1}{9} \int u^{\frac{3}{2}} - 10u^{\frac{1}{2}} \space du \\
&= \frac{1}{9} \left( \int u^{\frac{3}{2}} \space du - 10 \int u^{\frac{1}{2}} \space du \right) \\
&= \frac{1}{9} \left( \frac{u^{\frac{5}{2}}}{\frac{5}{2}} - 10 \int \frac{u^{\frac{3}{2}}}{\frac{3}{2}} \right) \\
&= \frac{2u^{\frac{5}{2}}}{45} - \frac{20u^{\frac{3}{2}}}{27} \\
&= \frac{6u^{\frac{5}{2}} - 100u^{\frac{3}{2}}}{1215} \\
&\underbrace{ = }_{ DCV } \frac{2(3x + 10)^{\frac{5}{2}} - 100(3x + 10)^{\frac{3}{2}}}{135} \\
&= \frac{6(3x + 10)^{2}\sqrt{ 3x + 10 } - 100(3x + 10)\sqrt{ 3x + 10 }}{135} \\
&= \frac{6(9x^{2} + 60x + 100)\sqrt{ 3x + 10 } - 100(3x + 10)\sqrt{ 3x + 10 }}{135} \\
&= \frac{(54x^{2} + 360x + 600)\sqrt{ 3x + 10 } - (300x + 1000)\sqrt{ 3x + 10 }}{135} \\
&= \frac{(54x^{2} + 360x + 600 - 300x - 1000 )\sqrt{ 3x + 10 }}{135} \\
&= \frac{(54x^{2} + 60x - 400)\sqrt{ 3x + 10 }}{135} \\
&= \frac{2(27x^{2} + 30x - 200)\sqrt{ 3x + 10 }}{135}
\end{align}
$$
En conclusión:
$$
\int x \sqrt{ 3x + 10 } \space dx = \frac{2(27x^{2} + 30x - 200)\sqrt{ 3x + 10 }}{135} + C
$$

### Parte b)
$$
\begin{align}
\int \sqrt[3]{ x } (2x + 1) \space dx
\end{align}
$$
$$
\begin{align}
\int \sqrt[3]{ x } (2x + 1) \space dx &= \int x^{\frac{1}{3}} (2x + 1) \space dx \\
&= \int 2x^{\frac{4}{3}} + x^{\frac{1}{3}} \space dx \\
&= 2 \int x^{\frac{4}{3}} \space dx + \int x^{\frac{1}{3}} \space dx \\
&= 2 \frac{x^{\frac{7}{3}}}{\frac{7}{3}} + \frac{x^{\frac{4}{3}}}{\frac{4}{3}} \\
&= \frac{6x^{\frac{7}{3}}}{7} + \frac{3x^{\frac{4}{3}}}{4} \\
&= \frac{24x^{\frac{7}{3}} + 21x^{\frac{4}{3}}}{28} \\
&= \frac{6}{7}x^{\frac{7}{3}} + \frac{3}{4}x^{\frac{4}{3}}
\end{align}
$$

En conclusión:
$$
\int \sqrt[3]{ x } (2x + 1) \space dx = \frac{6}{7}x^{\frac{7}{3}} + \frac{3}{4}x^{\frac{4}{3}} + C
$$

CONSEJO: Siempre que se trabaje con una raíz, conviene expresarla en forma de potencia. Por ejemplo:
$$
\begin{align}
\sqrt{ x } &= x^{\frac{1}{2}} \\
\sqrt[3]{ x } &= x^{\frac{1}{3}} \\
\sqrt[4]{ x } &= x^{\frac{1}{4}} \\
&\dots
\end{align}
$$

### Parte d)
$$
\int \sin(x) \cos(x) e^{\cos(x)} \space dx
$$
Aquí aplicaremos sustitución, ya que:
$$
\begin{align}
&g(x) = \cos(x) \implies g'(x) = -\sin(x) \\
&f(g(x)) = e^{\cos(x)}
\end{align}
$$
$$
\begin{align}
&u = \cos(x) \\
&du = -\sin(x) \space dx
\end{align}
$$
$$
\begin{align}
\int \sin(x) \cos(x) e^{\cos(x)} \space dx &= -\int -\sin(x) \cos(x) e^{\cos(x)} \space dx \\
&\underbrace{ = }_{  } -\int -\sin(x) \cos(x) e^{\cos(x)} \space dx
\end{align}
$$



---
## Ejercicio 7.2.6
Dos partes.

La idea del ejercicio es aplicar sustitución, pero en lugar de sustituir por una variable más "simple", sustituir por las funciones trigonométricas hiperbólicas.

### Parte a)
$$
\int \sqrt{ 1 + x^{2} } \space dx
$$
Aplicamos sustitución:
$$
\begin{align}
\int \sqrt{ 1 + x^{2} } \space dx &\underbrace{ = }_{ \begin{aligned}
&x = \sinh(u) \\
&dx = \cosh(u) \space du
\end{aligned} } \int \sqrt{ 1 + \sinh ^{2}(u) } \cosh(u) \space du \\
&= \int \sqrt{ \cosh ^{2}(u) } \cosh(u) \space du \\
&= \int \cosh(u) \cosh(u) \space du
\end{align}
$$
Ahora, aplicamos partes:
$$
\left[
\begin{align}
&f(x) = \cosh(u) && f'(x) = \sinh(u) \\
&g'(x) = \cosh(u) && g(x) = \sinh(u) 
\end{align}
\right]
$$
$$
\begin{align}
\int \cosh(u) \cosh(u) \space du &= \cosh(u)\sinh(u) - \int \sin(u) \sin(u) \space du \\
&= \cosh(u)\sinh(u) - \int \cosh(x) \cosh(x) - 1 \space du \\
&= \cosh(u)\sinh(u) - \int \cosh(x) \cosh(x) \space du - \int 1 \space du \\
2\int \cosh(u) \cosh(u) \space du &= \cosh(u)\sinh(u) - \int 1 \space du \\
2\int \cosh(u) \cosh(u) \space du &= \cosh(u)\sinh(u) - u \\
\int \cosh(u) \cosh(u) \space du &= \frac{\cosh(u)\sinh(u) - u}{2}
\end{align}
$$
Ahora, deshacemos el cambio de variable poco a poco, aplicando las igualdades de las funciones propuestas:
$$
\begin{align}
\sinh(u) = x \implies u = arcsinh(x) \\
\cosh(u) = \sqrt{ 1 + \sinh ^{2}(u) } = \sqrt{ 1 + x^{2} }
\end{align}
$$
$$
\implies \int \cosh(u) \cosh(u) \space du = \frac{x\sqrt{ 1 + x^{2} } - arcsinh(x)}{2}
$$

En conclusión:
$$
\int \sqrt{ 1 + x^{2} } \space dx = \frac{x\sqrt{ 1 + x^{2} } - arcsinh(x)}{2}
$$


### Parte d)
$$
\int \frac{1}{\sqrt{ x^{2} - 1 }} \space dx
$$
Aplicamos sustitución:
$$
\begin{align}
\int \frac{1}{\sqrt{ x^{2} - 1 }} \space dx &\underbrace{ = }_{ \begin{aligned}
&x = \cosh(u) \\
&dx = \sinh(u) \space du
\end{aligned} } \int \frac{\sinh(u)}{\sqrt{ \cosh^{2}(u) - 1 }} \space du \\
&= \int \frac{\sinh(u)}{\sqrt{ \cosh^{2}(u) - 1 }} \space du \\
&= \int \frac{\sinh(u)}{\sinh(u)} \space du \\
&= \int 1 \space du \\
&= u + C
\end{align}
$$
Finalmente, consideramos que
$$
x = \cosh(u) \implies u = arccosh(x)
$$

En conclusión:
$$
\int \frac{1}{\sqrt{ x^{2} - 1 }} \space dx = arccosh(x)
$$

---
# 3 - Áreas
## Ejercicio 7.3.1
Una parte.

Este ejercicio es similar a muchos realizados en el práctico de integrales. La única diferencia es que ahora tenemos métodos mucho más eficaces para calcular áreas, así como la posibilidad de hacerlo con nuevas funciones.

En general, tenemos que estudiar los puntos de intersección de las funciones, y ver que función es mayor que la otra según el intervalo considerado

### Parte a)
$$
f(x) = e^{x - 1} - 1, g(x) = 1 - x^{2}, I = [0, 2]
$$
Primero, identifiquemos intersecciones entre $f(x)$ y $g(x)$ que se encuentren en el intervalo $I$:
$$
\begin{align}
e^{x - 1} - 1 &= 1 - x^{2} \\
e^{x - 1} - 1 - 1 + x^{2} &= 0 \\
e^{x - 1} - 2 + x^{2} &= 0
\end{align}
$$
Podemos ver que, si $x = 1$:
$$
\begin{align}
e^{1 - 1} - 2 + 1^{2} &= 0 \\
e^{0} - 2 + 1 &= 0 \\
1 - 2 + 1 &= 0
\end{align}
$$

Entonces, ambas funciones se interceptan en $x = 1$.

Por el comportamiento de las funciones $f(x)$ es estrictamente creciente, mientras que $g(x)$ es estrictamente decreciente (al menos en el intervalo $I$). Por esta razón, sabemos que el único punto de intersección entre $f(x)$ y $g(x)$ es $(1, 0)$.

Si estudiamos el gráfico de ambas, podemos ver que $f(x)$ se encuentra por debajo de $g(x)$ en $[0, 1]$ y por encima en $[1, 2]$. Entonces, tenemos que operar de la siguiente forma:
$$
\int_{0}^{1} g(x) - f(x) \space dx + \int_{1}^{2} f(x) - g(x) \space dx
$$
$$
\begin{align}
&\int_{0}^{1} g(x) - f(x) \space dx = \int_{0}^{1} g(x) \space dx - \int_{0}^{1} f(x) \space dx \\
&\int_{1}^{2} f(x) - g(x) \space dx = \int_{1}^{2} f(x) \space dx - \int_{1}^{2} g(x) \space dx
\end{align}
$$

Entonces, tenemos que determinar:
$$
\begin{align}
&\int f(x) \space dx = \int e^{x - 1} - 1 \space dx = e^{x - 1} - x \\
&\int g(x) \space dx = \int 1 - x^{2} \space dx = x - \frac{x^{3}}{3}
\end{align}
$$
Ahora, podemos calcular las áreas en los intervalos propuestos:
$$
\begin{align}
\int_{0}^{1} 1 - x^{2} \space dx - \int_{0}^{1} e^{x - 1} - 1 \space dx &= x - \frac{x^{3}}{3} |_{0}^{1} - e^{x - 1} - x |_{0}^{1} \\
&= 1 - \frac{1^{3}}{3} - \cancel{ \left( 0 - \frac{0^{3}}{3} \right) } - (e^{1 - 1} - 1 - (e^{0 - 1} - 0)) \\
&= 1 - \frac{1}{3} - (\cancel{ e^{0} - 1 } - e^{-1}) \\
&= \frac{2}{3} + \frac{1}{e}
\end{align}
$$
$$
\begin{align}
\int_{1}^{2} e^{x - 1} - 1 \space dx - \int_{1}^{2} 1 - x^{2} \space dx &= e^{x - 1} - x |_{1}^{2} - x - \frac{x^{3}}{3} |_{1}^{2} \\
&= e^{2 - 1} - 2 - \cancel{ (e^{1 - 1} - 1) } - \left( 2 - \frac{2^{3}}{3} - \left( 1 - \frac{1^{3}}{3} \right) \right) \\
&= e^{1} - 2 - \left( 2 - \frac{8}{3} - \left( 1 - \frac{1}{3} \right) \right) \\
&= e - 2 - \left( -\frac{2}{3} - \frac{2}{3} \right) \\
&= e - 2 + \frac{4}{3} \\
&= e - \frac{2}{3}
\end{align}
$$

Finalmente, unimos ambos resultados:
$$
\begin{align}
\int_{0}^{1} g(x) - f(x) \space dx + \int_{1}^{2} f(x) - g(x) \space dx &= \frac{2}{3} + \frac{1}{e} + \left( e - \frac{2}{3} \right) \\
&= \cancel{ \frac{2}{3} } + \frac{1}{e} + e - \cancel{ \frac{2}{3} } \\
&= e + \frac{1}{e}
\end{align}
$$

En conclusión:
$$
\int_{0}^{1} g(x) - f(x) \space dx + \int_{1}^{2} f(x) - g(x) \space dx = e + \frac{1}{e}
$$

### Parte c)
$$
f(x) = \sin(x), g(x) = \cos(x), I = \left[ 0, \frac{\pi}{2} \right]
$$
Primero, identifiquemos intersecciones entre $f(x)$ y $g(x)$ que se encuentren en el intervalo $I$:
$$
\sin(x) = \cos(x)
$$
Consideramos $\sin(x) = \cos(x) = a$:
$$
\begin{align}
a^{2} + a^{2} &= 1 \\
2a^{2} &= 1 \\
a^{2} &= \frac{1}{2} \\
a &= \sqrt{ \frac{1}{2} } \\
a &= \frac{1}{\sqrt{ 2 }} = \frac{\sqrt{ 2 }}{2}
\end{align}
$$

Podemos ver que las funciones se interceptan en $\left( x, \frac{1}{\sqrt{ 2 }} \right)$, con $x = \frac{\pi}{4}$.

Si estudiamos el gráfico de ambas, podemos ver que $f(x)$ se encuentra por debajo de $g(x)$ en $\left[ 0, \frac{\pi}{4} \right]$ y por encima en $\left[ \frac{\pi}{4}, \frac{\pi}{2} \right]$. Entonces, tenemos que operar de la siguiente forma:
$$
\int_{0}^{\frac{\pi}{4}} g(x) - f(x) \space dx + \int_{\frac{\pi}{4}}^{\frac{\pi}{2}} f(x) - g(x) \space dx
$$
$$
\begin{align}
&\int_{0}^{\frac{\pi}{4}} g(x) - f(x) \space dx = \int_{0}^{\frac{\pi}{4}} g(x) \space dx - \int_{0}^{\frac{\pi}{4}} f(x) \space dx \\
&\int_{\frac{\pi}{4}}^{\frac{\pi}{2}} f(x) - g(x) \space dx = \int_{\frac{\pi}{4}}^{\frac{\pi}{2}} f(x) \space dx - \int_{\frac{\pi}{4}}^{\frac{\pi}{2}} g(x) \space dx
\end{align}
$$

Entonces, tenemos que determinar:
$$
\begin{align}
&\int f(x) \space dx = \int \sin(x) \space dx = -\cos(x) \\
&\int g(x) \space dx = \int \cos(x) \space dx = \sin(x)
\end{align}
$$

Ahora, podemos calcular las áreas en los intervalos propuestos:
$$
\begin{align}
\int_{0}^{\frac{\pi}{4}} g(x) \space dx - \int_{0}^{\frac{\pi}{4}} f(x) \space dx &= \sin(x) |_{0}^{\frac{\pi}{4}} - (-\cos(x)) |_{0}^{\frac{\pi}{4}} \\
&= \sin\left( \frac{\pi}{4} \right) - \sin(0) - \left( -\cos\left( \frac{\pi}{4} \right) - (-\cos(0)) \right) \\
&= \sin\left( \frac{\pi}{4} \right) - \left( -\cos\left( \frac{\pi}{4} \right) + 1 \right) \\
&= \frac{1}{\sqrt{ 2 }} - \left( -\frac{1}{\sqrt{ 2 }} + 1 \right) \\
&= \frac{1}{\sqrt{ 2 }} + \frac{1}{\sqrt{ 2 }} - 1 \\
&= \sqrt{ 2 } - 1
\end{align}
$$
$$
\begin{align}
\int_{\frac{\pi}{4}}^{\frac{\pi}{2}} f(x) \space dx - \int_{\frac{\pi}{4}}^{\frac{\pi}{2}} g(x) \space dx &= (-\cos(x)) |_{\frac{\pi}{4}}^{\frac{\pi}{2}} - \sin(x) |_{\frac{\pi}{4}}^{\frac{\pi}{2}} \\
&= \left( -\cos\left( \frac{\pi}{2} \right) \right) - \left( -\cos\left( \frac{\pi}{4} \right) \right) - \left( \sin\left( \frac{\pi}{2} \right) - \sin\left( \frac{\pi}{4} \right) \right) \\
&= \cancel{ -\cos\left( \frac{\pi}{2} \right) } + \cos\left( \frac{\pi}{4} \right) - \sin\left( \frac{\pi}{2} \right) + \sin\left( \frac{\pi}{4} \right) \\
&= \frac{1}{\sqrt{ 2 }} - 1 + \frac{1}{\sqrt{ 2 }} \\
&= \frac{2}{\sqrt{ 2 }} - 1 \\
&= \sqrt{ 2 } - 1
\end{align}
$$

Finalmente, unimos ambos resultados:
$$
\begin{align}
\int_{0}^{\frac{\pi}{4}} g(x) - f(x) \space dx + \int_{\frac{\pi}{4}}^{\frac{\pi}{2}} f(x) - g(x) \space dx &= \sqrt{ 2 } - 1 + \sqrt{ 2 } - 1 \\
&= 2\sqrt{ 2 } - 2
\end{align}
$$

En conclusión:
$$
\int_{0}^{\frac{\pi}{4}} g(x) - f(x) \space dx + \int_{\frac{\pi}{4}}^{\frac{\pi}{2}} f(x) - g(x) \space dx = 2\sqrt{ 2 } - 2
$$

---
## Ejercicio 7.3.2
Dos partes.

Aquí, tenemos que determinar los dos puntos de intersección entre las funciones dadas, y calcular el área en el intervalo delimitado por las intersecciones.

### Parte b)
Trabajamos con la hipérbola $9x^{2} - 4y^{2} = 36$ y la recta $x = 3$. Como la recta $x = 3$ es simplemente una recta vertical en la cual todos los puntos tienen la forma $(3, y), y \in \mathbb{R}$, sabemos que las ecuaciones se interceptan al menos dos veces en $x = 3$.

Ahora, tenemos que saber cual es el extremo inferior de la integral a definir:
$$
\begin{align}
9x^{2} - 4y^{2} &= 36 \\
-4y^{2} &= 36 - 9x^{2} \\
y^{2} &= \frac{36 - 9x^{2}}{-4} \\
y^{2} &= \frac{9x^{2} - 36}{4} \\
y^{2} &= \frac{9}{4}(x^{2} - 4) \\
y &= \sqrt{ \frac{9}{4}(x^{2} - 4) } \\
y &= \frac{3}{2} \sqrt{ x^{2} - 4 }
\end{align}
$$
En base a la expresión desarrollada, podemos ver que la hipérbola no está definida en el intervalo $(-2, 2)$. Por lo tanto, el límite inferior que nos interesa es 2. Entonces, tenemos que calcular el área interna de la hipérbola en el intervalo $[2, 3]$. Sabemos que la hipérbola tiene dos ramas, una positiva y una negativa, las cuales se encuentran en el vértice $(2, 0)$. Entonces, como ambas están espejadas con respecto al eje $x$, podemos considerarlas como dos funciones en espejo:
$$
\begin{align}
&f(x) = \frac{3}{2} \sqrt{ x^{2} - 4 } \\
&g(x) = -\frac{3}{2} \sqrt{ x^{2} - 4 }
\end{align}
$$
De esta manera, tenemos que calcular el área de la función positiva y duplicarla, o lo que es lo mismo, al área de la función positiva, restarle el área de la negativa:
$$
\begin{align}
2 \int_{2}^{3} \frac{3}{2} \sqrt{ x^{2} - 4 } \space dx &= \int_{2}^{3} 3 \sqrt{ x^{2} - 4 } \space dx \\
&= 3 \int_{2}^{3} \sqrt{ x^{2} - 4 } \space dx
\end{align}
$$
En este caso, aplicaremos sustitución, considerando las funciones vistas en el ejercicio 7.2.6, específicamente el coseno hiperbólico:
$$
\begin{align}
\int_{2}^{3} \sqrt{ x^{2} - 4 } \space dx &\underbrace{ = }_{ \begin{aligned}
&2 \cosh(u) = x \\
&2 \sinh(u) \space du = dx
\end{aligned} } \int_{0}^{arccosh\left( \frac{3}{2} \right)} \sqrt{ 4 \cosh ^{2}(u) - 4 } \cdot 2 \sinh(u) \space du \\
\end{align}
$$
Aclaración sobre el cambio de extremos: Lo que hacemos es sustituir el valor de $x$ por el de los extremos en la ecuación de cambio ($2 \cosh(u) = x$):
- Con $x = 2$:
$$
2 \cosh(u) = 2 \implies \cosh(u) = 1 \implies \frac{e^{u} + e^{-u}}{2} = 1 \implies u = 0
$$
- Con $x = 3$:
$$
2 \cosh(u) = 3 \implies \cosh(u) = \frac{3}{2} \implies u = arccosh\left( \frac{3}{2} \right)
$$
$$
\begin{align}
\int_{0}^{arccosh\left( \frac{3}{2} \right)} \sqrt{ 4 \cosh ^{2}(u) - 4 } \cdot 2 \sinh(u) \space du &= \int_{0}^{arccosh\left( \frac{3}{2} \right)} \sqrt{ 4 \sinh ^{2}(u) } \cdot 2 \sinh(u) \space du \\
&= \int_{0}^{arccosh\left( \frac{3}{2} \right)} 2 \sinh(u) 2 \sinh(u) \space du \\
&= 4 \int_{0}^{arccosh\left( \frac{3}{2} \right)} \sinh(u) \sinh(u) \space du
\end{align}
$$

Aplicamos partes:
$$
\left[
\begin{align}
&f(x) = \sinh(u) && f'(x) = \cosh(u) \\
&g'(x) = \sinh(u) && g(x) = \cosh(u)
\end{align}
\right]
$$
$$
\begin{align}
\int_{0}^{arccosh\left( \frac{3}{2} \right)} \sinh(u) \sinh(u) \space du &= \sinh(u) \cosh(u) |_{0}^{arccosh\left( \frac{3}{2} \right)} - \int_{0}^{arccosh\left( \frac{3}{2} \right)} \cosh(u) \cosh(u) \space du \\
&= \sinh(u) \cosh(u) |_{0}^{arccosh\left( \frac{3}{2} \right)} - \int_{0}^{arccosh\left( \frac{3}{2} \right)} 1 + \sinh(u) \sinh(u) \space du \\
&= \sinh(u) \cosh(u) |_{0}^{arccosh\left( \frac{3}{2} \right)} - \int_{0}^{arccosh\left( \frac{3}{2} \right)} 1 \space du - \int_{0}^{arccosh\left( \frac{3}{2} \right)} \sinh(u) \sinh(u) \space du \\
&= \sinh(u) \cosh(u) |_{0}^{arccosh\left( \frac{3}{2} \right)} - u |_{0}^{arccosh\left( \frac{3}{2} \right)} - \int_{0}^{arccosh\left( \frac{3}{2} \right)} \sinh(u) \sinh(u) \space du \\
2\int_{0}^{arccosh\left( \frac{3}{2} \right)} \sinh(u) \sinh(u) \space du &= \sinh(u) \cosh(u) |_{0}^{arccosh\left( \frac{3}{2} \right)} - u |_{0}^{arccosh\left( \frac{3}{2} \right)} \\
\int_{0}^{arccosh\left( \frac{3}{2} \right)} \sinh(u) \sinh(u) \space du &= \frac{\sinh(u) \cosh(u) |_{0}^{arccosh\left( \frac{3}{2} \right)} - u |_{0}^{arccosh\left( \frac{3}{2} \right)}}{2} \\
&= \frac{\sinh\left( arccosh\left( \frac{3}{2} \right) \right) \cosh\left( arccosh\left( \frac{3}{2} \right) \right) - \cancel{ \sinh(0) \cosh(0) } - \left( arccosh\left( \frac{3}{2} \right) - 0  \right)}{2} \\
&= \frac{\frac{3}{2}\sinh\left( arccosh\left( \frac{3}{2} \right) \right) - arccosh\left( \frac{3}{2} \right)}{2}
\end{align}
$$

Ahora, determinamos $\int_{0}^{arccosh\left( \frac{3}{2} \right)} \sqrt{ 4 \cosh ^{2}(u) - 4 } \cdot 2 \sinh(u) \space du$:
$$
\begin{align}
\int_{0}^{arccosh\left( \frac{3}{2} \right)} \sqrt{ 4 \cosh ^{2}(u) - 4 } \cdot 2 \sinh(u) \space du &= 4 \int_{0}^{arccosh\left( \frac{3}{2} \right)} \sinh(u) \sinh(u) \space du \\
&= 4 \cdot \frac{\frac{3}{2}\sinh\left( arccosh\left( \frac{3}{2} \right) \right) - arccosh\left( \frac{3}{2} \right)}{2} \\
&= 3\sinh\left( arccosh\left( \frac{3}{2} \right) \right) - 2 arccosh\left( \frac{3}{2} \right)
\end{align}
$$

Ahora, podemos realizar el calculo final:
$$
\begin{align}
3 \int_{2}^{3} \sqrt{ x^{2} - 4 } \space dx &= 3 \int_{0}^{arccosh\left( \frac{3}{2} \right)} \sqrt{ 4 \cosh ^{2}(u) - 4 } \cdot 2 \sinh(u) \space du \\
&= 3 \cdot 3\sinh\left( arccosh\left( \frac{3}{2} \right) \right) - 2 arccosh\left( \frac{3}{2} \right) \\
&= 9\sinh\left( arccosh\left( \frac{3}{2} \right) \right) - 6 arccosh\left( \frac{3}{2} \right)
\end{align}
$$

En conclusión, el área de la región encerrada entre la hipérbola y la recta es $9\sinh\left( arccosh\left( \frac{3}{2} \right) \right) - 6 arccosh\left( \frac{3}{2} \right)$.

Podemos simplificar el resultado:
$$
\begin{align}
9\sinh\left( arccosh\left( \frac{3}{2} \right) \right) - 6 arccosh\left( \frac{3}{2} \right) &= 9 \left( \sqrt{ \cosh ^{2}\left( arccosh\left( \frac{3}{2} \right) \right) - 1 } \right) - 6 arccosh\left( \frac{3}{2} \right) \\
&= 9 \left( \sqrt{ \frac{9}{4} - 1 } \right) - 6 arccosh\left( \frac{3}{2} \right) \\
&= 9 \left( \sqrt{ \frac{5}{4} } \right) - 6 arccosh\left( \frac{3}{2} \right) \\
&= \frac{9\sqrt{ 5 }}{2} - 6 arccosh\left( \frac{3}{2} \right)
\end{align}
$$

### Parte c)
Para comenzar, determinamos la intersección entre $e^{x}$ y $e^{-x}$:
$$
e^{x} = e^{-x} \implies x = -x \implies x = 0
$$
Como vemos, ambas se interceptan en $x = 0$.

Por lo tanto, estamos considerando el intervalo $[0, 1]$ (siendo el extremo superior la recta $x = 1$).

Entonces, tenemos que considerar la siguiente área:
$$
\begin{align}
\int_{0}^{1} e^{x} - e^{-x} \space dx &= \int_{0}^{1} e^{x} \space dx + \int_{0}^{1} -e^{-x} \space dx \\
&= e^{x} |_{0}^{1} + e^{-x} |_{0}^{1} \\
&= e^{1} - e^{0} + \frac{1}{e^{1}} - \frac{1}{e^{0}} \\
&= e - 1 + \frac{1}{e} - \frac{1}{1} \\
&= e + \frac{1}{e} - 2
\end{align}
$$

En conclusión, el área delimitada por las funciones $e^{x}, e^{-x}, x = 1$ es $e + \frac{1}{e} - 2$.

### Parte e)
Determinemos los puntos de intersección entre $x^{2} - 1$ y $\frac{3}{x^{2} + 1}$:
$$
\begin{align}
x^{2} - 1 &= \frac{3}{x^{2} + 1} \\
(x^{2} - 1)(x^{2} + 1) &= \frac{3}{\cancel{ x^{2} + 1 }} \cdot \cancel{ x^{2} + 1 } \\
x^{4} + \cancel{ x^{2} - x^{2} } - 1 &= 3 \\
x^{4} &= 3 + 1 \\
x^{4} &= 4 \\
x^{2} &= \sqrt{ 4 } = 2 \\
x &= \sqrt{ 2 }
\end{align}
$$
Entonces, sabemos que las funciones se interceptan en $x = \pm \sqrt{ 2 }$.

Ahora, sabemos cuales son los extremos de integración. Como en el intervalo $(-\sqrt{ 2 }, \sqrt{ 2 })$ se cumple que $\frac{3}{x^{2} + 1} > x^{2} - 1$, consideraremos la función $\frac{3}{x^{2} + 1} - (x^{2} - 1)$. Como son funciones espejo, incluso podríamos simplemente calcular la integral en el intervalo $(0, \sqrt{ 2 })$ y multiplicarlo por 2:
$$
2 \int_{0}^{\sqrt{ 2 }} \frac{3}{x^{2} + 1} - (x^{2} - 1) \space dx
$$

$$
\int_{0}^{\sqrt{ 2 }} \frac{3}{x^{2} + 1} - (x^{2} - 1) \space dx = \int_{0}^{\sqrt{ 2 }} \frac{3}{x^{2} + 1} \space dx - \int_{0}^{\sqrt{ 2 }} x^{2} - 1 \space dx
$$
$$
\begin{align}
\int_{0}^{\sqrt{ 2 }} \frac{3}{x^{2} + 1} \space dx &= 3 \int_{0}^{\sqrt{ 2 }} \frac{1}{x^{2} + 1} \space dx \\
&= 3 (\arctan(x) |_{0}^{\sqrt{ 2 }}) \\
&= 3 (\arctan(\sqrt{ 2 }) - \cancel{ \arctan(0) }) \\
&= 3 \arctan(\sqrt{ 2 })
\end{align}
$$
$$
\begin{align}
\int_{0}^{\sqrt{ 2 }} x^{2} - 1 \space dx &= \int_{0}^{\sqrt{ 2 }} x^{2} \space dx - \int_{0}^{\sqrt{ 2 }} 1 \space dx \\
&= \frac{x^{3}}{3} |_{0}^{\sqrt{ 2 }} - x |_{0}^{\sqrt{ 2 }} \\
&= \frac{\sqrt{ 2 }^{3}}{3} - \cancel{ \frac{0^{3}}{3} } - (\sqrt{ 2 } - \cancel{ 0 }) \\
&= \frac{2\sqrt{ 2 }}{3} - \sqrt{ 2 } \\
&= \frac{2\sqrt{ 2 } - 3\sqrt{ 2 }}{3} \\
&= -\frac{\sqrt{ 2 }}{3}
\end{align}
$$
$$
\begin{align}
\implies \int_{0}^{\sqrt{ 2 }} \frac{3}{x^{2} + 1} - (x^{2} - 1) \space dx &= \int_{0}^{\sqrt{ 2 }} \frac{3}{x^{2} + 1} \space dx - \int_{0}^{\sqrt{ 2 }} x^{2} - 1 \space dx \\
&= 3 \arctan(\sqrt{ 2 }) - \left( -\frac{\sqrt{ 2 }}{3} \right)\\
&= 3 \arctan(\sqrt{ 2 }) + \frac{\sqrt{ 2 }}{3}
\end{align}
$$
$$
\implies 2 \int_{0}^{\sqrt{ 2 }} \frac{3}{x^{2} + 1} - (x^{2} - 1) \space dx = 2 \left(3 \arctan(\sqrt{ 2 }) + \frac{\sqrt{ 2 }}{3} \right) = 6 \arctan(\sqrt{ 2 }) + \frac{2\sqrt{ 2 }}{3}
$$

En conclusión, el área delimitada por las funciones $x^{2} - 1$ y $\frac{3}{x^{2} + 1}$ es $6 \arctan(\sqrt{ 2 }) + \frac{2\sqrt{ 2 }}{3}$.

---
## Ejercicio 7.3.3

Comenzamos por el área del círculo de radio $r$. Sabiendo que la fórmula de la circunferencia de centro $(0, 0)$ y radio 1 está dada por $x^{2} + y^{2} = 1$, podemos determinar que $y = f(x) = \sqrt{ 1 - x^{2} }$.

Para calcular el área de la circunferencia sabiendo que tiene centro en $(0, 0)$, simplemente basta con calcular un cuarto de la circunferencia y multiplicar el valor obtenido por 4:
$$
A\circ = 4\int_{0}^{1} \sqrt{ 1 - x^{2} } \space dx
$$
Aplicamos sustitución utilizando un enfoque diferente:
$$
\begin{align}
\int_{0}^{1} \sqrt{ 1 - x^{2} } \space dx &\underbrace{ = }_{ \begin{aligned}
&\sin(u) = x \\
&\cos(u) \space du = dx
\end{aligned} } \int_{0}^{\frac{\pi}{2}} \sqrt{ 1 - \sin^{2}(u) } \cos(u) \space du \\
&= \int_{0}^{\frac{\pi}{2}} \cos(u)\cos(u) \space du
\end{align}
$$
Ahora, aplicamos partes:
$$
\left[
\begin{align}
&f(x) = \cos(u) &&f'(x) = -\sin(u) \\
&g'(x) = \cos(u) &&g(x) = \sin(u)
\end{align}
\right]
$$
$$
\begin{align}
\int_{0}^{\frac{\pi}{2}} \cos(u)\cos(u) \space du &= \sin(u)\cos(u) - \int_{0}^{\frac{\pi}{2}} -\sin(u)\sin(u) \space du \\
&= \sin(u)\cos(u) |_{0}^{\frac{\pi}{2}} + \int_{0}^{\frac{\pi}{2}} \sin(u)\sin(u) \space du \\
&= \sin(u)\cos(u) |_{0}^{\frac{\pi}{2}} + \int_{0}^{\frac{\pi}{2}} 1 - \cos(u)\cos(u) \space du \\
&= \sin(u)\cos(u) |_{0}^{\frac{\pi}{2}} + \int_{0}^{\frac{\pi}{2}} 1 \space du - \int_{0}^{\frac{\pi}{2}} \cos(u)\cos(u) \space du \\
&= \sin(u)\cos(u) |_{0}^{\frac{\pi}{2}} + u |_{0}^{\frac{\pi}{2}} - \int_{0}^{\frac{\pi}{2}} \cos(u)\cos(u) \space du \\
2\int_{0}^{\frac{\pi}{2}} \cos(u)\cos(u) \space du &= \sin(u)\cos(u) |_{0}^{\frac{\pi}{2}} + u |_{0}^{\frac{\pi}{2}} \\
\int_{0}^{\frac{\pi}{2}} \cos(u)\cos(u) \space du &= \frac{\sin(u)\cos(u) |_{0}^{\frac{\pi}{2}} + u |_{0}^{\frac{\pi}{2}}}{2} \\
&= \frac{\cancel{ \sin\left( \frac{\pi}{2} \right)\cos\left( \frac{\pi}{2} \right) } - \cancel{ \sin(0)\cos(0) } + \frac{\pi}{2} - 0}{2} \\
&= \frac{\frac{\pi}{2}}{2} \\
&= \frac{\pi}{4}
\end{align}
$$
De esta manera:
$$
\int_{0}^{1} \sqrt{ 1 - x^{2} } \space dx = \frac{\pi}{4}
$$

En conclusión:
$$
A\circ = 4\int_{0}^{1} \sqrt{ 1 - x^{2} } \space dx = 4 \cdot \frac{\pi}{4} = \pi
$$

Además, podemos confirmar dicho resultado tomando como referencia la fórmula de área del círculo, considerando que el radio es 1:
$$
A\circ = \pi \cdot r^{2} = \pi \cdot 1^{2} = \pi
$$

Aquí debajo se encuentra un desarrollo incompleto, el cual puede servir como ejemplo sobre un enforque incorrecto de resolución sin finalizar y con múltiples errores.
$$
\left[
\begin{align}
&f(x) = \sqrt{ 1 - x^{2} } &&f'(x) = -\frac{x}{\sqrt{ 1 - x^{2} }} \\
&g'(x) = 1 &&g(x) = x
\end{align}
\right]
$$
$$
\begin{align}
\int_{0}^{1} \sqrt{ 1 - x^{2} } \space dx &= x\sqrt{ 1 - x^{2} } |_{0}^{1} - \int_{0}^{1} - \frac{x^{2}}{\sqrt{ 1 - x^{2} }} \space dx \\
&= x\sqrt{ 1 - x^{2} } |_{0}^{1} + \int_{0}^{1} \frac{x^{2}}{\sqrt{ 1 - x^{2} }} \space dx
\end{align}
$$

Para resolver la nueva integral, aplicamos sustitución:
$$
\begin{align}
\int_{0}^{1} \frac{x^{2}}{\sqrt{ 1 - x^{2} }} \space dx &\underbrace{ = }_{ \begin{aligned}
&\sin(u) = x \\
&\cos(u) \space du = dx
\end{aligned} } \int_{0}^{\frac{\pi}{2}} \frac{\sin ^{2}(u)}{\sqrt{ 1 - \sin ^{2}(u) }} \cos(u) \space du \\
&= \int_{0}^{\frac{\pi}{2}} \frac{\sin ^{2}(u)}{\cancel{ \sqrt{ 1 - \sin ^{2}(u) } }} \cdot \cancel{ \sqrt{ 1 - \sin ^{2}(u) } } \space du \\
&= \int_{0}^{\frac{\pi}{2}} \sin ^{2}(u) \space du
\end{align}
$$
ACLARACIÓN: Al realizar un cambio de variable, también es fundamental verificar si los extremos de la integral se ajustan a la misma. Aquí, teníamos como extremos 0 y 1, ya que $x = 0$ para $x = 0$ y lo mismo para uno, pero cuando estudiamos $\sin(u)$, podemos ver que $\sin(u) = 0$ para $u = 0$ (limite inferior coincidente) y $\sin(u) = 1$ para $u = \frac{\pi}{2}$. Por lo tanto, es necesario sustituir el límite superior por $\frac{\pi}{2}$.

Volvemos a aplicar partes:
$$
\left[
\begin{align}
&f(x) = \sin(u) &&f'(x) = \cos(u) \\
&g'(x) = \sin(u) &&g(x) = -\cos(u)
\end{align}
\right]
$$
$$
\begin{align}
\int_{0}^{1} \sin ^{2}(u) \space du &= -\sin(u)\cos(u) |_{0}^{1} - \int_{0}^{1} -\cos ^{2}(u) \space du \\
&= -\sin(u)\cos(u) |_{0}^{1} + \int_{0}^{1} \cos ^{2}(u) \space du \\
&= -\sin(u)\cos(u) |_{0}^{1} + \int_{0}^{1} 1 - \sin ^{2}(u) \space du \\
&= -\sin(u)\cos(u) |_{0}^{1} + \int_{0}^{1} 1 \space du - \int_{0}^{1} \sin ^{2}(u) \space du \\
&= -\sin(u)\cos(u) |_{0}^{1} + u |_{0}^{1} - \int_{0}^{1} \sin ^{2}(u) \space du \\
2\int_{0}^{1} \sin ^{2}(u) \space du &= -\sin(u)\cos(u) |_{0}^{1} + u |_{0}^{1} \\
\int_{0}^{1} \sin ^{2}(u) \space du &= \frac{-\sin(u)\cos(u) |_{0}^{1} + u |_{0}^{1}}{2}
\end{align}
$$
Deshacemos el cambio de variable:
$$
\sin(u) = x \implies u = \arcsin(x)
$$
$$
\begin{align}
\int_{0}^{1} x^{2} \space du &= \frac{-x |_{0}^{1} + \arcsin(x) |_{0}^{1}}{2} \\
&= \frac{-1 + 0 + \arcsin(1) - \cancel{ \arcsin(0) }}{2} \\
&= \frac{\arcsin(1) - 1}{2}
\end{align}
$$

Quizás podríamos haber deshecho el cambio de variable previo a volver a aplicar partes (directamente sobre la integral $\int_{0}^{1} \sin ^{2}(u) \space du$).

CORRECCIÓN:
No es necesario realizar todo este desarrollo. Es mucho más simple aplicar directamente sustitución desde el principio:

El caso de la elipse es similar, aunque tenemos que considerar que la función cambia. Sabiendo que tiene ejes de medida $2a$ y $2b$, y asumiendo que es de centro $(0, 0)$, la función se expresa como $\frac{x^{2}}{a^{2}} + \frac{y^{2}}{b^{2}} = 1$, pudiendo despejar $y$ como
$$
\begin{align}
y = f(x) = \sqrt{ b^{2} \left( 1 - \frac{x^{2}}{a^{2}} \right) } = b\sqrt{ 1 - \frac{x^{2}}{a^{2}} }
\end{align}
$$
Entonces:
$$
f(x) = b\sqrt{ 1 - \frac{x^{2}}{a^{2}} }
$$

Nuevamente, al tener centro en el origen $(0, 0)$, podemos simplemente calcular la integral en el intervalo $[0, a]$ y multiplicarla por 4:
$$
A_{\text{elipse}} = 4 \int_{0}^{a} b\sqrt{ 1 - \frac{x^{2}}{a^{2}} } \space dx
$$
$$
\begin{align}
\int_{0}^{a} b\sqrt{ 1 - \frac{x^{2}}{a^{2}} } \space dx &= 2b \int_{0}^{a} \sqrt{ 1 - \frac{x^{2}}{4a^{2}} } \space dx \\
&= b \int_{0}^{a} \sqrt{ 1 - \frac{x^{2}}{(a)^{2}} } \space dx \\
&= b \int_{0}^{a} \sqrt{ 1 - \left( \frac{x}{a} \right)^{2} } \space dx \\
&\underbrace{ = }_{ \begin{aligned}
&\sin(u) = \frac{x}{a} \\
&a \cos(u) \space du = dx
\end{aligned} } b \int_{0}^{\frac{\pi}{2}} \sqrt{ 1 - \sin ^{2}(u) } a \cos(u) \space du \\
&= b \int_{0}^{\frac{\pi}{2}} a \cos(u) \cos(u) \space du \\
&= ab \int_{0}^{\frac{\pi}{2}} \cos(u) \cos(u) \space du
\end{align}
$$

Aclaración sobre el razonamiento de la sustitución:
$$
\sin(u) = \frac{x}{a} \implies x = a \sin(u) \implies \begin{align}
&x = 0 \implies \sin(u) = 0 \implies u = 0 \\
&x = a \implies \sin(u) = 1 \implies u = \frac{\pi}{2}
\end{align}
$$
Básicamente, proponemos $\frac{x}{a} = \sin(u)$, por lo que $x = a \sin(u)$. De esta forma, sabiendo que $a \neq 0$, cuando $x = 0 \implies \sin(u) = 0 \implies u = 0$, y cuando $x = a \implies \sin(u) = 1 \implies u = \frac{\pi}{2}$.

Además, para determinar el equivalente a $dx$, básicamente derivamos $x = a \sin(u)$ para hallar el diferencial, de forma que $(a \sin(u))' = \cancel{ (a)'\sin(u) } + a(\sin(u))' = a \cos(u)$, mas el diferencial.

Para concluir, estudiamos la integral $\int_{0}^{\frac{\pi}{2}} \cos(u) \cos(u) \space du$, la cual ya fue calculada en la parte anterior mediante partes:
$$
\int_{0}^{\frac{\pi}{2}} \cos(u) \cos(u) \space du = \frac{\pi}{4}
$$
Por lo tanto:
$$
\int_{0}^{a} b\sqrt{ 1 - \frac{x^{2}}{a^{2}} } \space dx = ab \cdot \frac{\pi}{4}
$$

En conclusión:
$$
A_{\text{elipse}} = 4 \int_{0}^{a} b\sqrt{ 1 - \frac{x^{2}}{a^{2}} } \space dx = \cancel{ 4 }ab \cdot \frac{\pi}{\cancel{ 4 }} = \pi ab
$$

---
## Ejercicio 7.3.4
Determinaremos cada una de las áreas por separado. Comenzaremos calculando el área de un cuarto de circunferencia (considerando una circunferencia con centro en el origen $(0, 0)$ y radio $r$):
$$
\begin{align}
x^{2} + y^{2} = r^{2} \\
y^{2} = r^{2} - x^{2} \\
y = \sqrt{ r^{2} - x^{2} }
\end{align}
$$
De esta forma, la función de una circunferencia es $f(x) = \sqrt{ r^{2} - x^{2} }$.

Antes de comenzar a calcular áreas, será de utilidad encontrar una primitiva de la función anterior:
$$
\begin{align}
&x = r \sin(u) \\
&dx = r \cos(u) \space du
\end{align}
$$
$$
\begin{align}
\int \sqrt{ r^{2} - x^{2} } \space dx &= \int \sqrt{ r^{2} - (r \sin(u))^{2} } \cdot r \cos(u) \space du \\
&= \int \sqrt{ r^{2} - r^{2} \sin ^{2}(u) } \cdot r \cos(u) \space du \\
&= \int \sqrt{ r^{2}(1 - \sin ^{2}(u)) } \cdot r \cos(u) \space du \\
&= \int r\sqrt{ 1 - \sin ^{2}(u) } \cdot r \cos(u) \space du \\
&= \int r \cos(u) \cdot r \cos(u) \space du \\
&= \int r^{2} \cos ^{2}(u) \space du \\
&= r^{2} \int \cos ^{2}(u) \space du
\end{align}
$$
Ahora, aplicamos partes para resolver la nueva integral:
$$
\left[
\begin{align}
&f(x) = \cos(u) &&f'(x) = -\sin(u) \\
&g'(x) = \cos(u) &&g(x) = \sin(u)
\end{align}
\right]
$$
$$
\begin{align}
\int \cos ^{2}(u) \space du &= \sin(u) \cos(u) - \int - \sin ^{2}(u) \space du \\
&= \sin(u) \cos(u) + \int \sin ^{2}(u) \space du \\
&= \sin(u) \cos(u) + \int 1 - \cos ^{2}(u) \space du \\
&= \sin(u) \cos(u) + \int 1 \space du - \int \cos ^{2}(u) \space du \\
2 \int \cos ^{2}(u) \space du &= \sin(u) \cos(u) + \int 1 \space du \\
\int \cos ^{2}(u) \space du &= \frac{\sin(u) \cos(u) + \int 1 \space du}{2} \\
&= \frac{\sin(u) \cos(u) + u}{2}
\end{align}
$$

Ahora, podemos deshacer el cambio de variable:
$$
\begin{align}
&x = r \sin(u) \implies \sin(u) = \frac{x}{r} \text{ y } u = \arcsin\left( \frac{x}{r} \right) \\
&\cos(u) = \sqrt{ 1 - \sin ^{2}(u) } = \sqrt{ 1 - \left( \frac{x}{r} \right)^{2} } = \sqrt{ \frac{r^{2}}{r^{2}} - \frac{x^{2}}{r^{2}} } = \sqrt{ \frac{r^{2} - x^{2}}{r^{2}} } = \frac{\sqrt{ r^{2} - x^{2} }}{r}
\end{align}
$$

Entonces, determinamos que:
$$
\begin{align}
\int \sqrt{ r^{2} - x^{2} } \space dx &= r^{2} \left( \frac{\sin(u) \cos(u) + u}{2} \right) \\
&= r^{2} \left( \frac{\frac{x}{r} \cdot \frac{\sqrt{ r^{2} - x^{2} }}{r} + \arcsin\left( \frac{x}{r} \right)}{2} \right) \\
&= r^{2} \left( \frac{\frac{x\sqrt{ r^{2} - x^{2} }}{r^{2}} + \arcsin\left( \frac{x}{r} \right)}{2} \right) \\
&= \frac{x\sqrt{ r^{2} - x^{2} } + r^{2}\arcsin\left( \frac{x}{r} \right)}{2}
\end{align}
$$
$$
\implies \int \sqrt{ r^{2} - x^{2} } \space dx = \frac{x\sqrt{ r^{2} - x^{2} } + r^{2}\arcsin\left( \frac{x}{r} \right)}{2} + C
$$

Ahora, procedemos a calcular el área de un cuarto de circunferencia, para lo que consideraremos el intervalo $(0, r)$:
$$
\begin{align}
\int_{0}^{r} \sqrt{ r^{2} - x^{2} } \space dx &= \frac{x\sqrt{ r^{2} - x^{2} } + r^{2}\arcsin\left( \frac{x}{r} \right)}{2} |_{0}^{r} \\
&= \frac{\cancel{ r\sqrt{ r^{2} - r^{2} } } + r^{2}\arcsin\left( \frac{r}{r} \right)}{2} - \frac{\cancel{ 0 \cdot \sqrt{ r^{2} - x^{2} } } + \cancel{ r^{2}\arcsin\left( \frac{0}{r} \right) }}{2} \\
&= \frac{r^{2}\arcsin\left( 1 \right)}{2} \\
&= \frac{r^{2} \cdot \frac{\pi}{2}}{2} \\
&= \frac{\pi r^{2}}{4}
\end{align}
$$

1. Calculemos las áreas pequeñas encerradas en los lados del cuadrado. Para esto, tenemos que investigar el punto de intersección entre las funciones involucradas, que son  y $r - \sqrt{ r^{2} - x^{2} }$
$$
\begin{align}
\sqrt{ r^{2} - x^{2} } &= r - \sqrt{ r^{2} - x^{2} } \\
2\sqrt{ r^{2} - x^{2} } &= r \\
\sqrt{ r^{2} - x^{2} } &= \frac{r}{2} \\
r^{2} - x^{2} &= \frac{r^{2}}{4} \\
-x^{2} &= \frac{r^{2}}{4} - r^{2} \\
-x^{2} &= -\frac{3r^{2}}{4} \\
x^{2} &= \frac{3r^{2}}{4} \\
x &= \sqrt{ \frac{3r^{2}}{4} } \\
x &= \frac{\sqrt{ 3 }r}{2}
\end{align}
$$

Como vemos, las funciones se interceptan en el punto $x = \frac{\sqrt{ 3 }r}{2}$.
Entonces, calculamos el área siguiente:
$$
\begin{align}
\int_{0}^{\frac{\sqrt{ 3 }r}{2}} r - \sqrt{ r^{2} - x^{2} } \space dx -  \int_{0}^{\frac{\sqrt{ 3 }r}{2}} \sqrt{ r^{2} - x^{2} } \space dx &= \int_{0}^{\frac{\sqrt{ 3 }r}{2}} r \space dx - \int_{0}^{\frac{\sqrt{ 3 }r}{2}} \sqrt{ r^{2} - x^{2} } \space dx - \int_{0}^{\frac{\sqrt{ 3 }r}{2}} \sqrt{ r^{2} - x^{2} } \space dx \\
&= \int_{0}^{\frac{\sqrt{ 3 }r}{2}} r \space dx - 2 \int_{0}^{\frac{\sqrt{ 3 }r}{2}} \sqrt{ r^{2} - x^{2} } \space dx \\
&= r \int_{0}^{\frac{\sqrt{ 3 }r}{2}} 1 \space dx - 2 \int_{0}^{\frac{\sqrt{ 3 }r}{2}} \sqrt{ r^{2} - x^{2} } \space dx
\end{align}
$$
$$
\begin{align}
r \int_{0}^{\frac{\sqrt{ 3 }r}{2}} 1 \space dx &= r \cdot x |_{0}^{\frac{\sqrt{ 3 }r}{2}} \\
&= r \cdot \frac{\sqrt{ 3 }r}{2} - 0 \\
&= r \cdot \frac{\sqrt{ 3 }r}{2} \\
&= \frac{\sqrt{ 3 }r^{2}}{2}
\end{align}
$$
$$
\begin{align}
2\int_{0}^{\frac{\sqrt{ 3 }r}{2}} \sqrt{ r^{2} - x^{2} } \space dx &= \frac{x\sqrt{ r^{2} - x^{2} } + r^{2}\arcsin\left( \frac{x}{r} \right)}{2} |_{0}^{\frac{\sqrt{ 3 }r}{2}} \\
&= 2 \cdot \left( \frac{\frac{\sqrt{ 3 }r}{2} \cdot \sqrt{ r^{2} - \left( \frac{\sqrt{ 3 }r}{2} \right)^{2} } + r^{2}\arcsin\left( \frac{\left( \frac{\sqrt{ 3 }r}{2} \right)}{r} \right)}{2} - \frac{\cancel{ 0\sqrt{ r^{2} - 0^{2} } } + \cancel{ r^{2}\arcsin\left( \frac{0}{r} \right) }}{2} \right) \\
&= \cancel{ 2 } \cdot \left( \frac{\frac{\sqrt{ 3 }r}{2} \cdot \sqrt{ r^{2} - \frac{3r^{2}}{4} } + r^{2}\arcsin\left( \frac{ \sqrt{ 3 }}{2} \right)}{\cancel{ 2 }} \right) \\
&= \frac{\sqrt{ 3 }r^{2}}{2} \sqrt{ \frac{1}{4} } + \frac{r^{2} \pi}{3} \\
&= \frac{\sqrt{ 3 }r^{2}}{2} \cdot \frac{1}{2} + \frac{r^{2} \pi}{3} \\
&= \frac{\sqrt{ 3 }r^{2}}{4} + \frac{r^{2} \pi}{3} \\
&= \frac{3\sqrt{ 3 }r^{2} + 4r^{2} \pi}{12}
\end{align}
$$

$$
\begin{align}
\int_{0}^{\frac{\sqrt{ 3 }r}{2}} r - \sqrt{ r^{2} - x^{2} } \space dx -  \int_{0}^{\frac{\sqrt{ 3 }r}{2}} \sqrt{ r^{2} - x^{2} } \space dx &= r \int_{0}^{\frac{\sqrt{ 3 }r}{2}} 1 \space dx - 2 \int_{0}^{\frac{\sqrt{ 3 }r}{2}} \sqrt{ r^{2} - x^{2} } \space dx \\
&= \frac{\sqrt{ 3 }r^{2}}{2} - \frac{3\sqrt{ 3 }r^{2} + 4r^{2} \pi}{12} \\
&= \frac{6\sqrt{ 3 }r^{2} - 3\sqrt{ 3 }r^{2} + 4r^{2} \pi}{12} \\
&= \frac{3\sqrt{ 3 }r^{2} + 4r^{2} \pi}{12}
\end{align}
$$

ACLARACIÓN: en realidad, el área que necesito es la siguiente:
$$
\begin{align}
\int_{\frac{\sqrt{ 3 }r}{2}}^{r} \sqrt{ r^{2} - x^{2} } \space dx - \int_{\frac{\sqrt{ 3 }r}{2}}^{r} r - \sqrt{ r^{2} - x^{2} } \space dx &= \int_{\frac{\sqrt{ 3 }r}{2}}^{r} \sqrt{ r^{2} - x^{2} } \space dx - \left( \int_{\frac{\sqrt{ 3 }r}{2}}^{r} r \space dx - \int_{\frac{\sqrt{ 3 }r}{2}}^{r} \sqrt{ r^{2} - x^{2} } \space dx \right) \\
&= \int_{\frac{\sqrt{ 3 }r}{2}}^{r} \sqrt{ r^{2} - x^{2} } \space dx -  \int_{\frac{\sqrt{ 3 }r}{2}}^{r} r \space dx + \int_{\frac{\sqrt{ 3 }r}{2}}^{r} \sqrt{ r^{2} - x^{2} } \space dx \\
&= 2 \int_{\frac{\sqrt{ 3 }r}{2}}^{r} \sqrt{ r^{2} - x^{2} } \space dx -  r\int_{\frac{\sqrt{ 3 }r}{2}}^{r} \space dx
\end{align}
$$

Luego, calculamos la siguiente integral (el área del medio):
$$
\begin{align}
2 \left( \int_{\frac{r}{2}}^{r} r - \sqrt{ r^{2} - x^{2} } \space dx - \int_{\frac{r}{2}}^{r} \sqrt{ r^{2} - x^{2} } \space dx \right) &= 2 \left( \int_{\frac{r}{2}}^{r} r \space dx - \int_{\frac{r}{2}}^{r} \sqrt{ r^{2} - x^{2} } \space dx - \int_{\frac{r}{2}}^{r} \sqrt{ r^{2} - x^{2} } \space dx \right) \\
&= 2 \left( \int_{\frac{r}{2}}^{r} r \space dx - 2 \int_{\frac{r}{2}}^{r} \sqrt{ r^{2} - x^{2} } \space dx \right) \\
&= 2 \int_{\frac{r}{2}}^{r} r \space dx - 4 \int_{\frac{r}{2}}^{r} \sqrt{ r^{2} - x^{2} } \space dx
\end{align}
$$


Luego tengo que quitar todas las regiones calculadas al cuadrado (4 de las pequeñas anteriores y 1 de la del medio):
$$
r^{2} - 4 \left( 2 \int_{\frac{\sqrt{ 3 }r}{2}}^{r} \sqrt{ r^{2} - x^{2} } \space dx -  r\int_{\frac{\sqrt{ 3 }r}{2}}^{r} \space dx \right) - 2 \int_{\frac{r}{2}}^{r} r \space dx - 4 \int_{\frac{r}{2}}^{r} \sqrt{ r^{2} - x^{2} } \space dx
$$

Finalmente, dividimos el resultado de lo anterior por 4, para obtener el área de la región faltante (la que se encuentra en todas las esquinas).

---
# 5 - Aplicaciones
## Ejercicio 7.5.4
Tenemos que determinar:
$$
M_{x} = \frac{\int_{a}^{b} f(x)x \space dx}{\int_{a}^{b} f(x) \space dx}
$$
y
$$
M_{y} = \frac{\int_{a}^{b} f(x)^{2} \space dx}{2\int_{a}^{b} f(x) \space dx}
$$

### Parte a)
$$
M_{x} = \frac{\int_{a}^{b} f(x)x \space dx}{\int_{a}^{b} f(x) \space dx} = \frac{\int_{a}^{b} x\sin(x) \space dx}{\int_{a}^{b} \sin(x) \space dx}
$$
$$
\left[
\begin{align}
&f(x) = x && f'(x) = 1 \\
&g'(x) = \sin(x) &&g(x) = -\cos(x)
\end{align}
\right]
$$
$$
\begin{align}
\int_{a}^{b} x\sin(x) \space dx &= -x \cos(x) |_{a}^{b} - \int_{a}^{b} - \cos(x) \space dx \\
&= -x \cos(x) |_{a}^{b} + \int_{a}^{b} \cos(x) \space dx \\
&= -x \cos(x) |_{a}^{b} + \sin(x) |_{a}^{b} \\
&= -b \cos(b) + a \cos(a) + \sin(b) - \sin(a) \\
&= a \cos(a) - b \cos(b) + \sin(b) - \sin(a)
\end{align}
$$
$$
\begin{align}
\int_{a}^{b} \sin(x) \space dx &= -\cos(x) |_{a}^{b} \\
&= -\cos(b) + \cos(a) \\
&= \cos(a) - \cos(b)
\end{align}
$$
$$
\frac{\int_{a}^{b} x\sin(x) \space dx}{\int_{a}^{b} \sin(x) \space dx} = \frac{a \cos(a) - b \cos(b) + \sin(b) - \sin(a)}{\cos(a) - \cos(b)}
$$

Entonces:
$$
M_{x} = \frac{a \cos(a) - b \cos(b) + \sin(b) - \sin(a)}{\cos(a) - \cos(b)}
$$

$$
M_{y} = \frac{\int_{a}^{b} f(x)^{2} \space dx}{2 \int_{a}^{b} f(x) \space dx} = \frac{\int_{a}^{b} \sin ^{2}(x) \space dx}{2 \int_{a}^{b} \sin(x) \space dx}
$$
$$
\left[
\begin{align}
&f(x) = \sin(x) && f'(x) = \cos(x) \\
&g'(x) = \sin(x) &&g(x) = -\cos(x)
\end{align}
\right]
$$
$$
\begin{align}
\int_{a}^{b} \sin(x) \sin(x) \space dx &= -\cos(x) \sin(x) |_{a}^{b} - \int_{a}^{b} - \cos(x) \cos(x) \space dx \\
&= -\cos(x) \sin(x) |_{a}^{b} + \int_{a}^{b} \cos ^{2}(x) \space dx \\
&= -\cos(x) \sin(x) |_{a}^{b} + \int_{a}^{b} 1 - \sin ^{2}(x) \space dx \\
&= -\cos(x) \sin(x) |_{a}^{b} + \int_{a}^{b} 1 \space dx - \int_{a}^{b} \sin ^{2}(x) \space dx \\
&= -\cos(x) \sin(x) |_{a}^{b} + x |_{a}^{b} - \int_{a}^{b} \sin ^{2}(x) \space dx \\
2 \int_{a}^{b} \sin(x) \sin(x) \space dx &= -\cos(x) \sin(x) |_{a}^{b} + x |_{a}^{b} \\
\int_{a}^{b} \sin(x) \sin(x) \space dx &= \frac{-\cos(x) \sin(x) |_{a}^{b} + x |_{a}^{b}}{2} \\
&= \frac{-\cos(b) \sin(b) + \cos(a) \sin(a) + b - a}{2} \\
&= \frac{\cos(a) \sin(a) - \cos(b) \sin(b) + b - a}{2}
\end{align}
$$
$$
\frac{\int_{a}^{b} \sin ^{2}(x) \space dx}{2 \int_{a}^{b} \sin(x) \space dx} = \frac{\frac{\cos(a) \sin(a) - \cos(b) \sin(b) + b - a}{2}}{2(\cos(a) - \cos(b))} = \frac{\cos(a) \sin(a) - \cos(b) \sin(b) + b - a}{4\cos(a) - 4\cos(b)}
$$

Entonces:
$$
M_{y} = \frac{\cos(a) \sin(a) - \cos(b) \sin(b) + b - a}{4\cos(a) - 4\cos(b)}
$$

### Parte b)
$$
M_{x} = \frac{\int_{a}^{b} f(x)x \space dx}{\int_{a}^{b} f(x) \space dx} = \frac{\int_{a}^{b} (x^{2} - 1)x \space dx}{\int_{a}^{b} x^{2} - 1 \space dx}
$$
$$
\begin{align}
\int_{a}^{b} (x^{2} - 1)x \space dx &= \int_{a}^{b} x^{3} - x \space dx \\
&= \int_{a}^{b} x^{3} \space dx - \int_{a}^{b} x \space dx \\
&= \frac{x^{4}}{4} |_{a}^{b} - \frac{x^{2}}{2} |_{a}^{b} \\
&= \frac{b^{4}}{4} - \frac{a^{4}}{4} - \left( \frac{b^{2}}{2} - \frac{a^{2}}{2} \right) \\
&= \frac{b^{4}}{4} - \frac{a^{4}}{4} - \frac{b^{2}}{2} + \frac{a^{2}}{2} \\
&= \frac{b^{4} - a^{4} - 2b^{2} + 2a^{2}}{4}
\end{align}
$$
$$
\begin{align}
\int_{a}^{b} x^{2} - 1 \space dx &= \int_{a}^{b} x^{2} \space dx - \int_{a}^{b} 1 \space dx \\
&= \frac{x^{3}}{3} |_{a}^{b} - x |_{a}^{b} \\
&= \frac{x^{3}}{3} |_{a}^{b} - x |_{a}^{b} \\
&= \frac{b^{3}}{3} - \frac{a^{3}}{3} - \left( b - a \right) \\
&= \frac{b^{3}}{3} - \frac{a^{3}}{3} - b + a \\
&= \frac{b^{3} - a^{3} - 3b + 3a}{3}
\end{align}
$$
$$
\frac{\int_{a}^{b} (x^{2} - 1)x \space dx}{\int_{a}^{b} x^{2} - 1 \space dx} = \frac{\frac{b^{4} - a^{4} - 2b^{2} + 2a^{2}}{4}}{\frac{b^{3} - a^{3} - 3b + 3a}{3}} = \frac{3(b^{4} - a^{4} - 2b^{2} + 2a^{2})}{4(b^{3} - a^{3} - 3b + 3a)} = \frac{3b^{4} - 3a^{4} - 6b^{2} + 6a^{2}}{4b^{3} - 4a^{3} - 12b + 12a}
$$

Entonces:
$$
M_{x} = \frac{3b^{4} - 3a^{4} - 6b^{2} + 6a^{2}}{4b^{3} - 4a^{3} - 12b + 12a}
$$

$$
M_{y} = \frac{\int_{a}^{b} f(x)^{2} \space dx}{2 \int_{a}^{b} f(x) \space dx} = \frac{\int_{a}^{b} (x^{2} - 1)^{2} \space dx}{2 \int_{a}^{b} x^{2} - 1 \space dx}
$$
$$
\begin{align}
\int_{a}^{b} (x^{2} - 1)^{2} \space dx &= \int_{a}^{b} x^{4} - 2x^{2} + 1 \space dx \\
&= \int_{a}^{b} x^{4} \space dx - 2\int_{a}^{b} x^{2} \space dx + \int_{a}^{b} 1 \space dx \\
&= \frac{x^{5}}{5} |_{a}^{b} - 2\left( \frac{x^{3}}{3} |_{a}^{b} \right) + x |_{a}^{b} \\
&= \frac{b^{5}}{5} - \frac{a^{5}}{5} - \left( \frac{2b^{3}}{3} - \frac{2a^{3}}{3} \right) + b - a \\
&= \frac{b^{5}}{5} - \frac{a^{5}}{5} - \frac{2b^{3}}{3} + \frac{2a^{3}}{3} + b - a \\
&= \frac{b^{5} - a^{5} - \frac{10}{3}b^{3} + \frac{10}{3}a^{3} + 5b - 5a}{5}
\end{align}
$$
$$
\frac{\int_{a}^{b} (x^{2} - 1)^{2} \space dx}{2 \int_{a}^{b} x^{2} - 1 \space dx} = \frac{\frac{b^{5} - a^{5} - \frac{10}{3}b^{3} + \frac{10}{3}a^{3} + 5b - 5a}{5}}{2\left( \frac{b^{3} - a^{3} - 3b + 3a}{3} \right)} = \frac{b^{5} - a^{5} - \frac{10}{3}b^{3} + \frac{10}{3}a^{3} + 5b - 5a}{\frac{10b^{3} - 10a^{3} - 30b + 30a}{3}} = \frac{b^{5} - a^{5} - \frac{10}{3}b^{3} + \frac{10}{3}a^{3} + 5b - 5a}{\frac{10}{3}b^{3} - \frac{10}{3}a^{3} - 10b + 10a}
$$

Entonces:
$$
M_{y} = \frac{b^{5} - a^{5} - \frac{10}{3}b^{3} + \frac{10}{3}a^{3} + 5b - 5a}{\frac{10}{3}b^{3} - \frac{10}{3}a^{3} - 10b + 10a}
$$





