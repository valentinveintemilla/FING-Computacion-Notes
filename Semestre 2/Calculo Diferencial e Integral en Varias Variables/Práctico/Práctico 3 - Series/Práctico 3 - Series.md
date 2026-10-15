# Ejercicios del práctico
## Ejercicio 1
En este caso, lo que haremos será estudiar el término general de la serie (la sucesión "interior"), y verificar que la misma converja a 0. En caso de no hacerlo, sabemos que las series no son convergentes.
### Parte a
$$
\sum_{n = 0}^{+\infty} \left( \frac{1}{3} \right)^{n}
$$
$$
\lim_{ n \to \infty } \left( \frac{1}{3} \right)^{n}  = \lim_{ n \to \infty } \frac{1}{3^{n}}
$$
$$
\begin{align}
\frac{1}{n^{n}} &\leq \frac{1}{3^{n}} \leq \frac{1}{n} \\
\lim_{ n \to \infty } \frac{1}{n^{n}} &\leq \lim_{ n \to \infty } \frac{1}{3^{n}} \leq \lim_{ n \to \infty } \frac{1}{n} \\
\lim_{ n \to \infty } \frac{1}{n} \cdot \frac{1}{n} \cdot \dots \cdot \frac{1}{n} &\leq \lim_{ n \to \infty } \frac{1}{3^{n}} \leq \lim_{ n \to \infty } \frac{1}{n} \\
\lim_{ n \to \infty } \frac{1}{n} \cdot \lim_{ n \to \infty } \frac{1}{n} \cdot \dots \cdot \lim_{ n \to \infty } \frac{1}{n} &\leq \lim_{ n \to \infty } \frac{1}{3^{n}} \leq \lim_{ n \to \infty } \frac{1}{n} \\
0 \cdot 0 \cdot \dots \cdot 0 &\leq \lim_{ n \to \infty } \frac{1}{3^{n}} \leq 0 \\
0 &\leq \lim_{ n \to \infty } \frac{1}{3^{n}} \leq 0 \implies \lim_{ n \to \infty } \left( \frac{1}{3} \right)^{n} = 0
\end{align}
$$

Ahora, estudiamos la reducida enésima:
$$
\sum_{n = 0}^{N} \left( \frac{1}{3} \right)^{n} = \text{?}
$$
$$
\begin{align}
\sum_{n = 1}^{N + 1} \left( \frac{1}{3} \right)^{n} - \sum_{n = 0}^{N} \left( \frac{1}{3} \right)^{n} = &\cancel{ \frac{1}{3} } + \cancel{ \frac{1}{3^{2}} } + \cancel{ \frac{1}{3^{3}} } + \dots + \cancel{ \frac{1}{3^{N}} } + \frac{1}{3^{N + 1}} \\
&- \left( 1 + \cancel{ \frac{1}{3} } + \cancel{ \frac{1}{3^{2}} } + \cancel{ \frac{1}{3^{3}} } + \dots + \cancel{ \frac{1}{3^{N}} } \right) \\
= &\frac{1}{3^{N + 1}} - 1
\end{align}
$$
Si seguimos analizando la misma expresión:
$$
\begin{align}
\sum_{n = 1}^{N + 1} \left( \frac{1}{3} \right)^{n} - \sum_{n = 0}^{N} \left( \frac{1}{3} \right)^{n} &= \sum_{n = 0}^{N} \left( \frac{1}{3} \right)^{n + 1} - \sum_{n = 0}^{N} \left( \frac{1}{3} \right)^{n} \\
&= \sum_{n = 0}^{N} \left( \frac{1}{3} \right)^{n + 1} - \left( \frac{1}{3} \right)^{n} \\
&= \sum_{n = 0}^{N} \left( \frac{1}{3} \right)^{n} \left( \frac{1}{3} - 1 \right) \\
&= \left( \frac{1}{3} - 1 \right) \cdot \sum_{n = 0}^{N} \left( \frac{1}{3} \right)^{n}
\end{align}
$$
Ahora, uniendo los resultados:
$$
\begin{align}
\left( \frac{1}{3} - 1 \right) \cdot \sum_{n = 0}^{N} \left( \frac{1}{3} \right)^{n} &= \frac{1}{3^{N + 1}} - 1 \\
\left( 1 - \frac{1}{3} \right) \cdot \sum_{n = 0}^{N} \left( \frac{1}{3} \right)^{n} &= 1 - \frac{1}{3^{N + 1}} \\
\sum_{n = 0}^{N} \left( \frac{1}{3} \right)^{n} &= \frac{1 - \frac{1}{3^{N + 1}}}{1 - \frac{1}{3}}
\end{align}
$$
Finalmente, encontramos una igualdad que podemos manejar con facilidad. Ahora, queda estudiar el límite de la serie:
$$
\begin{align}
\sum_{n = 0}^{+\infty} \left( \frac{1}{3} \right)^{n} &= \lim_{ N \to \infty } \frac{1 - \frac{1}{3^{N + 1}}}{1 - \frac{1}{3}} \\
&= \frac{\lim_{ N \to \infty } 1 - \lim_{ N \to \infty } \frac{1}{3^{N + 1}}}{ \lim_{ N \to \infty } 1 - \lim_{ N \to \infty } \frac{1}{3} } \\
&= \frac{1 - 0}{ 1 - \frac{1}{3} } \\
&= \frac{1}{ \frac{2}{3} } \\
&= 1 \cdot \frac{3}{2} \\
&= \frac{3}{2}
\end{align}
$$

En conclusión:
$$
\sum_{n = 0}^{+\infty} \left( \frac{1}{3} \right)^{n} = \frac{3}{2}
$$

### Parte b
$$
\sum_{n = 1}^{+\infty} \left( \frac{1}{\sqrt{ 3 }} \right)^{n + 3}
$$
$$
\lim_{ n \to \infty } \left( \frac{1}{\sqrt{ 3 }} \right)^{n + 3} \leq \lim_{ n \to \infty } \left( \frac{1}{\sqrt{ 3 }} \right)^{n} = \lim_{ n \to \infty } \frac{1}{(\sqrt{ 3 })^{n}}
$$
$$
\begin{align}
\frac{1}{n^{n}} &\leq \frac{1}{(\sqrt{ 3 })^{n}} \leq \frac{1}{3^{n}} \\
\lim_{ n \to \infty } \frac{1}{n^{n}} &\leq \lim_{ n \to \infty } \frac{1}{(\sqrt{ 3 })^{n}} \leq \lim_{ n \to \infty } \frac{1}{3^{n}} \\
0 &\leq \lim_{ n \to \infty } \frac{1}{(\sqrt{ 3 })^{n}} \leq 0 \implies \lim_{ n \to \infty } \frac{1}{(\sqrt{ 3 })^{n}} = 0 \implies \lim_{ n \to \infty } \left( \frac{1}{\sqrt{ 3 }} \right)^{n + 3} = 0
\end{align}
$$

Ahora, proseguimos a analizar la reducida enésima:
$$
\begin{align}
\sum_{n = 2}^{N + 1} \left( \frac{1}{\sqrt{ 3 }} \right)^{n + 3} - \sum_{n = 1}^{N} \left( \frac{1}{\sqrt{ 3 }} \right)^{n + 3} = &\cancel{ \left( \frac{1}{\sqrt{ 3 }} \right)^{5} } + \cancel{ \left( \frac{1}{\sqrt{ 3 }} \right)^{6} } + \dots + \cancel{ \left( \frac{1}{\sqrt{ 3 }} \right)^{N + 3} } + \left( \frac{1}{\sqrt{ 3 }} \right)^{N + 4} \\
&- \left( \left( \frac{1}{\sqrt{ 3 }} \right)^{4} + \cancel{ \left( \frac{1}{\sqrt{ 3 }} \right)^{5} } + \cancel{ \left( \frac{1}{\sqrt{ 3 }} \right)^{6} } + \dots + \cancel{ \left( \frac{1}{\sqrt{ 3 }} \right)^{N + 3} } \right) \\
= &\left( \frac{1}{\sqrt{ 3 }} \right)^{N + 4} - \left( \frac{1}{\sqrt{ 3 }} \right)^{4}
\end{align}
$$

Además:
$$
\begin{align}
\sum_{n = 2}^{N + 1} \left( \frac{1}{\sqrt{ 3 }} \right)^{n + 3} - \sum_{n = 1}^{N} \left( \frac{1}{\sqrt{ 3 }} \right)^{n + 3} &= \sum_{n = 1}^{N} \left( \frac{1}{\sqrt{ 3 }} \right)^{n + 4} - \sum_{n = 1}^{N} \left( \frac{1}{\sqrt{ 3 }} \right)^{n + 3} \\
&= \sum_{n = 1}^{N} \left( \frac{1}{\sqrt{ 3 }} \right)^{n + 4} - \left( \frac{1}{\sqrt{ 3 }} \right)^{n + 3} \\
&= \sum_{n = 1}^{N} \left( \frac{1}{\sqrt{ 3 }} \right)^{n + 3} \cdot \left( \frac{1}{\sqrt{ 3 }} - 1 \right) \\
&= \left( \frac{1}{\sqrt{ 3 }} - 1 \right) \cdot \sum_{n = 1}^{N} \left( \frac{1}{\sqrt{ 3 }} \right)^{n + 3}
\end{align}
$$
Ahora, igualamos ambas expresiones:
$$
\begin{align}
\left( \frac{1}{\sqrt{ 3 }} - 1 \right) \cdot \sum_{n = 1}^{N} \left( \frac{1}{\sqrt{ 3 }} \right)^{n + 3} &= \left( \frac{1}{\sqrt{ 3 }} \right)^{N + 4} - \left( \frac{1}{\sqrt{ 3 }} \right)^{4} \\
\left( 1 - \frac{1}{\sqrt{ 3 }} \right) \cdot \sum_{n = 1}^{N} \left( \frac{1}{\sqrt{ 3 }} \right)^{n + 3} &= \left( \frac{1}{\sqrt{ 3 }} \right)^{4} - \left( \frac{1}{\sqrt{ 3 }} \right)^{N + 4} \\
\sum_{n = 1}^{N} \left( \frac{1}{\sqrt{ 3 }} \right)^{n + 3} &= \frac{\left( \frac{1}{\sqrt{ 3 }} \right)^{4} - \left( \frac{1}{\sqrt{ 3 }} \right)^{N + 4}}{1 - \frac{1}{\sqrt{ 3 }}}
\end{align}
$$
Finalmente, calculamos la suma:
$$
\begin{align}
\sum_{n = 1}^{+\infty} \left( \frac{1}{\sqrt{ 3 }} \right)^{n + 3} &= \lim_{ N \to \infty } \frac{\left( \frac{1}{\sqrt{ 3 }} \right)^{4} - \left( \frac{1}{\sqrt{ 3 }} \right)^{N + 4}}{1 - \frac{1}{\sqrt{ 3 }}} \\
&= \frac{\left( \lim_{ N \to \infty } \frac{1}{\sqrt{ 3 }} \right)^{4} - \lim_{ N \to \infty } \left( \frac{1}{\sqrt{ 3 }} \right)^{N + 4}}{\lim_{ N \to \infty } 1 - \lim_{ N \to \infty } \frac{1}{\sqrt{ 3 }}} \\
&= \frac{\left( \frac{1}{\sqrt{ 3 }} \right)^{4} - 0}{1 - \frac{1}{\sqrt{ 3 }}} \\
&= \frac{\frac{1}{9}}{1 - \frac{1}{\sqrt{ 3 }}} \\
&= \frac{\frac{1}{9}}{\frac{\sqrt{ 3 } - 1}{\sqrt{ 3 }}} \\
&= \frac{1}{9} \cdot \frac{\sqrt{ 3 }}{\sqrt{ 3 } - 1} \\
&= \frac{\sqrt{ 3 }}{9\sqrt{ 3 } - 9} \\
&= \frac{\cancel{ \sqrt{ 3 } }}{\cancel{ \sqrt{ 3 } }(9 - 3\sqrt{ 3 })} \\
&= \frac{1}{9 - 3\sqrt{ 3 }}
\end{align}
$$

En conclusión:
$$
\sum_{n = 1}^{+\infty} \left( \frac{1}{\sqrt{ 3 }} \right)^{n + 3} = \frac{1}{9 - 3\sqrt{ 3 }}
$$

ALCARACIÓN:
Tanto esta parte como la anterior, se pueden resolver de formas más sencillas. Por ejemplo: podemos reconocer que ambas son series geométricas (una razón $q$ elevada a $n$). Para todas las series geométricas convergentes, la suma se expresa de la siguiente forma:
$$
S = \sum_{n = i}^{+\infty} q^{n} = \frac{q^{i}}{1 - q}
$$
En este caso particular:
$$
\sum_{n = 1}^{+\infty} \left( \frac{1}{\sqrt{ 3 }} \right)^{n + 3} = \frac{\left( \frac{1}{\sqrt{ 3 }} \right)^{4}}{1 - \frac{1}{\sqrt{ 3 }}} = \frac{\frac{1}{9}}{1 - \frac{1}{\sqrt{ 3 }}} = \frac{1}{9 - \frac{9}{\sqrt{ 3 }}} = \frac{1}{9 - 3\sqrt{ 3 }}
$$

### Parte c
$$
\sum_{n = 1}^{+\infty} 5^{n + 1}
$$
Comenzamos analizando el término general:
$$
\lim_{ n \to \infty } 5^{n + 1} = \text{?}
$$
$$
\begin{align}
n &\leq 5^{n + 1} \\
\lim_{ n \to \infty } n &\leq \lim_{ n \to \infty } 5^{n + 1} \\
+\infty &\leq \lim_{ n \to \infty } 5^{n + 1} \implies \lim_{ n \to \infty } 5^{n + 1} = +\infty
\end{align}
$$
Como vemos, la sucesión no converge a 0. Por lo tanto, la serie diverge.

### Parte d
$$
\sum_{n = 1}^{+\infty} \frac{3}{n(n + 3)}
$$
En este caso, el enfoque será diferente al de las partes anteriores, ya que se trata de una serie telescópica: tenemos que expresar el término general como una diferencia para lograr que al expresar la enésima reducida, los términos se cancelen.

Para esto, tenemos que separar el término general en fracciones simples:
$$
\frac{3}{n(n + 3)} = \frac{A}{n} + \frac{B}{n + 3} = \frac{A(n + 3) + Bn}{n(n + 3)} = \frac{3A + (A + B)n}{n(n + 3)}
$$
$$
\begin{cases}
3A = 3 \\
A + B = 0
\end{cases} \implies A = 1 \implies B = -1
$$
$$
\implies \frac{3}{n(n + 3)} = \frac{1}{n} - \frac{1}{n + 3}
$$
Ahora, desarrollamos la reducida enésima:
$$
\begin{align}
\sum_{n = 1}^{N} \frac{3}{n(n + 3)} &= \sum_{n = 1}^{N} \frac{1}{n} - \frac{1}{n + 3} \\
&= \left( 1 - \cancel{ \frac{1}{4} } \right) + \left( \frac{1}{2} - \cancel{ \frac{1}{5} } \right) + \left( \frac{1}{3} - \cancel{ \frac{1}{6} } \right) + \left( \cancel{ \frac{1}{4} } - \cancel{ \frac{1}{7} } \right) + \dots \\
&+ \left( \cancel{ \frac{1}{N - 3} } - \cancel{ \frac{1}{N} } \right) + \left( \cancel{ \frac{1}{N - 2} } - \frac{1}{N + 1} \right) + \left( \cancel{ \frac{1}{N - 1} } - \frac{1}{N + 2} \right) + \left( \cancel{ \frac{1}{N} } - \frac{1}{N + 3} \right) \\
&= 1 + \frac{1}{2} + \frac{1}{3} - \frac{1}{N + 1} - \frac{1}{N + 2} - \frac{1}{N + 3} \\
&= \frac{11}{6} - \frac{1}{N + 1} - \frac{1}{N + 2} - \frac{1}{N + 3}
\end{align}
$$

Finalmente, podemos determinar la suma:
$$
\begin{align}
\sum_{n = 1}^{+\infty} \frac{3}{n(n + 3)} &= \lim_{ N \to \infty }  \frac{11}{6} - \frac{1}{N + 1} - \frac{1}{N + 2} - \frac{1}{N + 3} \\
&= \lim_{ N \to \infty }  \frac{11}{6} - \lim_{ N \to \infty } \frac{1}{N + 1} - \lim_{ N \to \infty } \frac{1}{N + 2} - \lim_{ N \to \infty } \frac{1}{N + 3} \\
&= \frac{11}{6} - 0 - 0 - 0 \\
&= \frac{11}{6}
\end{align}
$$

En conclusión:
$$
\sum_{n = 1}^{+\infty} \frac{3}{n(n + 3)} = \frac{11}{6}
$$

### Parte e
$$
\sum_{n = 1}^{+\infty} \log\left( \frac{n^{2} + 2n + 1}{n^{2}} \right) = \sum_{n = 1}^{+\infty} \log\left( \frac{(n + 1)^{2}}{n^{2}} \right) = \sum_{n = 1}^{+\infty} \log((n + 1)^{2}) - \log(n^{2})
$$
Desarrollamos la reducida enésima:
$$
\begin{align}
\sum_{n = 1}^{N} \log\left( \frac{n^{2} + 2n + 1}{n^{2}} \right) &= \sum_{n = 1}^{N} \log((n + 1)^{2}) - \log(n^{2}) \\
&= \cancel{ \log(4) } - \log(1) + \cancel{ \log(9) } - \cancel{ \log(4) } + \cancel{ \log(16) } - \cancel{ \log(9) } + \dots \\
&+ \cancel{ \log((N - 1)^{2}) } - \cancel{ \log((N - 2)^{2}) } + \cancel{ \log(N^{2}) } - \cancel{ \log((N - 1)^{2}) } + \log((N + 1)^{2}) - \cancel{ \log(N^{2}) } \\
&= \log((N + 1)^{2}) - \log(1) \\
&= \log(N^{2} + 2N + 1)
\end{align}
$$

Finalmente, podemos determinar la suma:
$$
\begin{align}
\sum_{n = 1}^{+\infty} \log\left( \frac{n^{2} + 2n + 1}{n^{2}} \right) &= \lim_{ N \to \infty } \log(N^{2} + 2N + 1) \\
&= + \infty
\end{align}
$$

En este caso, la serie diverge, ya que la suma tiende a infinito.

### Parte f
$$
\sum_{n = 1}^{+\infty} \frac{n}{(n + 1)(n + 2)(n + 3)}
$$
Primero, descompongamos la expresión en fracciones simples:
$$
\begin{align}
\frac{n}{(n + 1)(n + 2)(n + 3)} &= \frac{A}{n + 1} + \frac{B}{n + 2} + \frac{C}{n + 3} \\
&= \frac{A(n + 2) + B(n + 1)}{(n + 1)(n + 2)} + \frac{C}{n + 3} \\
&= \frac{A(n + 2)(n + 3) + B(n + 1)(n + 3) + C(n + 1)(n + 2)}{(n + 1)(n + 2)(n + 3)} \\
&= \frac{A(n^{2} + 5n + 6) + B(n^{2} + 4n + 3) + C(n^{2} + 3n + 2)}{(n + 1)(n + 2)(n + 3)} \\
&= \frac{An^{2} + 5An + 6A + Bn^{2} + 4Bn + 3B + Cn^{2} + 3Cn + 2C}{(n + 1)(n + 2)(n + 3)} \\
&= \frac{(A + B + C)n^{2} + (5A + 4B + 3C)n + (6A + 3B + 2C)}{(n + 1)(n + 2)(n + 3)}
\end{align}
$$
$$
\begin{cases}
A + B + C = 0 \\
5A + 4B + 3C = 1 \\
6A + 3B + 2C = 0
\end{cases}
$$
$$
\begin{align}
&\implies 2A + B = 1 \land 4A + B = 0 \implies 2A = -1 \implies A = -\frac{1}{2} \\
&\implies -1 + B = 1 \implies B = 2 \implies -\frac{1}{2} + 2 + C = 0 \implies C = -\frac{3}{2}
\end{align}
$$
De esta forma:
$$
\frac{n}{(n + 1)(n + 2)(n + 3)} = -\frac{\frac{1}{2}}{n + 1} + \frac{2}{n + 2} - \frac{\frac{3}{2}}{n + 3}
$$
Ahora, proseguimos a estudiar la reducida enésima:
$$
\begin{align}
\sum_{n = 1}^{N} \frac{n}{(n + 1)(n + 2)(n + 3)} &= \sum_{n = 1}^{N} -\frac{\frac{1}{2}}{n + 1} + \frac{2}{n + 2} - \frac{\frac{3}{2}}{n + 3} \\
&= -\frac{\frac{1}{2}}{2} + \frac{2}{3} - \cancel{ \frac{\frac{3}{2}}{4} } - \frac{\frac{1}{2}}{3} + \cancel{ \frac{2}{4} } - \cancel{ \frac{\frac{3}{2}}{5} } - \cancel{ \frac{\frac{1}{2}}{4} } + \cancel{ \frac{2}{5} } - \cancel{ \frac{\frac{3}{2}}{6} } - \dots \\
&- \cancel{ \frac{\frac{1}{2}}{N - 1} } + \cancel{ \frac{2}{N} } - \cancel{ \frac{\frac{3}{2}}{N + 1} } - \cancel{ \frac{\frac{1}{2}}{N} } + \cancel{ \frac{2}{N + 1} } - \frac{\frac{3}{2}}{N + 2} - \cancel{ \frac{\frac{1}{2}}{N + 1} } + \frac{2}{N + 2} - \frac{\frac{3}{2}}{N + 3} \\
&= -\frac{\frac{1}{2}}{2} + \frac{2}{3} - \frac{\frac{1}{2}}{3} - \frac{\frac{3}{2}}{N + 2} + \frac{2}{N + 2} - \frac{\frac{3}{2}}{N + 3} \\
&= -\frac{\frac{1}{2}}{2} + \frac{\frac{3}{2}}{3} + \frac{\frac{1}{2}}{N + 2} - \frac{\frac{3}{2}}{N + 3} \\
&= \frac{1}{4} + \frac{1}{2N + 4} - \frac{3}{2N + 6}
\end{align}
$$

Finalmente, determinamos la suma:
$$
\begin{align}
\sum_{n = 1}^{+\infty} \frac{n}{(n + 1)(n + 2)(n + 3)} &= \lim_{ N \to \infty } \frac{1}{4} + \frac{1}{2N + 4} - \frac{3}{2N + 6} \\
&= \lim_{ N \to \infty } \frac{1}{4} + \lim_{ N \to \infty } \frac{1}{2N + 4} - \lim_{ N \to \infty } \frac{3}{2N + 6} \\
&= \frac{1}{4} + 0 - 0 \\
&= \frac{1}{4}
\end{align}
$$

En conclusión:
$$
\sum_{n = 1}^{+\infty} \frac{n}{(n + 1)(n + 2)(n + 3)} = \frac{1}{4}
$$

### Parte g
$$
\sum_{n = 1}^{+\infty} \frac{n \cdot \arctan(n + 1) - (n + 1) \cdot \arctan(n)}{n(n + 1)}
$$
Simplificamos la expresión:
$$
\begin{align}
\frac{n \cdot \arctan(n + 1) - (n + 1) \cdot \arctan(n)}{n(n + 1)} &= \frac{\cancel{ n } \cdot \arctan(n + 1)}{\cancel{ n }(n + 1)} - \frac{\cancel{ (n + 1) } \cdot \arctan(n)}{n\cancel{ (n + 1) }} \\
&= \frac{\arctan(n + 1)}{n + 1} - \frac{\arctan(n)}{n}
\end{align}
$$

Estudiamos la reducida enésima:
$$
\begin{align}
\sum_{n = 1}^{N} \frac{\arctan(n + 1)}{n + 1} - \frac{\arctan(n)}{n} &= \cancel{ \frac{\arctan(2)}{2} } - \frac{\arctan(1)}{1} + \cancel{ \frac{\arctan(3)}{3} } - \cancel{ \frac{\arctan(2)}{2} } + \cancel{ \frac{\arctan(4)}{4} } - \cancel{ \frac{\arctan(3)}{3} } + \dots \\
&+ \cancel{ \frac{\arctan(N - 1)}{N - 1} } - \cancel{ \frac{\arctan(N - 2)}{N - 2} } + \cancel{ \frac{\arctan(N)}{N} } - \cancel{ \frac{\arctan(N - 1)}{N - 1} } + \frac{\arctan(N + 1)}{N + 1} - \cancel{ \frac{\arctan(N)}{N} } \\
&= \frac{\arctan(N + 1)}{N + 1} - \arctan(1) \\
&= \frac{\arctan(N + 1)}{N + 1} - \frac{\pi}{4}
\end{align}
$$

Finalmente, estudiamos la suma:
$$
\begin{align}
\sum_{n = 1}^{+\infty} \frac{n \cdot \arctan(n + 1) - (n + 1) \cdot \arctan(n)}{n(n + 1)} &= \lim_{ N \to \infty } \frac{\arctan(N + 1)}{N + 1} - \frac{\pi}{4} \\
&= \frac{\lim_{ N \to \infty } \arctan(N + 1)}{\lim_{ N \to \infty } N + 1} - \lim_{ N \to \infty } \frac{\pi}{4} \\
&= \frac{\frac{\pi}{2}}{+\infty} - \frac{\pi}{4} \\
&= 0 - \frac{\pi}{4} \\
&= -\frac{\pi}{4}
\end{align}
$$

En conclusión:
$$
\sum_{n = 1}^{+\infty} \frac{n \cdot \arctan(n + 1) - (n + 1) \cdot \arctan(n)}{n(n + 1)} = -\frac{\pi}{4}
$$

---
## Ejercicio 2
Para resolver el ejercicio propuesto, tenemos que recordar en que consiste el criterio de comparación:

> [!Proposición - Criterio de comparación]
> Sean $\sum a_{n}$ y $\sum b_{n}$ series de términos positivos, tales que $a_{n} \leq b_{n}$ para todo $n > n_{0}$. Entonces:
> - Si $\sum b_{n}$ converge $\implies$ $\sum a_{n}$ converge.
> - Si $\sum a_{n}$ diverge $\implies$ $\sum b_{n}$ diverge.

### Parte a
$$
\sum_{n = 1}^{+\infty} \frac{1}{n^{n}}
$$
Sabemos que la serie $\sum_{n = 1}^{+\infty} \frac{1}{n^{2}}$ converge, y como se cumple que $\frac{1}{n^{n}} \leq \frac{1}{n^{2}}$, podemos afirmar que la serie $\sum_{n = 1}^{+\infty} \frac{1}{n^{n}}$ es convergente.

### Parte b
$$
\sum_{n = 1}^{+\infty} e^{-\sqrt{ n + 1 }}
$$
Estudiemos el término general:
$$
e^{-\sqrt{ n + 1 }} = \frac{1}{e^{\sqrt{ n + 1 }}}
$$
La serie puede converger, ya que su término general cumple la condición:
$$
\lim_{ n \to \infty } \frac{1}{e^{\sqrt{ n + 1 }}} = 0
$$
Ahora, resta comparar el término general con otros cuyo comportamiento sea conocido. Por ejemplo, si podemos verificar que $\frac{1}{e^{\sqrt{ n + 1 }}} \leq \frac{1}{n^{2}}$, habremos probado que la serie es convergente.
$$
\begin{align}
\frac{1}{e^{\sqrt{ n + 1 }}} &\leq \frac{1}{n^{2}} \\
e^{\sqrt{ n + 1 }} &\geq n^{2} \\
\frac{e^{\sqrt{ n + 1 }}}{n^{2}} &\geq 1
\end{align}
$$
$$
\begin{align}
\frac{e^{\sqrt{ n + 1 }}}{n^{2}} &= \exp\left( \log\left( \frac{e^{\sqrt{ n + 1 }}}{n^{2}} \right) \right) \\
&= \exp\left( \log(e^{\sqrt{ n + 1 }}) - \log(n^{2}) \right) \\
&= \exp\left( \sqrt{ n + 1 } \cdot \log(e) - 2 \cdot \log(n) \right) \\
&= \exp\left( \sqrt{ n + 1 } - 2 \cdot \log(n) \right) \\
&= e^{\sqrt{ n + 1 } - 2 \cdot \log(n)} \\
&= \frac{e^{\sqrt{ n + 1 }}}{e^{2 \cdot \log(n)}}
\end{align}
$$
Entonces, resta verificar la relación de los exponentes, para lo que utilizaremos L'Hôpital:
$$
\lim_{ n \to +\infty } \frac{\sqrt{ n + 1 }}{2 \cdot \log(n)} = \frac{+\infty}{+\infty}
$$
$$
(\sqrt{ n + 1 })' = \frac{1}{2 \cdot \sqrt{ n + 1 }}
$$
$$
(2 \cdot \log(n))' = \frac{2}{n}
$$
$$
\begin{align}
\implies \lim_{ n \to +\infty } \frac{\sqrt{ n + 1 }}{2 \cdot \log(n)} &= \lim_{ n \to +\infty } \frac{\frac{1}{2 \cdot \sqrt{ n + 1 }}}{\frac{2}{n}} \\
&= \lim_{ n \to +\infty } \frac{n}{4 \cdot \sqrt{ n + 1 }} \\
&= \lim_{ n \to +\infty } \frac{\sqrt{ n } \cdot \sqrt{ n }}{4 \cdot \sqrt{ n + 1 }} \\
&\simeq \lim_{ n \to +\infty } \frac{\sqrt{ n }}{4} \\
&= +\infty
\end{align}
$$

De esta forma, probamos que $e^{\sqrt{ n + 1 }} \geq n^{2}$, por lo que $\frac{1}{e^{\sqrt{ n + 1 }}} \leq \frac{1}{n^{2}}$.

En conclusión, la serie $\sum_{n = 1}^{+\infty} e^{-\sqrt{ n + 1 }}$ converge.

---
## Ejercicio 3
En este caso, para lograr clasificar las series propuestas, tenemos que aplicar el criterio del equivalente:

> [!Proposición - Criterio de equivalentes]
> Sean $\sum a_{n}$ y $\sum b_{n}$ series de términos positivos:
> - Si $\lim \frac{a_{n}}{b_{n}} = L > 0$, entonces las dos series son de la misma clase (ambas convergen o ambas divergen).
> - Si $\lim \frac{a_{n}}{b_{n}} = 0$, entonces si $\sum b_{n}$ converge, $\sum a_{n}$ también lo hace.

### Parte a
$$
\sum_{n = 1}^{+\infty} \frac{1}{n^{2} + 1}
$$
Compararemos el término $\frac{1}{n^{2} + 1}$ con un equivalente conocido:
$$
\frac{1}{n^{2} + 1} \sim \frac{1}{n^{2}}
$$
Para esto, estudiamos el siguiente límite:
$$
\begin{align}
\lim_{ n \to +\infty } \frac{\frac{1}{n^{2} + 1}}{\frac{1}{n^{2}}} &= \lim_{ n \to +\infty } \frac{n^{2}}{n^{2} + 1} \\
&= \lim_{ n \to +\infty } \frac{\cancel{ n^{2} }}{\cancel{ n^{2} }\left( 1 + \frac{1}{n^{2}} \right)} \\
&= \lim_{ n \to +\infty } \frac{1}{1 + \frac{1}{n^{2}}} \\
&= \frac{\lim_{ n \to +\infty } 1}{\lim_{ n \to +\infty } 1 + \lim_{ n \to +\infty } \frac{1}{n^{2}}} \\
&= \frac{1}{1 + 0} \\
&= \frac{1}{1} \\
&= 1
\end{align}
$$

Entonces, nos encontramos en el primer caso de la proposición, por lo que $\sum_{n = 1}^{+\infty} \frac{1}{n^{2} + 1}$ es de la misma clase que $\sum_{n = 1}^{+\infty} \frac{1}{n^{2}}$.

Sabemos que $\sum_{n = 1}^{+\infty} \frac{1}{n^{2}}$ es convergente.

En conclusión, la serie $\sum_{n = 1}^{+\infty} \frac{1}{n^{2} + 1}$ es convergente.

### Parte b
$$
\sum_{n = 1}^{+\infty} \frac{n^{2} + 1}{n^{3}}
$$
En este caso, utilizaremos como referencia la serie $\sum_{n = 1}^{+\infty} \frac{1}{n}$, la cual sabemos que no converge.

Entonces, calculamos el límite del cociente:
$$
\begin{align}
\lim_{ n \to \infty } \frac{\frac{n^{2} + 1}{n^{3}}}{\frac{1}{n}} &= \lim_{ n \to \infty } \frac{n^{3} + n}{n^{3}} \\
&= \lim_{ n \to \infty } \frac{n^{3}}{n^{3}} + \frac{n}{n^{3}} \\
&= \lim_{ n \to \infty } 1 + \frac{1}{n^{2}} \\
&= \lim_{ n \to \infty } 1 + \lim_{ n \to \infty } \frac{1}{n^{2}} \\
&= 1 + 0 \\
&= 1
\end{align}
$$

De esta forma, determinamos que el límite del cociente es 1. Por lo tanto, ambas series son de la misma clase.

En conclusión, sabiendo que $\sum_{n = 1}^{+\infty} \frac{1}{n}$ es divergente, $\sum_{n = 1}^{+\infty} \frac{n^{2} + 1}{n^{3}}$ también es divergente.

ACLARACIÓN:
Cuando aplicamos el criterio del equivalente, es importante que el término divisor sea el término general de una serie la cual sabemos como se comporta.

### Parte c
$$
\sum_{n = 1}^{+\infty} \frac{\log(n + 1) - \log(n)}{10n + 1}
$$
Trabajamos el término general:
$$
\begin{align}
\frac{\log(n + 1) - \log(n)}{10n + 1} &= \frac{\log\left( \frac{n + 1}{n} \right)}{10n + 1} \\
&= \frac{\log\left( 1 + \frac{1}{n} \right)}{10n + 1}
\end{align}
$$
Ahora, trabajaremos con un término que conocemos, el cual es convergente, ya que nos sirve tanto si el límite es finito o 0: $\frac{1}{n^{2}}$

$$
\begin{align}
\frac{\frac{\log\left( 1 + \frac{1}{n} \right)}{10n + 1}}{\frac{1}{n^{2}}} &= \frac{n^{2} \cdot \log\left( 1 + \frac{1}{n} \right)}{10n + 1} \\
&= \frac{n^{2} \cdot \log\left( 1 + \frac{1}{n} \right)}{n\left( 10 + \frac{1}{n} \right)} \\
&= \frac{n \cdot \log\left( 1 + \frac{1}{n} \right)}{10 + \frac{1}{n}}
\end{align}
$$
Ahora, hay un resultado muy útil que conocemos para simplificar la expresión anterior:
$$
\lim_{ n \to \infty } n \cdot \log\left( 1 + \frac{1}{n} \right) = 1
$$
De esta manera:
$$
\begin{align}
\lim_{ n \to \infty } \frac{n \cdot \log\left( 1 + \frac{1}{n} \right)}{10 + \frac{1}{n}} &= \frac{\lim_{ n \to \infty } n \cdot \log\left( 1 + \frac{1}{n} \right)}{\lim_{ n \to \infty } 10 + \lim_{ n \to \infty } \frac{1}{n}} \\
&= \frac{1}{10 + 0} \\
&= \frac{1}{10}
\end{align}
$$
En conclusión, como $\lim_{ n \to \infty } \frac{n \cdot \log\left( 1 + \frac{1}{n} \right)}{10 + \frac{1}{n}} = \frac{1}{10} > 0$, ambas series son de la misma clase, y como $\sum_{n = 1}^{+\infty} \frac{1}{n^{2}}$ es convergente, entonces $\sum_{n = 1}^{+\infty} \frac{\log(n + 1) - \log(n)}{10n + 1}$ también lo es.

---
## Ejercicio 4
En este ejercicio, tenemos que aplicar el criterio del cociente:
> [!Proposición - Criterio del cociente o criterio de D'Alambert]
> Sean $\sum a_{n}$ una serie de términos positivos, tal que existe $\lim_{ n \to \infty } \frac{a_{n + 1}}{a_{n}} = L$. Entonces:
> - Si $L < 1 \implies \sum a_{n} < \infty$.
> - Si $L > 1 \implies \sum a_{n}$ diverge.
> - Si $L = 1$, el criterio no decide.

### Parte a
$$
\sum_{n = 1}^{+\infty} \frac{2n - 1}{(\sqrt{ 2 })^{n}}
$$
Desarrollamos el cociente $\lim_{ n \to \infty } \frac{a_{n + 1}}{a_{n}}$:
$$
\begin{align}
\lim_{ n \to \infty } \frac{a_{n + 1}}{a_{n}} &= \lim_{ n \to \infty } \frac{\frac{2(n + 1) - 1}{(\sqrt{ 2 })^{n + 1}}}{\frac{2n - 1}{(\sqrt{ 2 })^{n}}} \\
&= \lim_{ n \to \infty } \frac{2(n + 1) - 1}{(\sqrt{ 2 })^{n + 1}} \cdot \frac{(\sqrt{ 2 })^{n}}{2n - 1} \\
&= \lim_{ n \to \infty } \frac{2n + 1}{\sqrt{ 2 } \cdot \cancel{ (\sqrt{ 2 })^{n} }} \cdot \frac{\cancel{ (\sqrt{ 2 })^{n} }}{2n - 1} \\
&= \lim_{ n \to \infty } \frac{1}{\sqrt{ 2 }} \cdot \frac{2n + 1}{2n - 1} \\
&= \lim_{ n \to \infty } \frac{1}{\sqrt{ 2 }} \cdot \frac{\cancel{ n }\left( 2 + \frac{1}{n} \right)}{\cancel{ n }\left( 2 - \frac{1}{n} \right)} \\
&= \lim_{ n \to \infty } \frac{1}{\sqrt{ 2 }} \cdot \frac{2 + \frac{1}{n}}{2 - \frac{1}{n}} \\
&= \frac{1}{\sqrt{ 2 }} \cdot \frac{2 + 0}{2 - 0} \\
&= \frac{1}{\sqrt{ 2 }} \cdot 1 \\
&= \frac{1}{\sqrt{ 2 }}
\end{align}
$$

En conclusión, como $\lim_{ n \to \infty } \frac{a_{n + 1}}{a_{n}} = \lim_{ n \to \infty } \frac{2(n + 1) - 1}{(\sqrt{ 2 })^{n + 1}} \cdot \frac{(\sqrt{ 2 })^{n}}{2n - 1} = \frac{1}{\sqrt{ 2 }} < 1$, concluimos que la serie es convergente.

### Parte b
$$
\sum_{n = 1}^{+\infty} \frac{n!}{n^{n}}
$$
Desarrollamos el cociente $\lim_{ n \to \infty } \frac{a_{n + 1}}{a_{n}}$:
$$
\begin{align}
\lim_{ n \to \infty } \frac{a_{n + 1}}{a_{n}} &= \lim_{ n \to \infty } \frac{\frac{(n + 1)!}{(n + 1)^{n + 1}}}{\frac{n!}{n^{n}}} \\
&= \lim_{ n \to \infty } \frac{(n + 1)!}{(n + 1)^{n + 1}} \cdot \frac{n^{n}}{n!} \\
&= \lim_{ n \to \infty } \frac{(n + 1) \cdot \cancel{ n! }}{(n + 1)^{n + 1}} \cdot \frac{n^{n}}{\cancel{ n! }} \\
&= \lim_{ n \to \infty } \frac{n^{n}}{(n + 1)^{n}} \\
&= \lim_{ n \to \infty } \left( \frac{n}{n + 1} \right)^{n} \\
&= \lim_{ n \to \infty } \left( \frac{\cancel{ n }}{\cancel{ n }\left( 1 + \frac{1}{n} \right)} \right)^{n} \\
&= \lim_{ n \to \infty } \left( \frac{1}{1 + \frac{1}{n}} \right)^{n} \\
&= \lim_{ n \to \infty } \frac{1}{\left( 1 + \frac{1}{n} \right)^{n}} \\
&= \frac{1}{e}
\end{align}
$$

En conclusión, como $\lim_{ n \to \infty } \frac{a_{n + 1}}{a_{n}} = \lim_{ n \to \infty } \frac{(n + 1)!}{(n + 1)^{n + 1}} \cdot \frac{n^{n}}{n!} = \frac{1}{e} < 1$, concluimos que la serie es convergente.

---
## Ejercicio 5
En este ejercicio, tenemos que aplicar el criterio de la raíz:
> [!Proposición - Criterio de la raíz enésima o criterio de Cauchy]
> Sean $\sum a_{n}$ una serie de términos positivos, tal que existe $\lim_{ n \to \infty } \sqrt[n]{ a_{n} } = L$. Entonces:
> - Si $L < 1 \implies \sum a_{n} < \infty$.
> - Si $L > 1 \implies \sum a_{n}$ diverge.
> - Si $L = 1$, el criterio no decide.

### Parte a
$$
\sum_{n = 1}^{+\infty} \frac{2n - 1}{(\sqrt{ 2 })^{n}}
$$
Aplicamos la raíz enésima al término general:
$$
\begin{align}
\lim_{ n \to \infty } \sqrt[n]{ \frac{2n - 1}{(\sqrt{ 2 })^{n}} } &= \frac{\sqrt[n]{ 2n - 1 }}{\sqrt[n]{ (\sqrt{ 2 })^{n} }} \\
&= \frac{(2n - 1)^{\frac{1}{n}}}{\sqrt{ 2 }} \\
&= \frac{\exp \left( \log \left( (2n - 1)^{\frac{1}{n}} \right) \right)}{\sqrt{ 2 }} \\
&= \frac{\exp \left( \frac{1}{n} \cdot \log \left( 2n - 1 \right) \right)}{\sqrt{ 2 }}
\end{align}
$$
Analizamos el límite:
$$
\lim_{ n \to \infty } \frac{1}{n} \cdot \log \left( 2n - 1 \right) = \lim_{ n \to \infty } \frac{\log \left( 2n - 1 \right)}{n} = \frac{+\infty}{+\infty}
$$
Aplicamos L'Hôpital:
$$
\lim_{ n \to \infty } \frac{\log \left( 2n - 1 \right)}{n} = \lim_{ n \to \infty } \frac{\frac{2}{2n - 1}}{1} = \lim_{ n \to \infty } \frac{2}{2n - 1} = 0
$$
Entonces:
$$
\begin{align}
\lim_{ n \to \infty } \sqrt[n]{ \frac{2n - 1}{(\sqrt{ 2 })^{n}} } &= \frac{\exp \left( \frac{1}{n} \cdot \log \left( 2n - 1 \right) \right)}{\sqrt{ 2 }} \\
&= \frac{\exp(0)}{\sqrt{ 2 }} \\
&= \frac{1}{\sqrt{ 2 }}
\end{align}
$$

En conclusión, como $\lim_{ n \to \infty } \sqrt[n]{ \frac{2n - 1}{(\sqrt{ 2 })^{n}} } = \frac{1}{\sqrt{ 2 }} < 1$, concluimos que la serie es convergente.

### Parte b
$$
\sum_{n = 1}^{+\infty} \left( \frac{n + 1}{2n - 1} \right)^{n}
$$
Aplicamos la raíz enésima al término general:
$$
\begin{align}
\lim_{ n \to \infty } \sqrt[n]{ \left( \frac{n + 1}{2n - 1} \right)^{n} } &= \frac{n + 1}{2n - 1} \\
&= \frac{\cancel{ n }\left( 1 + \frac{1}{n} \right)}{\cancel{ n }\left( 2 - \frac{1}{n} \right)} \\
&= \frac{1 + \frac{1}{n}}{2 - \frac{1}{n}} \\
&= \frac{1}{2}
\end{align}
$$

En conclusión, como $\lim_{ n \to \infty } \sqrt[n]{ \left( \frac{n + 1}{2n - 1} \right)^{n} } = \frac{1}{2} < 1$, concluimos que la serie es convergente.

---
## Ejercicio 6
En varios de los casos, consideraremos que: $a_{n} \geq 0$ y $\sum a_{n}$ converge $\implies$ $\lim_{ n \to \infty } a_{n} = 0$. Esto significa que la expresión (no constante, a excepción de 0) va disminuyendo a medida que $n$ aumenta, es decreciente (o al menos en términos generales, quizá no pasa que $a_{n} \geq a_{n + 1}, \forall n \in \mathbb{N}$).

### Parte a
$$
\sum \frac{1}{a_{n}}
$$
En este caso, analicemos el comportamiento del término general en el infinito: si $\lim_{ n \to \infty } a_{n} = 0$, entonces necesariamente:
$$
\lim_{ n \to \infty } \frac{1}{a_{n}} = \frac{\lim_{ n \to \infty } 1}{\lim_{ n \to \infty } a_{n}} = \frac{1}{0} = +\infty
$$
Por lo tanto, la serie $\sum \frac{1}{a_{n}}$ es divergente.

### Parte b
$$
\sum a_{n}^{2}
$$
Desarrollamos el límite del término general, considerando el límite de $a_{n}$:
$$
\lim_{ n \to \infty } a_{n} = 0 \implies \lim_{ n \to \infty } a_{n}^{2} = \lim_{ n \to \infty } a_{n} \cdot a_{n} = \lim_{ n \to \infty } a_{n} \cdot \lim_{ n \to \infty } a_{n} = 0 \cdot 0 = 0
$$
Entonces, podemos ver que dicha sucesión tiende a 0 aún más rápido. De esta manera, se cumple que $a_{n} \geq a_{n}^{2}, \forall n \geq n_{0}$, y por el criterio de comparación, $\sum a_{n}^{2}$ es convergente.

### Parte c
$$
\sum \sqrt{ a_{n} }
$$
En este caso, buscaremos diferentes formas de expresar el término general para llegar a una conclusión:
$$
\sqrt{ a_{n} } = a_{n}^{\frac{1}{2}}
$$
Ahora, comparémoslo con $a_{n}$:
$$
\begin{align}
a_{n} > \sqrt{ a_{n} } &\Longleftrightarrow a_{n} > 1 \\
a_{n} = \sqrt{ a_{n} } &\Longleftrightarrow a_{n} = 1 \\
a_{n} < \sqrt{ a_{n} } &\Longleftrightarrow a_{n} < 1
\end{align}
$$
De esta forma, cuando $n \to +\infty$, $\sqrt{ a_{n} }$ se acerca más lentamente a 0 que $a_{n}$.

En este caso, intentaremos aplicar el criterio de equivalentes:
$$
\lim_{ n \to \infty } \frac{\sqrt{ a_{n} }}{a_{n}} = \lim_{ n \to \infty } \frac{\sqrt{ a_{n} }}{\sqrt{ a_{n} } \cdot \sqrt{ a_{n} }} = \lim_{ n \to \infty } \frac{1}{\sqrt{ a_{n} }} = \frac{1}{0} = +\infty
$$
Esto nos genera la sospecha de que la serie puede no converger. Por lo tanto, busquemos un contraejemplo:
Sea $a_{n} = \frac{1}{n^{2}}$ y $\sqrt{ a_{n} } = \sqrt{ \frac{1}{n^{2}} } = \frac{1}{n}$.

Sabemos que $\sum \frac{1}{n^{2}}$ es una serie convergente. Sin embargo, $\sum \frac{1}{n}$ es divergente. Por lo tanto, la serie $\sum \sqrt{ a_{n} }$ no es necesariamente convergente, puede divergir.

### Parte d
$$
\sum \log(1 + a_{n})
$$
En este caso, consideraremos la siguiente desigualdad:
$$
\log(1 + x) \leq x \implies \log(1 + a_{n}) \leq a_{n}
$$
De esta forma, sabiendo que $\sum a_{n}$ converge, por el criterio de comparación, concluimos que $\sum \log(1 + a_{n})$ es convergente.

---
## Ejercicio 7
En este caso, tendremos que recurrir a dos criterios vistos en la parte de series alternadas:
> [!Teorema]
> Toda serie absolutamente convergente es convergente:
> $$
> \sum |a_{n}| \text{ converge} \implies \sum a_{n} \text{ converge}
> $$

> [!Proposición - Criterio de Leibnitz]
> Si $a_{n}$ es una sucesión monótona decreciente que tiende a cero, entonces la seria alternada $\sum (-1)^{n}a_{n}$ es convergente:
> $$
> a_{n + 1} \leq a_{n}, \forall n \in \mathbb{N} \land \lim_{ n \to \infty } a_{n} = 0 \implies \sum (-1)^{n}a_{n} \text{ es convergente}
> $$

Por esta razón, en todos los casos comenzaremos estudiando si son absolutamente convergentes, y si no lo son, tendremos que analizar la convergencia por separado.
### Parte a
$$
\sum_{n = 1}^{+\infty} \frac{(-1)^{n + 1}}{3^{n}}
$$
Analizamos si $\sum_{n = 1}^{+\infty} \frac{(-1)^{n + 1}}{3^{n}}$ es absolutamente convergente: $\sum_{n = 1}^{+\infty} \left| \frac{(-1)^{n + 1}}{3^{n}} \right| = \sum_{n = 1}^{+\infty} \frac{1}{3^{n}}$

Ahora, si estudiamos la expresión:
$$
\frac{1}{3^{n}} = \left( \frac{1}{3} \right)^{n} \implies \sum_{n = 1}^{+\infty} \frac{1}{3^{n}} = \sum_{n = 1}^{+\infty} \left( \frac{1}{3} \right)^{n}
$$
Esta última se trata de una serie geométrica, las cuales sabemos que convergen cuando $q < 1$, y su reducida enésima se expresa como:
$$
\sum_{n = 1}^{N} \left( \frac{1}{3} \right)^{n} = \frac{1}{3} \cdot \frac{1 - \left( \frac{1}{3} \right)^{N + 1}}{1 - \frac{1}{3}} = \frac{1}{3} \cdot \frac{1}{\frac{2}{3}} = \frac{1}{2}
$$
En conclusión, $\sum_{n = 1}^{+\infty} \frac{(-1)^{n + 1}}{3^{n}}$ es absolutamente convergente, y por el teorema presentado, también es convergente.

### Parte b
$$
\sum_{n = 1}^{+\infty} \frac{(-1)^{n + 1}n}{n^{2} + 1}
$$
Analizamos si $\sum_{n = 1}^{+\infty} \frac{(-1)^{n + 1}n}{n^{2} + 1}$ es absolutamente convergente: $\sum_{n = 1}^{+\infty} \left| \frac{(-1)^{n + 1}n}{n^{2} + 1} \right| = \sum_{n = 1}^{+\infty} \frac{n}{n^{2} + 1}$

Ahora, si estudiamos la expresión:
$$
\frac{n}{n^{2} + 1} = \frac{\cancel{ n }}{\cancel{ n }\left( n + \frac{1}{n} \right)} = \frac{1}{n + \frac{1}{n}}
$$

Entonces, podemos aplicar el criterio de equivalentes con la serie $\frac{1}{n}$:
$$
\begin{align}
\lim_{ n \to \infty } \frac{\frac{1}{n + \frac{1}{n}}}{\frac{1}{n}} &= \lim_{ n \to \infty } \frac{n}{n + \frac{1}{n}} \\
&= \lim_{ n \to \infty } \frac{\cancel{ n }}{\cancel{ n }\left( 1 + \frac{1}{n^{2}} \right)} \\
&= \lim_{ n \to \infty } \frac{1}{1 + \frac{1}{n^{2}}} \\
&= 1
\end{align}
$$
Como $\lim_{ n \to \infty } \frac{\frac{1}{n + \frac{1}{n}}}{\frac{1}{n}} = 1 > 0$, las series son de la misma clase, y sabiendo que $\sum_{n = 1}^{+\infty} \frac{1}{n}$ diverge, entonces $\sum_{n = 1}^{+\infty} \frac{n}{n^{2} + 1}$ es divergente.

Entonces, $\sum_{n = 1}^{+\infty} \frac{(-1)^{n + 1}n}{n^{2} + 1}$ no es absolutamente convergente, por lo que tendremos que estudiar por separado su convergencia.

Para esto, aplicaremos el criterio de Leibnitz:
$$
\begin{align}
a_{n + 1} \leq a_{n} \implies \frac{a_{n + 1}}{a_{n}} \leq 1 \implies &\frac{n + 1}{(n + 1)^{2} + 1} \cdot \frac{n^{2} + 1}{n} \\
&= \frac{n^{3} + n^{2} + n + 1}{n^{3} + 2n^{2} + 2n} \\
&= \frac{\cancel{ n^{3} }\left( 1 + \frac{1}{n} + \frac{1}{n^{2}} + \frac{1}{n^{3}} \right)}{\cancel{ n^{3} }\left( 1 + \frac{2}{n} + \frac{2}{n^{2}} \right)} \\
&= \frac{1 + \frac{1}{n}\left( 1 + \frac{1}{n} + \frac{1}{n^{2}} \right)}{1 + \frac{1}{n}\left( 2 + \frac{2}{n} \right)}
\end{align}
$$
Resta comparar los términos que diferencian numerador y denominador:
$$
\begin{align}
\lim_{ n \to \infty } 1 + \frac{1}{n} + \frac{1}{n^{2}} &= 1 \\
\lim_{ n \to \infty } 2 + \frac{2}{n} &= 2
\end{align}
$$
Como vemos, $1 + \frac{1}{n} + \frac{1}{n^{2}} < 2 + \frac{2}{n}$, por lo que
$$
\frac{1 + \frac{1}{n}\left( 1 + \frac{1}{n} + \frac{1}{n^{2}} \right)}{1 + \frac{1}{n}\left( 2 + \frac{2}{n} \right)} \leq 1
$$
Ahora, si analizamos el límite al infinito de la sucesión:
$$
\lim_{ n \to \infty } \frac{n}{n^{2} + 1} = \lim_{ n \to \infty } \frac{\cancel{ n }}{\cancel{ n }\left( n + \frac{1}{n} \right)} = \lim_{ n \to \infty } \frac{1}{n + \frac{1}{n}} = 0
$$
Entonces, se cumplen las dos condiciones establecidas en el criterio de Leibnitz.

En conclusión, $\sum_{n = 1}^{+\infty} \frac{(-1)^{n + 1}n}{n^{2} + 1}$ es convergente, pero no es absolutamente convergente (es condicionalmente convergente).

### Parte c
$$
\sum_{n = 1}^{+\infty} \frac{(-1)^{n}n}{6n - 5}
$$
Analizamos si $\sum_{n = 1}^{+\infty} \frac{(-1)^{n}n}{6n - 5}$ es absolutamente convergente: $\sum_{n = 1}^{+\infty} \left| \frac{(-1)^{n}n}{6n - 5} \right| = \sum_{n = 1}^{+\infty} \frac{n}{6n - 5}$

Ahora, si estudiamos la expresión:
$$
\frac{n}{6n - 5} = \frac{\cancel{ n }}{\cancel{ n }\left( 6 - \frac{5}{n} \right)} = \frac{1}{6 - \frac{5}{n}}
$$

Analizamos el límite de la sucesión:
$$
\lim_{ n \to \infty } \frac{n}{6n - 5} = \lim_{ n \to \infty } \frac{1}{6 - \frac{5}{n}} = \frac{1}{6}
$$

Como vemos, la sucesión no tiende a 0, por lo que es divergente.

Sin embargo, esto también rompe con el segundo punto del criterio de Leibnitz.

Por lo tanto, concluimos que la serie no es absolutamente convergente, y tampoco es convergente.
### Parte d
$$
\sum_{n = 1}^{+\infty} \frac{(-1)^{n}(n^{3} + 2n^{2} + 8n + 5)}{n^{5} + 4n^{3} + 15}
$$
Analizamos si $\sum_{n = 1}^{+\infty} \frac{(-1)^{n}(n^{3} + 2n^{2} + 8n + 5)}{n^{5} + 4n^{3} + 15}$ es absolutamente convergente: $\sum_{n = 1}^{+\infty} \left| \frac{(-1)^{n}(n^{3} + 2n^{2} + 8n + 5)}{n^{5} + 4n^{3} + 15} \right| = \sum_{n = 1}^{+\infty} \frac{n^{3} + 2n^{2} + 8n + 5}{n^{5} + 4n^{3} + 15}$

Ahora, si estudiamos la expresión:
$$
\begin{align}
\frac{n^{3} + 2n^{2} + 8n + 5}{n^{5} + 4n^{3} + 15} &= \frac{n^{3}\left( 1 + \frac{2}{n} + \frac{8}{n^{2}} + \frac{5}{n^{3}} \right)}{n^{5}\left( 1 + \frac{4}{n^{2}} + \frac{15}{n^{5}} \right)} \\
&= \frac{1}{n^{2}} \cdot \frac{1 + \frac{2}{n} + \frac{8}{n^{2}} + \frac{5}{n^{3}}}{1 + \frac{4}{n^{2}} + \frac{15}{n^{5}}}
\end{align}
$$

Analizamos el límite de la sucesión:
$$
\begin{align}
\lim_{ n \to \infty } \frac{n^{3} + 2n^{2} + 8n + 5}{n^{5} + 4n^{3} + 15} &= \lim_{ n \to \infty } \frac{1}{n^{2}} \cdot \frac{1 + \frac{2}{n} + \frac{8}{n^{2}} + \frac{5}{n^{3}}}{1 + \frac{4}{n^{2}} + \frac{15}{n^{5}}} \\
&= \lim_{ n \to \infty } \frac{1}{n^{2}} \cdot \lim_{ n \to \infty } \frac{1 + \frac{2}{n} + \frac{8}{n^{2}} + \frac{5}{n^{3}}}{1 + \frac{4}{n^{2}} + \frac{15}{n^{5}}} \\
&= 0 \cdot 1 \\
&= 0
\end{align}
$$

Como vemos, la sucesión se comporta de forma muy similar a $\frac{1}{n^{2}}$, por lo que aplicamos criterio de equivalentes:
$$
\begin{align}
\lim_{ n \to \infty } \frac{\frac{n^{3} + 2n^{2} + 8n + 5}{n^{5} + 4n^{3} + 15}}{\frac{1}{n^{2}}} &= \lim_{ n \to \infty } \cancel{ \frac{1}{n^{2}} } \cdot \frac{1 + \frac{2}{n} + \frac{8}{n^{2}} + \frac{5}{n^{3}}}{1 + \frac{4}{n^{2}} + \frac{15}{n^{5}}} \cdot \cancel{ n^{2} } \\
&= \lim_{ n \to \infty } \frac{1 + \frac{2}{n} + \frac{8}{n^{2}} + \frac{5}{n^{3}}}{1 + \frac{4}{n^{2}} + \frac{15}{n^{5}}} \\
&= \frac{1}{1} \\
&= 1
\end{align}
$$
Como $\lim_{ n \to \infty } \frac{\frac{n^{3} + 2n^{2} + 8n + 5}{n^{5} + 4n^{3} + 15}}{\frac{1}{n^{2}}} = 1 > 0$, las series son de la misma clase, y sabiendo que $\sum_{n = 1}^{+\infty} \frac{1}{n^{2}}$ converge, entonces $\sum_{n = 1}^{+\infty} \frac{n^{3} + 2n^{2} + 8n + 5}{n^{5} + 4n^{3} + 15}$ es convergente.

En conclusión, probamos que $\sum_{n = 1}^{+\infty} \frac{(-1)^{n}(n^{3} + 2n^{2} + 8n + 5)}{n^{5} + 4n^{3} + 15}$ es absolutamente convergente, y por el teorema inicial, también es convergente.

---
## Ejercicio 8
### Parte a
$$
\sum_{n = 1}^{+\infty} \frac{n}{(n + 1)(n + 2)}
$$
Estudiamos el término general:
$$
\frac{n}{(n + 1)(n + 2)} = \frac{n}{n^{2} + 3n + 2} = \frac{\cancel{ n }}{\cancel{ n }\left( n + 3 + \frac{2}{n} \right)} = \frac{1}{n + 3 + \frac{2}{n}}
$$
Verificamos que el límite es 0:
$$
\lim_{ n \to \infty } \frac{n}{(n + 1)(n + 2)} = \lim_{ n \to \infty } \frac{1}{n + 3 + \frac{2}{n}} = 0
$$

Ahora, aplicamos el criterio de equivalentes para verificar si la serie es convergente o no. Para esto, consideraremos la sucesión $\frac{1}{n}$:
$$
\begin{align}
\lim_{ n \to \infty } \frac{\frac{n}{(n + 1)(n + 2)}}{\frac{1}{n}} &= \lim_{ n \to \infty } \frac{n^{2}}{(n + 1)(n + 2)} \\
&= \lim_{ n \to \infty } \frac{n^{2}}{n^{2} + 3n + 2} \\
&= \lim_{ n \to \infty } \frac{\cancel{ n^{2} }}{\cancel{ n^{2} }\left( 1 + \frac{3}{n} + \frac{2}{n^{2}} \right)} \\
&= \lim_{ n \to \infty } \frac{1}{1 + \frac{3}{n} + \frac{2}{n^{2}}} \\
&= \frac{1}{1} \\
&= 1
\end{align}
$$

Como $\lim_{ n \to \infty } \frac{\frac{n}{(n + 1)(n + 2)}}{\frac{1}{n}} = 1 > 0$, por el criterio de equivalentes, ambas son de la misma clase.

En conclusión, $\sum_{n = 1}^{+\infty} \frac{n}{(n + 1)(n + 2)}$ es divergente.

### Parte b
$$
\sum_{n = 1}^{+\infty} \frac{n}{(n + 1) \cdot \log(n + 1)}
$$
Estudiamos el término general:
$$
\begin{align}
\frac{n}{(n + 1) \cdot \log(n + 1)} &= \frac{n}{n\log(n + 1) + \log(n + 1)} \\
&= \frac{\cancel{ n }}{\cancel{ n }\left( \log(n + 1) + \frac{\log(n + 1)}{n} \right)} \\
&= \frac{1}{\log(n + 1) + \frac{\log(n + 1)}{n}}
\end{align}
$$
Analizamos el límite:
$$
\begin{align}
\lim_{ n \to \infty } \frac{n}{(n + 1) \cdot \log(n + 1)} &= \lim_{ n \to \infty } \frac{1}{\log(n + 1) + \frac{\log(n + 1)}{n}} \\
&= \frac{1}{\lim_{ n \to \infty } \log(n + 1) + \frac{\lim_{ n \to \infty } \log(n + 1)}{n}} \\
&= \frac{1}{\lim_{ n \to \infty } \log(n + 1)} \\
&= 0
\end{align}
$$
Entonces, la serie puede converger. Aplicamos el criterio de comparación, para el cual utilizaremos la serie de termino general $\frac{1}{n}$: Sabemos que $\frac{n}{(n + 1) \cdot \log(n + 1)} = \frac{1}{\log(n + 1) + \frac{\log(n + 1)}{n}} > \frac{1}{n}$, ya que:
$$
\begin{align}
\log(n + 1) + \frac{\log(n + 1)}{n} &< n \\
\frac{\log(n + 1)}{n} + \frac{\log(n + 1)}{n^{2}} = \frac{\log(n + 1)}{n} \cdot \left( 1 + \frac{1}{n} \right) &< 1, \forall n \geq n_{0}
\end{align}
$$
De esta forma, como sabemos que $\sum_{n = 1}^{+\infty} \frac{1}{n}$ diverge, necesariamente $\sum_{n = 1}^{+\infty} \frac{n}{(n + 1) \cdot \log(n + 1)}$ también lo hace.

En conclusión, $\sum_{n = 1}^{+\infty} \frac{n}{(n + 1) \cdot \log(n + 1)}$ es divergente.

### Parte c
$$
\sum_{n = 1}^{+\infty} \frac{n^{3}}{e^{n}}
$$
Viendo la forma del termino general, quizás sea una buena estrategia utilizar el criterio del cociente:
$$
\begin{align}
\frac{a_{n + 1}}{a_{n}} &= \frac{(n + 1)^{3}}{e^{n + 1}} \cdot \frac{e^{n}}{n^{3}} \\
&= \frac{(n + 1)^{3}}{\cancel{ e^{n} } \cdot e} \cdot \frac{\cancel{ e^{n} }}{n^{3}} \\
&= \frac{(n + 1)^{3}}{e \cdot n^{3}} \\
&= \frac{n^{3} + 3n^{2} + 3n + 1}{e \cdot n^{3}} \\
&= \frac{n^{3}}{e \cdot n^{3}} + \frac{3n^{2}}{e \cdot n^{3}} + \frac{3n}{e \cdot n^{3}} + \frac{1}{e \cdot n^{3}} \\
&= \frac{1}{e} + \frac{3}{e \cdot n} + \frac{3}{e \cdot n^{2}} + \frac{1}{e \cdot n^{3}}
\end{align}
$$
Ahora, resta estudiar el límite del cociente:
$$
\begin{align}
\lim_{ n \to \infty } \frac{a_{n + 1}}{a_{n}} &= \lim_{ n \to \infty } \frac{1}{e} + \frac{3}{e \cdot n} + \frac{3}{e \cdot n^{2}} + \frac{1}{e \cdot n^{3}} \\
&= \frac{1}{e} + \frac{3}{e \cdot +\infty} + \frac{3}{e \cdot +\infty} + \frac{1}{e \cdot +\infty} \\
&= \frac{1}{e} + 0 + 0 + 0 \\
&= \frac{1}{e}
\end{align}
$$
Sabemos que $e > 1$, por lo que $\frac{1}{e} < 1$. De esta manera, considerando lo establecido por el criterio del cociente, la serie $\sum_{n = 1}^{+\infty} \frac{n^{3}}{e^{n}}$ converge.

### Parte d
$$
\sum_{n = 1}^{+\infty} \frac{(-1)^{n + 1}}{\sqrt{ n }}
$$
En este caso, aplicaremos el criterio de convergencia absoluta: si $\sum a_{n}$ es absolutamente convergente, entonces es convergente. Esto significa que:
$$
\sum |a_{n}| \text{ converge} \implies \sum a_{n} \text{ converge}
$$
Entonces, estudiamos $\sum_{n = 1}^{+\infty} \left| \frac{(-1)^{n + 1}}{\sqrt{ n }} \right| = \sum_{n = 1}^{+\infty} \frac{1}{\sqrt{ n }}$

Sabemos que $\lim_{ n \to \infty } \frac{1}{\sqrt{ n }} = 0$, por lo que puede converger.

Podemos expresar la raíz como un exponente:
$$
\frac{1}{\sqrt{ n }} = \frac{1}{n^{\frac{1}{2}}}
$$
Sin embargo, ahora podemos comparar dicha sucesión con una conocida: $\frac{1}{n}$.

Sabemos que $\frac{1}{n^{\frac{1}{2}}} \geq \frac{1}{n}$, y como $\sum_{n = 1}^{+\infty} \frac{1}{n}$ diverge, entonces $\sum_{n = 1}^{+\infty} \frac{1}{\sqrt{ n }}$ también es divergente.

Sin embargo, esto no implica que $\sum_{n = 1}^{+\infty} \frac{(-1)^{n + 1}}{\sqrt{ n }}$ no sea convergente.

Para finalizar el razonamiento, consideremos el criterio de Leibnitz: si $a_{n}$ es una sucesión monótona decreciente que tiende a 0, entonces la serie alternada $\sum (-1)^{n} a_{n}$ es convergente.

Entonces, tenemos que estudiar las propiedades de $\frac{1}{\sqrt{ n }}$:
Sabemos que $\lim_{ n \to \infty } \frac{1}{\sqrt{ n }} = 0$, por lo que nos queda confirmar que es monótona decreciente: $\frac{a_{n + 1}}{a_{n}} < 1$?
$$
\begin{align}
\frac{\frac{1}{\sqrt{ n + 1 }}}{\frac{1}{\sqrt{ n }}} &= \frac{\sqrt{ n }}{\sqrt{ n + 1 }} \\
&= \frac{\sqrt{ n }}{\sqrt{ n\left( 1 + \frac{1}{n} \right) }} \\
&= \frac{\cancel{ \sqrt{ n } }}{\cancel{ \sqrt{ n } }\sqrt{ 1 + \frac{1}{n} }} \\
&= \frac{1}{\sqrt{ 1 + \frac{1}{n} }}
\end{align}
$$
$$
1 + \frac{1}{n} > 1 \implies \sqrt{ 1 + \frac{1}{n} } > 1 \implies \frac{1}{\sqrt{ 1 + \frac{1}{n} }} < 1
$$
De esta manera, $\frac{a_{n + 1}}{a_{n}} < 1$, por lo que $\frac{1}{\sqrt{ n }}$ es monótona decreciente.

En conclusión, $\sum_{n = 1}^{+\infty} \frac{(-1)^{n + 1}}{\sqrt{ n }}$ es convergente por el criterio de Leibnitz.

---
## Ejercicio 9
Entonces, tenemos la siguiente suma:

Si pensamos como se desarrolla la suma:
$$
\sum_{n = 0}^{N} 8^{n} \cdot \left( \frac{1}{3^{2n}} \right) = 1 + 8\left( \frac{1}{3^{2}} \right) + 8^{2}\left( \frac{1}{9^{2}} \right) + \dots + 8^{N}\left( \frac{1}{3^{2N}} \right)
$$
$$
8^{n} \cdot \left( \frac{1}{3^{2n}} \right) = \frac{8^{n}}{3^{2n}} = \left( \frac{8}{3^{2}} \right)^{n} = \left( \frac{8}{9} \right)^{n}
$$
Ahora, estudiamos la reducida enésima, con este nuevo término simplificado:
$$
\sum_{n = 0}^{N} 8^{n} \cdot \left( \frac{1}{3^{2n}} \right) = \sum_{n = 0}^{N} \left( \frac{8}{9} \right)^{n} = \text{?}
$$
$$
\begin{align}
\sum_{n = 1}^{N + 1} \left( \frac{8}{9} \right)^{n} - \sum_{n = 0}^{N} \left( \frac{8}{9} \right)^{n} &= \cancel{ \left( \frac{8}{9} \right)^{2} } + \cancel{ \left( \frac{8}{9} \right)^{3} } + \cancel{ \left( \frac{8}{9} \right)^{4} } + \dots + \cancel{ \left( \frac{8}{9} \right)^{N - 1} } + \cancel{ \left( \frac{8}{9} \right)^{N} } + \left( \frac{8}{9} \right)^{N + 1} \\
&- 1 - \cancel{ \left( \frac{8}{9} \right)^{2} } - \cancel{ \left( \frac{8}{9} \right)^{3} } - \cancel{ \left( \frac{8}{9} \right)^{4} } - \dots - \cancel{ \left( \frac{8}{9} \right)^{N - 1} } - \cancel{ \left( \frac{8}{9} \right)^{N} } \\
&= \left( \frac{8}{9} \right)^{N + 1} - 1
\end{align}
$$
Si seguimos analizando la misma expresión:
$$
\begin{align}
\sum_{n = 1}^{N + 1} \left( \frac{8}{9} \right)^{n} - \sum_{n = 0}^{N} \left( \frac{8}{9} \right)^{n} &= \sum_{n = 0}^{N} \left( \frac{8}{9} \right)^{n + 1} - \sum_{n = 0}^{N} \left( \frac{8}{9} \right)^{n} \\
&= \sum_{n = 0}^{N} \left( \frac{8}{9} \right)^{n + 1} - \left( \frac{8}{9} \right)^{n} \\
&= \sum_{n = 0}^{N} \left( \frac{8}{9} \right)^{n} \left( \frac{8}{9} - 1 \right) \\
&= \left( \frac{8}{9} - 1 \right) \cdot \sum_{n = 0}^{N} \left( \frac{8}{9} \right)^{n}
\end{align}
$$
Ahora, uniendo los resultados:
$$
\begin{align}
\left( \frac{8}{9} - 1 \right) \cdot \sum_{n = 0}^{N} \left( \frac{8}{9} \right)^{n} &= \left( \frac{8}{9} \right)^{N + 1} - 1 \\
\left( 1 - \frac{8}{9} \right) \cdot \sum_{n = 0}^{N} \left( \frac{8}{9} \right)^{n} &= 1 - \left( \frac{8}{9} \right)^{N + 1} \\
\sum_{n = 0}^{N} \left( \frac{8}{9} \right)^{n} &= \frac{1 - \left( \frac{8}{9} \right)^{N + 1}}{1 - \frac{8}{9}}
\end{align}
$$
Finalmente, encontramos una igualdad que podemos manejar con facilidad. Ahora, queda estudiar el límite de la serie:
$$
\begin{align}
\sum_{n = 0}^{+\infty} \left( \frac{8}{9} \right)^{n} &= \lim_{ N \to \infty } \frac{1 - \left( \frac{8}{9} \right)^{N + 1}}{1 - \frac{8}{9}} \\
&= \frac{\lim_{ N \to \infty } 1 - \lim_{ N \to \infty } \left( \frac{8}{9} \right)^{N + 1}}{\lim_{ N \to \infty } 1 - \lim_{ N \to \infty } \frac{8}{9}} \\
&= \frac{1 - 0}{1 - \frac{8}{9}} \\
&= \frac{1}{ \frac{1}{9} } \\
&= 1 \cdot \frac{9}{1} \\
&= 9
\end{align}
$$

En conclusión:
$$
\sum_{n = 0}^{+\infty} \left( \frac{8}{9} \right)^{n} = 9
$$

Si realizamos el mismo análisis con el perímetro del área pintada:
$$
\sum_{n = 0}^{N} 4 \cdot \left( \frac{8}{3} \right)^{n} = 4 + 4 \cdot \left( \frac{8}{3} \right) + 4 \cdot \left( \frac{8}{3} \right)^{2} + \dots + 4 \cdot \left( \frac{8}{3} \right)^{N}
$$
$$
4 \cdot \sum_{n = 0}^{N} \left( \frac{8}{3} \right)^{n} = 4 \cdot \left( 1 + \left( \frac{8}{3} \right) + \left( \frac{8}{3} \right)^{2} + \dots + \left( \frac{8}{3} \right)^{N} \right)
$$

En realidad, aquí basta con verificar si el término general de la serie converge a 0, para lo que aplicaremos criterio del cociente:
$$
\lim_{ n \to \infty } \frac{\left( \frac{8}{3} \right)^{n + 1}}{\left( \frac{8}{3} \right)^{n}} = \lim_{ n \to \infty } \frac{\left( \frac{8}{3} \right) \cdot \cancel{ \left( \frac{8}{3} \right)^{n} }}{\cancel{ \left( \frac{8}{3} \right)^{n} }} = \lim_{ n \to \infty } \left( \frac{8}{3} \right) > 1
$$
Como el límite obtenido es mayor que 1, según el criterio del cociente, la serie diverge.


