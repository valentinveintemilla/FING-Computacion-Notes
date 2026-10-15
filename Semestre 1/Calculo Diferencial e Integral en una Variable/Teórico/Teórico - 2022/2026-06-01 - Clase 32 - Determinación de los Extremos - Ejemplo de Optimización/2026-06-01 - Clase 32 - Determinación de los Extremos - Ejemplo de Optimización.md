Comenzamos en el minuto 35.
# Concavidad

## Signo de la derivada

Cuando estudiamos el signo de la derivada, podemos determinar cuando crece y cuando decrece, que es algo de información sobre la función. Sin embargo, no sabemos hacia donde se curva la función. Esto es la concavidad de la función, hacia donde se "dobla la función en ese momento"

![[Semestre 1/Calculo Diferencial e Integral en una Variable/Teórico/Teórico - 2022/2026-06-01 - Clase 32 - Determinación de los Extremos - Ejemplo de Optimización/Imágenes/1 - Signo de la derivada.png]]

Muchas veces, nos referíamos a la concavidad de una función como "feliz" (positiva) o "triste" (negativa). En realidad, hay una relación con la concavidad de la función y las pendientes de las rectas tangentes a la función punto a punto. En realidad, lo que sucede en cada uno de los casos es que las pendientes de las rectas tangentes crecen (concavidad positiva), o decrecen (concavidad negativa).

![[Semestre 1/Calculo Diferencial e Integral en una Variable/Teórico/Teórico - 2022/2026-06-01 - Clase 32 - Determinación de los Extremos - Ejemplo de Optimización/Imágenes/2 - Concavidad.png]]

## Derivada segunda

Lo interesante aquí es que, estudiando el crecimiento o decrecimiento de $f'$, sabemos como se curva el gráfico. Ahora, la pregunta es, ¿Qué herramienta nos da dicha información? La respuesta es el signo de la derivada de $f'$, $f''$, o la derivada segunda de $f$.

Si la derivada segunda de $f$ es positiva en un intervalo, entonces la derivada primera está creciendo en dicho intervalo (aumenta a medida que aumenta $x$), por lo que la concavidad es positiva (en ese intervalo). Si $f''$ es negativa, es el caso contrario.

IMPORTANTE: SIEMPRE NOS REFERIMOS A UN INTERVALO, NO TIENE PORQUE DARSE EN TODA LA FUNCIÓN.

Puede suceder que en una función tengamos cambios de concavidad (de signo), lo que se llama "puntos de inflexión".

### Ejemplos:
$$
f''(x) > 0 \qquad \forall x
$$
![[Semestre 1/Calculo Diferencial e Integral en una Variable/Teórico/Teórico - 2022/2026-06-01 - Clase 32 - Determinación de los Extremos - Ejemplo de Optimización/Imágenes/3 - Ejemplo 1.png]]

### Derivada segunda y clasificación de puntos críticos
Los puntos críticos son aquellos en los que se anula la derivada. Aquí, podemos tener un máximo relativo, mínimo relativo, o ninguna de las dos. La derivada segunda nos permite clasificar dichos puntos sin conocer el signo de la función.

Esto es muy útil, ya que no siempre es sencillo determinar el signo de $f'$, pues rara vez hallamos las raíces. Sin embargo, si tenemos un punto crítico, podemos determinar la derivada de $f'$ en el punto crítico (sin conocer el signo de toda la función, puesto que necesitamos todas las raíces). 

Cuando hablamos de puntos críticos, estamos hablando de puntos en los cuales la derivada es 0. Tomando como referencia esto, podemos considerar la derivada segunda en dicho punto:
- Si es positiva ($f''(a) > 0$), entonces se trata de un mínimo relativo.
- Si es negativa ($f''(a) < 0$), entonces se trata de un máximo relativo.
![[Semestre 1/Calculo Diferencial e Integral en una Variable/Teórico/Teórico - 2022/2026-06-01 - Clase 32 - Determinación de los Extremos - Ejemplo de Optimización/Imágenes/4 - Extremos relativos.png]]

Respecto al criterio de clasificación:
Si $c$ es punto crítico y $f''(c) = 0$, entonces no podemos determinar nada, puede pasar cualquier cosa (mínimo relativo, máximo relativo, o ninguno de los dos).

Por ejemplo:
$x^{3}, x^{4}, - x^{4}$ en 0.

Dichas funciones tienen puntos críticos en 0, pero la derivada segunda de dichas funciones en 0 es 0. Por lo tanto, no podemos tomar como referencia dicho resultado en caso de que la derivada segunda se anule.
En los tres suceden cosas distintas:
- $x^{4}$: mínimo relativo en 0.
- $-x^{4}$: mínimo máximo en 0.
- $x^{3}$: ninguno de los dos casos.

Concluimos con los usos de la derivada segunda para determinar la concavidad de la función, además de hallar extremos relativos.

Finalizamos en el minuto 65.