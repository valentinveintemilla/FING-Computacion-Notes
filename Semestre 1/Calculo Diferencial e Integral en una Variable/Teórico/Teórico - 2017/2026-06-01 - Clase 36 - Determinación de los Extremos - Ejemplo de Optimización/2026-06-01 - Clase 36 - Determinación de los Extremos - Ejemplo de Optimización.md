# Derivadas
La clase pasada abordamos la regla de L'Hôpital.

## Extremos
Durante esta instancia, abordaremos el tema de extremos. 
Un problema típico dentro del tema es el de optimización en el cual se busca hallar un máximo de $x$ cantidad en base a otras cantidades. Tomaremos como ejemplo uno de los ejercicios parciales:
### Ejemplo
El problema de los extremos es que abordamos un único teorema: Si un intervalo contiene un extremo en un punto $a$, entonces $f'(a) = 0$, pero esto no garantiza que haya un extremo en dicho punto (no es recíproca). Por esta razón, generalmente hay que indagar un poco más.

ACLARACIÓN: $f'(a) = 0$ no implica que $a$ sea un extremo. Lo que es seguro es que, si $f'(a) \neq 0$, entonces $a$ no es un extremo. Básicamente, hay que estudiar los puntos para los cuales la derivada es 0 e ignorar el resto.

El ejercicio es el siguiente:
Una copa de vermut tiene la forma de un (medio) cono.

![[Semestre 1/Calculo Diferencial e Integral en una Variable/Teórico/Teórico - 2017/2026-06-01 - Clase 36 - Determinación de los Extremos - Ejemplo de Optimización/Imágenes/1 - Ejemplo.png]]

Se trabaja con una cantidad fija de cristal, determinada por el área lateral $A_{0}$.

Se trata de maximizar el volumen (dentro de la copa).

Recordemos las fórmulas que permiten calcular el área lateral y el volumen:
$$
A_{0} = \pi r g
$$
Aclaración: $g$ es la generatriz.
$$
V = \frac{1}{3}\pi r^{2} h
$$
Dicha fórmula surge de la fórmula del volumen un cilindro de base con radio $r$ y altura $h$: el área de la base es $\pi r^{2}$, y sabiendo que es regular, multiplicamos el resultado por $h$. Demócrito descubrió que el cono siempre tiene un tercero del volumen del cilindro con la misma base y altura, por lo que multiplicamos por $\frac{1}{3}$.

A partir de la representación, también podemos deducir el valor de $g$:
$$
g^{2} = r^{2} + h^{2}
$$

Tenemos una constante: $A_{0}$
El resto son cantidades variables: $r, h, g, V$

El enunciado de la letra establece: "hallar en función de $A_{0}$ el valor de $r$ que maximiza el volumen de la copa fabricada".

Esto nos indica que $V$ es la función que queremos maximizar, por lo tanto, la expresaremos como $V(r)$ (pues estamos buscando el valor máximo de $r$). Ahora, la idea es hacer desaparecer el resto de variables $g$ y $h$, expresándolas en función de las constante y de la variable $r$.

Primero, sobre el signo de las variables, en un primer caso, supondremos que $r > 0, h\geq 0, g > 0$ (por la fórmula de Pitágoras). Esto para evitar hacer cosas que no se puedan (como dividir por valores que pueden ser nulos).

Ahora, eliminemos $g$ en base a $A_{0}$:
$$
g = \frac{A_{0}}{\pi r}
$$
$$
h^{2} = g^{2} - r^{2} \implies h = \sqrt{ g^{2} - r^{2} } = \sqrt{ \frac{A_{0}^{2}}{\pi^{2} r^{2}} - r^{2} }
$$
Aquí tenemos un problema: tenemos que asegurarnos de que $\frac{A_{0}^{2}}{\pi^{2} r^{2}} - r^{2} \geq 0$.
Antes de proseguir, resolveremos la desigualdad anterior:
$$
\begin{align}
\frac{A_{0}^{2}}{\pi^{2} r^{2}} \geq r^{2} &\Longleftrightarrow \frac{A_{0}^{2}}{\pi^{2}} \geq r^{4} \\
&\Longleftrightarrow \frac{A_{0}^{2}}{\pi^{2}} \geq r^{4} \\
&\Longleftrightarrow \frac{A_{0}}{\pi} \geq r^{2} \\
&\Longleftrightarrow \sqrt{ \frac{A_{0}}{\pi} } \geq r
\end{align}
$$
De esta forma, sabemos que $r$ no puede ir al infinito, tiene un tope superior. El caso $r = \sqrt{ \frac{A_{0}}{\pi} }$, corresponde con $h = 0$, puesto que originalmente la desigualdad surgió de la definición de $h$.

Esto establece el intervalo de definición:
$$
r \in \left( 0, \sqrt{ \frac{A_{0}}{\pi} } \right]
$$
$r$ no puede ser 0, ya que $r$ es divisor en algunas expresiones que hemos desarrollado.

Ahora, se trata de calcular el volumen (cuando hablamos de $V$, nos referimos a $V(r)$).
$$
V = V(r) = \frac{1}{3} \pi r^{2} h = \frac{1}{3} \pi r^{2} \sqrt{ \frac{A_{0}^{2}}{\pi^{2} r^{2}} - r^{2} }
$$
Para quitar el $\pi^{2} r^{2}$ del denominador de uno de los términos dentro de la raíz cuadrada, podemos "meter" $r$ y $\pi$ que están multiplicando (fuera de la raíz) como $\pi^{2}$ y $r^{2}$
$$
= \frac{1}{3} r \sqrt{ A_{0}^{2} - \pi^{2} r^{4} }
$$

Ahora, queremos maximizar la función, para lo que tenemos que derivar. Podemos ver que la función puede ser algo complicada de derivar. Sin embargo, podemos utilizar el siguiente truco: cuando trabajamos con funciones positivas o nulas (como en este caso), maximizar la función es equivalente a maximizar su cuadrado (lo que nos facilitará la derivación).

> [!Lema]
> $f \geq 0$ alcanza un mínimo/máximo/extremo en un punto $x_{0}$ si y sólo si $f^{2}$ alcanza un mínimo/máximo/extremo en el mismo punto.

Los valores de los extremos no serán los mismos, pero estarán en los mismos lugares.
Dicho lema es útil cuando estudiamos funciones con raíces cuadradas.

Entonces:
$$
V^{2} = \frac{1}{9} r^{2} (A_{0}^{2} - \pi^{2} r^{4}) = \frac{1}{9} (A_{0}^{2}r^{2} - \pi^{2} r^{6})
$$
Ahora, derivamos la función:
$$
\begin{align}
(V^{2})' &= \frac{1}{9} (2A_{0}^{2}r - 6\pi^{2} r^{5}) \\
&= \frac{1}{9} r(2A_{0}^{2} - 6\pi^{2} r^{4})
\end{align}
$$

Ahora, tenemos que ver para que valores de $r$ la función se anula. Podemos ver fácilmente que se anula para $r = 0$, pero 0 no forma parte del intervalo considerado. En realidad, acabamos de ver que no hay problema en caso de que formara parte del dominio, pero igualmente consideraremos que la función no está definida en dicho punto por el intervalo inicial.

$$
(V^{2})' = 0 \Longleftrightarrow r = 0 \lor 6\pi^{2} r^{4} = 2A_{0}^{2}
$$
Pero $r = 0$ es imposible, ya que no se encuentra en el dominio $\left( 0, \sqrt{ \frac{A_{0}}{\pi} } \right]$.
Entonces, nos quedamos con:
$$
\begin{align}
(V^{2})' = 0 &\Longleftrightarrow 6\pi^{2} r^{4} = 2A_{0}^{2} \\
&\Longleftrightarrow r^{4} = \frac{A_{0}^{2}}{3\pi^{2}} \\
&\Longleftrightarrow r^{2} = \frac{A_{0}}{\pi \sqrt{ 3 }} \\
&\Longleftrightarrow r = \underbrace{ \sqrt{ \frac{A_{0}}{\pi \sqrt{ 3 }} } }_{ > 0 } \qquad \left( \leq \sqrt{ \frac{A_{0}}{\pi} } \right)
\end{align}
$$
Verificamos que el resultado está contenido en el intervalo de definición:
$$
r_{0} = \sqrt{ \frac{A_{0}}{\pi \sqrt{ 3 }} } \in \left( 0, \sqrt{ \frac{A_{0}}{\pi} } \right]
$$
Según el teorema, como tengo un extremo, y el extremo está dentro del intervalo considerado, entonces se encuentra en el punto $r = \sqrt{ \frac{A_{0}}{\pi \sqrt{ 3 }} }$. Sin embargo, no podemos concluir que dicho extremo es un máximo (lo que estamos buscando). Para esto, analizaremos el signo de la derivada.

Si hacemos una tabla de valores para estudiar las variaciones:

|                |  0  |                         | $r_{0} = \sqrt{ \frac{A_{0}}{\pi \sqrt{ 3 }} }$ |                           | $r_{max} = \sqrt{ \frac{A_{0}}{\pi} }$ |
| :------------: | :-: | :---------------------: | :---------------------------------------------: | :-----------------------: | :------------------------------------: |
| **$(V^{2})'$** |     |            +            |                                                 |             -             |                                        |
|  **$V^{2}$**   |     | Estrictamente creciente |                                                 | Estrictamente decreciente |                                        |
| **$V \geq 0$** |     | Estrictamente creciente |                                                 | Estrictamente decreciente |                                        |
Para establecer el + y -, tomamos como referencia la fórmula de $h$.

Sabíamos que $r_{0} = \sqrt{ \frac{A_{0}}{\pi \sqrt{ 3 }} }$ era un extremo, pero ahora, estamos seguros de que $r_{0} = \sqrt{ \frac{A_{0}}{\pi \sqrt{ 3 }} }$ es un máximo.

En conclusión:
$V$ alcanza su valor máximo (es maximal) cuando
$$
r = r_{0} = \sqrt{ \frac{A_{0}}{\pi \sqrt{ 3 }} }
$$

En caso de que el valor para el cual la función toma su valor máximo no hubiera formado parte del intervalo estudiado, entonces tendríamos un signo constante (positivo o negativo), y el máximo y mínimo serían los extremos del intervalo.

Entonces, cuando trabajamos con un problema de extremos, tenemos que hacer una tabla de variaciones, comenzando estudiando el signo de la derivada, y en base a eso, podemos deducir el comportamiento del resto de funciones, estableciendo si el punto tomado como referencia es un extremo y el tipo del mismo.

En caso de haber varios extremos, puntualmente varios máximos, habría sido necesario comparar el valor de cada uno, y quedarnos con el mayor.

En base al $r$ encontrado, podemos determinar el resto de valores ajustados a dicha variable:
$$
\begin{align}
h^{2} &= \frac{A_{0}^{2}}{\pi^{2}r^{2}} - r^{2} \\
&= \frac{1}{r^{2}} \left( \frac{A_{0}^{2}}{\pi^{2}} - r^{4} \right) \\
&= \frac{1}{r^{2}} \left( \frac{A_{0}^{2}}{\pi^{2}} - \frac{A_{0}^{2}}{3\pi^{2}} \right) \\
&= \frac{2 A_{0}^{2}}{3 r^{2} \pi^{2}}
\end{align}
$$

Si seguimos operando, la expresión se logra simplificar. Luego, con el valor de $h$, podemos calcular el ángulo $\alpha$ formado por los lados $h$ y $g$ (en base al triángulo rectángulo representado en un inicio).

Ahora, considerando que se trata de el ángulo formado por un cateto (adyacente) $h$ y la hipotenusa $g$, podemos expresar lo siguiente:
$$
\cos \alpha = \frac{h}{g} \implies \alpha = \arccos\left( \frac{h}{g} \right)
$$
De esta forma, se obtiene un valor constante que no depende de ninguna variable, y se trata del ángulo perfecto para construir una copa de vermut.

Con esto concluimos la clase.
