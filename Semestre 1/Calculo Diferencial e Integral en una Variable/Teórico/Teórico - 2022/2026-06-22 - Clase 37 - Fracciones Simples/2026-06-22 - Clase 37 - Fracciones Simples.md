# Integración por fracciones simples
En el día de hoy abordaremos el método de integración de fracciones simples, permitiendo integrar coeficientes de polinomios:
$$
\int \frac{f(x)}{g(x)} \space dx
$$
con $f, g$ polinomios.

Ya sabemos integrar polinomios, y con este método podremos integrar cualquier cociente. A diferencia de los métodos de partes y sustitución, aquí podemos suponer cual será la forma de la primitiva, funcionando siempre (siempre existe una primitiva que podemos expresar mediante uan función).

## Pasos a seguir
El método se aplica de la siguiente forma:
### 1 - Reducción al caso grado (numerador) < grado (denominador)
Partimos de un cociente cualquiera, y lo expresamos como $$
   \frac{f(x)}{g(x)} = Q(x) + \frac{R(x)}{g(x)}
   $$
siendo $Q(x), R(x), g(x)$ polinomios, pero con la particular de que el grado de $R(x)$ es menor que el grado de $g(x)$: $gr(R(x)) < gr(g(x))$.
   
En caso de que $gr(f(x)) < gr(g(x))$, este paso no se realiza.

### 2 - Descomposición en fracciones simples
Este es el paso más importante.

Teniendo $\frac{f(x)}{g(x)}$ con $gr(f(x)) < gr(g(x))$, descompondremos la expresión como una suma de funciones racionales más simples, las cuales sabremos integrar:
$$
\frac{f(x)}{g(x)} = \frac{P_{1}(x)}{Q_{1}(x)} + \frac{P_{2}(x)}{Q_{2}(x)} + \dots + \frac{P_{n}(x)}{Q_{n}(x)}
$$

### 3 - Integrar
$$
\int \frac{f(x)}{g(x)} \space dx = \int \frac{P_{1}(x)}{Q_{1}(x)} \space dx + \int \frac{P_{2}(x)}{Q_{2}(x)} \space dx + \dots + \int \frac{P_{n}(x)}{Q_{n}(x)} \space dx
$$

¿Cuáles son las "fracciones simples"?

Luego de realizar el paso dos, obtendremos esas "fracciones simples", pero, ¿Cuáles son? ¿Qué forma tienen?
Existe un teorema que establece que cuando tenemos un coeficiente de polinomios $\frac{f(x)}{g(x)}$ que cumple que $gr(f(x)) < gr(g(x))$, entonces es posible descomponer dicho polinomio en "fracciones simples", apareciendo términos como los siguientes:
1. $\frac{1}{x - \alpha}$
$$
\int \frac{1}{(x - \alpha)} \space dx \underbrace{ = }_{ \begin{align}
&u = x - \alpha \\
&du = dx
\end{align} } \int \frac{du}{u} = \log(|u|) + C = \log(|x + \alpha|) + C
$$
$\log(|u|)$ es una primitiva de $\frac{1}{u}$ en $\mathbb{R} \setminus \{ 0 \}$. En cambio, $\log(|u|)$ es una primitiva de $\frac{1}{u}$ en $\mathbb{R}^{+}$

2. $\frac{1}{(x - \alpha)^{n}}$ con $n \in \mathbb{N}, n \geq 2$
$$
\int \frac{1}{(x - \alpha)^{n}} \space dx = \int (x - \alpha)^{-n} \space dx \underbrace{ = }_{ \begin{align}
&u = x - \alpha \\
&du = dx
\end{align} } \int u^{-n} \space du = \frac{u^{-n + 1}}{-n + 1} + C = \frac{(x - \alpha)^{-n + 1}}{-n + 1} + C
$$

Hay otras dos fracciones que pueden aparecer, aunque no las integraremos aún:
3. $\frac{Ax + B}{ax^{2} + bx + c}$ con $b^{2} - 4ac < 0$ (sin raíces reales).
La aprenderemos a integrar en el correr de la clase.

4. $\frac{Ax + B}{(ax^{2} + bx + c)^{n}}$ con $b^{2} - 4ac < 0$ (sin raíces reales) y $n \in \mathbb{N}, n \geq 2$.
Se muestra en el libro de Apostol, aunque no la veremos en el curso.

### Aplicación del método

Primero que nada, veremos como reducir un cociente de polinomios que no cumple la condición de grados, y luego empezaremos a estudiar el método de descomposición en fracciones simples.

#### Reducción al caso grado (numerador) < grado (denominador)
Comenzaremos a estudiar ejemplos presentados en el Apostol:
$$
\int \frac{x^{3} + 3x}{x^{2} - 2x - 3} \space dx
$$
En este caso, como no se cumple la condición de grados, desarrollamos la división de polinomios:
![[1 - Reducción al caso grado - Ejemplo 1.png]]
Básicamente, en la división de polinomios, intentamos obtener un resultado de menor grado que el divisor. Vamos agregando términos en el resultado de acuerdo al valor de mayor grado del dividendo que queremos eliminar (multiplicaremos dicho valor por el divisor y se lo restaremos al dividendo).

Luego de finalizada la división, podemos expresar
$$
x^{3} + 3x = (x^{2} - 2x - 3) \cdot (x + 2) + (10x + 6)
$$
Ahora, sustituimos esto en la integral:
$$
\begin{align}
\int \frac{x^{3} + 3x}{x^{2} - 2x - 3} \space dx &= \int \frac{(x^{2} - 2x - 3) \cdot (x + 2) + (10x + 6)}{x^{2} - 2x - 3} \space dx \\
&= \int \frac{\cancel{ (x^{2} - 2x - 3) } \cdot (x + 2)}{x^{2} - 2x - 3} + \frac{10x + 6}{x^{2} - 2x - 3} \space dx \\
&= \int \frac{\cancel{ (x^{2} - 2x - 3) } \cdot (x + 2)}{\cancel{ x^{2} - 2x - 3 }} + \frac{10x + 6}{x^{2} - 2x - 3} \space dx \\
&= \int (x + 2) + \frac{10x + 6}{x^{2} - 2x - 3} \space dx \\
&= \int x + 2 \space dx + \int \frac{10x + 6}{x^{2} - 2x - 3} \space dx
\end{align}
$$
Finalmente, obtuvimos una expresión que cumple con la condición de grados establecida. Con esto concluimos el primer paso.

Ahora, pasamos al segundo paso: como realizar la descomposición en fracciones simples.

#### Descomposición en fracciones simples
Ahora, aplicaremos un teorema para descomponer la expresión, el cual tiene como hipótesis que el numerador tenga menor grado que el denominador.
$$
\int \frac{5x + 3}{x^{2} + 2x - 3} \space dx
$$
En general, lo que hay que hacer en este método es factorizar el denominador lo más que podamos, básicamente determinar las raíces del polinomio y expresarlo como un producto de varios factores de la forma $x + r$, siendo $r$ una raíz.
$$
\frac{5x + 3}{(x - 1)(x + 3)}
$$
$$
\int \frac{5x + 3}{x^{2} + 2x - 3} \space dx = \int \frac{5x + 3}{(x - 1)(x + 3)} \space dx
$$
Al final del procedimiento, hallaremos una primitiva de la función $\frac{5x + 3}{x^{2} + 2x - 3}$, la cual, en base a sus raíces, podemos ver que está definida en cualquier $x$ donde no se anule el denominador (en este caso $x \in \{ -3, 1 \}$.

Como la función no está definida en $x \in \{ -3, 1 \}$, lo mismo pasa para su primitiva (en cualquier número fuera de $\{ -3, 1 \}$). Además, hay que tener cuidado al aplicar Barrow: En este caso, no es posible aplicar Barrow para determinar la integral entre, por ejemplo, 0 y 5, debido a que la función no es integrable en dicho intervalo (seguramente tienda a infinito en los puntos mencionados). Igualmente, es integrable en cualquier intervalo que no contenga puntos en los que la función no está definida.

Ahora, ¿Cómo proseguimos los cálculos? Luego de tener un polinomio de menor grado como numerador y expresar el denominador como un producto en base a sus raíces, según el teorema de "fracciones simples", necesariamente (siempre) podemos expresar dicho cociente como:
$$
\begin{align}
\frac{5x + 3}{x^{2} + 2x - 3} &= \frac{5x + 3}{(x - 1)(x + 3)} \\
&= \frac{A}{x - 1} + \frac{B}{x + 3} \\
&= \frac{A(x + 3) + B(x - 1)}{(x - 1)(x + 3)} \\
&= \frac{(A + B)x + (3A - B)}{(x - 1)(x + 3)}
\end{align}
$$
Ahora, nos queda resolver un sistema para determinar cada coeficiente de los nuevos numeradores:
$$
\begin{cases}
A + B = 5 \\
3A - B = 3
\end{cases} \implies \begin{align}
&A = 2 \\
&B = 3
\end{align}
$$
A continuación, el último paso:

#### Integrar
De esta forma:
$$
\begin{align}
\int \frac{5x + 3}{x^{2} + 2x - 3} \space dx &= \int \frac{2}{x - 1} + \frac{3}{x + 3} \space dx \\
&= 2\int \frac{1}{x - 1} \space dx + 3\int \frac{1}{x + 3} \space dx \\
&= 2\log(|x - 1|) + 3\log(|x + 3|) + C
\end{align}
$$
Así finaliza la aplicación del método.

Es importante entender que esto fue un caso particular del teorema de descomposición en fracciones simples, donde el denominador se descompone como producto de polinomios de grado 1 todos con multiplicidad uno:
$$
\frac{f(x)}{g(x)} \text{ con } gr(f) < gr(g) \text{ donde } g(x) = (x - \alpha_{1})(x - \alpha_{2}) \dots (x- \alpha_{n}) \text{ y } \alpha_{i} \neq \alpha_{j} \text{ si } i \neq j
$$
Esto quiere decir que no vimos raíces múltiples en el ejemplo.

El teorema de descomposición en fracciones simples (TDFS) establece que $\exists A_{1}, A_{2}, \dots, A_{n} \in \mathbb{R}$ tal que
$$
\frac{f(x)}{g(x)} = \frac{A_{1}}{x - \alpha_{1}} + \frac{A_{2}}{x - \alpha_{2}} + \dots + \frac{A_{n}}{x - \alpha_{n}}
$$

El procedimiento sería el siguiente:
1. Expresar el cociente de tal forma que cumpla la condición $gr(f) < gr(g)$ (mediante división de polinomios).
2. Teniendo la nueva expresión, buscamos las raíces del denominador y lo expresamos como un producto.
3. Expresamos el cociente como $n$ términos sumados con numeradores desconocidos, siendo $n$ la cantidad de factores en los que expresamos $g(x)$.
4. Hacemos denominador común con todos los términos e igualamos los coeficientes del polinomio numerador original con los numeradores desconocidos.
5. Resolvemos el sistema para hallar los valores de dichos numeradores.
6. Hallamos las primitivas de los nuevos términos, que ahora consisten en funciones más sencillas que sabemos integrar.

Existe otro método para hallar $A_{1}, \dots, A_{n}$, llamado el método de la "tapadita", el cual es más eficiente que resolver el sistema de la expresión en forma de denominador común.

Ahora, esto funciona cuando todas las raíces son distintas. Sin embargo, abordaremos un ejemplo con un caso así:

### Ejemplos
#### Ejemplo 1
$$
\int \frac{x^{2} + 2x + 3}{(x - 1)(x + 1)^{2}} \space dx
$$
Los factores simples se separan con normalidad. Sin embargo, ==cuando hay alguna raíz múltiple n-ésima, se agregan $n$ términos, cada uno con exponente mayor, hasta llegar a $n$==:
$$
\frac{x^{2} + 2x + 3}{(x - 1)(x + 1)^{2}} = \frac{A}{x - 1} + \frac{B}{x + 1} + \frac{C}{(x + 1)^{2}}
$$
En este caso, no haremos los cálculos para determinar $A, B, C$.
$$
\begin{align}
&A = \frac{3}{2} \\
&B = -\frac{1}{2} \\
&C = -1
\end{align}
$$
$$
\frac{x^{2} + 2x + 3}{(x - 1)(x + 1)^{2}} = \frac{\frac{3}{2}}{x - 1} - \frac{\frac{1}{2}}{x + 1} - \frac{1}{(x + 1)^{2}}
$$
De esta forma:
$$
\int \frac{x^{2} + 2x + 3}{(x - 1)(x + 1)^{2}} \space dx = \frac{3}{2} \int \frac{1}{x - 1} \space dx - \frac{1}{2} \int \frac{1}{x + 1} \space dx - \int \frac{1}{(x + 1)^{2}} \space dx
$$
Determinamos una primitiva de $\frac{1}{(x + 1)^{2}}$:
$$
\begin{align}
\int \frac{1}{(x + 1)^{2}} \space dx &= \int (x + 1)^{-2} \space dx \\
&\underbrace{ = }_{ \begin{aligned}
&u = x + 1 \\
&du = dx
\end{aligned} } \int (x + 1)^{-2} \space dx \\
&= \frac{u^{-2 + 1}}{-2 + 1} + C \\
&= \frac{(x + 1)^{-1}}{-1} \\
&= -\frac{1}{x + 1}
\end{align}
$$
En conclusión:
$$
\frac{3}{2} \int \frac{1}{x - 1} \space dx - \frac{1}{2} \int \frac{1}{x + 1} \space dx - \int \frac{1}{(x + 1)^{2}} \space dx = \frac{3}{2} \log(|x - 1|) - \frac{1}{2} \log(|x + 1|) + \frac{1}{x + 1}
$$

Este es otro ejemplo de DFS donde el denominador se descompone como el producto de las raíces, algunas de las cuales tienen multiplicidad mayor a uno.

De esta forma, vimos un ejemplo en el que el denominador tiene una raíz con multiplicidad diferente de 1. La única diferencia es como se expresa en forma de fracciones simples, que ya explicamos al comienzo.

Veremos otro ejemplo para que quede claro:

#### Ejemplo 2
$$
\int \frac{x^{5} - 7x^{3} + 4}{(x - 1) (x + 2)^{2} (x + 3)^{2}} \space dx
$$
Aplicando todo lo visto hasta ahora, descomponemos la expresión en fracciones simples:
$$
\frac{x^{5} - 7x^{3} + 4}{(x - 1) (x + 2)^{2} (x + 3)^{2}} = \frac{A}{x - 1} + \frac{B}{x + 2} + \frac{C}{(x + 2)^{2}} + \frac{D}{x + 3} + \frac{E}{(x + 3)^{2}} + \frac{F}{(x + 3)^{3}}
$$
Como vemos, cada factor elevado a la $n$ aporta $n$ sumandos.

El TDFS nos dice que vamos a poder hallar $A, B, C, \dots, F$ de forma que se verifique la ecuación.

En general, cada raíz del denominador va a aportar a la descomposición en fracciones simples tantos sumandos como su multiplicidad (es lo mismo que hemos dicho anteriormente).

¿Qué otras funciones pueden aparecer cuando descomponemos?

### Más fracciones simples

#### Caso 1
$$
\int \frac{1}{1 + x^{2}} \space dx = \arctan(x) + C
$$

#### Caso 2
$$
\begin{align}
\int \frac{1}{x^{2} + \beta^{2}} \space dx &= \int \frac{1}{\beta^{2}\left( \frac{x^{2}}{\beta^{2}} + 1 \right)} \space dx \\
&= \int \frac{1}{\beta^{2}\left( \left( \frac{x}{\beta} \right)^{2} + 1 \right)} \space dx \\
&= \beta \int \frac{\frac{dx}{\beta}}{\beta^{2}\left( \left( \frac{x}{\beta} \right)^{2} + 1 \right)} \\
&\underbrace{ = }_{ \begin{aligned}
&u = \frac{x}{\beta} \\
&du = \frac{dx}{b}
\end{aligned} } \frac{\beta}{\beta^{2}} \int \frac{du}{u^{2} + 1} \\
&= \frac{1}{\beta} \arctan(u) + C \\
&\underbrace{ = }_{ DCV } \frac{1}{\beta} \arctan\left( \frac{x}{\beta} \right) + C
\end{align}
$$

#### Caso 3
$$
\int \frac{1}{ax^{2} + bx + c} \space dx
$$
donde $(b^{2} - 4ac) < 0$ (no tiene raíces reales).

Por ejemplo:
$$
\int \frac{1}{x^{2} + x + 1} \space dx
$$
$1^{2} - 4 \cdot 1 \cdot 1 = -3$, por lo que no tiene raíces reales.
La idea es expresarlo de la siguiente forma:
$$
x^{2} + x + 1 = (x + a)^{2} + b
$$
siendo $a, b \in \mathbb{R}$.

Esta técnica se llama ==completar cuadrados==.

Analizando la estructura, y sabiendo que el cuadrado desarrollado es $x^{2} + 2a x + a^{2}$. Podemos expresarlo como:
$$
x^{2} + x + 1 = \underbrace{ \left( x + \frac{1}{2} \right)^{2} }_{ x^{2} + x + \frac{1}{4} } + \frac{3}{4}
$$
$a$ busca que el término intermedio sea correcto ($2a x$), sin preocuparse por el término independiente, mientras que $b$ agrega (o quita) lo que falta (o sobra) del termino independiente resultante de la expresión cuadrado. En general, podemos utilizar la siguiente fórmula:
$$
x^{2} + ax + b = \left( x + \frac{a}{2} \right)^{2} + \left( b - \frac{a^{2}}{4} \right)
$$
Igualmente, es más sencillo recordarlo cada vez, con ejemplos, en lugar de memorizar la fórmula.

Entonces:
$$
\begin{align}
\int \frac{1}{x^{2} + x + 1} \space dx &= \int \frac{1}{\left( x + \frac{1}{2} \right)^{2} + \frac{3}{4}} \space dx \\
&\underbrace{ = }_{ \begin{aligned}
&u = x + \frac{1}{2} \\
&du = dx
\end{aligned} } \int \frac{1}{u^{2} + \frac{3}{4}} \space dx
\end{align}
$$
Sabemos resolver esta integral, ya que tiene la misma estructura que $\int \frac{1}{x^{2} + \beta^{2}} \space dx$, con $\beta^{2} = \frac{3}{4}$. Entonces $\beta = \frac{\sqrt{ 3 }}{2}$.
$$
\begin{align}
\int \frac{1}{u^{2} + \frac{3}{4}} \space dx &= \frac{1}{\frac{\sqrt{ 3 }}{2}} \arctan\left( \frac{u}{\frac{\sqrt{ 3 }}{2}} \right) + C \\
&\underbrace{ = }_{ DCV } \frac{2}{\sqrt{ 3 }} \arctan\left( \frac{x + \frac{1}{2}}{\frac{\sqrt{ 3 }}{2}} \right) + C \\
&\underbrace{ = }_{ DCV } \frac{2}{\sqrt{ 3 }} \arctan\left( \frac{2x + 1}{{\sqrt{ 3 }}} \right) + C
\end{align}
$$
Entonces, cuando tenemos uno sobre un polinomio que no tiene raíces reales, tenemos que:
1. Completar cuadrados: pasar $x^{2} + ax + b$ a la forma $\left( x + \frac{a}{2} \right)^{2} + \left( b - \frac{a^{2}}{4} \right)$.
2. Realizar un cambio de variable, con lo que está dentro del cuadrado.
3. Trabajar con la integral $\int \frac{du}{u^{2} + \beta^{2}}$.

Observación:
Si el coeficiente principal $\alpha x^{2}$ no es 1 ($\alpha \neq 1$), dividimos todo entre $\alpha$ y multiplicamos la integral por $\frac{1}{\alpha}$.

#### Caso 4
$$
\int \frac{2x + 1}{x^{2} + x + 1} \space dx
$$
En este caso, el numerador es derivada del denominador. Aplicaremos sustitución:
$$
\begin{align}
\int \frac{2x + 1}{x^{2} + x + 1} \space dx &\underbrace{ = }_{ \begin{aligned}
&u = x^{2} + x + 1 \\
&du = (2x + 1) \space dx
\end{aligned} } \int \frac{du}{u} \\
&= \log(|u|) + C \\
&\underbrace{ = }_{ DCV } \log(|x^{2} + x + 1|) + C
\end{align}
$$

Continuamos abordando otros ejemplos:

### Ejemplos

#### Ejemplo 3
$$
\int \frac{3x^{2} + 2x - 2}{x^{3} - 1} \space dx
$$
¿Cómo se descompone el denominador?
$$
x^{3} - 1 = (x - 1)(x^{2} + x + 1)
$$
Ya vimos que $x^{2} + x + 1$ no tiene raíces reales. ¿Qué dice el teorema de fracciones simples en este caso?
Según el TDFS, podemos descomponer la fracción como:
$$
\frac{3x^{2} + 2x - 2}{(x - 1)(x^{2} + x + 1)} = \frac{A}{x - 1} + \frac{Bx + C}{x^{2} + x + 1}
$$
Como vemos, se suma otro término, pero en lugar de tener como numerador una constante, tiene otro polinomio de grado 1.

Ahora, resolvemos utilizando cualquiera de los métodos:
- Denominador común e igualar los polinomios del numerador coeficiente a coeficiente (camino más largo).
- Método de la "tapadita" (método más corto).

El resultado es:
$$
\begin{align}
&A = 1 \\
&B = 2 \\
&C = 3
\end{align}
$$
Calculamos la integral:
$$
\begin{align}
\int \frac{3x^{2} + 2x - 2}{(x - 1)(x^{2} + x + 1)} \space dx &= \int \frac{1}{x - 1} \space dx + \int \frac{2x + 3}{x^{2} + x + 1} \space dx
\end{align}
$$
Tenemos que integrar el segundo término:
$$
\int \frac{2x + 3}{x^{2} + x + 1} \space dx
$$
Nos gustaría aplicar el método de la derivada: $\int \frac{du}{u}$. Sin embargo, $(x^{2} + x + 1)' = 2x + 1 \neq 2x + 3$. Entonces, expresaremos el numerador como:
$$
2x + 3 = (2x + 1) + 2
$$

En general, cuando trabajamos con integrales de este tipo ($\int \frac{f(x)}{g(x)}$, donde $f(x) \sim g'(x)$), lo que buscamos es expresar el numerador como $f(x) = \alpha g'(x) + \beta$, siendo $\alpha, \beta$ valores constantes.

De esta forma:
$$
\int \frac{2x + 3}{x^{2} + x + 1} \space dx = \int \frac{2x + 1}{x^{2} + x + 1} \space dx + \int \frac{2}{x^{2} + x + 1} \space dx
$$
Ahora, resolvemos cada una por separado:
$$
\begin{align}
\int \frac{2x + 1}{x^{2} + x + 1} \space dx &\underbrace{ = }_{ \begin{aligned}
&u = x^{2} + x + 1 \\
&du = (2x + 1) dx
\end{aligned} } \int \frac{du}{u} \\
&= \log(|u|) + C \\
&\underbrace{ = }_{ DCV } \log(|x^{2} + x + 1|) + C
\end{align}
$$
$$
\begin{align}
\int \frac{2}{x^{2} + x + 1} \space dx &= 2\int \frac{1}{x^{2} + x + 1} \space dx \\
&= 2 \cdot \left[ \frac{2}{\sqrt{ 3 }} \arctan\left( \frac{2x + 1}{{\sqrt{ 3 }}} \right) \right] + C \\
&= \frac{4}{\sqrt{ 3 }} \arctan\left( \frac{2x + 1}{{\sqrt{ 3 }}} \right) + C
\end{align}
$$

Finalmente, sustituimos los valores calculados en la ecuación original:
$$
\begin{align}
\int \frac{3x^{2} + 2x - 2}{(x - 1)(x^{2} + x + 1)} \space dx &= \int \frac{1}{x - 1} \space dx + \int \frac{2x + 1}{x^{2} + x + 1} \space dx + \int \frac{2}{x^{2} + x + 1} \space dx \\
&= \log(|x - 1|) + \log(|x^{2} + x + 1|) + \frac{4}{\sqrt{ 3 }} \arctan\left( \frac{2x + 1}{{\sqrt{ 3 }}} \right) + C
\end{align}
$$

Concluiremos viendo un último ejemplo:

#### Ejemplo 4
$$
\int \frac{4x + 5}{x^{2} + 2x + 4} \space dx
$$
Como el numerador tiene menor grado que el denominador podemos proseguir con normalidad. Sin embargo, el denominador no tiene raíces reales: $2^{2} - 4 \cdot 1 \cdot 4 = -12 < 0$.

En este caso, tenemos que (nuevamente) dividir el problema en dos: una mitad que se resuelva por sustitución, y la otra completando con cuadrados y arco tangente.

Primero, escribimos el numerador tomando en cuenta la derivada del denominador:
$$
(x^{2} + 2x + 4)' = 2x + 2
$$
$$
4x + 5 = A(2x + 2) + B \implies \begin{cases}
A = 2 \\
B = 1
\end{cases}
$$
De esta forma:
$$
4x + 5 = 2(2x + 2) + 1
$$
Entonces:
$$
\int \frac{4x + 5}{x^{2} + 2x + 4} \space dx = 2\int \frac{2x + 2}{x^{2} + 2x + 4} \space dx + \int \frac{1}{x^{2} + 2x + 4} \space dx
$$

Resolvemos las integrales por separado:
- Término 1 (sustitución):
$$
\begin{align}
2\int \frac{2x + 2}{x^{2} + 2x + 4} \space dx &\underbrace{ = }_{ \begin{aligned}
&u = x^{2} + 2x + 4 \\
&du = 2x + 2
\end{aligned} } 2\int \frac{du}{u} \\
&= 2\log(|u|) + C \\
&\underbrace{ = }_{ DCV } 2\log(|x^{2} + 2x + 4|) + C
\end{align}
$$
- Término 2 (completar cuadrados):
$$
\begin{align}
\int \frac{1}{x^{2} + 2x + 4} \space dx &= \int \frac{1}{(x + 1)^{2} + 3} \space dx \\
&\underbrace{ = }_{ \begin{aligned}
&u = x + 1 \\
&du = dx
\end{aligned} } \int \frac{du}{(u)^{2} + 3} \\
&= \int \frac{du}{u^{2} + (\sqrt{ 3 })^{2}} \\
&= \int \frac{du}{(\sqrt{ 3 })^{2}\left( \frac{u^{2}}{(\sqrt{ 3 })^{2}} + 1 \right)} \\
&= \int \frac{du}{(\sqrt{ 3 })^{2}\left( \left( \frac{u}{\sqrt{ 3 }} \right)^{2} + 1 \right)} \\
&= \sqrt{ 3 } \int \frac{\frac{du}{\sqrt{ 3 }}}{(\sqrt{ 3 })^{2}\left( \left( \frac{u}{\sqrt{ 3 }} \right)^{2} + 1 \right)} \\
&= \frac{\sqrt{ 3 }}{3} \int \frac{\frac{du}{\sqrt{ 3 }}}{\left( \left( \frac{u}{\sqrt{ 3 }} \right)^{2} + 1 \right)} \\
&= \frac{\sqrt{ 3 }}{3} \arctan\left( \frac{u}{\sqrt{ 3 }} \right) + C \\
&\underbrace{ = }_{ DCV } \frac{1}{\sqrt{ 3 }} \arctan\left( \frac{x + 1}{\sqrt{ 3 }} \right) + C
\end{align}
$$

Ahora, sustituimos los resultados:
$$
\begin{align}
\int \frac{4x + 5}{x^{2} + 2x + 4} \space dx &= 2\int \frac{2x + 2}{x^{2} + 2x + 4} \space dx + \int \frac{1}{x^{2} + 2x + 4} \space dx \\
&= 2\log(|x^{2} + 2x + 4|) + \frac{\sqrt{ 3 }}{3} \arctan\left( \frac{x + 1}{\sqrt{ 3 }} \right) + C
\end{align}
$$

ACLARACIÓN: Una forma más sencilla de ver la técnica de completar cuadrados:
$$
\int \frac{1}{u^{2} + a^{2}} \space du = \frac{1}{a} \arctan\left( \frac{u}{a} \right) + C
$$

Para concluir, veremos un caso general, con necesidad de aplicar múltiples métodos:
#### Ejemplo 5
$$
\int \frac{7x^{4} - 3x^{2} + 7}{(x - 1) (x + 2)^{2} (x^{2} + x + 1) (x^{2} + 7)}
$$
Donde $x^{2} + x + 1$ y $x^{2} + 7$ no tienen raíces reales.

Descomponemos en fracciones simples
$$
\frac{7x^{4} - 3x^{2} + 7}{(x - 1) (x + 2)^{2} (x^{2} + x + 1) (x^{2} + 7)} = \frac{A}{x - 1} + \frac{B}{x + 2} + \frac{C}{(x + 2)^{2}} + \frac{Dx + E}{x^{2} + x + 1} + \frac{Fx + G}{x^{2} + 7}
$$

Ahora, hay que realizar un paso más con los últimos dos términos (que tienen como numerador un polinomio de primer grado). Básicamente, hay que hacer aparecer la derivada del denominador, considerando los valores del numerador:
$$
\begin{align}
&\frac{Dx + E}{x^{2} + x + 1} = \frac{H(2x + 1)}{x^{2} + x + 1} + \frac{I}{x^{2} + x + 1} \\
&\frac{Fx + G}{x^{2} + 7} = \frac{J(2x)}{x^{2} + 7} + \frac{K}{x^{2} + 7}
\end{align}
$$
Luego, los primeros tres términos son funciones sencillas que ya sabemos integrar, y los últimos dos se dividen en otros dos términos, los cuales se resuelven mediante métodos diferentes:
- $\frac{H(2x + 1)}{x^{2} + x + 1}$ y $\frac{J(2x)}{x^{2} + 7}$ se calculan por sustitución, quedando $H \int \frac{2x + 1}{x^{2} + x + 1} \space dx = H \log(|x^{2} + x + 1|) + C$ y $J \int \frac{2x}{x^{2} + 7} \space dx = J \log(|x^{2} + 7|) + C$.
- $\frac{I}{x^{2} + x + 1}$ y $\frac{K}{x^{2} + 7}$ se calculan al completar el cuadrado, quedando
$$
\begin{align}
\int \frac{I}{x^{2} + x + 1} \space dx &= I \int \frac{1}{\left( x + \frac{1}{2} \right)^{2} + \frac{3}{4}} \space dx \\
&= I \int \frac{1}{\left( x + \frac{1}{2} \right)^{2} + \left( \frac{\sqrt{ 3 }}{2} \right)^{2}} \space dx \\
&\underbrace{ = }_{ \begin{aligned}
&u = x + \frac{1}{2} \\
&du = dx
\end{aligned} } I \int \frac{du}{u^{2} + \left( \frac{\sqrt{ 3 }}{2} \right)^{2}} \\
&= I \int \frac{du}{\left( \frac{\sqrt{ 3 }}{2} \right)^{2} \left( \frac{u^{2}}{\left( \frac{\sqrt{ 3 }}{2} \right)^{2}} + 1 \right)} \\
&= I \int \frac{du}{\left( \frac{\sqrt{ 3 }}{2} \right)^{2} \left( \left( \frac{u}{\frac{\sqrt{ 3 }}{2}} \right)^{2} + 1 \right)} \\
&= I \cdot \frac{\sqrt{ 3 }}{2} \int \frac{\frac{du}{\frac{\sqrt{ 3 }}{2}}}{\left( \frac{\sqrt{ 3 }}{2} \right)^{2} \left( \left( \frac{u}{\frac{\sqrt{ 3 }}{2}} \right)^{2} + 1 \right)} \\
&= I \cdot \frac{\frac{\sqrt{ 3 }}{2}}{\left( \frac{\sqrt{ 3 }}{2} \right)^{2}} \int \frac{\frac{du}{\frac{\sqrt{ 3 }}{2}}}{ \left( \frac{u}{\frac{\sqrt{ 3 }}{2}} \right)^{2} + 1} \\
&= I \cdot \frac{\frac{\sqrt{ 3 }}{2}}{\left( \frac{\sqrt{ 3 }}{2} \right)^{2}} \cdot \arctan\left( \frac{u}{\frac{\sqrt{ 3 }}{2}} \right) + C \\
&= I \cdot \frac{1}{\frac{\sqrt{ 3 }}{2}} \cdot \arctan\left( \frac{u}{\frac{\sqrt{ 3 }}{2}} \right) + C \\
&= I \cdot \frac{2}{\sqrt{ 3 }} \cdot \arctan\left( \frac{2u}{\sqrt{ 3 }} \right) + C \\
&\underbrace{ = }_{ DCV } I \cdot \frac{2}{\sqrt{ 3 }} \cdot \arctan\left( \frac{2(x + \frac{1}{2})}{\sqrt{ 3 }} \right) + C \\
&= I \cdot \frac{2}{\sqrt{ 3 }} \cdot \arctan\left( \frac{2x + 1}{\sqrt{ 3 }} \right) + C
\end{align}
$$
Por el mismo mecanismo se calcula $\frac{K}{x^{2} + 7}$.


Esto solo funciona si no tienen raíces reales. En caso contrario, hay que factorizarla conociendo sus raíces.

La próxima clase, concluiremos con el tema, abordando el último caso de fracciones simples, donde el denominador es algo más complejo que el del último ejemplo.