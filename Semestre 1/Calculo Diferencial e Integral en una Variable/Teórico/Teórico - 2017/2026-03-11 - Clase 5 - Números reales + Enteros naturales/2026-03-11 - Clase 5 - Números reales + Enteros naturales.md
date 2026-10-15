# Repaso de los axiomas vistos en la clase anterior.
En la clase pasada vimos los primeros 14 de los 15 axiomas de los números reales. Repasando:
1. $(I.1-4) \rightarrow$ $+$ es:
	1. asociativa
	2. conmutativa
	3. tiene neutro $0 \in \mathbb{R}$
	4. cada $x \in \mathbb{R}$ tiene opuesto $-x$ (único) $\rightarrow$ $x-y:=x+(-y)$
2. $(II.1-5) \rightarrow$ $\times$ es:
	1. asociativo
	2. conmutativo
	3. distributivo respecto a $+$
	4. tiene neutro $1 \neq 0$
	5. cada elemento $x \neq 0$ tiene inverso $x^{-1}$ (único) $\rightarrow$ $\frac{x}{y}=x \times y^{-1}$
A partir de estas reglas tenemos todas las reglas algebraicas usuales, y se dice que cuando un conjunto tiene una adición y un producto que cumple todos los axiomas anteriores, es un conjunto donde se puede sumar, restar, multiplicar y dividir sin problemas (todas las propiedades deseadas), y lo llamamos <u>cuerpo</u>.
Un <u>cuerpo</u> es cualquier conjunto que tiene una adición, un producto que cumplen todos los axiomas anteriores.

El cuerpo más pequeño del universo es aquel que contiene 2 elementos, 0 y 1, tal que:
- $0+0=0$
- $0+1=1$
- $1+0=1$
- $1+1=0$
La adición anterior, junto con el producto normal entre 0 y 1, da como resultado el cuerpo más pequeño posible. Sin embargo, no cumple las reglas de orden.
Otros cuerpos pueden ser $\mathbb{Q}, \mathbb{R} \text{ y } \mathbb{C}$.

También había una relación de orden total:
3. $(III.1-5)$:
	1. $x\leq y \text{ o } y\leq x \qquad (\forall x,y)$
	2. $x\leq y \land y\leq z \implies x\leq z \qquad (\forall x,y,z)$
	3. $x\leq y \land y\leq x \implies x=y \qquad (\forall x,y)$
	4. $x\leq y \implies x+z\leq y+z \qquad (\forall x,y,z)$
	5. $x\geq0 \land y\geq0 \implies xy\geq 0 \qquad (\forall x,y)$
Orden estricto: $x<y \Longleftrightarrow x\leq y \land x\neq y$
de tal modo que: $x\leq y \Longleftrightarrow x<y \lor x=y$

Reglas:
* $x\leq y \Longleftrightarrow x+z\leq y+z\Longleftrightarrow x-z\leq y-z$
	$\Longleftrightarrow -x \geq -y$
	Se puede representar gráficamente como una traslación, de tal forma que si yo tengo dos valores x e y, x+z y y+z serán exactamente la suma de los vectores $\vec{x}$ y $\vec{z}$ por un lado, e $\vec{y}$ y $\vec{z}$ por el otro, la diferencia entre $\vec{x} + \vec{z}$ y $\vec{y} + \vec{z}$ es la misma que entre los vectores $\vec{x}$ y $\vec{y}$
	![[Representación de traslación.png]]
	Lo mismo aplica para $<$ en lugar de $\leq$.
- $x\leq y \implies xz \leq yz \text{ si } z\geq0$
	$\implies xz \geq yz \text{ si } z \leq 0$
	$\Longleftrightarrow xz \leq yz \text{ si } z > 0$ (en este caso, la implicación es bidireccional, ya que tenemos la suficiente información para saber que se cumple el caso $x\leq y$. Por ejemplo, si z puede ser negativo, entonces no importa los números que multiplique, siempre dará 0, por lo que no se cumple el enunciado)
	$\Longleftrightarrow xz \geq yz \text{ si } z < 0$
	$\Longleftrightarrow \frac{x}{z} \leq \frac{y}{z} \text{ si } z > 0$
	$\Longleftrightarrow \frac{x}{z} \geq \frac{y}{z} \text{ si } z < 0$
	
	Para establecer las reglas sobre $x < y$ estricto, simplemente debemos eliminar las primeras dos implicaciones (ya que no tienen sentido en dicho caso), y en el resto debemos modificar los símbolos $\leq$ y $\geq$ por $<$ y $>$ respectivamente.

A continuación, representamos gráficamente una multiplicación, tratándose de una dilatación, en caso de que z sea mayor que 1 o menor que -1 (cambiando el signo en este caso), o una compresión, si $-1\leq z\leq 1$. Si el número es positivo, no cambia la posición, mientras que si es negativo, si lo hace.
![[Representación de dilatación - contracción.png]]

Ahora, pasaremos a revisar las reglas de orden y el inverso:
- $x\leq y \implies x^{-1} \geq y^{-1} \text{ si } x,y>0 \text{ o } x,y <0$
Es fundamental que x e y sean del mismo signo, ya que en caso contrario, la igualdad no se cumple.
Lo podemos representar de la siguiente forma:
![[Representación del inverso.png]]

<u>Signos</u>: $\forall x,y \in \mathbb{R}, x<y \oplus x=y \oplus x>y$
En particular: $\forall x \in \mathbb{R}, x<0 \oplus x=0 \oplus x>0$
$$
\begin{align}
&\mathbb{R}^{+}={x \in \mathbb{R}: x > 0} \\
&\mathbb{R}^{-}={x \in \mathbb{R}: x < 0} \\
&\mathbb{R}=\mathbb{R}^{-} \cup {0} \cup \mathbb{R}^{+}
\end{align}
$$
# Propiedades surgidas de los axiomas

## Regla de los signos

| **$+$**      | Positivo | Negativo |
| ------------ | -------- | -------- |
| **Positivo** | Positivo | ?        |
| **Negativo** | ?        | Negativo |

| **$\times$** | Positivo | Negativo |
| ------------ | -------- | -------- |
| **Positivo** | Positivo | Negativo |
| **Negativo** | Negativo | Positivo |
Estas propiedades son consecuencias de los axiomas anteriores, deben demostrarse, puesto que no hay axiomas que establezcan dichas reglas. Todo parte de las reglas algebraicas, si las aceptamos, tenemos que respetar las propiedades anteriores (cosas como producto de dos negativos es positivo).

## Intervalos
Teniendo todo lo anterior, podemos definir los intervalos
$$
\begin{align}
&[a, b] ::= {x \in \mathbb{R}: a \leq x \leq b} \\
&(a, b) ::= {x \in \mathbb{R}: a < x < b} \\
&(a, b] ::= {x \in \mathbb{R}: a < x \leq b} \\
&[a, b) ::= {x \in \mathbb{R}: a \leq x < b} \\
&\text{Las definiciones anteriores únicamente tienen sentido si } a \leq b \\
&\text{En caso contrario, se tendrá un conjunto vacío } (\emptyset) \\ \\

&(-\infty, a] ::= {x \in \mathbb{R}: x \leq a} \\
&(-\infty, a) ::= {x \in \mathbb{R}: x < a} \\
&[a, +\infty) ::= {x \in \mathbb{R}: x \geq a}  \\
&(a, +\infty) ::= {x \in \mathbb{R}: x > a} \\ \\

&(-\infty, +\infty) ::= \mathbb{R} \\
&\text{El conjunto vacío } (\emptyset) \text{ también se puede considerar un intervalo, aunque no hay una notación específica para el el mismo}
\end{align}
$$
Ejemplo:
Vamos a calcular la intersección entre dos intervalos.
$$
\begin{align}
&[a,b] \cap [c,d] \qquad \text{Damos por hecho que } a \leq b \text{ y } c \leq d \\
&[a,b] \cap [c,d] = \emptyset \text{ si } b<c \\
&[a,b] \cap [c,d] = [c,b] \text{ si } a\leq c \leq b \leq d \\
&\dots \\ \\

&\text{Existen un montón de casos dados por la posición relativa de los extremos.} \\
&\text{Sin embargo, veremos una fórmula general:} \\ \\

&= [máx(a,c), mín(b,d)] \text{ si } máx(a,c) \leq mín(b,d) \\
& \text{si no } = \emptyset
\end{align}
$$
Pasando al siguiente tema, trataremos las estructuras de un cuerpo totalmente ordenado.

## Estructura de cuerpo totalmente ordenado
Ya vimos que un cuerpo R es aquel en el que se puede sumar, restar, multiplicar y dividir sin problemas (considerando que se cumplan los axiomas de suma y producto). Si además, tenemos un orden total que cumple los axiomas del grupo 3, entonces se dice que R es un cuerpo totalmente ordenado.

$\mathbb{R}$ cumple los axiomas
- $(I.1-4)$
- $(II.1-5)$
- $(III.1-5)$
y es un cuerpo totalmente ordenado.
Con solo especificar que se trata de un cuerpo ordenado, ya se asume que cumple los axiomas mencionados.
El conjunto de los racionales $(\mathbb{Q})$ es el único ejemplo que conocemos de cuerpos totalmente ordenados, ya que $\mathbb{C}$ y el ejemplo de 0 y 1 que vimos la clase anterior no lo son. Sabiendo esto, surge una pregunta importante: ¿Qué distingue a $\mathbb{Q}$ de $\mathbb{R}$ si todas estas propiedades son compartidas por ambos?

Aquí es donde entra en juego el **axioma de completitud** $(IV)$, el que marca la diferencia entre $\mathbb{R}$ y $\mathbb{Q}$, y veremos porque $\mathbb{Q}$ no lo cumple.

$(IV) \longrightarrow \text{Todo subconjunto no vacío de } \mathbb{R} \text{ y superiormente acotado tiene un supremo}$
Los conceptos de "superiormente acotado" y "supremo" serán cubiertos en clases posteriores.

# El conjunto $\mathbb{N}$ de los enteros naturales
Ya vimos una definición vaga de los enteros naturales, algo como: $\mathbb{N}={\dots,-1,0,1,\dots}$
Vamos a partir de $\mathbb{R}$, y queremos extraer un subconjunto $\mathbb{N}$ a partir del mismo, en base a los elementos de $\mathbb{R}$ que cumplen la propiedad "ser un entero natural":
$$
\begin{align}
&\text{Sea s: }\mathbb{R} \rightarrow \mathbb{R} \text{ definida por } S(x):=x+1 \\
&\text{Ya tenemos } 0,1 \in \mathbb{R}, se definen \\
&2:= S(1):= 1+1 \\
&3:= S(2):= 2+1 \\
&4:= S(4):= 4+1 \\
&\dots
\end{align}
$$
Queremos llegar a un subconjunto de $\mathbb{R}$ que contenga a los elementos de $\mathbb{N}$ y ninguno más.

<u>Definición de conjunto inductivo</u>: Se dice que un subconjunto $A \subset \mathbb{R}$ es <u>inductivo</u> cuando:
1. $0 \in A$
2. $\text{Si } x \in A \text{, enconces } s(x) \in A \qquad \text{("A es estable por sucesor")}$

Ejemplos
Los siguientes conjuntos son inductivos:
- $[0,+\infty]$
- $\mathbb{Z}$
- $\mathbb{Q}$

Los siguientes conjuntos no son inductivos:
- $\mathbb{R}^{+} \rightarrow \text{0 no está incluido}$
- $[0,42] \rightarrow \text{42 está incluido, pero no 43}$
- $[0,42) \rightarrow \text{41 está incluido, pero no 42}$

<u>Definición</u>: Se llama un <u>entero natural</u> todo real $x \in \mathbb{R}$ que pertenece a todos los subconjuntos inductivos.
$$
\begin{align}
&\mathbb{N}:= {x \in \mathbb{R}: \forall A \subset \mathbb{R}, A \text{ inductivo } \implies x \in A}
\end{align}
$$
Equivale a "el conjunto de los reales que pertenecen a todos los conjuntos inductivos".
De esta forma, llegamos a una definición formal, por comprensión. Esta definición coincide con la intersección de todos los subconjuntos inductivos.

Una propiedad fundamental es que, por construcción, el conjunto anterior también es inductivo, aunque es el inductivo más pequeño:
<u>Propiedad</u>: $\mathbb{N}$ es el subconjunto inductivo de $\mathbb{R}$ más pequeño:
1. $\mathbb{N}$ es inductivo
2. $\mathbb{N} \subset A$ para todo subconjunto inductivo $A \subset \mathbb{R}$

Ahora hablaremos de la propiedad más importante de los naturales: **la inducción completa**
A continuación, demostraremos el **principio de inducción completa**:

# Principio de inducción completa
$$
\begin{align}
&\text{Sea } P(n) \text{ un enunciado sobre } n \in \mathbb{N}. \\
&\text{Si} P(0) \qquad \text{(caso de base)} \\
&\text{Si} \forall n \in \mathbb{N}, P(n) \implies P(n+1) \qquad \text{(paso de inducción)} \\
&\text{Entonces: } \forall n \in \mathbb{N}, P(n)
\end{align}
$$
Si puedo probar que una propiedad se aplica para 0, y en base a eso, tomando como referencia que funciona para n (siendo n un elemento de $\mathbb{N}$), demuestro que se aplica para el sucesor de n $(n+1)$.
El paso base y paso inductivo funcionan como el punto de partida de la demostración, siendo el "entonces" a lo que queremos llegar: probar que se cumple para todo elemento de $\mathbb{N}$.

Para que funcione, es fundamental:
1. Tener el caso base. Confirmar que la propiedad funciona para 0.
2. No tener ninguna "rotura de caída". Demostrar correctamente que si se cumple para un elemento, también se cumple para el siguiente.

<u>Demo</u>: $\text{Sea } A:= {x \in \mathbb{N}: P(n)}$
Para nosotros, P(n) significa "n cae".
- $0 \in A$, pues P(0) $\rightarrow$ es una hipótesis, así que se cumple.
- $x\in A \implies P(x) \implies P(x+1) \implies x+1 \in A \text{ (x+1=s(x))} \rightarrow$ significa que A es estable por sucesor.
Luego A es un conjunto inductivo.
Entonces $\mathbb{N} \subset A \rightarrow$ recordemos que $\mathbb{N}$ es un subconjunto de todos los conjuntos inductivos.
- $\forall n \in \mathbb{N}, n \in A$
- $\forall n\in \mathbb{N}, P(n)$

## Variante
Sean:
- P(n) un enunciado sobre $n \in \mathbb{N}$
- $n_{0} \in \mathbb{N} \text{ fijado}$
$$
\begin{align}
&\text{Si } P(n_{0}) \\
&\text{y } \forall n\geq n_{0}, P(n)\implies P(n+1) \\
&\text{Entonces } \forall n\geq n_{0}, P(n) 
\end{align}
$$
Es exactamente el mismo principio, aunque en lugar de comenzar en 0, partimos de $n_{0}$, puesto que a veces se realizan inducciones a partir de 1 u otro valor. Se demuestra de forma similar a la anterior.
