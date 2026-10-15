En esta clase hablaremos sobre los números reales, además de tratar el último axioma de los números reales ($IV$).
La vez pasada hablamos sobre los enteros naturales, que son los números utilizados para contar, y están cerrados por suma y producto (todos los resultados de suma y multiplicación de dos enteros naturales forman parte de $\mathbb{N}$).
A continuación, hablaremos sobre otros dos subconjuntos de $\mathbb{R}$, siendo específicamente $\mathbb{Z}$ y $\mathbb{Q}$.
# Los subconjuntos $\mathbb{Z}$ y $\mathbb{Q}$
Vimos que los enteros naturales tienen un montón de propiedades que salen del principio de inducción (clase anterior que aún no he visto), pero tienen un defecto importante, pues no se pueden ni restar ni dividir en general, pues el resultado puede no ser un entero natural. De esta forma, cerramos los enteros naturales por la resta, y esto nos va a definir $\mathbb{Z}$.

## Enteros - $\mathbb{Z}$
<u>Definición</u>: $\mathbb{Z}:= \{c-d:c,d \in \mathbb{N}\}$
Se definen como el conjunto de todas las restas posibles entre dos enteros naturales.
Como la resta es definida sobre todo $\mathbb{R}$, pero no sobre todo $\mathbb{N}$, salimos del conjunto de los naturales, para definir así un nuevo conjunto. Elegimos las letras c y d por "crédito" y "débito".

<u>Propiedad</u>: $\mathbb{Z} \text{ es cerrado por } +,-,\times$
<u>Demostración</u>: $n_{1}=c_{1}-d_{1}, n_{2}=c_{2}-d_{2}$
$$
\begin{align}
&n_{1}+n_{2}=(c_{1}-d_{1})+(c_{2}-d_{2})=(c_{1}+c_{2})-(d_{1}+d_{2}) \in \mathbb{Z} \\
&n_{1}-n_{2}=(c_{1}-d_{1})-(c_{2}-d_{2})=(c_{1}+d_{2})-(d_{1}+c_{2}) \in \mathbb{Z} \\
&n_{1}\times n_{2}=(c_{1}-d_{1})\times(c_{2}-d_{2})=(c_{1}c_{2}+d_{1}d_{2})-(c_{1}d_{2}+d_{1}c_{2}) \in \mathbb{Z}
\end{align}
$$
De esta manera demostramos que:
- La suma de dos enteros se puede expresar como la resta de un natural y otro natural.
- La diferencia de dos enteros se puede expresar como la resta de un natural y otro natural.
- El producto de dos enteros se puede expresar como la resta de un natural y otro natural.
Por esta razón, $\mathbb{Z}$ es cerrado por la suma, resta y producto. Técnicamente se llama anillo conmutativo totalmente ordenado.

<u>Propiedad</u>: $\mathbb{Z}=\mathbb{N} \cup (-\mathbb{N})=\mathbb{N} \cup \{ -n: n \in \mathbb{N} \}$
Podemos definir a $\mathbb{Z}$ como la unión de $\mathbb{N}$ y el conjunto de todos los opuestos a $\mathbb{N}$ (denotado como $-\mathbb{N}$). No es disjunto porque el cero forma parte de $\mathbb{N} \text{ y } (-\mathbb{N})$ al mismo tiempo.

Lo único que nos falta definir es la clausura por cociente:

## Racionales - $\mathbb{Q}$
<u>Definición</u>: $\mathbb{Q}=\left\{  \frac{n}{d}: n,d \in \mathbb{Z}, d \neq 0 \right\}$

De esta manera, partiendo de los enteros naturales, hicimos una clausura por resta, obteniendo los enteros relativos, y después hacemos una clausura por cociente para obtener a los racionales.

<u>Propiedad</u>: $\mathbb{Q} \text{ es cerrado por } +,-,\times,\div$
<u>Demostración</u>:
$$
\begin{align}
&\frac{n_{1}}{d_{1}}+\frac{n_{2}}{d_{2}}=\frac{n_{1}d_{2}+n_{2}d_{1}}{d_{1}d_{2}} \qquad \text{(análogo para -)} \\
&\frac{n_{1}}{d_{1}}\times \frac{n_{2}}{d_{2}}=\frac{n_{1}n_{2}}{d_{1}d_{2}} \\
&\frac{\frac{n_{1}}{d_{1}}}{\frac{n_{2}}{d_{2}}}= \frac{n_{1}d_{2}}{d_{1}n_{2}}
\end{align}
$$
**ACLARACIÓN**: La clausura (o cerradura) es una propiedad matemática que garantiza que, al operar dos o más elementos de un conjunto específico (como números naturales, enteros, reales, etc.), el resultado permanece dentro de ese mismo conjunto.
Tenemos un conjunto de partida, aplicamos todas las operaciones posibles y vemos que pasa. De esta manera obtenemos $\mathbb{N}$, después $\mathbb{Z}$ y luego $\mathbb{Q}$.

<u>Propiedad</u>: $\mathbb{Q} \text{ es un cuerpo totalmente ordenado}$
$\mathbb{Q} \text{ cumple los axiomas (I.1-4), (II.1-5) y (III.1-5)}$

Hasta este punto (con las propiedades que hemos visto), no hemos logrado diferenciar a $\mathbb{Q}$ de $\mathbb{R}$. Sin embargo, existe una propiedad que el conjunto $\mathbb{Q}$ no cumple, pero si $\mathbb{R}$.

### Incompletitud de $\mathbb{Q}$
Inicialmente los números racionales servían para representar los puntos de la recta. Sin embargo, se descubrió un número de la recta que no se puede representar por ningún racional.
Todo fue a partir de dibujar un cuadrado de lado 1, y aplicando Pitágoras, se dieron cuenta de que la diagonal de dicho cuadrado (hipotenusa de un triangulo rectángulo isósceles de cateto 1) era igual a $\sqrt{ 2 }$. Sin embargo, no se descubrió que no era racional hasta mucho tiempo después.

#### Teorema
$\text{No existe ningún } r \in \mathbb{Q}^{+} tal que r^{2}=2$

La demostración se basa en dos lemas:
<u>Lema 1</u>: $\text{todo racional se puede escribir como fracción irreducible } \frac{p}{q} \text{ donde p, q no tienen divisor común } d>1$.
<u>Lema 2</u>: $\text{para todo } n \in \mathbb{Z} \text{, n es par } \Longleftrightarrow n^{2} \text{ es par}$

<u>Demostración</u>: Dos casos:
- O bien n es par: $n = 2p \implies n^{2}=4p^{2}=2\times 2p^{2}: \text{par (múltiplo de 2)}$
- O bien n es impar: $n = 2p+1 \implies (2p+1)^{2} = 4p^{2}+4p+1 = 2(2p^{2}+2p)+1$
Aquí de mostramos que un numero es par, si y solo si su cuadrado es par.

<u>Demostración del teorema</u>
Supongamos que $r=\frac{p}{q}$ en forma irreducible con $r^{2}=2$, es decir $\frac{p^{2}}{q^{2}}=2$, $p^{2}=2q^{2}$.
Tenemos que: $p^{2}=2q^{2}$
$\implies$ p es par: $p=2p'$
$$
\begin{align}
&(2p')^{2}=2q^{2} \\
&\implies 4p'^{2}=2q^{2} \\
&\implies q^{2}=2p'^{2} \text{ (par)} \\
&\implies \text{q es par}
\end{align}
$$
Sabiendo esto, ya podríamos simplificar. Sin embargo, es imposible, puesto que partimos de una fracción que no se puede reducir. Esto demuestra que no existe una fracción que sea igual a $\sqrt{ 2 }$. Partimos suponiendo que algo era falso (la raíz de 2 es un número racional), justamente para demostrar lo contrario.
Es fundamental entender esto, puesto que en matemáticas tenemos todo el derecho de desarrollar hipótesis y considerarlas verdaderas, lo sean o no, con la idea de probar la validez del argumento, llegando al absurdo cuando no tienen sentido (o cuando queremos probar que $A\implies B$, pero siendo A falso, B nunca será verdadero). De la misma forma, podemos demostrar la irracionalidad de raiz de 3, 5, 7, etc., todos los enteros cuyo cuadrado no es entero.

Tenemos que restaurar la armonía de los números, puesto que nos faltan números para completar la recta. Ahora veremos la diferencia de textura entre $\mathbb{R}$ y $\mathbb{Q}$.

# Axioma de completitud

$\text{(IV) Todo subconjunto de } \mathbb{R} \text{ no vacío y superiormente acotado tiene supremo}$
Vamos a hablar de cotas inferiores, superiores, mínimo, máximo, ínfimo y supremo, conceptos fundamentales para entender dicho axioma.

## Cota inferior/superior, mínimo/máximo, ínfimo/supremo
<u>Definición</u>: $\text{Sean } A\subset \mathbb{R} y k \in \mathbb{R}$
- k es cota inferior de A si $\forall x \in A, k \leq x$. No es un valor único, puesto que si tenemos una cota inferior y reducimos su valor, aún sigue siendo una cota inferior.
- k es cota superior de A si $\forall x \in A, k\geq x$. Al contrario de cota inferior.
No siempre existen cotas superiores e inferiores. Por ejemplo, para $\mathbb{Z}$ no existe ningún $k \in \mathbb{R}$, tal que $\forall x \in \mathbb{Z}, k \leq x \oplus k \geq x$.
<u>Observación</u>:
Si k es cota inferior de A, entonces todo $k'\leq k$ también lo es.
Si k es cota superior de A, entonces todo $k'\geq k$ también lo es.
![[Cota inferior y superior.png]]

<u>Definición</u>: $\text{Sea } A \subset \mathbb{R} \text{, y } k \in \mathbb{R}$
- Se dice que k es el mínimo de A si k es cota inferior de A y $k \in A$. De esta forma, es un valor único.
- Se dice que k es el máximo de A si k es cota superior de A y $k \in A$. También es un valor único.
Cuando existen, el mínimo y el máximo son únicos. Existe una notación específica:
$$
\begin{align}
mín(A) \\
máx(A)
\end{align}
$$
![[Mínimo y máximo.png]]

<u>Definición</u>: $A \subset \mathbb{R} \text{ no vacío. Se dice que } k \in \mathbb{R} \text{ es:}$
- El ínfimo de A si es la cota inferior de A más grande. También es el máximo del conjunto de las cotas inferiores de A.
- El supremo de A si es la cota superior de A más pequeña. También es el mínimo del conjunto de las cotas superiores de A.
No siempre existen, pero si existen, son únicos. También tiene una notación particular:
$$
\begin{align}
&ínf(A)= máx\{ k\in \mathbb{R}: \forall x \in A, k\leq x \} \\
&sup(A)= mín\{ k\in \mathbb{R}: \forall x \in A, k\geq x \}
\end{align}
$$
<u>Observación</u>:
$$
\begin{align}
&sup(A) \in A \Longleftrightarrow sup(A)=máx(A) \\
&ínf(A) \in A \Longleftrightarrow ínf(A)=mín(A)
\end{align}
$$
Si el supremo pertenece a A, entonces el supremo y el máximo coinciden. Ídem para el ínfimo y el mínimo.

Lo que distingue a $\mathbb{R}$ y $\mathbb{Q}$ es la propiedad fundamental de $\mathbb{R}$: si tengo un subconjunto no vacío que tiene cota superior, necesariamente tiene supremo.

## Axioma IV (Completitud)
Si $A \subset \mathbb{R}, A\neq \emptyset$ y si tiene una cota superior, entonces tiene supremo.
Esto no ocurre en $\mathbb{Z}$ y lo probaremos a continuación, aprovechando las operaciones definidas anteriormente para definir nuevos números.

### Ejemplo
$\text{Sea } A:=\{ x\in \mathbb{R}^{+}: x^{2}\leq 2 \}$
$1 \in \mathbb{A}$, y 2 es cota superior
tiene supremo $\sqrt{ 2 }:= \text{sup(A)}$

No es claro según la definición anterior, que el cuadrado de este nuevo número ($\sqrt{ 2 }$) es 2. Próximamente lo demostraremos.

La idea aquí es ver que si hiciéramos lo mismo en $\mathbb{Q}$, obtendríamos un conjunto que no tiene $\sqrt{ 2 }$, por lo tanto, aunque esté superiormente acotado, no tiene supremo, rompiendo con el axioma IV, y diferenciándolo de $\mathbb{R}$.

Ahora, podemos decir que $\mathbb{R}$ es un cuerpo ordenado completo. Hay un axioma que establece que $\mathbb{R}$ es el único cuerpo que cumple con todas las características necesarias (axiomas), para categorizarse como ordenado y completo.

Pregunta: con la definición anterior, ¿Cuál sería el resultado de $\sqrt{ 2 }$?
Vamos a demostrar que es dos, pero no es una demostración sencilla.

Otra cosa que se puede demostrar es que hay infinitamente mas reales que racionales. Valores como $\log2, \pi, e$ surgen del axioma correspondiente.

<u>Observación</u>: Si $A \subset \mathbb{R}, A\neq \emptyset$ y si tiene una cota inferior, entonces tiene ínfimo.

A partir de construir la figura en espejo y el opuesto, vamos a demostrar dicha propiedad (acercándonos a la idea establecida en el axioma anterior). No es un axioma, ya que surge del establecido anteriormente.

<u>Demostración</u>:
$\text{Sea } A':=\{ -x:x\in \mathbb{R}^{+} \}$
Por construcción, $A' \neq \emptyset$
y está acotado superiormente por -k
![[Propiedad del ínfimo.png]]

Por completitud: A' tiene supremo $sup(A')$
Nos interesa el ínfimo, no el supremo. Sin embargo, como es un espejo, el opuesto del supremo de A' es el ínfimo de A.
Se verifica que $-sup(A')=ínf(A)$

# Razonamiento a menos de $\epsilon$
Necesitamos un montón de herramientas para trabajar con este nuevo axioma, puesto que trajo nuevos números.

<u>Proposición</u>: 
$\text{Sean } a,b \in \mathbb{R}$
$\text{Si }a\leq b+\epsilon \text{ para todo } \epsilon>0 \text{, entonces } a\leq b$

Esto es útil para demostrar desigualdades "a menos de $\epsilon$", se agrega una distancia "$\epsilon$" con la idea de facilitar, buscando llegar a la idea de que si logro demostrar que dicha desigualdad se cumple para todo $\epsilon>0$, entonces la propiedad es verdadera.

<u>Variante</u>: $\text{Si }a < b+\epsilon \space (\forall \epsilon>0) \text{, entonces } a \leq b$
Importante: No es $a<b$, puesto que si sabemos que $a < b+\epsilon$, al quitar $\epsilon$, puede ser que $a=b$. El caso más claro de esto es $0 < 0 +\epsilon \implies 0<0$, que no es correcto.

<u>Demostración</u>: Por el absurdo, supongamos que $a \not \leq b$. Entonces $a>b$ (axioma III.1)
Sea $\epsilon = \frac{a-b}{2} > 0$
$b+\epsilon < b+2 \epsilon \implies b+(a-b) = a$
Luego $b+\epsilon \not \geq a : \text{contradicción}$
Demostramos que $b+\epsilon < a$, de forma que contradijimos épsilon.

Es fundamental entender que épsilon es necesario durante la demostración, pero como épsilon es cualesquiera, se puede concluir la desigualdad deseada.

<u>Proposición</u>: Sean $a,b \in \mathbb{R}$
Si $|a-b|<\epsilon$ para todo $\epsilon>0$
entonces $a=b$.

<u>Demostración</u>: Por la Proposición anterior:
$|a-b| \leq 0$
Entonces $|a-b| = 0$
Entonces $a=b$

Lo útil de "a menos de épsilon" es demostrar igualdades entre números teóricos, manejando un parámetro extra, un espacio, pero nunca se demuestra directamente que son iguales. Es la técnica más importante de todo el análisis.
Cuando tenemos expresiones complicadas, no podemos demostrar directamente que son iguales, pero si se puede razonar "a menos de épsilon".