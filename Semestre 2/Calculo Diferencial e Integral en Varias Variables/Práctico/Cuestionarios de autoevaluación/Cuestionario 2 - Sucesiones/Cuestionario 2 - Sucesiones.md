# Ejercicio 1
Sea $a_{n}$ una sucesión de números reales. La única opción verdadera en todos los casos es: si $a_{n}$ es convergente entonces está acotada.

---
# Ejercicio 2
Sea $(a_{n})$ una sucesión de términos positivos. Sabemos que: 
- $a_{2n}$ es acotada.
- $a_{2n + 1}$ no converge y es acotada. 

Considere las siguientes afirmaciones:
1. $a_{n}$ no puede converger.
2. $a_{2n + 1}$ tiene una subsucesión convergente.
3. $a_{4n}$ es necesariamente convergente.
4. $a_{3n}$ no puede converger.  

(1) es ==verdadera==, ya que si convergiera, entonces todas sus subsucesiones serían convergentes (y convergerían a lo mismo).

(2) es ==verdadera==, ya que si una sucesión es acotada, entonces necesariamente tiene al menos una subsucesión convergente (el teorema correspondiente se demuestra utilizando el teorema de Bolzano-Weierstrass).

(3) es ==falso==. Que $a_{2n}$ sea acotada implica que alguna subsucesión es convergente, pero no tiene porque ser $a_{4n}$.

(4) es ==falso==. No podemos confirmar que la sucesión $a_{3n}$ no converja, ya que está construida con elementos de $a_{2n}$ que es acotada, y $a_{2n + 1}$ que también es acotada y, aunque no converge, no se comporta igual, ya que no coincide en todos sus elementos.

OBSERVACIÓN: Puede ser de gran ayuda construir ejemplos ficticios (sin fórmula) a mano.

---
# Ejercicio 3
Considere $a \geq 0$ y $(a_{n})$ una sucesión definida por recurrencia:
$$
\begin{cases}
a_{1} = a \\
a_{n + 1}=a^{2}_{n}
\end{cases}
$$

$a_{n} = (a, a^{2}, a^{4}, a^{8}, a^{16}, \dots, a^{2^{n - 1}})$

De esta forma, podemos distinguir los siguientes comportamientos:
- Si $0 \leq a < 1$, entonces la sucesión converge a 0.
- Si $a = 1$, entonces la sucesión converge a 1.
- Si $a > 1$, entonces la sucesión diverge.

---
# Ejercicio 4
$\lim_{ n \to \infty } a_{n} = 4$ si:
1. Existe $\epsilon > 0$ y $n_{0}$ tal que si $n > n_{0}$ se verifica que $|a_{n} − 4| < \epsilon$
2. Para todo $\epsilon > 0$ existe $n_{0} \in \mathbb{N}$ que verifica que $|a_{n}| < \epsilon$ para todo $n > n_{0}$
3. Para todo $\epsilon > 0$ y para todo $n \in \mathbb{N}$ se verifica que $|a_{n} − 4| < \epsilon$
4. Para todo $\epsilon > 0$ existe $n_{0}$ tal que si $n > n_{0}$ se verifica que $|a_{n} − 4| < \epsilon$

(1) Queda descartado, puesto que la condición tiene que cumplirse $\forall \epsilon > 0$, no para uno solo.

(2) En este caso, el límite no sería 4, sino 0 (tendría que verificarse $|a_{n} − 4| < \epsilon$, no $|a_{n}| < \epsilon$).

(3) La igualdad solo se cumple si $a_{n} = 4$, sucesión que efectivamente converge a 4, pero no es la única.

(4) La definición de límite, adaptada para corresponderse con $L = 4$. Lo importante es que la desigualdad se verifique en el infinito, no para todos los valores (como en (3)).

Entonces, la opción correcta es la ==4==.

---
# Ejercicio 5
La sucesión $a_{n} = \frac{(−1)^{n} + 3}{n^{2}}$:

1. Está acotada.
2. Es monótona creciente.
3. No tiene límite, pues oscila.
4. Es monótona decreciente.

Podemos ver que el numerador oscila entre 2 (cuando $n$ es par) y 4 (cuando $n$ es impar), mientras que el numerador tiende a infinito. Por lo tanto, podemos confirmar que la sucesión converge a 0 ((==3 es falsa==)), por lo que está acotada ((==1 es verdadera==)), aunque no es monótona decreciente (basta con estudiar los primeros valores: $a_{3} = \frac{2}{9}$, $a_{4} = \frac{2}{8}$, $a_{4} > a_{3}$ ((==4 es falsa==))). Y definitivamente no es monótona creciente, pues basta ver que comienza con $a_{1} = 4$ y converge a 0 ((==2 es falsa==)).


