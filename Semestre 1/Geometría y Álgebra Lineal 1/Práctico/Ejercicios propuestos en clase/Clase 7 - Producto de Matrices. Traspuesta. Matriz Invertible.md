Mostrar que toda matriz cuadrada $A \in M_{n \times n}$ se puede escribir
$$
A = A_{1} + A_{2} \text{ donde } A_{1} \text{ es simétrica, y } A_{2} \text{ es antisimétrica}
$$
Segunda pregunta: demostrar que esta descomposición es única.

Sugerencia: tomar
$$
\begin{align}
&A_{1} = \frac{1}{2}(A + A^{t}) \\
&A_{2} = \frac{1}{2}(A - A^{t}) \\
&\implies A_{1} + A_{2} = A \\
 \\
&\text{Además:} \\
&A_{1}^{t} = \frac{1}{2}(A + A^{t})^{t} = \frac{1}{2}(A^{t} + (A^{t})^{t}) = \frac{1}{2}(A^{t} + A) = A_{1} \\
&A_{2}^{t} = \frac{1}{2}(A - A^{t})^{t} = \frac{1}{2}(A^{t} - (A^{t})^{t}) = \frac{1}{2}(A^{t} - A) = -A_{2}
\end{align}
$$
De esta forma, $A_{1}^{t} = A_{1}$ ($A_{1}$ es simétrica), y $A_{2}^{t} = -A_{2}$ ($A_{2}$ es antisimétrica).
Lo interesante es que no es necesario analizar los coeficientes internos, es una demostración puramente matemática.