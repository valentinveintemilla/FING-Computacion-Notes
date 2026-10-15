# 1 - Ejercicios del práctico
## Ejercicio 1
### Conjunto $A_{1}$:
El conjunto $A_{1}$ se representa en $\mathbb{R}^{2}$ como:
![[Semestre 2/Calculo Diferencial e Integral en Varias Variables/Práctico/Práctico 5 - Topología en Rn/Imágenes/Ejercicio 1 - Conjunto A1.png]]



### Conjunto $B = A_{1} \cap \mathbb{Q}$:
El conjunto $B$ se representa en $\mathbb{R}^{2}$ como:
![[Semestre 2/Calculo Diferencial e Integral en Varias Variables/Práctico/Práctico 5 - Topología en Rn/Imágenes/Ejercicio 1 - Conjunto B.png]]



### Conjunto $A_{2}$:
El conjunto $A_{2}$ se representa en $\mathbb{R}^{2}$ como:
![[Semestre 2/Calculo Diferencial e Integral en Varias Variables/Práctico/Práctico 5 - Topología en Rn/Imágenes/Ejercicio 1 - Conjunto A2.png]]



### Conjunto $A_{3}$:
El conjunto $A_{3}$ se representa en $\mathbb{R}^{2}$ como:
![[Semestre 2/Calculo Diferencial e Integral en Varias Variables/Práctico/Práctico 5 - Topología en Rn/Imágenes/Ejercicio 1 - Conjunto A3.png]]





---
## Ejercicio 2
### Parte a
Sea $B(a, \delta) = \{ x \in \mathbb{R}^{n} : d(x, a) < \delta \}$ una bola abierta genérica, tenemos que probar que todos los puntos de $B(a, \delta)$ son interiores. Para esto, consideramos un punto genérico $p \in B(a, \delta)$, y determinemos una bola $B(p, \delta')$ tal que $B(p, \delta') \subset B(a, \delta)$. El problema consiste encontrar el valor de $\delta'$:

Sabemos que $\delta'$ puede ser como máximo la distancia de $p$ al borde de la bola $B(a, \delta)$, puesto que si fuera mayor, la bola $B(p, \delta')$ tendría elementos fuera de $B(a, \delta)$ y no se cumpliría la inclusión. Entonces, necesariamente $d(p, a) + \delta' \leq \delta$, por lo que podemos considerar $\delta' = \delta - d(p, a)$.

Verifiquemos que el $\delta'$ elegido satisface la inclusión: consideramos un punto genérico $x \in B(p, \delta')$ y comprobemos que efectivamente se encuentra en $B(a, \delta)$. Para esto, utilizaremos la desigualdad triangular:
$$
\underbrace{ d(a, x) \leq d(a, p) + d(p, x) }_{ \text{Desigualdad triangular} } < d(a, p) + \delta' = \delta
$$

En conclusión, como se verifica $d(a, x) < \delta$, comprobamos que $\forall x \in B(p, \delta')$ se cumple que $x \in B(a, \delta)$, por lo que necesariamente $B(p, \delta') \subset B(a, \delta)$.

### Parte b
Sabemos que $A$ es abierto, lo que significa que todos los puntos de $A$ son interiores: $\forall x \in A$, $\exists \delta \in \mathbb{R}^{+}$ tal que $B(x, \delta) \subset A$. Como $p \in A$, entonces $\exists \delta \in \mathbb{R}^{+}$ tal que $B(p, \delta) \subset A$.

Tenemos que probar que el conjunto $A - p$ mantiene también es abierto, lo que implica que quitar un punto (o una cantidad finita de puntos) de un conjunto abierto no afecta a su calidad de abierto:
Sea $x \in A - p$. Queremos probar que $\exists \delta \in \mathbb{R}^{+}$ tal que $B(x, \delta) \subset A$. Basta considerar un $\delta$ que verifique que:
$$
\begin{align}
&p \not \in B(x, \delta) \\
&B(x, \delta) \subset A
\end{align} \implies B(x, \delta) \subset A - \{ p \}
$$

Por esta razón, es importante establecer un $\delta$ que sea el mínimo entre la distancia de $x$ a $p$, y la distancia al borde más cercano de $A$. Podemos aprovechar que $A$ es abierto para determinar dicha distancia, sabiendo que $x \in A - p \subset A \implies x \in A$. Entonces, existe una distancia "segura" al borde más cercano $\delta'$, tal que $B(x, \delta') \subset A$.

Habiendo dicho esto, podemos considerar $\delta = \min \{ d(x, p), \delta' \}$. Por construcción, sabemos que se verifican las dos condiciones mencionadas:
- Como $\delta \leq \delta'$, podemos confirmar que $B(x, \delta) \subset A$.
- Como $\delta \leq d(x, p)$, podemos confirmar que $p \not \in B(x, \delta)$.
Entonces, se verifica $B(x, \delta) \subset A - \{ p \}$.

En conclusión, $A - p$ también es abierto.
