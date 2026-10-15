# Ejercicio 1
Sea $a_{n}$ una sucesión de términos positivos. 

Si  $\sum_{n = 1}^{+\infty} \frac{a_{n}}{1 + a_{n}}$ converge, ¿Entonces $\sum_{n = 1}^{+\infty} a_{n}$ converge?

Si $\frac{a_{n}}{1 + a_{n}}$ converge, esto significa que $\lim_{ n \to +\infty } \frac{a_{n}}{1 + a_{n}} = \frac{1}{\frac{1}{a_{n}} + 1} = 0$.

Por lo tanto, $\lim_{ n \to +\infty } a_{n} = 0$.

Intentamos aplicar el criterio de equivalentes
$$
\frac{a_{n}}{\frac{a_{n}}{1 + a_{n}}} = \frac{a_{n} \cdot (1 + a_{n})}{a_{n}} = \frac{a_{n} + a_{n}^{2}}{a_{n}} = 1 + a_{n}
$$

Ahora, analizamos el límite:
$$
\lim_{ n \to +\infty } a_{n} + 1 = 0 + 1 = 1
$$

De esta forma, $\lim_{ n \to +\infty } \frac{a_{n}}{\frac{a_{n}}{1 + a_{n}}} > 0$, por lo que los dos series son de la misma clase.

En conclusión, $\sum_{n = 1}^{+\infty} a_{n}$ es convergente.

---
# Ejercicio 2
Sean $a_{n}$ y $b_{n}$ sucesiones de términos positivos tal que la sucesión $b_{n}$ está acotada. Definimos $c_{n} = \frac{a_{n}}{b_{n}}$. Considere las siguientes afirmaciones:

1. Si $\sum_{n = 1}^{+\infty} c_{n}$ converge, entonces $\sum_{n = 1}^{+\infty} b_{n}$ converge.
2. Si $\sum_{n = 1}^{+\infty} c_{n}$ converge, entonces $\sum_{n = 1}^{+\infty} a_{n}$ converge.
3. Si la sucesión $c_{n}$ converge a cero y $\sum_{n = 1}^{+\infty} b_{n}$ converge, entonces $\sum_{n = 1}^{+\infty} a_{n}$ converge.

(1) Es ==falso==. Contraejemplo:
$b_{n} = 1$, $a_{n} = \frac{1}{n^{2}}$.

En este caso, $c_{n} = \frac{\frac{1}{n^{2}}}{1} = \frac{1}{n^{2}}$, por lo que $\sum_{n = 1}^{+\infty} c_{n}$ converge. Sin embargo, $\sum_{n = 1}^{+\infty} b_{n}$ diverge.

(2) Es ==verdadera==. Si $\sum_{n = 1}^{+\infty} c_{n} = \sum_{n = 1}^{+\infty} \frac{a_{n}}{b_{n}}$ converge, y considerando que $b_{n}$ está acotada, significa que $b_{n}$ crece (o decrece), hasta cierto punto. Por lo tanto, necesariamente $\sum_{n = 1}^{+\infty} a_{n}$ tiene que converger. Además, si chequeamos la definición de $c_{n} = \frac{a_{n}}{b_{n}}$, esto indica que $a_{n}$ decrece muchísimo más rápido de lo que $b_{n}$ lo hace, por lo que la convergencia está dada por $a_{n}$ (ya que $b_{n}$ está acotada, si no estuviera acotada $a_{n}$ no tendría por que converger).

(3) Es ==verdadera==, ya que se corresponde con el segundo punto del criterio de equivalentes:

Sean $\sum a_{n}$ y $\sum b_{n}$ dos series de términos positivos, tal que $\lim_{ n \to +\infty } \frac{a_{n}}{b_{n}} = \lim_{ n \to +\infty } c_{n} = L$, entonces:
- Si $L > 0$, $\sum a_{n}$ y $\sum b_{n}$ son de la misma clase.
- Si $L = 0$ y $\sum b_{n}$ es convergente, entonces $\sum a_{n}$ es convergente.

---
# Ejercicio 3
La serie
$$
\sum_{n = 2}^{+\infty} \frac{(-1)^{n} \log(n)}{n}
$$

En este caso, aplicaremos el criterio de Leibnitz:
Sea $a_{n}$ una sucesión monótona decreciente que tiende a 0, entonces la serie alternada $\sum (-1)^{n} a_{n}$ es convergente.

En este caso, $\frac{\log(n)}{n}$ es efectivamente una serie monótona decreciente (o al menos a partir de un $n_{0}$ determinado), y es positiva durante todo su intervalo, ya que $n > 0$ y $\log(n) > 0$, $\forall n \geq 2$, podemos aplicar el criterio:

La serie $\sum_{n = 2}^{+\infty} \frac{(-1)^{n} \log(n)}{n}$ es convergente.

Sin embargo, no converge absolutamente, ya que:
$$
\sum_{n = 2}^{+\infty} \frac{\log(n)}{n} \geq \sum_{n = 2}^{+\infty} \frac{1}{n}
$$
y es bien sabido que $\sum_{n = 2}^{+\infty} \frac{1}{n}$ es divergente.

---
# Ejercicio 4
Sea $a_{n}$ una sucesión de números reales no negativos  y $A_{n} = a_{1} + \dots + a_{n}$ la reducida enésima.

Lo único que sabemos de la reducida enésima es que necesariamente tiene límite (aunque puede no ser finito), ya que como la sucesión es de reales no negativos, no puede oscilar.

No tenemos seguridad de que sea convergente, ni tampoco de que esté acotada (pudiendo darse si $\lim_{ n \to +\infty } a_{n} > 0$)

En caso de converger, necesariamente tiene que cumplirse que $\lim_{ n \to +\infty } a_{n} = 0$.