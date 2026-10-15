# Cheat Sheet de Notación Matemática para Obsidian (LaTeX / MathJax)

Esta hoja resume la mayoría de símbolos y notaciones matemáticas utilizadas en:

- matemática
- ingeniería
- física
- informática teórica

En Obsidian:

- Inline: `$formula$` $formula$
- Bloque: `$$formula$$`

$$
formula
$$

---

# 1. Operaciones básicas

| Símbolo | Código |
|-------|------|
| + | `+` |
| − | `-` |
| ± | `\pm` |
| ∓ | `\mp` |
| × | `\times` |
| ÷ | `\div` |
| · | `\cdot` |
| ∘ | `\circ` |
| √ | `\sqrt{x}` |
| ⁿ√ | `\sqrt[n]{x}` |
| x² | `x^2` |
| x₁ | `x_1` |

Ejemplo:

```
$x^2 + y^2 = z^2$
```
$$x^2 + y^2 = z^2$$
---

# 2. Fracciones

| Símbolo         | Código         |
| --------------- | -------------- |
| a/b             | `\frac{a}{b}`  |
| fracción grande | `\dfrac{a}{b}` |

Ejemplo:

```
$\frac{a+b}{c+d}$
```
$$\frac{a+b}{c+d}$$
---

# 3. Potencias y subíndices

| Símbolo | Código |
|------|------|
| x² | `x^2` |
| xⁿ | `x^n` |
| x₁ | `x_1` |
| xᵢ | `x_i` |

Ejemplo:

```
$x_i^2$
```
$$x_i^2$$
---

# 4. Raíces

| Símbolo | Código |
|------|------|
| √x | `\sqrt{x}` |
| ³√x | `\sqrt[3]{x}` |

Ejemplo:

```
$\sqrt{x+1}$
```
$$\sqrt{x+1}$$
---

# 5. Letras griegas

## Minúsculas

| Símbolo | Código |
|------|------|
| α | `\alpha` |
| β | `\beta` |
| γ | `\gamma` |
| δ | `\delta` |
| ε | `\epsilon` |
| ζ | `\zeta` |
| η | `\eta` |
| θ | `\theta` |
| ι | `\iota` |
| κ | `\kappa` |
| λ | `\lambda` |
| μ | `\mu` |
| ν | `\nu` |
| ξ | `\xi` |
| π | `\pi` |
| ρ | `\rho` |
| σ | `\sigma` |
| τ | `\tau` |
| φ | `\phi` |
| χ | `\chi` |
| ψ | `\psi` |
| ω | `\omega` |

## Mayúsculas

| Símbolo | Código |
|------|------|
| Γ | `\Gamma` |
| Δ | `\Delta` |
| Θ | `\Theta` |
| Λ | `\Lambda` |
| Ξ | `\Xi` |
| Π | `\Pi` |
| Σ | `\Sigma` |
| Φ | `\Phi` |
| Ψ | `\Psi` |
| Ω | `\Omega` |

---

# 6. Comparaciones

| Símbolo | Código |
|------|------|
| = | `=` |
| ≠ | `\neq` |
| < | `<` |
| > | `>` |
| ≤ | `\le` |
| ≥ | `\ge` |
| ≈ | `\approx` |
| ≅ | `\cong` |
| ≡ | `\equiv` |
| ∼ | `\sim` |
| ∝ | `\propto` |

---

# 7. Conjuntos

| Símbolo | Código |
|------|------|
| ∈ | `\in` |
| ∉ | `\notin` |
| ⊂ | `\subset` |
| ⊆ | `\subseteq` |
| ⊃ | `\supset` |
| ⊇ | `\supseteq` |
| ∪ | `\cup` |
| ∩ | `\cap` |
| ∅ | `\emptyset` |

Ejemplo:

```
$x \in A$
```
$$x \in A$$
---

# 8. Conjuntos numéricos

| Conjunto | Código |
|------|------|
| ℕ | `\mathbb{N}` |
| ℤ | `\mathbb{Z}` |
| ℚ | `\mathbb{Q}` |
| ℝ | `\mathbb{R}` |
| ℂ | `\mathbb{C}` |

Ejemplo:

```
$x \in \mathbb{R}$
```
$$x \in \mathbb{R}$$
---

# 9. Sumatorias y productos

| Símbolo | Código |
|------|------|
| ∑ | `\sum` |
| ∏ | `\prod` |

Ejemplo:

```
$$
\sum_{i=1}^{n} i
$$
```
$$\sum_{i=1}^{n} i$$
---

# 10. Límites

| Símbolo | Código |
|------|------|
| límite | `\lim` |

Ejemplo:

```
$$
\lim_{x \to 0} \frac{\sin x}{x}
$$
```
$$\lim_{x \to 0} \frac{\sin x}{x}$$
---

# 11. Derivadas

| Símbolo | Código |
|------|------|
| derivada | `\frac{d}{dx}` |
| parcial | `\partial` |

Ejemplo:

```
$$
\frac{d}{dx}x^2
$$
```
$$\frac{d}{dx}x^2$$
Parcial:

```
$$
\frac{\partial f}{\partial x}
$$
```
$$\frac{\partial f}{\partial x}$$
---

# 12. Integrales

| Símbolo | Código |
|------|------|
| ∫ | `\int` |
| ∬ | `\iint` |
| ∮ | `\oint` |

Ejemplo:

```
$$
\int_a^b f(x) dx
$$
```
$$\int_a^b f(x) dx$$
---

# 13. Vectores

| Símbolo | Código |
|------|------|
| vector | `\vec{v}` |
| vector negrita | `\mathbf{v}` |

Ejemplo:

```
$\vec{v}$
```
$$\vec{v}$$
---

# 14. Matrices

Ejemplo:

```
$$
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
$$
```
$$
\begin{bmatrix}
a & b \\
c & d
\end{bmatrix}
$$
Tipos:

| Tipo | Código |
|----|----|
| paréntesis | `pmatrix` |
| corchetes | `bmatrix` |
| barras | `vmatrix` |

---

# 15. Lógica

| Símbolo | Código            |
| ------- | ----------------- |
| ∧       | `\land`           |
| ∨       | `\lor`            |
| ¬       | `\neg`            |
| ⇒       | `\Rightarrow`     |
| ⇔       | `\Leftrightarrow` |
| ∀       | `\forall`         |
| ∃       | `\exists`         |

---

# 16. Flechas

| Símbolo | Código |
|------|------|
| → | `\to` |
| ← | `\leftarrow` |
| ↔ | `\leftrightarrow` |
| ⇒ | `\Rightarrow` |
| ⇐ | `\Leftarrow` |
| ⇔ | `\Leftrightarrow` |

---

# 17. Funciones comunes

| Función | Código |
|------|------|
| log | `\log` |
| ln | `\ln` |
| sin | `\sin` |
| cos | `\cos` |
| tan | `\tan` |
| exp | `\exp` |

Ejemplo:

```
$\sin(x)$
```
$$\sin(x)$$
---

# 18. Probabilidad y estadística

| Símbolo | Código |
|------|------|
| esperanza | `\mathbb{E}` |
| varianza | `\mathrm{Var}` |
| probabilidad | `\mathbb{P}` |

Ejemplo:

```
$\mathbb{P}(A)$
```
$$\mathbb{P}(A)$$
---

# 19. Notación de normas y valores absolutos

| Símbolo | Código  |
| ------- | ------- |
| \|x\|   | x       |
| norma   | `\|x\|` |

Ejemplo:

```
$\|v\|$
```
$$\|v\|$$
---

# 20. Texto dentro de ecuaciones

```
\text{texto}
```

Ejemplo:

```
$$
x = 1 \text{ si } y > 0
$$
```
$$x = 1 \text{ si } y > 0$$
---

# 21. Espaciado

| Código | Resultado |
|------|------|
| `\,` | pequeño |
| `\:` | medio |
| `\;` | grande |
| `\quad` | muy grande |

---

# 22. Casos

```
$$
f(x)=
\begin{cases}
x^2 & x>0 \\
0 & x=0
\end{cases}
$$
```
$$
f(x)=
\begin{cases}
x^2 & x>0 \\
0 & x=0
\end{cases}
$$
---

# 23. Overline y subrayados

| Símbolo | Código |
|------|------|
| línea arriba | `\overline{x}` |
| sombrero | `\hat{x}` |
| tilde | `\tilde{x}` |

---

# 24. Ejemplo completo

```
$$
\int_0^\infty e^{-x^2} dx = \frac{\sqrt{\pi}}{2}
$$
```
$$\int_0^\infty e^{-x^2} dx = \frac{\sqrt{\pi}}{2}$$
---

# Consejos

Para escribir más rápido:

- `/frac` → fracción (con plugin LaTeX Suite)
- `/sum`
- `/int`

---

# Nota final

Esta hoja cubre la **gran mayoría de notación utilizada en ingeniería, matemática, física e informática teórica**.

Puedes expandirla con:

- diagramas Mermaid
- gráficos
- matrices grandes
- notación de teoría de grafos
- notación de complejidad algorítmica