# 1 - Determinantes
## Ejercicio 1.1
### Parte a)
$$
\left|
\begin{array}{ccc}
1 & 1 & 1 \\
-1 & 0 & 1 \\
-1 & -1 & 0
\end{array}
\right|
$$
$$
\left|
\begin{array}{ccc}
1 & 1 & 1 \\
0 & 1 & 2 \\
0 & 0 & 1
\end{array}
\right|
\begin{align}
&F_{2} \leftarrow F_{2} + F_{1} \\
&F_{3} \leftarrow F_{3} + F_{1}
\end{align}
$$
$$
\left|
\begin{array}{ccc}
1 & 1 & 1 \\
0 & 1 & 2 \\
0 & 0 & 1
\end{array}
\right| = 1^{2} \cdot \left|
\begin{array}{cc}
1 & 2 \\
0 & 1
\end{array}
\right| = 1 \times 1 - 0 \times 2 = 1 - 0 = 1
$$
$$
\implies \left|
\begin{array}{ccc}
1 & 1 & 1 \\
-1 & 0 & 1 \\
-1 & -1 & 0
\end{array}
\right| = 1
$$

### Parte d)
$$
\left|
\begin{array}{ccc}
e^{2a} & 0 & e^{a} \\
e^{a} & 0 & 1 \\
0 & 1 & 0
\end{array}
\right|
$$
$$
\left|
\begin{array}{ccc}
1 & 0 & \frac{1}{e^{a}} \\
1 & 0 & \frac{1}{e^{a}} \\
0 & 1 & 0
\end{array}
\right|
\begin{align}
&F_{1} \leftarrow \frac{1}{e^{2a}}F_{1} \\
&F_{2} \leftarrow \frac{1}{e^{a}}F_{2}
\end{align}
$$
$$
\left|
\begin{array}{ccc}
1 & 0 & \frac{1}{e^{a}} \\
0 & 0 & 0 \\
0 & 1 & 0
\end{array}
\right|
\begin{align}
&F_{2} \leftarrow F_{2} - F_{1}
\end{align}
$$
$$
\left|
\begin{array}{ccc}
1 & 0 & \frac{1}{e^{a}} \\
0 & 0 & 0 \\
0 & 1 & 0
\end{array}
\right| = 1^{2} \cdot \left|
\begin{array}{cc}
0 & 0 \\
1 & 0
\end{array}
\right| = 0 \times 0 - 1 \times 0 = 0 - 0 = 0
$$
$$
\left|
\begin{array}{ccc}
e^{2a} & 0 & e^{a} \\
e^{a} & 0 & 1 \\
0 & 1 & 0
\end{array}
\right| = 0
$$

### Parte f)
$$
\left|
\begin{array}{ccc}
0 & 0 & \sin(\theta) \\
\sin(\theta) & \cos(\theta) & \tan(\theta) \\
-\cos(\theta) & \sin(\theta) & -\cos(\theta)
\end{array}
\right|
$$
$$
-\left|
\begin{array}{ccc}
\sin(\theta) & \cos(\theta) & \tan(\theta) \\
0 & 0 & \sin(\theta) \\
-\cos(\theta) & \sin(\theta) & -\cos(\theta)
\end{array}
\right|
\begin{align}
&F_{1} \longleftrightarrow F_{2}
\end{align}
$$
$$
\left|
\begin{array}{ccc}
\sin(\theta) & \cos(\theta) & \tan(\theta) \\
-\cos(\theta) & \sin(\theta) & -\cos(\theta) \\
0 & 0 & \sin(\theta)
\end{array}
\right|
\begin{align}
&F_{2} \longleftrightarrow F_{3}
\end{align}
$$
$$
\sin(\theta) \times \left|
\begin{array}{ccc}
1 & \frac{\cos(\theta)}{\sin(\theta)} & \frac{\tan(\theta)}{\sin(\theta)} \\
-\cos(\theta) & \sin(\theta) & -\cos(\theta) \\
0 & 0 & \sin(\theta)
\end{array}
\right|
\begin{align}
&F_{1} \leftarrow \frac{1}{\sin(\theta)}F_{1}
\end{align}
$$
$$
\sin(\theta) \times \left|
\begin{array}{ccc}
1 & \frac{\cos(\theta)}{\sin(\theta)} & \frac{\tan(\theta)}{\sin(\theta)} \\
0 & \sin(\theta) + \frac{\cos(\theta)^{2}}{\sin(\theta)} & 1 - \cos(\theta) \\
0 & 0 & \sin(\theta)
\end{array}
\right|
\begin{align}
&F_{2} \leftarrow F_{2} + \cos(\theta)F_{1}
\end{align}
$$
$$
\sin(\theta) \times \left|
\begin{array}{ccc}
1 & \frac{\cos(\theta)}{\sin(\theta)} & \frac{\tan(\theta)}{\sin(\theta)} \\
0 & \sin(\theta) + \frac{\cos(\theta)^{2}}{\sin(\theta)} & 1 - \cos(\theta) \\
0 & 0 & \sin(\theta)
\end{array}
\right| = \sin(\theta) \times 1 ^{2} \times \left| \begin{array}{cc}
\sin(\theta) + \frac{\cos(\theta)^{2}}{\sin(\theta)} & 1 - \cos(\theta) \\
0 & \sin(\theta)
\end{array}
\right|
$$
$$
\sin(\theta) \times \left| \begin{array}{cc}
\sin(\theta) + \frac{\cos(\theta)^{2}}{\sin(\theta)} & 1 - \cos(\theta) \\
0 & \sin(\theta)
\end{array}
\right| = \sin(\theta) \times \left( \left( \sin(\theta) + \frac{\cos(\theta)^{2}}{\sin(\theta)} \right) \times \sin(\theta) - \cancel{ 0 \times (1 - \cos(\theta)) } \right)
$$
$$
= \sin(\theta) \times \left( \left( \sin(\theta) + \frac{\cos(\theta)^{2}}{\sin(\theta)} \right) \times \sin(\theta) \right) = \sin(\theta) \times (\sin(\theta)^{2} + \cos(\theta)^{2}) = \sin(\theta) \times 1 = \sin(\theta)
$$
$$
\implies \left|
\begin{array}{ccc}
0 & 0 & \sin(\theta) \\
\sin(\theta) & \cos(\theta) & \tan(\theta) \\
-\cos(\theta) & \sin(\theta) & -\cos(\theta)
\end{array}
\right| = \sin(\theta)
$$

### Parte k)
$$
\left|
\begin{array}{ccc}
1 + i & 2 & 3i \\
2 - i & 1 + 2i & 1 \\
3 & -i & 2 + i
\end{array}
\right|
$$
$$
-\left|
\begin{array}{ccc}
3 & -i & 2 + i \\
2 - i & 1 + 2i & 1 \\
1 + i & 2 & 3i
\end{array}
\right|
\begin{align}
&F_{1} \longleftrightarrow F_{3}
\end{align}
$$
$$
\left|
\begin{array}{ccc}
3 & -i & 2 + i \\
1 + i & 2 & 3i \\
2 - i & 1 + 2i & 1
\end{array}
\right|
\begin{align}
&F_{2} \longleftrightarrow F_{3}
\end{align}
$$
$$
3 \times \left|
\begin{array}{ccc}
1 & -\frac{1}{3}i & \frac{2}{3} + \frac{1}{3}i \\
1 + i & 2 & 3i \\
2 - i & 1 + 2i & 1
\end{array}
\right|
\begin{align}
&F_{1} \leftarrow \frac{1}{3}F_{1}
\end{align}
$$
$$
3 \times \left|
\begin{array}{ccc}
1 & -\frac{1}{3}i & \frac{2}{3} + \frac{1}{3}i \\
0 & \frac{5}{3} - \frac{1}{3}i & -\frac{1}{3} + 2i \\
0 & \frac{4}{3} + \frac{8}{3}i & 1
\end{array}
\right|
\begin{align}
&F_{2} \leftarrow F_{2} - (1 + i)F_{1} \\
&F_{3} \leftarrow F_{3} - (2 - i)F_{1}
\end{align}
$$
$$
3 \times \left|
\begin{array}{ccc}
1 & -\frac{1}{3}i & \frac{2}{3} + \frac{1}{3}i \\
0 & \frac{5}{3} - \frac{1}{3}i & -\frac{1}{3} + 2i \\
0 & \frac{4}{3} + \frac{8}{3}i & -\frac{2}{3}
\end{array}
\right| = 3 \times 1^{2} \times \left|
\begin{array}{ccc}
\frac{5}{3} - \frac{1}{3}i & -\frac{1}{3} + 2i \\
\frac{4}{3} + \frac{8}{3}i & -\frac{2}{3}
\end{array}
\right|
$$
$$
= 3 \times \left|
\begin{array}{ccc}
\frac{5}{3} - \frac{1}{3}i & -\frac{1}{3} + 2i \\
\frac{4}{3} + \frac{8}{3}i & -\frac{2}{3}
\end{array}
\right| = 3 \times \left( \left( \frac{5}{3} - \frac{1}{3}i \right)\left( -\frac{2}{3} \right) - \left( \frac{4}{3} + \frac{8}{3}i \right)\left( -\frac{1}{3} + 2i \right) \right) 
$$
$$
= 3 \times \left( -\frac{10}{9} + \frac{2}{9}i - \left( \frac{52}{9} + \frac{19}{9}i \right) \right) = 3 \times \left( -\frac{10}{9} + \frac{2}{9}i - \frac{52}{9} - \frac{19}{9}i \right) = 3 \times \left( -\frac{62}{9} - \frac{17}{9}i \right)
$$
$$
= -\frac{62}{3} - \frac{17}{3}i
$$
$$
\implies \left|
\begin{array}{ccc}
1 + i & 2 & 3i \\
2 - i & 1 + 2i & 1 \\
3 & -i & 2 + i
\end{array}
\right| = -\frac{62}{3} - \frac{17}{3}i
$$

## Ejercicio 1.2

$$
\left|
\begin{array}{ccc}
a & b & c \\
d & e & f \\
g & h & j
\end{array}
\right| = 5
$$

### Parte a)
$$
\left|
\begin{array}{ccc}
d & e & f \\
g & h & j \\
a & b & c
\end{array}
\right| = \text{?}
$$
$$
\left|
\begin{array}{ccc}
d & e & f \\
g & h & j \\
a & b & c
\end{array}
\right| = -\left|
\begin{array}{ccc}
a & b & c \\
g & h & j \\
d & e & f
\end{array}
\right| = \left|
\begin{array}{ccc}
a & b & c \\
d & e & f \\
g & h & j
\end{array}
\right| = 5
$$
$$
\implies \left|
\begin{array}{ccc}
d & e & f \\
g & h & j \\
a & b & c
\end{array}
\right| = 5
$$
### Parte b)
$$
\left|
\begin{array}{ccc}
-a & -b & -c \\
2d & 2e & 2f \\
-g & -h & -j
\end{array}
\right| = \text{?}
$$
$$
\left|
\begin{array}{ccc}
-a & -b & -c \\
2d & 2e & 2f \\
-g & -h & -j
\end{array}
\right| = - \left|
\begin{array}{ccc}
a & b & c \\
2d & 2e & 2f \\
-g & -h & -j
\end{array}
\right| = \left|
\begin{array}{ccc}
a & b & c \\
2d & 2e & 2f \\
g & h & j
\end{array}
\right| = 2 \times \left|
\begin{array}{ccc}
a & b & c \\
d & e & f \\
g & h & j
\end{array}
\right| = 2 \times 5 = 10
$$
$$
\implies \left|
\begin{array}{ccc}
-a & -b & -c \\
2d & 2e & 2f \\
-g & -h & -j
\end{array}
\right| = 10
$$

### Parte c)
$$
\left|
\begin{array}{ccc}
a & b & c \\
d - 3a & e - 3b & f - 3c \\
2g & 2h & 2j
\end{array}
\right| = \text{?}
$$
$$
\left|
\begin{array}{ccc}
a & b & c \\
d - 3a & e - 3b & f - 3c \\
2g & 2h & 2j
\end{array}
\right| = \left|
\begin{array}{ccc}
a & b & c \\
d & e & f \\
2g & 2h & 2j
\end{array}
\right| + \left|
\begin{array}{ccc}
a & b & c \\
-3a & -3b & -3c \\
2g & 2h & 2j
\end{array}
\right| = 2 \times \left|
\begin{array}{ccc}
a & b & c \\
d & e & f \\
g & h & j
\end{array}
\right| + 2 \times \left|
\begin{array}{ccc}
a & b & c \\
-3a & -3b & -3c \\
g & h & j
\end{array}
\right|
$$
$$
= 2 \times \left|
\begin{array}{ccc}
a & b & c \\
d & e & f \\
g & h & j
\end{array}
\right| + 2 \times \underbrace{ \left|
\begin{array}{ccc}
a & b & c \\
0 & 0 & 0 \\
g & h & j
\end{array}
\right| }_{ F_{2} \leftarrow F_{2} + 3F_{1} } = 2 \times \left|
\begin{array}{ccc}
a & b & c \\
d & e & f \\
g & h & j
\end{array}
\right| = 2 \times 5 = 10
$$
$$
\implies \left|
\begin{array}{ccc}
a & b & c \\
d - 3a & e - 3b & f - 3c \\
2g & 2h & 2j
\end{array}
\right| = 10
$$

### Parte d)
$$
\left|
\begin{array}{ccc}
a + 5c & 3b & c \\
d + 5f & 3e & f \\
2g + 10j & 6h & 2j
\end{array}
\right| = \text{?}
$$
$$
\left|
\begin{array}{ccc}
a + 5c & 3b & c \\
d + 5f & 3e & f \\
2g + 10j & 6h & 2j
\end{array}
\right| = \left|
\begin{array}{ccc}
a & 3b & c \\
d & 3e & f \\
2g & 6h & 2j
\end{array}
\right| + \left|
\begin{array}{ccc}
5c & 3b & c \\
5f & 3e & f \\
10j & 6h & 2j
\end{array}
\right| = \left|
\begin{array}{ccc}
a & 3b & c \\
d & 3e & f \\
2g & 6h & 2j
\end{array}
\right| + \underbrace{ \left|
\begin{array}{ccc}
0 & 3b & c \\
0 & 3e & f \\
0 & 6h & 2j
\end{array}
\right| }_{ C_{1} \leftarrow C_{1} - 5C_{3} } = \left|
\begin{array}{ccc}
a & 3b & c \\
d & 3e & f \\
2g & 6h & 2j
\end{array}
\right| + 0
$$
$$
\left|
\begin{array}{ccc}
a & 3b & c \\
d & 3e & f \\
2g & 6h & 2j
\end{array}
\right| = 2 \times \left|
\begin{array}{ccc}
a & 3b & c \\
d & 3e & f \\
g & 3h & j
\end{array}
\right| = 2 \times 3 \times \left|
\begin{array}{ccc}
a & b & c \\
d & e & f \\
g & h & j
\end{array}
\right| = 2 \times 3 \times 5 = 30
$$
$$
\implies \left|
\begin{array}{ccc}
a + 5c & 3b & c \\
d + 5f & 3e & f \\
2g + 10j & 6h & 2j
\end{array}
\right| = 30
$$

## Ejercicio 1.3
### Parte a)
$$
\left|
\begin{array}{ccc}
k & -k & 3 \\
0 & k + 1 & 1 \\
k & -8 & k - 1
\end{array}
\right| = \text{?}
$$
$$
\left|
\begin{array}{ccc}
k & 1 & 4 \\
0 & k + 1 & 1 \\
k & -8 & k - 1
\end{array}
\right|
\begin{align}
&F_{1} \leftarrow F_{1} + F_{2}
\end{align}
$$
$$
\left|
\begin{array}{ccc}
k & 1 & 4 \\
0 & k + 1 & 1 \\
0 & -9 & k - 5
\end{array}
\right|
\begin{align}
&F_{3} \leftarrow F_{3} - F_{1}
\end{align}
$$
$$
\left|
\begin{array}{ccc}
k & 1 & 4 \\
0 & k + 1 & 1 \\
0 & -9 & k - 5
\end{array}
\right| = k \times \left|
\begin{array}{ccc}
k + 1 & 1 \\
-9 & k - 5
\end{array}
\right| = k \times ((k + 1)(k - 5) - ((-9) \times 1))
$$
$$
= k \times ((k^{2} - 5k + k - 5) - (-9)) = k \times (k^{2} - 5k + k - 5 + 9) = k \times (k^{2} - 4k + 4)
$$
Hay que calcular las raíces de $k^{2} - 4k + 4$
$$
\begin{align}
&a = 1 \\
&b = -4 \\
&c = 4
\end{align}
$$
$$
\begin{align}
&k = \frac{4 \pm \sqrt{ (-4)^{2} - 4 \times 1 \times 4 }}{2 \times 1} \\
&k = \frac{4 \pm \sqrt{ 16 - 16 }}{2} \\
&k = \frac{4 \pm \sqrt{ 0 }}{2} \\
&k = \frac{4 \pm 0}{2} \\
\end{align}
$$
$$
\begin{align}
&\implies &&k_{1} = \frac{4 + 0}{2} = \frac{4}{2} = 2 \\
&&&k_{2} = \frac{4 - 0}{2} = \frac{4}{2} = 2
\end{align}
$$
También lo podríamos determinar por factorización:
$$
k^{2} - 4k + 4 = (k - 2)(k - 2) = (k - 2)^{2}
$$
De esta forma, sabemos que $k \times (k^{2} - 4k + 4) = 0$, si
$$
k = 0 \qquad \text{o} \qquad k = 2
$$

Por lo tanto:
$$
\left|
\begin{array}{ccc}
k & -k & 3 \\
0 & k + 1 & 1 \\
k & -8 & k - 1
\end{array}
\right| = 0 \qquad \text{(no es invertible) para} \qquad k = 0 \text{ o } k = 2
$$

### Parte b)
$$
\left|
\begin{array}{ccc}
k & k & 0 \\
k^{2} & 4 & k^{2} \\
0 & k & k
\end{array}
\right| = \text{?}
$$
$$
\left|
\begin{array}{ccc}
k & k & 0 \\
0 & 4 - k^{2} & k^{2} \\
0 & k & k
\end{array}
\right|
\begin{align}
&F_{2} \leftarrow F_{2} - kF_{1}
\end{align}
$$
$$
\left|
\begin{array}{ccc}
k & k & 0 \\
0 & 4 - 2k^{2} & 0 \\
0 & k & k
\end{array}
\right|
\begin{align}
&F_{2} \leftarrow F_{2} - kF_{3}
\end{align}
$$
Desarrollamos por la primer columna:
$$
\left|
\begin{array}{ccc}
k & k & 0 \\
0 & 4 - 2k^{2} & 0 \\
0 & k & k
\end{array}
\right| = k \times \left( (4 - 2k^{2})k - k \times 0 \right) = k \times \left( (4 - 2k^{2})k \right) = k \times k \times (4 - 2k^{2}) = k \times k \times 2 (2 - k^{2})
$$
Nuevamente, tenemos que determinar las raíces de $2 - k^{2}$. Vamos a factorizarlo:
$$
2 - k^{2} = (\sqrt{ 2 } - k)(\sqrt{ 2 } + k)
$$
De esta forma, podemos determinar que:
$$
\text{Si } k = \pm \sqrt{ 2 } \implies 2 - k^{2} = 0
$$
En conclusión:
$$
k \times k \times 2 (2 - k^{2}) = 0 \qquad (\text{para } k = \pm \sqrt{ 2 } \text{ o } k = 0)
$$
Por lo tanto:
$$
\left|
\begin{array}{ccc}
k & k & 0 \\
k^{2} & 4 & k^{2} \\
0 & k & k
\end{array}
\right| = 0 \qquad \text{(no es invertible) para} \qquad k = 0 \text{ o } k = \pm \sqrt{ 2 }
$$

### Parte c)
$$
\left|
\begin{array}{ccc}
k - 4 & 0 & 0 \\
1 & k & 2 \\
3 & 3 & k - 1
\end{array}
\right| = \text{?}
$$
$$
\left|
\begin{array}{ccc}
k - 4 & 0 & 0 \\
1 & k & 2 \\
3 & 3 & k - 1
\end{array}
\right| = (k - 4) \times \left( k(k - 1) - 3 \times 2 \right) = (k - 4) \times \left( k^{2} - k - 6 \right)
$$
Básicamente, tenemos que calcular las raíces de $k^{2} - k - 6$, y lo haremos factorizando:
$$
k^{2} - k - 6 = (k - 3)(k + 2)
$$
De esta forma, podemos determinar que:
$$
\text{Si } k = 3 \text{ o } k = -2 \implies k^{2} - k - 6 = 0
$$
En conclusión:
$$
(k - 4) \times \left( k^{2} - k - 6 \right) = 0 \qquad (\text{para } k = 0, k = 3 \text{ o } k = -2)
$$
Por lo tanto:
$$
\left|
\begin{array}{ccc}
k - 4 & 0 & 0 \\
1 & k & 2 \\
3 & 3 & k - 1
\end{array}
\right| = 0 \qquad \text{(no es invertible) para} \qquad k = 0, k = 3 \text{ o } k = -2
$$

## Ejercicio 1.4
### Parte a)
#### a)
$$
\det(-AB) = (-1)^{n} \cdot \det(AB) = (-1)^{n} \cdot (\det(A) \cdot \det(B)) = (-1)^{n} \times (3 \times (-2))
$$
$$
= (-1)^{n} \times (-6) = (-1)^{n + 1} \times 6
$$

#### b)
$$
\det(A^{2}) = \det(AA) = \det(A) \cdot \det(A) = 3 \times 3 = 9
$$

#### c)
$$
\det(B^{-1}A) = \det(B^{-1}) \cdot \det(A) = \frac{1}{\det (B)} \cdot \det(A) = - \frac{1}{2} \times 3 = -\frac{3}{2}
$$

#### d)
$$
\det(2A) = 2^{n} \cdot \det(A) = 2^{n} \times 3
$$

#### e)
$$
\det(3B^{T}) = 3^{n} \cdot \det(B^{T}) = 3^{n} \cdot \det(B) = 3^{n} \times (-2)
$$

#### f)
$$
\det(AA^{T}) = \det(A) \cdot \det(A^{T}) = \det(A) \cdot \det(A) = 3 \times 3 = 9
$$

### Parte b)
$$
\det(A^{T} C^{-1} B^{-1} (3D^{T})^{-1}) - \det(4CD^{-1} (A^{-1} B)^{T})
$$

Comenzamos calculando $\det(A^{T} C^{-1} B^{-1} (3D^{T})^{-1})$:
$$
\det(A^{T} C^{-1} B^{-1} (3D^{T})^{-1}) = \det(A^{T}) \cdot \det(C^{-1}) \cdot \det(B^{-1}) \cdot \det((3D^{T})^{-1})
$$
$$
= \det(A) \cdot \frac{1}{\det(C)} \cdot \frac{1}{\det(B)} \cdot \frac{1}{\det(3D^{T})} = \det(A) \cdot \frac{1}{\det(C)} \cdot \frac{1}{\det(B)} \cdot \frac{1}{\det(3D)}
$$
$$
= \det(A) \cdot \frac{1}{\det(C)} \cdot \frac{1}{\det(B)} \cdot \frac{1}{3^{5} \det(D)} = \det(A) \cdot \frac{1}{\det(C)} \cdot \frac{1}{\det(B)} \cdot \frac{1}{3^{5} \cdot \det(D)}
$$
$$
= \det(A) \cdot \frac{1}{\det(C)} \cdot \frac{1}{\det(B)} \cdot \frac{1}{243 \cdot \det(D)} = \det(A) \cdot \frac{1}{4} \cdot \frac{1}{\det(B)} \cdot \frac{1}{243 \times 2}
$$
$$
= \det(A) \cdot \frac{1}{4} \cdot \frac{1}{\det(B)} \cdot \frac{1}{486}
$$
Como $\det(A) = \det(B) \neq 0$:
$$
= \det(A) \cdot \frac{1}{4} \cdot \frac{1}{\det(A)} \cdot \frac{1}{486} = \frac{1}{4} \cdot \frac{\det(A)}{\det(A)} \cdot \frac{1}{486} = \frac{1}{4} \times 1 \times \frac{1}{486} = \frac{1}{486 \times 4} = \frac{1}{1944}
$$

Proseguimos con $\det(4CD^{-1} (A^{-1} B)^{T})$:
$$
\det(4CD^{-1} (A^{-1} B)^{T}) = \det(4CD^{-1}) \cdot \det((A^{-1} B)^{T}) = \det(4CD^{-1}) \cdot \det(A^{-1} B)
$$
$$
= \det(4CD^{-1}) \cdot \det(A^{-1}) \cdot \det(B) = 4^{5} \cdot \det(CD^{-1}) \cdot \det(A^{-1}) \cdot \det(B)
$$
$$
= 4^{5} \cdot \det(C) \cdot \det(D^{-1}) \cdot \det(A^{-1}) \cdot \det(B) = 1024 \cdot \det(C) \cdot \det(D^{-1}) \cdot \det(A^{-1}) \cdot \det(B)
$$
$$
= 1024 \cdot \det(C) \cdot \frac{1}{\det(D)} \cdot \frac{1}{\det(A)} \cdot \det(B) = 1024 \times 4 \times \frac{1}{2} \cdot \frac{1}{\det(A)} \cdot \det(B)
$$
Como $\det(A) = \det(B) \neq 0$:
$$
= 1024 \times 4 \times \frac{1}{2} \cdot \frac{1}{\det(A)} \cdot \det(A) = 1024 \times 4 \times \frac{1}{2} \cdot \frac{\det(A)}{\det(A)} = 1024 \times 4 \times \frac{1}{2} \times 1
$$
$$
= 1024 \times 2 = 2048
$$

De esta forma:
$$
\det(A^{T} C^{-1} B^{-1} (3D^{T})^{-1}) - \det(4CD^{-1} (A^{-1} B)^{T}) = \frac{1}{1944} - 2048 = \frac{1}{1944} - \frac{3981312}{1944} = - \frac{3981311}{1944}
$$

## Ejercicio 1.5
Para facilitar el cálculo de la matriz provista, podemos escalerizarla, hasta alcanzar una matriz triangular superior. Para esto, a todas las filas le restaremos la primera, con tal de llegar la forma deseada:
$$
\left|
\begin{array}{cccccc}
1 & 1 & 1 & \dots & 1 & 1 \\
1 & 0 & 1 & \dots & 1 & 1 \\
1 & 1 & 0 & \dots & 1 & 1 \\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots \\
1 & 1 & 1 & \dots & 0 & 1 \\
1 & 1 & 1 & \dots & 1 & 0
\end{array}
\right|
$$
$$
\left|
\begin{array}{cccccc}
1 & 1 & 1 & \dots & 1 & 1 \\
0 & -1 & 0 & \dots & 0 & 0 \\
0 & 0 & -1 & \dots & 0 & 0 \\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots \\
0 & 0 & 0 & \dots & -1 & 0 \\
0 & 0 & 0 & \dots & 0 & -1
\end{array}
\right|
\begin{align}
&F_{2} \leftarrow F_{2} - F_{1} \\
&F_{3} \leftarrow F_{3} - F_{1} \\
&\dots \leftarrow \dots - F_{1} \\
&F_{n - 1} \leftarrow F_{n - 1} - F_{1} \\
&F_{n} \leftarrow F_{n} - F_{1}
\end{align}
$$
De esta forma, tenemos un total de $n - 1$ -1s, y como la matriz está en forma triangular superior, el determinante se calcula mediante el producto de los elementos de la diagonal:
$$
\left|
\begin{array}{cccccc}
1 & 1 & 1 & \dots & 1 & 1 \\
0 & -1 & 0 & \dots & 0 & 0 \\
0 & 0 & -1 & \dots & 0 & 0 \\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots \\
0 & 0 & 0 & \dots & -1 & 0 \\
0 & 0 & 0 & \dots & 0 & -1
\end{array}
\right| = 1 \times \underbrace{ (-1) \times (-1) \times \dots \times (-1) \times (-1) }_{ n - 1 \text{ veces} }
$$
$$
\left|
\begin{array}{cccccc}
1 & 1 & 1 & \dots & 1 & 1 \\
0 & -1 & 0 & \dots & 0 & 0 \\
0 & 0 & -1 & \dots & 0 & 0 \\
\vdots & \vdots & \vdots & \vdots & \vdots & \vdots \\
0 & 0 & 0 & \dots & -1 & 0 \\
0 & 0 & 0 & \dots & 0 & -1
\end{array}
\right| = 1 \times (-1)^{n - 1} = (-1)^{n - 1}
$$
De esta forma, para cualquier matriz de la forma provista, su determinante se calcula con la fórmula $(-1)^{n - 1}$, siendo $n$ el tamaño de la matriz. De esta manera, si $n$ es par, el determinante es 1, siendo -1 en caso contrario.

---
# 2 - Matrices especiales

## Ejercicio 2.1

Sea $A \in M_{n \times n}$ una matriz antisimétrica con $n$ impar, por lo que
$$
A^{T} = -A
$$
De esta forma, deducimos que:
$$
\det(A^{T}) = \det(-A) = (-1)^{n} \cdot \det(A)
$$
Sin embargo, sabemos que
$$
\det(A^{T}) = \det(A)
$$
Por lo tanto:
$$
\det(A) = (-1)^{n} \cdot \det(A)
$$

Como $n$ es impar, entonces $(-1)^{n} = -1$, por lo tanto:
$$
\det(A) = (-1)^{n} \cdot \det(A) = - \det(A)
$$

Sabiendo que el determinante es un número, el cual es equivalente a su opuesto, el único valor que cumple con dicha característica es 0. En conclusión:
$$
\det(A) = -\det(A) = 0
$$

## Ejercicio 2.2

Sea $A \in M_{n \times n}$ una matriz nilpotente. De esta forma, existe algún número natural $k$, tal que $A^{k} = O$. Por esta razón:
$$
\det(A^{k}) = 0
$$
De esta forma, también podemos desarrollar $\det(A^{k})$:
$$
\det(A^{k}) = k^{n} \cdot \det(A) = 0
$$
Como $k^{n} \cdot \det(A) = 0$, con $k \in \mathbb{N}, k \neq 0$, es necesario que $\det(A) = 0$. Por lo tanto, para cualquier matriz nilpotente, su determinante es nulo.