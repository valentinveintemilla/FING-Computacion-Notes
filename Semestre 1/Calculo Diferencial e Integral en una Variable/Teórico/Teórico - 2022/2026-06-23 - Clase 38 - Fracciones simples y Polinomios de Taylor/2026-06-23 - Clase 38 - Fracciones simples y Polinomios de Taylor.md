En esta clase, finalizaremos el tema de fracciones simples y se aborda el último capítulo del libro: Polinomios de Taylor.

Igualmente, en el curso de 2026, no se aborda con esta clase, sino con el teórico de 2017.

Recordamos el método de fracciones simples:
Nos permite integrar cualquier cociente de polinomios presentado.

Básicamente se reduce el problema a expresar el cociente como la suma de varias fracciones más simples. Para esto, se deben seguir una serie de pasos aplicados a un cociente de polinomios donde el numerador tiene grado menor que el denominador, en función de como se factorice el denominador, podemos descomponer la expresión en una suma de términos, los cuales son fracciones más simples que sabemos integrar.

No enunciamos el teorema de fracciones simples, aunque abordamos su uso y utilidad con ejemplos.

Abordando un ejemplo:
$$
\frac{5x^{4} + 3x + 1}{(x - 1) (x - 2)^{2} (x^{2} + x + 5) (x^{2} + 2x + 3)}
$$
donde $x^{2} + x + 5$ y $x^{2} + 2x + 3$ no tienen raíces reales. En caso de que tuvieran raíces reales, tendríamos que factorizarlos (descomponerlos en un producto de polinomios más simples).

En base a las reglas vistas la clase pasada:
$$
\frac{5x^{4} + 3x + 1}{(x - 1) (x - 2)^{2} (x^{2} + x + 5) (x^{2} + 2x + 3)} = \frac{A}{x - 1} + \frac{B}{x - 2} + \frac{C}{(x - 2)^{2}} + \frac{Dx + E}{x^{2} + x + 5} + \frac{Fx + G}{x^{2} + 2x + 3}
$$

Existían dos métodos para hallar las constantes:
1. Desarrollar denominador común y resolver el sistema conociendo el numerador inicial (algo costoso).
2. Aplicar el método de la tapadita (más simple y explicado en el libro).

Para completar el método, hay que enunciar una observación:

Hasta ahora, hemos trabajado con el denominador factorizado, pareciendo que solo funciona para polinomios que tienen cierto nivel de factorización. Sin embargo, en realidad se puede demostrar (no lo haremos) que dado cualquier polinomio, el mismo se puede factorizar con polinomios de grado 1 o grado 2 (sin raíces reales).

Hasta ahora, algo que no hemos visto y podría ocurrir, es que apareciera en la factorización un polinomio de grado 2 que tuviese multiplicidad. Por ejemplo, que en lugar de $(x^{2} + 2x + 3)$, tuviéramos $(x^{2} + 2x + 3)^{2}$.

¿Cómo se descompone la función en este caso? Es similar al caso de un polinomio de grado 1 con multiplicidad:

$$
\frac{5x^{4} + 3x + 1}{(x - 1) (x - 2)^{2} (x^{2} + x + 5) (x^{2} + 2x + 3)^{2}} = \frac{A}{x - 1} + \frac{B}{x - 2} + \frac{C}{(x - 2)^{2}} + \frac{Dx + E}{x^{2} + x + 5} + \frac{Fx + G}{x^{2} + 2x + 3} + \frac{Hx + I}{(x^{2} + 2x + 3)^{2}}
$$

No abordaremos dicho caso durante el curso, aunque es importante entender como se maneja dicho caso. Su integración es algo más compleja y no forma parte del programa, aunque si es de interés, en el libro de Apostol se detalla como trabajar con dichos polinomios.

Hasta aquí va la clase de hoy, ya que a partir de este momento, se aborda el tema "Polinomios de Taylor".