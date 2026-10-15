# Ejercicio 1
Demostrar que
$$
\log \sqrt{ x } = \frac{1}{2} \log x
$$
$$
\frac{1}{2} \log x = \frac{1}{2} \log (\sqrt{ x } \times \sqrt{ x }) = \frac{1}{2}(\log \sqrt{ x } + \log \sqrt{ x }) = \frac{1}{2} \log \sqrt{ x } + \frac{1}{2} \log \sqrt{ x } = \frac{2}{2} \log \sqrt{ x } = \log \sqrt{ x }
$$
Esta es una posible justificación de la notación $x^{\frac{1}{2}} = \sqrt{ x }$.

# Ejercicio 2
Demostrar que
$$
\log(x^{n}) = n \cdot \log x
$$
$$
\log(x^{n}) = \log\left( \prod_{i = 1}^{n} x \right) = \sum_{i = 1}^{n} \log(x) = n \cdot \log(x)
$$
De esta forma, podemos decir que:
$$
\log \left( \prod_{i = 1}^{n} a_{i} \right) = \sum_{i = 1}^{n} \log (a_{i})
$$
Siguiendo esta misma lógica:
$$
\log n! = \log \left( \prod_{i = 1}^{n} i \right) = \sum_{i = 1}^{n} \log i
$$

En lugar de hacerlo así, habría que utilizarse la demostración por inducción (o demostrar por inducción la generalización de productoria y sumatoria).

# Ejercicio 3
Demostrar que
$$
\log(\sqrt[n]{ x }) = \frac{1}{n} \log x \qquad (\forall n \geq 1)
$$
$$
\log(\sqrt[n]{ x }) = \frac{n}{n} \log(\sqrt[n]{ x }) = \frac{1}{n}n \cdot \log (\sqrt[n]{ x }) = \frac{1}{n}\log ((\sqrt[n]{ x })^{n}) = \frac{1}{n} \log x
$$