## $$ \textcolor{red}{\text{Esercizi Lez. 16b - Teoria}} $$

### $$ \textcolor{blue}{\text{Esercizi Aspettazione - Casi Discreti}} $$

#### Esercizio 1

$X$ ed $Y$ sono due v.a. discrete con funzione di probabilità data dalla tabella di seguito. Calcolare $E[X+Y]$.

|$Y$ \ $X$| 0 | 1 | 2 |
|:-:|:-:|:-:|:-:|
| -1 | $\frac16$ | $\frac16$ | $\frac16$ |
|  1 | $0$ | $\frac12$ | $0$ |

a. $0$
b. $\frac12$
c. $-1$
d. $1$

##### Risoluzione

Esistono due metodi per calcolare l'aspettazione di una distribuzione congiunta nel caso discreto.

1. **Primo metodo (calcolo diretto).**

    Prendiamo $g(x,y)=x+y$.

    $$\begin{aligned}
    E[X+Y]
    &= \sum_{(x,\,y)} (x+y)\cdot p_{X,Y}(x,y) \\
    &= (0-1)\frac16 + (1-1)\frac16 + (2-1)\frac16 \\
    &\quad + (0+1)\cdot0 + (1+1)\frac12 + (2+1)\cdot0 \\
    &= -\frac16 + 0 + \frac16 + 0 + 1 + 0 \\
    &= \boxed{1}\;.
    \end{aligned}$$

    > **Nota.** Nel caso discreto:
    >
    > $$
    > E[g(X,Y)]
    > = \sum_x \sum_y g(x,y)\,p_{X,Y}(x,y).
    > $$

2. **Secondo metodo (linearità dell'aspettazione).**

    Vale la proprietà:

    $$
    E[X+Y]=E[X]+E[Y].
    $$

    Calcoliamo le marginali.

    $$\begin{aligned}
    p_X(0) &= \frac16+0=\frac16,\\
    p_X(1) &= \frac16+\frac12=\frac23,\\
    p_X(2) &= \frac16+0=\frac16.
    \end{aligned}$$

    $$\begin{aligned}
    p_Y(-1) &= \frac16+\frac16+\frac16=\frac12,\\
    p_Y(1) &= 0+\frac12+0=\frac12.
    \end{aligned}$$

    Calcoliamo le singole aspettazioni.

    $$\begin{aligned}
    E[X]
    &= \sum_x x\cdot p_X(x) \\
    &= 0\cdot\frac16 + 1\cdot\frac23 + 2\cdot\frac16 \\
    &= \frac23+\frac13
    = 1.
    \end{aligned}$$

    $$\begin{aligned}
    E[Y]
    &= \sum_y y\cdot p_Y(y) \\
    &= (-1)\frac12 + (1)\frac12
    = 0.
    \end{aligned}$$

    Calcoliamo l'aspettazione totale.

    $$
    E[X+Y]
    = E[X]+E[Y]
    = 1+0
    = \boxed{1}\;.
    $$

---

<div style="page-break-after: always;"></div>

#### Esercizio 2

Siano $X$ ed $Y$ due v.a. la cui funzione di probabilità congiunta è data dalla tabella a lato.

|$Y$ \ $X$| 0 | 1 | 2 |
|:-:|:-:|:-:|:-:|
| 0 | $0$ | $\frac14$ | $0$ |
| 1 | $\frac14$ | $0$ | $\frac14$ |
| 2 | $0$ | $\frac14$ | $0$ |

- Calcolare $E[3X-2Y+1]$.
- Calcolare $E[X^2Y]$.

##### Risoluzione

1. **Calcolare $E[3X-2Y+1]$.**

    Per la linearità dell'aspettazione vale:

    $$
    E[3X-2Y+1]
    = 3E[X]-2E[Y]+1.
    $$

    Calcoliamo le aspettazioni richieste.

    $$\begin{aligned}
    E[X]
    &= \sum_{x\,\in\,\{0,1,2\}} x\,p_X(x) \\
    &= 0\cdot\frac14
    +1\left(\frac14+\frac14\right)
    +2\cdot\frac14 \\
    &= 0+\frac12+\frac12 \\
    &= 1.
    \end{aligned}$$

    $$\begin{aligned}
    E[Y]
    &= \sum_{y\,\in\,\{0,1,2\}} y\,p_Y(y) \\
    &= 0\cdot\frac14
    +1\left(\frac14+\frac14\right)
    +2\cdot\frac14 \\
    &= 0+\frac12+\frac12 \\
    &= 1.
    \end{aligned}$$

    Calcoliamo quindi l'aspettazione richiesta:

    $$\begin{aligned}
    E[3X-2Y+1]
    &= 3E[X]-2E[Y]+1 \\
    &= 3\cdot1-2\cdot1+1 \\
    &= \boxed{2}\;.
    \end{aligned}$$

2. **Calcolare $E[X^2Y]$.**

    Poniamo

    $$
    g(x,y)=x^2y.
    $$

    Allora

    $$\begin{aligned}
    E[X^2Y]
    &= \sum_{(x,y)} x^2y\cdot p_{X,Y}(x,y) \\
    &= (0^2\cdot0)\cdot0
    +(1^2\cdot0)\cdot\frac14
    +(2^2\cdot0)\cdot0 \\
    &\quad +(0^2\cdot1)\cdot\frac14
    +(1^2\cdot1)\cdot0
    +(2^2\cdot1)\cdot\frac14 \\
    &\quad +(0^2\cdot2)\cdot0
    +(1^2\cdot2)\cdot\frac14
    +(2^2\cdot2)\cdot0 \\
    &= 0+0+0+0+0+1+0+\frac12+0 \\
    &= \boxed{\frac32}\;.
    \end{aligned}$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 3

Siano $X$ ed $Y$ due v.a. tali che

$$
E[X]=2, \quad E[Y]=3, \quad \text{Var}(X)=4.
$$

Calcolare:
1. $E[X^2]$,
2. $E[-2X^2 + Y]$.

##### Risoluzione

1. **Calcolare $E[X^2]$.**

    Sappiamo che la varianza soddisfa la relazione:

    $$
    \text{Var}(X)=E[X^2]-(E[X])^2.
    $$

    Ricaviamo quindi $E[X^2]$:

    $$\begin{aligned}
    E[X^2]
    &= \text{Var}(X)+(E[X])^2 \\
    &= 4+2^2 \\
    &= \boxed{8}\;.
    \end{aligned}$$

2. **Calcolare $E[-2X^2 + Y]$.**

    Per la linearità dell'aspettazione:

    $$\begin{aligned}
    E[-2X^2+Y]
    &= -2E[X^2]+E[Y] \\
    &= -2\cdot 8 + 3 \\
    &= -16+3 \\
    &= \boxed{-13}\;.
    \end{aligned}$$

> **Nota.** Dalla formula della varianza
>
> $$
> \text{Var}(X)=E[X^2]-(E[X])^2
> $$
>
> si ricava spesso:
>
> $$
> E[X^2]=\text{Var}(X)+(E[X])^2.
> $$

---

<div style="page-break-after: always;"></div>

---

> **Nota (Linearità dell'aspettazione).** Siano $X$ ed $Y$ due variabili aleatorie e siano $r,s\in\mathbb{R}$. Allora
>
> $$
> E[rX+sY]=r\,E[X]+s\,E[Y].
> $$
>
> Questa proprietà vale sempre, indipendentemente dal fatto che $X$ ed $Y$ siano indipendenti oppure no.
>
> **Attenzione.** La stessa proprietà **non vale** per la varianza. In generale:
>
> $$
> \operatorname{Var}(rX+sY)
> = r^2\operatorname{Var}(X) + 
> s^2\operatorname{Var}(Y) + 
> 2rs\,\operatorname{Cov}(X,Y).
> $$
>
> Se $X$ ed $Y$ sono indipendenti (e quindi $\operatorname{Cov}(X,Y)=0$), allora:
>
> $$
> \operatorname{Var}(rX+sY)
> = r^2\operatorname{Var}(X) + s^2\operatorname{Var}(Y).
> $$

---

<div style="page-break-after: always;"></div>

### $$ \textcolor{blue}{\text{Esercizi Aspettazione - Casi Continui}} $$

#### Esercizio 4

Siano $X$ ed $Y$ due v.a. a.c. la cui densità congiunta è

$$
f_{X,Y}(x,y) =
\begin{cases}
\frac{12}5 xy(1+y) & \text{per } (x,y)\in[0,1]^2 \\
0 & \text{altrimenti}
\end{cases}
$$

Calcolare $E[YX + X^2]$.

##### Risoluzione

Per la linearità dell'aspettazione abbiamo che:

$$
E[YX + X^2] = E[YX] + E[X^2].
$$

1. **Calcoliamo le due aspettazioni.**

    $$\begin{aligned}
    E[YX]
    &= \int_{-\infty}^{+\infty}\int_{-\infty}^{+\infty}
    xy\,f_{X,Y}(x,y)\,dy\,dx \\
    &= \int_0^1 \left(
    \int_0^1 xy\cdot\frac{12}{5}xy(1+y)\,dy
    \right)dx \\
    &= \frac{12}{5}\int_0^1 x^2
    \left(
    \int_0^1 (y^2+y^3)\,dy
    \right)dx \\
    &= \frac{12}{5}\int_0^1 x^2
    \left[
    \frac{y^3}{3}+\frac{y^4}{4}
    \right]_0^1 dx \\
    &= \frac{12}{5}
    \left(
    \frac13+\frac14
    \right)
    \int_0^1 x^2\,dx \\
    &= \frac{12}{5}\cdot\frac{7}{12}
    \left[
    \frac{x^3}{3}
    \right]_0^1 \\
    &= \frac75\cdot\frac13 \\
    &= \boxed{\frac{7}{15}} \;.
    \end{aligned}$$

    $$\begin{aligned}
    E[X^2]
    &= \int_{-\infty}^{+\infty}\int_{-\infty}^{+\infty}
    x^2\,f_{X,Y}(x,y)\,dy\,dx \\
    &= \int_0^1 \left(
    \int_0^1 x^2\cdot\frac{12}{5}xy(1+y)\,dy
    \right)dx \\
    &= \frac{12}{5}
    \int_0^1 x^3
    \left(
    \int_0^1 (y+y^2)\,dy
    \right)dx \\
    &= \frac{12}{5}
    \int_0^1 x^3
    \left[
    \frac{y^2}{2}+\frac{y^3}{3}
    \right]_0^1 dx \\
    &= \frac{12}{5}
    \left(
    \frac12+\frac13
    \right)
    \int_0^1 x^3\,dx \\
    &= \frac{12}{5}\cdot\frac56
    \left[
    \frac{x^4}{4}
    \right]_0^1 \\
    &= 2\cdot\frac14 \\
    &= \boxed{\frac12} \;.
    \end{aligned}$$

2. **Calcoliamo l'aspettazione richiesta:**

    $$\begin{aligned}
    E[YX + X^2]
    &= E[YX] + E[X^2] \\
    &= \frac{7}{15} + \frac12 \\
    &= \frac{14}{30}+\frac{15}{30} \\
    &= \boxed{\frac{29}{30}} \;.
    \end{aligned}$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 5

Siano $X$ ed $Y$ due v.a. a.c. la cui densità di probabilità congiunta è

$$
f_{X,Y}(x,y)=
\frac1{10}(3x^2+8xy)
\quad\text{per}\quad
\begin{aligned}
0\le x\le1 \\
0\le y\le2
\end{aligned}
$$

e uguale a $0$ per gli altri valori di $x$ ed $y$.

Calcolare $E[YX + X^2]$.

##### Risoluzione

Per la linearità dell'aspettazione abbiamo che

$$
E[YX + X^2] = E[YX] + E[X^2].
$$

1. **Calcoliamo separatamente le due aspettazioni.**

    $$\begin{aligned}
    E[YX]
    &= \int_{-\infty}^{+\infty}\int_{-\infty}^{+\infty}
    xy\,f_{X,Y}(x,y)\,dy\,dx \\
    &= \int_0^1 \left(
    \int_0^2 xy\cdot \frac1{10}(3x^2+8xy)\,dy
    \right)dx \\
    &= \frac1{10}\int_0^1
    \left(
    \int_0^2 (3x^3y+8x^2y^2)\,dy
    \right)dx \\
    &= \frac1{10}\int_0^1
    \left(
    3x^3\int_0^2 y\,dy
    +
    8x^2\int_0^2 y^2\,dy
    \right)dx \\
    &= \frac1{10}\int_0^1
    \left(
    3x^3\left[\frac{y^2}{2}\right]_0^2
    +
    8x^2\left[\frac{y^3}{3}\right]_0^2
    \right)dx \\
    &= \frac1{10}\int_0^1
    \left(
    6x^3+\frac{64}{3}x^2
    \right)dx \\
    &= \frac1{10}
    \left(
    6\int_0^1 x^3\,dx
    +
    \frac{64}{3}\int_0^1 x^2\,dx
    \right) \\
    &= \frac1{10}
    \left(
    6\left[\frac{x^4}{4}\right]_0^1
    +
    \frac{64}{3}\left[\frac{x^3}{3}\right]_0^1
    \right) \\
    &= \frac1{10}
    \left(
    \frac32+\frac{64}{9}
    \right) \\
    &= \boxed{\frac{31}{36}} \;.
    \end{aligned}$$

    $$\begin{aligned}
    E[X^2]
    &= \int_{-\infty}^{+\infty}\int_{-\infty}^{+\infty}
    x^2\,f_{X,Y}(x,y)\,dy\,dx \\
    &= \int_0^1 \left(
    \int_0^2 x^2\cdot\frac1{10}(3x^2+8xy)\,dy
    \right)dx \\
    &= \frac1{10}\int_0^1
    \left(
    3x^4\int_0^2 dy
    +
    8x^3\int_0^2 y\,dy
    \right)dx \\
    &= \frac1{10}\int_0^1
    \left(
    3x^4\,[y]_0^2
    +
    8x^3\left[\frac{y^2}{2}\right]_0^2
    \right)dx \\
    &= \frac1{10}\int_0^1
    \left(
    6x^4+16x^3
    \right)dx \\
    &= \frac1{10}
    \left(
    6\left[\frac{x^5}{5}\right]_0^1
    +
    16\left[\frac{x^4}{4}\right]_0^1
    \right) \\
    &= \frac1{10}
    \left(
    \frac65+4
    \right) \\
    &= \boxed{\frac{13}{25}} \;.
    \end{aligned}$$

2. **Calcoliamo l'aspettazione richiesta.**

    $$\begin{aligned}
    E[YX + X^2]
    &= E[YX] + E[X^2] \\
    &= \frac{31}{36} + \frac{13}{25} \\
    &= \boxed{\frac{1243}{900}}
    \approx 1.381 \;.
    \end{aligned}$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 6

Siano $X$ ed $Y$ due v.a. a.c. la cui distribuzione congiunta è

$$
F_{X,Y}(x,y) = 
\begin{cases}
1-e^{-2x}-e^{-y}+e^{-(2x+y)} & \text{per } x,y>0 \\
0 & \text{altrimenti}
\end{cases}
$$

Calcolare $E[e^{-(X+Y)}+e^{-3X}]$.

##### Risoluzione

Per la linearità dell'aspettazione abbiamo che

$$
E[e^{-(X+Y)}+e^{-3X}]
= E[e^{-(X+Y)}] + E[e^{-3X}].
$$

1. **Ricaviamo la funzione di densità congiunta.**

    $$\begin{aligned}
    f_{X,Y}(x,y)
    &= \frac{\partial^2}{\partial x\,\partial y}F_{X,Y}(x,y) \\
    &= \frac{\partial}{\partial y}\left(
    \frac{\partial}{\partial x}
    (1-e^{-2x}-e^{-y}+e^{-2x}e^{-y})
    \right) \\
    &= \frac{\partial}{\partial y}\left(
    2e^{-2x}-2e^{-2x}e^{-y}
    \right) \\
    &= 2e^{-2x}e^{-y}.
    \end{aligned}$$

    Quindi

    $$
    \boxed{
    f_{X,Y}(x,y)=2e^{-2x}e^{-y}
    }
    \qquad \text{per } x,y>0.
    $$

<div style="page-break-after: always;"></div>

2. **Calcoliamo separatamente le due aspettazioni.**

    $$\begin{aligned}
    E[e^{-(X+Y)}]
    &= \int_{-\infty}^{+\infty}
    \int_{-\infty}^{+\infty}
    e^{-(x+y)}f_{X,Y}(x,y)\,dy\,dx \\
    &= \int_0^{+\infty}
    \int_0^{+\infty}
    e^{-x}e^{-y}\,2e^{-2x}e^{-y}
    \,dy\,dx \\
    &= \int_0^{+\infty}
    \int_0^{+\infty}
    2e^{-3x}e^{-2y}
    \,dy\,dx \\
    &= \int_0^{+\infty}
    2e^{-3x}
    \left[\!-\frac12e^{-2y}\right]_0^{+\infty}
    dx \\
    &= \int_0^{+\infty}
    e^{-3x}\,dx \\
    &= \left[\!-\frac13e^{-3x}\right]_0^{+\infty} \\
    &= \boxed{\frac13}.
    \end{aligned}$$

    $$\begin{aligned}
    E[e^{-3X}]
    &= \int_{-\infty}^{+\infty}
    \int_{-\infty}^{+\infty}
    e^{-3x}f_{X,Y}(x,y)\,dy\,dx \\
    &= \int_0^{+\infty}
    \int_0^{+\infty}
    e^{-3x}\,2e^{-2x}e^{-y}
    \,dy\,dx \\
    &= \int_0^{+\infty}
    \int_0^{+\infty}
    2e^{-5x}e^{-y}
    \,dy\,dx \\
    &= \int_0^{+\infty}
    2e^{-5x}
    \left[-e^{-y}\right]_0^{+\infty}
    dx \\
    &= \int_0^{+\infty}
    2e^{-5x}\,dx \\
    &= \left[\!-\frac25e^{-5x}\right]_0^{+\infty} \\
    &= \boxed{\frac25}.
    \end{aligned}$$

<div style="page-break-after: always;"></div>


3. **Calcoliamo l'aspettazione richiesta.**

    $$\begin{aligned}
    E[e^{-(X+Y)}+e^{-3X}]
    &= E[e^{-(X+Y)}] + E[e^{-3X}] \\
    &= \frac13+\frac25 \\
    &= \boxed{\frac{11}{15}}.
    \end{aligned}$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 7

Siano $X$, $Y$ e $Z$ tre v.a. a.c. la cui densità congiunta è

$$
f_{X,Y,Z}(x,y,z) =
\begin{cases}
\frac23(x+y+z) & \text{per } (x,y,z)\in[0,1]^3 \\
0 & \text{altrimenti}
\end{cases}
$$

Calcolare $E[XYZ]$.

##### Risoluzione

Calcoliamo l'aspettazione richiesta.

$$\begin{aligned}
E[XYZ]
&=
\int_{-\infty}^{+\infty}
\int_{-\infty}^{+\infty}
\int_{-\infty}^{+\infty}
xyz\,f_{X,Y,Z}(x,y,z)\,dz\,dy\,dx \\
&=
\int_0^1
\int_0^1
\int_0^1
xyz\,\frac23(x+y+z)
\,dz\,dy\,dx \\
&=
\frac23
\int_0^1
\int_0^1
\int_0^1
\left(x^2yz+xy^2z+xyz^2\right)
\,dz\,dy\,dx
\end{aligned}$$

Calcoliamo uno dei tre integrali. Gli altri si ottengono per simmetria e hanno lo stesso valore.

$$\begin{aligned}
\int_0^1
\int_0^1
\int_0^1
x^2yz
\,dz\,dy\,dx
&=
\int_0^1
\int_0^1
x^2y
\left(
\int_0^1 z\,dz
\right)
dy\,dx \\
&=
\frac12
\int_0^1
\int_0^1
x^2y
\,dy\,dx \\
&=
\frac12
\int_0^1
x^2
\left(
\int_0^1 y\,dy
\right)
dx \\
&=
\frac14
\int_0^1 x^2\,dx \\
&=
\frac14
\left[\frac{x^3}{3}\right]_0^1 \\
&=
\frac14\cdot\frac13 \\
&=
\frac1{12}
\end{aligned}$$

Pertanto

$$\begin{aligned}
E[XYZ]
&=
\frac23
\left(
\frac1{12}
+
\frac1{12}
+
\frac1{12}
\right) \\
&=
\frac23\cdot\frac3{12} \\
&=
\boxed{\frac16} \;.
\end{aligned}$$

---

<div style="page-break-after: always;"></div>