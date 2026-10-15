# Integrales
Continuamos con las propiedades algebraicas de las integrales.

## Linealidad
### Teorema
Sean $f,g: [a,b] \to \mathbb{R}$ son integrables. Entonces:
1. $f + g$ es integrable, $\int_{a}^{b}(f + g) = \int_{a}^{b}f + \int_{a}^{b}g$.
2. Para todo $\alpha \in \mathbb{R}, \alpha f$ es integrable y $\int_{a}^{b} (\alpha f) = \alpha \cdot \int_{a}^{b} f$.

Como se interpreta este resultado:
El conjunto de las funciones integrales constituye un subespacio vectorial del conjunto de todas las funciones. Es decir, ignorando la igualdad, establece que el conjunto de las funciones integrales es estable por suma y es estable por producto por escalares. En definitiva, es la definición de lo que es un subespacio vectorial.
Para asegurarnos de que esté completa, habría que verificar que la función nula es integrable, pero es obvio (tiene integral nula).

Es fundamental entender que en análisis, todos los conjuntos de funciones notables son espacio vectoriales, habiendo una jerarquía de los mismos.
$$
\begin{align}
&\text{funciones} f: [a,b] \to \mathbb{R} \text{ (generales)} \\
&\supset \\
&\text{funciones acotadas} \\
&\supset \\
&\text{funciones integrales} \\
&\supset \\
&\text{funciones continuas} \\
&\supset \\
&\text{funciones derivables} \\
&\supset \\
&\text{funciones derivables dos veces} \\
 \\
&\dots \text{ Habiendo muchos más}
\end{align}
$$
Vamos a ver que los conjuntos están ordenados del menos regular al más regular, y los espacios de funciones regulares son cada vez más pequeños.

La segunda cosa que establece el teorema, es que un operador que toma una función y devuelve su integral, es decir, es una función que toma una función y devuelve un número real, es una transformación lineal. Estos son temas de Álgebra Lineal dentro de Cálculo I.

La noción de función continua y derivada funcionan del mismo modo, pero esto lo veremos posteriormente.
Lo importante es saber que siempre estamos trabajando con subespacios vectoriales, estructuras que aparecen constantemente en matemáticas.

A continuación, demostramos las propiedades:

### 1. Aditividad
#### Lema
Sean $f, g: [a,b] \to \mathbb{R}$ acotadas. Entonces para todo subintervalo $[a', b'] \subset [a, b]$
$$
\begin{align}
&ínf(f+g, [a', b']) \geq ínf(f, [a',b']) + ínf(g, [a', b']) \\
&sup(f+g, [a', b']) \leq sup(f, [a',b']) + sup(g, [a', b'])
\end{align}
$$
Podemos, por ejemplo, pensar en dos funciones opuestas, las cuales sumadas den la función nula (0):
$$
\begin{align}
&\text{Consideramos el intervalo } [0,1] \\
 \\

&f(x) = x \\
&g(x) = -x \\
&(f + g)(x) = 0 \\
 \\
&sup(f, [0,1]) = 1 \\
&sup(g, [0,1]) = 0 \\
&sup((f + g), [0,1]) = 0 \\
 \\
&ínf(f, [0,1]) = 0 \\
&ínf(g, [0,1]) = -1 \\
&ínf((f + g), [0,1]) = 0 \\
 \\
&\text{En conclusión: } \\
 \\
&sup((f + g), [0,1]) = 0 \leq sup(f, [0,1]) + sup(g, [0,1]) = 1 \\
&ínf((f + g), [0,1]) = 0 \geq ínf(f, [0,1]) + ínf(g, [0,1]) = -1
\end{align}
$$
Este lema nos va a facilitar la demostración de aditividad.

#### Demostración de aditividad
Usando el lema anterior, se verifica que
$$
\begin{align}
&S_{*}(f+g, P) \geq S_{*}(f, P) + S_{*}(g, P) \\
&S^{*}(f+g, P) \leq S^{*}(f, P) + S^{*}(g, P) \\
 \\
&\text{(para toda partición } P \subset [a, b])
\end{align}
$$
Queremos demostrar que
$$
\begin{align}
&I_{*}(f+g, P) \geq I_{*}(f, P) + I_{*}(g, P) \\
&I^{*}(f+g, P) \leq I^{*}(f, P) + I^{*}(g, P)
\end{align}
$$
Esto no es trivial (hay que razonar cuidadosamente). Es posible equivocarse utilizando las propiedades de ínfimo y supremo. En este caso, optaremos por utilizar el método "a menos de $\epsilon$".
Hay que recordar que la integral inferior es un supremo (el supremo de las sumas inferiores), por lo que utilizaremos $\epsilon > 0$:

Sea $\epsilon > 0$. Se consideran
- Una partición $P_{1} \subset [a, b]$ tal que $S_{*}(f, P_{1}) > I_{*}(f) - \frac{\epsilon}{2}$
- Una partición $P_{2} \subset [a, b]$ tal que $S_{*}(g, P_{2}) > I_{*}(g) - \frac{\epsilon}{2}$
(Las aproximaciones no tienen por que ser iguales, puesto que se trata de funciones diferentes.)
(Reemplazamos $\epsilon$ por $\frac{\epsilon}{2}$, ya que en caso contrario, al sumar las desigualdades obtendremos $2\epsilon$.)

Sea $P := P_{1} \cup P_{2}$
$$
\begin{align}
&I_{*}(f) + I_{*}(g) - \epsilon < S_{*}(f, P_{1}) + S_{*}(g, P_{2}) \leq S_{*}(f, P) + S_{*}(g, P) \leq S_{*}(f + g, P) \leq I_{*}(f + g) \\

\end{align}
$$
(Reemplazamos $P_{1}$ y $P_{2}$ por $P$, ya que así manejamos la misma partición en ambos casos, e incluso, como se trata de una partición más fina, utilizamos dos sumas inferiores mejores, más grandes.)
(Agregamos $S_{*}(f + g, P)$ a la desigualdad, basados en la verificación del lema anterior.)
(Por último, sabemos que la integral inferior es el supremo de las sumas inferiores, por lo que puedo agregarlo a la derecha.)

Demostramos que $I_{*}(f) + I_{*}(g) \leq I_{*}(f + g) + \epsilon \qquad (\forall \epsilon > 0)$

Para este tipo de demostraciones, es fundamental tener en cuenta los conceptos relacionados a supremo, ínfimo, suma inferior, suma superior, integral inferior, integral superior, entre otros.

**EJERCICIO**: Demostrar el análogo
Sea $\epsilon > 0$. Se consideran
- Una partición $P_{1} \subset [a, b]$ tal que $S^{*}(f, P_{1}) < I^{*}(f) + \frac{\epsilon}{2}$
- Una partición $P_{2} \subset [a, b]$ tal que $S^{*}(g, P_{2}) < I^{*}(g) + \frac{\epsilon}{2}$

Sea $P := P_{1} \cup P_{2}$
$$
\begin{align}
&I^{*}(f) + I^{*}(g) + \epsilon > S^{*}(f, P_{1}) + S^{*}(g, P_{2}) \geq S^{*}(f, P) + S^{*}(g, P) \geq S^{*}(f + g, P) \geq I^{*}(f + g) \\

\end{align}
$$

Demostramos que $I^{*}(f) + I^{*}(g) \geq I^{*}(f + g) - \epsilon \qquad (\forall \epsilon > 0)$

**FIN DEL EJERCICIO**

Esto funciona para cualquier par de funciones acotadas, sin importar si son integrables.

Ahora, si f y g son integrables, tenemos que $I_{*}(f) = I^{*}(f)$ y $I_{*}(g) = I^{*}(g)$. Luego:
$$
\int_{a}^{b} f + \int_{a}^{b} g = I_{*}(f) + I_{*}(g) \leq I_{*}(f + g) \leq I^{*}(f + g) \leq I^{*}(f) + I^{*}(g) = \int_{a}^{b} f + \int_{a}^{b} g
$$
De esta forma, se demuestra que todos los números que escribí aquí son iguales, puesto que tenemos una sucesión de desigualdades y obtuvimos la misma cosa en ambos lados.
Lo que nos interesa es que obtuvimos $I_{*}(f + g) = I^{*}(f + g)$, por lo que llegamos a la conclusión de que la suma de las funciones también es integrable y además que la integral de la suma de las funciones es igual a la suma de las integrales de cada función ($\int_{a}^{b} (f + g) = \int_{a}^{b} f + \int_{a}^{b} g$).

Lo importante para resolver este tipo de problemas es "enchufar" las cosas en el orden correcto, con la idea de demostrar lo que buscamos.

### 2. Homogeneidad
Se distinguen 3 casos: ¿$\int_{a}^{b} \alpha f = \alpha \int_{a}^{b} f$? (queremos demostrar que $\alpha f$ es integrable).
- Caso donde $\alpha = 0$.
$$
\int_{a}^{b} 0 \cdot f = 0 = 0 \cdot \int_{a}^{b} f
$$
(Este caso es trivial, ya que $\alpha f$ es la función nula, que sabemos que es integrable, y su integral es nula.)

- Caso donde $\alpha > 0$. Se verifica fácilmente que
$$
\begin{align}
&S_{*}(\alpha f, P) = \alpha S_{*}(f, P) \\
&S^{*}(\alpha f, P) = \alpha S^{*}(f, P) \\
 \\
&\text{ (Para toda partición } P \subset [a,b])
\end{align}
$$
($S_{*}(\alpha f, P) = \alpha S_{*}(f, P)$ es válido, ya que el ínfimo local de $\alpha f$ será igual a $\alpha$ por el ínfimo local de f. Ídem para el supremo local.)
(Esto funciona bien ya que $\alpha > 0$, de forma que se mantienen los signos y el orden correspondiente).
(Habría que demostrarlo)

y se deduce (lo mismo para las integrales superiores e inferiores):
$$
\begin{align}
&I_{*}(\alpha f) = \alpha I_{*} (f) \\
&I^{*}(\alpha f) = \alpha I^{*} (f)
\end{align}
$$
Siempre considerar que ==f es acotada==, de otra forma todo lo anterior no tiene sentido.

Como f es integrable:
$$
I_{*}(\alpha f) = \alpha \cdot I_{*}(f) = \alpha \cdot \int_{a}^{b} f = \alpha \cdot I^{*}(f) = I^{*}(\alpha f)
$$
(Recordar siempre que por hipótesis: $I_{*}(f) = I^{*}(f) = \int_{a}^{b} f$).

En conclusión, $\alpha f$ tiene misma integral inferior y superior ($I_{*}(\alpha f) = I^{*}(\alpha f)$), por lo que es integrable, y el valor de su integral es $\alpha \cdot \int_{a}^{b} f$.

Ahora, realizaremos el mismo caso, pero para cuando $\alpha < 0$:

- Caso donde $\alpha < 0$
(Aquí, el orden de las sumas inferiores y superiores se invierte, los ínfimos se van a transformar en supremos y viceversa.)
$$
\begin{align}
&S_{*}(\alpha f, P) = \alpha \cdot S^{*}(f, P) \\
&S^{*}(\alpha f, P) = \alpha \cdot S_{*}(f, P)
\end{align}
$$
De esto, deducimos lo mismo para las integrales:
$$
\begin{align}
&I_{*}(\alpha f) = \alpha \cdot I^{*}(f) \\
&I^{*}(\alpha f) = \alpha \cdot I_{*}(f)
\end{align}
$$
Ahora, tomando en cuenta la desigualdad anterior ("Como f es integrable"), desarrollamos la misma idea para $\alpha < 0$:
$$
I_{*}(\alpha f) = \alpha \cdot I^{*}(f) = \alpha \cdot \int_{a}^{b} f = \alpha \cdot I_{*}(f) = I^{*}(\alpha f)
$$
Logramos demostrar la linealidad. Proseguimos a enunciar un corolario importante, además de un montón de propiedades que no vamos a demostrar:

## Corolario - Combinaciones lineales
Si $f_{1}, \dots, f_{n}: [a, b] \to \mathbb{R}$ son integrables, entonces para todos $\alpha_{1}, \dots, \alpha_{n} \in \mathbb{R}$, la función $\alpha_{1}f_{1} + \dots + \alpha_{n}f_{n}$ es integrable, y:
$$
\int_{a}^{b}(\alpha_{1}f_{1} + \dots + \alpha_{n}f_{n}) = \alpha_{1} \int_{a}^{b} f_{1} + \dots + \alpha_{n} \int_{a}^{b} f_{n}
$$
Esta propiedad funciona para cualquier transformación lineal. Aquí, las funciones son los vectores, y establezco que la imagen por mi transformación lineal de mi combinación lineal de vectores (funciones), es igual a la combinación lineal correspondiente de las imágenes de los vectores.

Es importante entender que las funciones son excelentes vectores, puesto que una función tiene muchas coordenadas, pues para cualquier punto del intervalo, me da una coordenada, por lo que son cosas de dimensión infinita.

Lo interesante de esta propiedad es que a veces no sabemos calcular la integral de $(\alpha_{1}f_{1} + \dots + \alpha_{n}f_{n})$, pero si sabemos calcular la integral de cada componente: $\alpha_{1} \int_{a}^{b} f_{1} + \dots + \alpha_{n} \int_{a}^{b} f_{n}$, y también sabemos calcular la integral de la función.

**Caso particular**
Si $f \leq g$ (todos los puntos de f están debajo de los puntos de g).
En este caso particular:
$$
\text{Área } = \int_{a}^{b} g - \int_{a}^{b} f = \int_{a}^{b}(g - f)
$$
(Le restamos el "área de abajo" (f) a g).

## Integral y valor absoluto
Recordatorio:
El sentido de la integral es calcular el área algebraica de una función. Sin embargo, a veces lo que nos interesa no es el área algebraica, sino el área geométrica. La diferencia radica en que, en el área geométrica se cuenta todo con signo positivo, incluidas incluso las partes negativas.

Pero entonces, ¿Cómo pasamos de un problema de área geométrica a uno de área algebraica (que es lo que sabemos calcular)?

El truco consiste en reemplazar la función f por su valor absoluto, de forma que todos los valores con y negativo se sustituyen por el opuesto ("se reflejan"). Aplicamos el valor absoluto a la función en si.
==Es la compuesta de la función f con el valor absoluto.==
$$
\begin{align}
&|f|: [a,b] \to \mathbb{R} \\
&|f|(x) = |f(x)|
\end{align}
$$
Como la función resultante es positiva o nula, no hay diferencia entre el área algebraica y el área geométrica.
Si calculamos el área algebraica de esta nueva función, dicho valor será equivalente al área geométrica de la función original.

Sin embargo, hay un problema que hay que verificar: suponiendo que f es integrable, hay que demostrar que |f| es integrable.
Dicha demostración no es trivial.

No la haremos, aunque daremos un vistazo a las ideas que hay que considerar.
Para comenzar, hay que introducir la descomposición de una función en su parte positiva y su parte negativa.

### Definición
Dada $f: [a,b] \to \mathbb{R}$
- se llama parte positiva de f a la función $f^{+}: [a,b] \to \mathbb{R}$ definida por
$$
\begin{align}
&f^{+}(x) = máx(0, f(x))
\end{align}
$$
- Parte negativa:
$$
f^{-} := (-f)^{+}
$$
La podemos ver como "la parte positiva de la función opuesta", que por ende será la parte negativa de f.

### Observación
- $f^{+}, f^{-} \geq 0$ (son positivas o nulas por construcción)
- $f = f^{+} - f^{-}$ (f por construcción equivale a la diferencia entre la parte positiva y la parte negativa)
- $|f| = f^{+} + f^{-}$

#### Lema
$$
f: [a, b] \to \mathbb{R} \text{ integrable} \implies f^{+},f^{-}: [a,b] \to \mathbb{R} \text{ integrables}
$$
No existe ninguna relación entre las integrales. No hay fórmula para vincular las integrales de  $f^{+}$ y $f^{-}$ con la integral de $f$.

No vamos a demostrar el lema, pero analizaremos la idea del mismo:

**Idea**
$$
0 \leq S^{*}(f^{+}, P) - S_{*}(f^{+}, P) \leq S^{*}(f, P) - S_{*}(f, P) \qquad \text{Para toda partición } P \subset [a, b]
$$
No es difícil demostrar lo anterior, simplemente hay que demostrar que la aproximación para $f^{+}$ es mejor que para f, puesto que la diferencia entre la suma inferior y superior es menor.

Queremos demostrar que $f^{+}$ es integrable a menos de $\epsilon$. Es sencillo, ya que como sabemos que f es integrable, podemos considerar una partición para que la diferencia sea menor que $\epsilon$. Pero si $S^{*}(f, P) - S_{*}(f, P) < \epsilon \implies S^{*}(f^{+}, P) - S_{*}(f^{+}, P) < \epsilon$, puesto que $S^{*}(f, P) - S_{*}(f, P) \geq S^{*}(f^{+}, P) - S_{*}(f^{+}, P)$. De esta forma, el aproximar la integral de f a menos de $\epsilon$, también aproxima la integral de $f^{+}$ a menos de $\epsilon$.
En conclusión, por el criterio de integración, deducimos que $f^{+}$ también es integrable.

Es importante entender la idea. Usamos el criterio de integración en ambas direcciones. Como f es integrable, entonces para cada $\epsilon > 0$ existe una partición tal que $S^{*}(f, P) - S_{*}(f, P) < \epsilon$. Esto implica que también existe una partición (la misma), que cumple la misma desigualdad para $S^{*}(f^{+}, P) - S_{*}(f^{+}, P)$. Entonces, usando el criterio al revés deduzco que la función es integrable.

También se puede hacer para $f^{-}$: ahora que se que, como f es integrable, $f^{+}$ es integrable, luego:
$$
f^{-} = (-f)^{+}
$$
Como f es integrable, -f es integrable, entonces $(-f)^{+}$ también es integrable, lo que significa que $f^{-}$ es integrable.

Ahora, podemos demostrar la proposición fundamental con el valor absoluto.

### Proposición
Si $f: [a,b] \to \mathbb{R}$ es integrable, entonces $|f|$ también es integrable y
$$
\left| \int_{a}^{b} f \right| \leq \int_{a}^{b} |f|
$$
Esto es la desigualdad triangular infinita, continua.
Podemos reemplazar la suma continua por una suma usual (el valor absoluto de una suma es menor o igual a la suma de los valores absolutos, esto se conoce como desigualdad triangular infinita).
$$
\begin{align}
&|x + y| \leq |x| + |y| \\
 \\ \\
&\text{Por inducción llegamos a:} \\
&\left| \sum_{i=1}^{n} ai \right| \leq \sum_{i=1}^{n} |ai|
\end{align}
$$
Como vemos, siempre hallamos las mismas relaciones, aunque aplicadas a diferentes objetos.
A continuación, demostramos $\left| \int_{a}^{b} f \right| \leq \int_{a}^{b} |f|$

### Demostración
f es integrable, luego $f^{+}, f^{-}$ son integrables (por el lema anterior).
$$
\left| \int_{a}^{b} f \right| = \left| \int_{a}^{b} (f^{+} - f^{-}) \right| = \left| \int_{a}^{b} f^{+} - \int_{a}^{b} f^{-} \right| \leq \left| \int_{a}^{b} f^{+} \right| + \left| \int_{a}^{b} f^{-} \right| = \int_{a}^{b} f^{+} + \int_{a}^{b} f^{-} = \int_{a}^{b} (f^{+} + f^{-}) = \int_{a}^{b} |f|
$$
(Quitamos los valores absolutos de $\left| \int_{a}^{b} f^{+} \right| + \left| \int_{a}^{b} f^{-} \right|$, ya que sabemos que ambos valores son positivos SIEMPRE.)

Con esto, tenemos la propiedad importante de las integrales, y lo que hay que recordar de esto es que esto es nada mas que la ==desigualdad triangular extendida a las sumas continuas==.

Concluiremos con la aditividad respecto al intervalo.

## Aditividad respecto al intervalo
Hasta ahora, fijamos un intervalo y nunca salimos de este. Sin embargo, a continuación propondremos cambios con respecto a esto.

Cuando tenemos una función que es integrable en un intervalo dado, podemos restringir el tamaño del intervalo y lo que nos queda también será integrable. Sin embargo, no habrá ninguna proporcionalidad entre el área del intervalo restringido y del general, es impredecible.

### Proposición
Si $f: [a, b] \to \mathbb{R}$ es integrable en $[a, b]$ entonces también es integrable en cualquier subintervalo $[a', b'] \subset [a, b] \qquad (a \leq a' < b' \leq b)$.

La demostración de este lema es bastante pesada, pero consiste en observar que cuando tengo una partición sobre el gran intervalo, puedo reducir la partición en una partición del pequeño intervalo y que la distancia entre la suma inferior y la suma superior se reduce. Luego, se concluye usando el criterio de integrabilidad a menos de $\epsilon$.

Lo importante es que considerando la proposición, puedo definir la noción de función localmente integrable. Por primera vez, vamos a aceptar los intervalos abiertos, infinitos.

**Definición**
Sea $f: I \to \mathbb{R}$ definida en un intervalo $I \subset \mathbb{R}$ cualquiera.
Se dice que f es ==localmente integrable== si es integrable en todo subintervalo $[a,b] \subset I \qquad \text{(con } a < b)$.

Una observación es que cuando $I$ ya es de la forma $[a, b]$, tomando como referencia el lema anterior, ya vimos que es integrable en todo subintervalo, entonces es localmente integrable. Entonces, si una función es integrable en un intervalo cerrado, también es localmente integrable. Recíprocamente, si es localmente integrable en un intervalo cerrado, también es integrable en el intervalo lleno, que es un caso particular de inclusión.
De esta forma, la noción de función integrable coincide con la noción de función localmente integrable en el caso de los intervalos cerrados.

Por esta razón, el único interés de la nueva radica en el caso de intervalo no cerrado.

### Proposición
Sean $f: I \to \mathbb{R}$ definida en un intervalo $I \subset \mathbb{R}$, y $a,b,c \in I$ tales que $a < b < c$.
Si f es integrable en ambos intervalos $[a,b]$ y $[b,c]$, entonces f es integrable en $[a, c]$.
Además
$$
\int_{a}^{c} f = \int_{a}^{b} + \int_{b}^{c}
$$
No vamos a demostrar la propiedad. Esta demostración consiste en utilizar el criterio de integración (cuando ya conocemos el valor de la integral) a menos de $\epsilon$. Utilizamos este criterio (el primer criterio), puesto que tenemos una idea del valor de la integral: sabemos que es la suma de las dos integrales.

Durante la demostración, vamos a mostrar que la función entre a y c es integrable a menos de $\epsilon$ y que el candidato para la integral es la suma de ambas integrales. Después proseguimos de modo usual, dividimos a $\epsilon$ en dos, ya que tenemos dos integrales, aproximamos a menos de $\frac{\epsilon}{2}$ en cada intervalo, pegamos las particiones, verificamos que las sumas inferiores y superiores se comportan bien, etc.