## $$ \textcolor{red}{\text{Esercizi Ex. 18 - Lez. 14}} $$

#### Esercizio 1

Sia $X \sim U(−3, 3)$ e sia $Y = X^2$. Trova la densità di probabilità di $Y$.

##### Risoluzione

Notiamo che la parabola non è una funzione strettamente crescente o decrescente nell'intervallo $(-3,3)$. Quindi non possiamo applicare direttamente il teorema della trasformazione.

Come prima cosa calcoliamo $F_Y$ in termini di $F_X$.

$$\begin{aligned}
F_Y(y)
&= P(Y \le y) \\
&= P(X^2 \le y) \\
&= P(-\sqrt{y} \le X \le \sqrt{y}) \\
&= P(X \le \sqrt{y}) - P(X < -\sqrt{y}) \\
&= F_X(\sqrt{y}) - F_X(-\sqrt{y})
\end{aligned}$$

Ora calcoliamo $f_Y$ in termini di $F_Y$.

$$\begin{aligned}
f_Y(y)
&= \frac{d}{dy}\left\{ F_Y(y) \right\} \\
&= \frac{d}{dy}\left\{ F_X(\sqrt{y}) - F_X(-\sqrt{y}) \right\} \\
&= \frac1{2\sqrt{y}}f_X(\sqrt{y}) - \left( -\frac1{2\sqrt{y}}f_X(-\sqrt{y}) \right) \\
&= \frac1{2\sqrt{y}}
\left(
f_X(\sqrt{y}) + f_X(-\sqrt{y})
\right)
\end{aligned}$$

Poiché $X \sim U(-3,3)$, la densità è costante sul supporto:

$$
f_X(\sqrt{y})
= f_X(-\sqrt{y})
= \frac1{3-(-3)}
= \frac16
$$

<div style="page-break-after: always;"></div>

Quindi:

$$\begin{aligned}
f_Y(y)
&= \frac1{2\sqrt{y}}
\left(
\frac16 + \frac16
\right) \\
&= \frac1{2\sqrt{y}}\cdot\frac13 \\
&= \frac1{6\sqrt{y}}
\end{aligned}$$

Calcoliamo il supporto di $Y$.

$$
-3 < X < 3
$$

$$
0 \le X^2 < 9
$$

$$
0 \le Y < 9
$$

Quindi:

$$
\boxed{
f_Y(y) =
\begin{cases}
\frac1{6\sqrt{y}} & 0 < y < 9 \\
0 & \text{altrimenti}
\end{cases}
}
\;.
$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 2

Sia $X$ una v.a. normale di media $0$ e varianza $3$. Trova la densità di probabilità di $Y = X^{10}$.

##### Risoluzione

Notiamo che la funzione $g(x)=x^{10}$ non è strettamente crescente o decrescente su tutto $\mathbb{R}$. Quindi non possiamo applicare direttamente il teorema della trasformazione.

Come prima cosa calcoliamo $F_Y$ in termini di $F_X$.

$$\begin{aligned}
F_Y(y)
&= P(Y \le y) \\
&= P(X^{10} \le y) \\
&= P(-\sqrt[10]{y} \le X \le \sqrt[10]{y}) \\
&= P(X \le \sqrt[10]{y}) - P(X < -\sqrt[10]{y}) \\
&= F_X(\sqrt[10]{y}) - F_X(-\sqrt[10]{y})
\end{aligned}$$

Ora calcoliamo $f_Y$ derivando $F_Y$.

$$\begin{aligned}
f_Y(y)
&= \frac{d}{dy}\left\{ F_Y(y) \right\} \\
&= \frac{d}{dy}\left\{ F_X(\sqrt[10]{y}) - F_X(-\sqrt[10]{y}) \right\} \\
&= \frac1{10}y^{-\frac9{10}}f_X(\sqrt[10]{y}) -
\left(
-\frac1{10}y^{-\frac9{10}}f_X(-\sqrt[10]{y})
\right) \\
&= \frac1{10}y^{-\frac9{10}}
\left(
f_X(\sqrt[10]{y}) + f_X(-\sqrt[10]{y})
\right)
\end{aligned}$$

Dato che $X$ è una normale di media $0$, la sua densità è una funzione pari. Quindi:

$$
f_X(x)=f_X(-x)
$$

<div style="page-break-after: always;"></div>

Continuando i calcoli:

$$\begin{aligned}
f_Y(y)
&= \frac1{10}y^{-\frac9{10}}
\left(
f_X(\sqrt[10]{y}) + f_X(-\sqrt[10]{y})
\right) \\
&= \frac1{10}y^{-\frac9{10}}
\left(
2f_X(\sqrt[10]{y})
\right) \\
&= \frac1{5}y^{-\frac9{10}}f_X(\sqrt[10]{y}) \\
&= \frac1{5}y^{-\frac9{10}}
\frac1{\sqrt{2\pi\cdot3}}
e^{-\frac{(\sqrt[10]{y})^2}{2\cdot3}} \\
&= \frac1{5\sqrt{6\pi}}
y^{-\frac9{10}}
e^{-\frac16y^{\frac15}}
\end{aligned}$$

Calcoliamo il supporto di $Y$.

$$
Y=X^{10}\ge0 \quad\Longrightarrow\quad 0 \le Y < +\infty
$$

Quindi:

$$
\boxed{
f_Y(y)=
\begin{cases}
\frac1{5\sqrt{6\pi}} y^{-\frac9{10}} e^{-\frac16y^{\frac15}} & y>0 \\
0 & \text{altrimenti}
\end{cases}
}
\;.
$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 3

Sia $X \sim U(0, 9)$ e sia $Y = X^{-1}$. Trova la densità di probabilità di $Y$.

##### Risoluzione

Osserviamo che il reciproco è una funzione strettamente decrescente nell'intervallo $(0,9)$. Quindi possiamo applicare direttamente il teorema di trasformazione.

Per prima cosa invertiamo la funzione $g(x)=x^{-1}$.

$$
g^{-1}(y)=y^{-1}
$$

Ora applichiamo il teorema e troviamo $f_Y(y)$.

$$\begin{aligned}
f_Y(y)
&= f_X(g^{-1}(y))
\left|
\frac{d}{dy}g^{-1}(y)
\right| \\
&= f_X(y^{-1})
\left|
\frac{d}{dy}y^{-1}
\right| \\
&= \frac1{9-0}
\left|
-y^{-2}
\right| \\
&= \frac1{9y^2}
\end{aligned}$$

Calcoliamo il supporto di $Y$.

$$
0 < X < 9 \\[4pt]
0 < \frac1Y < 9 \\[4pt]
Y > \frac19
$$

Poiché $X$ può assumere valori arbitrariamente vicini a $0$ senza mai raggiungerlo:

$$
Y < +\infty
$$

allora:

$$
\frac19 < Y < +\infty
$$

Quindi:

$$
\boxed{
f_Y(y)=
\begin{cases}
\frac1{9y^2}
&
y>\frac19
\\
0
&
\text{altrimenti}
\end{cases}
}
\;.
$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 4

Sia $X$ una v.a. con densità di probabilità

$$
f_X(x) =
\begin{cases}
\frac{125}2 x^2 e^{-5x} & 0 < x < \infty \\
0 & \text{altrove}
\end{cases}
$$

Sia $Y = \frac1X$. Trova la densità di probabilità di $Y$.

##### Risoluzione

Osserviamo che il reciproco è una funzione strettamente decrescente nell'intervallo $(0,+\infty)$. Quindi possiamo applicare direttamente il teorema di trasformazione.

Per prima cosa invertiamo la funzione $g(x)=x^{-1}$.

$$
g^{-1}(y)=y^{-1}
$$

Ora applichiamo il teorema e troviamo $f_Y(y)$.

$$\begin{aligned}
f_Y(y)
&= f_X(g^{-1}(y))
\left|
\frac{d}{dy}g^{-1}(y)
\right| \\
&= f_X(y^{-1})
\left|
\frac{d}{dy}y^{-1}
\right| \\
&= \frac{125}2 (y^{-1})^2 e^{-5y^{-1}}
\left|
-y^{-2}
\right| \\
&= \frac{125}2 y^{-2} e^{-\frac5y} y^{-2} \\
&= \frac{125}2 y^{-4} e^{-\frac5y}
\end{aligned}$$

Calcoliamo il supporto di $Y$.

$$
0 < X < +\infty
$$

Poiché $Y=\frac1X$:

$$
0 < Y < +\infty
$$

<div style="page-break-after: always;"></div>

Quindi:

$$
\boxed{
f_Y(y)=
\begin{cases}
\frac{125}2 y^{-4} e^{-\frac5y}
&
0 < y < +\infty
\\
0
&
\text{altrimenti}
\end{cases}
}
\;.
$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 5

Sia $X$ normale di media $0$ e varianza $36$. Trova la densità di probabilità della v.a. $Y = \ln(1 + X^2)$.

##### Risoluzione

Osserviamo che la funzione $g(x)=\ln(1+x^2)$ non è strettamente crescente o decrescente su tutto $\mathbb{R}$, quindi non possiamo applicare direttamente il teorema di trasformazione.

Calcoliamo $F_Y$ in termini di $F_X$.

$$\begin{aligned}
F_Y(y)
&= P(Y \le y) \\
&= P(\ln(1+X^2) \le y) \\
&= P(1+X^2 \le e^y) \\
&= P(X^2 \le e^y-1) \\
&= P(-\sqrt{e^y-1} \le X \le \sqrt{e^y-1}) \\
&= P(X \le \sqrt{e^y-1}) - P(X < -\sqrt{e^y-1}) \\
&= F_X(\sqrt{e^y-1}) - F_X(-\sqrt{e^y-1})
\end{aligned}$$

Calcoliamo $f_Y$ in termini di $F_Y$.

$$\begin{aligned}
f_Y(y)
&= \frac{d}{dy}\left\{ F_Y(y) \right\} \\
&= \frac{d}{dy}\left\{ F_X(\sqrt{e^y-1}) - F_X(-\sqrt{e^y-1}) \right\} \\
&= \frac{e^y}{2\sqrt{e^y-1}}f_X(\sqrt{e^y-1}) -
\left(
-\frac{e^y}{2\sqrt{e^y-1}}f_X(-\sqrt{e^y-1})
\right) \\
&= \frac{e^y}{2\sqrt{e^y-1}}
\left(
f_X(\sqrt{e^y-1}) + f_X(-\sqrt{e^y-1})
\right)
\end{aligned}$$

Dato che $X$ è una normale di media $0$, la sua densità è una funzione pari. Quindi:

$$
f_X(x)=f_X(-x)
$$

<div style="page-break-after: always;"></div>

Continuando i calcoli:

$$\begin{aligned}
f_Y(y)
&= \frac{e^y}{2\sqrt{e^y-1}}
\left(
f_X(\sqrt{e^y-1}) + f_X(-\sqrt{e^y-1})
\right) \\
&= \frac{e^y}{2\sqrt{e^y-1}}
\left(
2f_X(\sqrt{e^y-1})
\right) \\
&= \frac{e^y}{\sqrt{e^y-1}}
f_X(\sqrt{e^y-1}) \\
&= \frac{e^y}{\sqrt{e^y-1}}
\cdot
\frac1{\sqrt{2\pi\cdot36}}
e^{-\frac{(\sqrt{e^y-1})^2}{2\cdot36}} \\
&= \frac{e^y}{6\sqrt{2\pi(e^y-1)}}
e^{-\frac{e^y-1}{72}}
\end{aligned}$$

Calcoliamo il supporto di $Y$.

Poiché:

$$
X^2 \ge 0
$$

abbiamo:

$$
1+X^2 \ge 1
$$

e quindi:

$$
Y=\ln(1+X^2)\ge 0
$$

Inoltre $X$ può assumere valori arbitrariamente grandi in valore assoluto, quindi:

$$
Y<+\infty
$$

Pertanto:

$$
0 \le Y < +\infty
$$

Quindi:

$$
\boxed{
f_Y(y)=
\begin{cases}
\frac{e^y}{6\sqrt{2\pi(e^y-1)}}
e^{-\frac{e^y-1}{72}}
&
y>0
\\
0
&
\text{altrimenti}
\end{cases}
}
\;.
$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 6

Sia $X\sim U(0,11)$, calcolare la densità di probabilità di $Y=\max\{X, 11-X\}$.

##### Risoluzione

Notiamo subito che la funzione

$$
Y=\max\{X,11-X\}
$$

non è una trasformazione monotona su tutto il dominio, quindi non possiamo applicare direttamente il teorema di trasformazione.

1) Osserviamo prima il comportamento della funzione:

    - se $X \in (0, 11/2]$, allora $11-X \ge X$ quindi $Y=11-X$
    - se $X \in [11/2, 11)$, allora $X \ge 11-X$ quindi $Y=X$

    Quindi:

    $$
    Y =
    \begin{cases}
    11-X & \text{se } X \le \frac{11}{2} \\
    X & \text{se } X \ge \frac{11}{2}
    \end{cases}
    $$

    Supporto:

    $$
    Y \in \left[\frac{11}{2}, 11\right]
    $$

2) Scriviamo $F_Y$ in termini di $F_X$:

    $$\begin{aligned}
    F_Y(y) = P(Y\le y)
    &= P(\max\{x,11-x\}\le y) \\
    &= P(11-y \le x \le y) \\
    &= P(x\le y) - P(x< 11-y) \\
    &= F_X(y) - F_X(11-y) \\
    \end{aligned}$$

<div style="page-break-after: always;"></div>

3) Calcoliamo $f_Y$ in termini di $F_Y$:

    $$\begin{aligned}
    f_Y(y) &= \frac{d}{dy}\Big\{ F_X(y) - F_X(11-y) \Big\} \\
    &= \frac{d}{dy}\Big\{ F_X(y) \Big\} -
    \frac{d}{dy}\Big\{ F_X(11-y) \Big\} \\
    &= f_X(y) - (-f_X(11-y)) \\
    &= f_X(y) + (f_X(11-y)) \\
    &= 2\cdot\frac1{11}
    \end{aligned}$$

3) Densità di probabilità finale:

    $$
    \boxed{
    f_Y(y)=\frac{2}{11}\cdot \mathbf{1}_{\left[\frac{11}{2},\,11\right]}(y)
    }
    $$

---

<div style="page-break-after: always;"></div>