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
