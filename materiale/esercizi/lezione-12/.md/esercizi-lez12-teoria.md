## $$ \textcolor{red}{\text{Esercizi Lez. 12 - Teoria}} $$

#### Esercizio 1

Sia $X$ una v.a. discreta con funzione di probabilità

$$
p_X(x) : \quad
\begin{pmatrix}
-1 & 0 & 1 \\
1/5 & 2/5 & 2/5
\end{pmatrix}.
$$

Calcolare:

+ $E[X]$;
+ $E[X^2]$ usando $p_Y$ con $Y=X^2$;
+ $E[X^2]$ usando la formula del cambio di variabile;
+ $\mathrm{Var}(X)$.

##### Risoluzione

1. Calcolo di $E[X]$:

    $$\begin{aligned}
    E[X]
    &= \sum_{x\in S_X} x\cdot p_X(x) \\
    &= (-1)\cdot\frac15 + 0\cdot\frac25 + 1\cdot\frac25 \\
    &= -\frac15 + \frac25 \\
    &= \boxed{\frac15} \;.
    \end{aligned}$$

<div style="page-break-after: always;"></div>

2. Calcolo di $E[X^2]$ usando $Y=X^2$.

    1. Supporto di $Y$:

        $$
        S_Y=\{0,1\}
        $$

    2. Funzione di probabilità di $Y$:

        $$\begin{aligned}
        p_Y(0)
        &= P(Y=0)
        = P(X^2=0)
        = P(X=0)
        = \frac25
        \\
        p_Y(1)
        &= P(Y=1)
        = P(X^2=1)
        = P(X\in\{-1,1\}) \\
        &= P(X=-1)+P(X=1)
        = \frac15+\frac25
        = \frac35
        \end{aligned}$$

        $$
        p_Y(y) : \quad
        \begin{pmatrix}
        0 & 1 \\
        2/5 & 3/5
        \end{pmatrix}.
        $$

    3. Aspettazione di $Y$:

        $$\begin{aligned}
        E[Y]
        &= \sum_{y\in S_Y} y\cdot p_Y(y) \\
        &= 0\cdot\frac25 + 1\cdot\frac35 \\
        &= \boxed{\frac35} \;.
        \end{aligned}$$

    Quindi:

    $$
    E[X^2]=E[Y]=\frac35 \;.
    $$

3. Calcolo di $E[X^2]$ con il cambio di variabile:

    $$\begin{aligned}
    E[X^2]
    &= \sum_{x\in S_X} x^2\cdot p_X(x) \\
    &= (-1)^2\cdot\frac15 + 0^2\cdot\frac25 + 1^2\cdot\frac25 \\
    &= \frac15 + \frac25 \\
    &= \boxed{\frac35} \;.
    \end{aligned}$$

<div style="page-break-after: always;"></div>

4. Calcolo della varianza:

    $$\begin{aligned}
    \mathrm{Var}(X)
    &= E[X^2]-(E[X])^2 \\
    &= \frac35-\left(\frac15\right)^2 \\
    &= \frac{15}{25}-\frac1{25} \\
    &= \boxed{\frac{14}{25}=0.56} \;.
    \end{aligned}$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 2

Sia $X\sim\mathrm{Exp}(\lambda)$. Calcolare $E[X]$, $E[X^2]$ e $\mathrm{Var}(X)$.

##### Risoluzione

Ricordiamo che la densità della variabile esponenziale è

$$
f(x)=
\begin{cases}
\lambda e^{-\lambda x} & x\ge0 \\
0 & \text{altrimenti}
\end{cases}
$$

Calcoliamo $E[X]$:

$$\begin{aligned}
E[X]
&= \int_{-\infty}^{+\infty} x\,f(x)\,dx
= \int_0^{+\infty} x\lambda e^{-\lambda x}\,dx \\
&= \left[ x\cdot\left(-e^{-\lambda x}\right)\right]_0^{+\infty}
-\int_0^{+\infty}1\cdot\left(-e^{-\lambda x}\right)\,dx \\
&= \underbrace{\left[-\frac{x}{e^{\lambda x}}\right]_0^{+\infty}}_{0}
+\int_0^{+\infty}e^{-\lambda x}\,dx \\
&= -\frac1\lambda\int_0^{+\infty}-\lambda e^{-\lambda x}\,dx \\
&= -\frac1\lambda\left[e^{-\lambda x}\right]_0^{+\infty} \\
&= -\frac1\lambda\left[\frac1{e^{\lambda x}}\right]_0^{+\infty} \\
&= -\frac1\lambda(0-1)
= \boxed{\frac1\lambda} \;.
\end{aligned}$$

<div style="page-break-after: always;"></div>

Calcoliamo ora $E[X^2]$:

$$\begin{aligned}
E[X^2]
&= \int_{-\infty}^{+\infty} x^2\,f(x)\,dx
= \int_0^{+\infty} x^2\lambda e^{-\lambda x}\,dx \\
&= \left[x^2\cdot\left(-e^{-\lambda x}\right)\right]_0^{+\infty}
-\int_0^{+\infty}2x\cdot\left(-e^{-\lambda x}\right)\,dx \\
&= \underbrace{\left[-\frac{x^2}{e^{\lambda x}}\right]_0^{+\infty}}_{0}
+\frac2\lambda\underbrace{\int_0^{+\infty}x\lambda e^{-\lambda x}\,dx}_{E[X]} \\
&= \frac2\lambda\cdot E[X]
= \frac2\lambda\cdot\frac1\lambda \\
&= \boxed{\frac2{\lambda^2}} \;.
\end{aligned}$$

Infine:

$$\begin{aligned}
\mathrm{Var}(X)
&= E[X^2]-(E[X])^2 \\
&= \frac2{\lambda^2}-\left(\frac1\lambda\right)^2 \\
&= \boxed{\frac1{\lambda^2}} \;.
\end{aligned}$$

> **Nota**. Nell'integrazione per parti si usa:
>
> $$ \int u\,dv = uv-\int v\,du $$
>
> Se $X$ è continua e $F'(x)=f(x)$, all'ora applicando l'integrazione per parti:
>
> $$ E[g(x)] = \Big[g(x)F(x)\Big]_{-\infty}^{+\infty}-\int_{-\infty}^{+\infty} g'(x)F(x)\,dx $$

> **Nota**. Vale
>
> $$
> \lim_{x\to+\infty}\frac{x}{e^{\lambda x}}=0,
> $$
>
> poiché l'esponenziale cresce più velocemente di ogni polinomio.

---

<div style="page-break-after: always;"></div>

#### Esercizio 3

Sia $X\sim\text{Par}(\alpha)$,
+ calcolare $\mathrm{Var}(X)$;
+ per quali valori di $\alpha$ la varianza è finita?

##### Risoluzione

Ricordiamo che la densità della variabile di Pareto è

$$
f(x)=
\begin{cases}
\dfrac{\alpha}{x^{\alpha+1}} & x\ge1 \\
0 & \text{altrimenti}
\end{cases}
$$

Calcoliamo $E[X]$:

$$\begin{aligned}
E[X]
&= \int_{-\infty}^{+\infty} x\,f(x)\,dx
= \int_1^{+\infty} x\,\frac\alpha{x^{\alpha+1}}\,dx \\
&= \alpha \int_1^{+\infty} x\,x^{-\alpha-1}\,dx
= \alpha \int_1^{+\infty} x^{-\alpha}\,dx \\
&= \alpha \left[\frac{x^{-\alpha+1}}{-\alpha+1}\right]_1^{+\infty}
= -\alpha \left[\frac{x^{-\alpha+1}}{\alpha-1}\right]_1^{+\infty} \\
&= -\alpha\left(\underbrace{\lim_{x\to+\infty} \frac1{x^{-\alpha+1}(\alpha-1)}}_{0}
-\frac1{1^{-\alpha+1}(\alpha-1)}\right) \\
&= -\alpha\left(0-\frac1{\alpha-1}\right)
= \boxed{\frac{\alpha}{\alpha-1}\quad\text{se}\quad\alpha>1} \;.
\end{aligned}$$

<div style="page-break-after: always;"></div>

Calcoliamo ora $E[X^2]$:

$$\begin{aligned}
E[X^2]
&= \int_{-\infty}^{+\infty} x^2\,f(x)\,dx
= \int_1^{+\infty} x^2\,\frac\alpha{x^{\alpha+1}}\,dx \\
&= \alpha \int_1^{+\infty} x^2\,x^{-\alpha-1}\,dx
= \alpha \int_1^{+\infty} x^{-\alpha+1}\,dx \\
&= \alpha \left[\frac{x^{-\alpha+2}}{-\alpha+2}\right]_1^{+\infty}
= -\alpha \left[\frac{x^{-\alpha+2}}{\alpha-2}\right]_1^{+\infty} \\
&= -\alpha \left(\underbrace{\lim_{x\to+\infty} \frac1{x^{-\alpha+2}(\alpha-2)}}_{0}
-\frac1{1^{-\alpha+2}(\alpha-2)}\right) \\
&= -\alpha \left(0-\frac1{\alpha-2}\right)
= \boxed{\frac\alpha{\alpha-2}\quad\text{se}\quad\alpha>2} \;.
\end{aligned}$$

Infine:

$$\begin{aligned}
\mathrm{Var}(X)
&= E[X^2]-(E[X])^2 \\
&= \frac{\alpha}{\alpha-2} - \left(\frac{\alpha}{\alpha-1}\right)^2 \\
&= \frac{\alpha(\alpha-1)^2-\alpha^2(\alpha-2)}{(\alpha-1)^2(\alpha-2)} \\
&= \frac{\alpha(\alpha^2-2\alpha+1)-\alpha^3+2\alpha^2}{(\alpha-1)^2(\alpha-2)} \\
&= \frac{\cancel{\alpha^3}\cancel{-2\alpha^2}+\alpha\;\cancel{-\alpha^3}\cancel{+2\alpha^2}}{(\alpha-1)^2(\alpha-2)} \\
&= \boxed{\frac{\alpha}{(\alpha-1)^2(\alpha-2)}\quad\text{se}\quad\alpha>2} \;.
\end{aligned}$$

Quindi la varianza è finita se e solo se

$$
\boxed{\alpha>2} \;.
$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 4

Sia $X$ una v.a. tale che $E[X]=3$ e $\mathrm{Var}(X)=2$. Calcolare $E[X^2]$.

##### Risoluzione

Ricordiamo la formula della varianza:

$$
\mathrm{Var}(X)=E[X^2]-(E[X])^2 \;.
$$

Ricaviamo quindi $E[X^2]$:

$$\begin{aligned}
E[X^2]
&= \mathrm{Var}(X)+(E[X])^2 \\
&= 2 + 3^2
= 2 + 9
= \boxed{11} \;.
\end{aligned}$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 5

Sia $X$ una v.a. tale che $E[X]=2$ ed $E[X^2]=9$, e sia $Y=3-2X$. Calcolare $E[Y]$ e $\mathrm{Var}(Y)$.

A) $E[Y]=1,\quad \mathrm{Var}(Y)=-10$
B) $E[Y]=-1,\quad \mathrm{Var}(Y)=-10$
C) $E[Y]=-1,\quad \mathrm{Var}(Y)=20$
D) $E[Y]=1,\quad \mathrm{Var}(Y)=20$

##### Risoluzione

Calcoliamo prima $E[Y]$:

$$\begin{aligned}
E[Y]
&= E[3-2X] \\
&= 3-2E[X] \\
&= 3-2\cdot2
= \boxed{-1} \;.
\end{aligned}$$

Calcoliamo ora $\mathrm{Var}(X)$:

$$\begin{aligned}
\mathrm{Var}(X)
&= E[X^2]-(E[X])^2 \\
&= 9-2^2 \\
&= 9-4
= 5 \;.
\end{aligned}$$

Infine:

$$\begin{aligned}
\mathrm{Var}(Y)
&= \mathrm{Var}(3-2X) \\
&= (-2)^2\mathrm{Var}(X) \\
&= 4\cdot5
= \boxed{20} \;.
\end{aligned}$$

Quindi la risposta corretta è:

$$
\boxed{\text{C}}
$$

> **Nota**: Si potevano escludere subito le risposte A e B perché una varianza non può mai essere negativa.

---

<div style="page-break-after: always;"></div>

#### Esercizio 6

Il raggio di una pizza $X$ è una v.a. uniforme in $[9,11]$.

1. Qual è l’area media?
2. Qual è l’area di una pizza di raggio medio?

##### Risoluzione

Ricordiamo che la densità della uniforme continua è:

$$
f_X(x)=
\begin{cases}
\dfrac1{\beta-\alpha} & x\in[\alpha,\beta] \\
0 & \text{altrimenti}
\end{cases}
$$

e che l’area di un cerchio di raggio $r$ è:

$$
A=\pi r^2 \;.
$$

1. Calcoliamo l’area media:

    $$\begin{aligned}
    E[A]
    &= E[\pi X^2]
    = \pi E[X^2] \\
    &= \pi \int_\alpha^\beta x^2\frac1{\beta-\alpha}\,dx \\
    &= \pi \int_9^{11} x^2\frac1{11-9}\,dx \\
    &= \frac{\pi}{2}\int_9^{11} x^2\,dx \\
    &= \frac{\pi}{2}\left[\frac{x^3}{3}\right]_9^{11} \\
    &= \frac{\pi}{2}\cdot\frac{11^3-9^3}{3} \\
    &= \frac{\pi}{2}\cdot\frac{1331-729}{3} \\
    &= \frac{\pi}{2}\cdot\frac{602}{3} \\
    &= \boxed{\frac{301\pi}{3}\approx315.21} \;.
    \end{aligned}$$

2. Calcoliamo ora l’area della pizza di raggio medio.

    Per una uniforme:

    $$
    E[X]=\frac{\alpha+\beta}{2}
    $$

    quindi:

    $$\begin{aligned}
    E[X]
    &= \frac{9+11}{2}
    = 10 \;.
    \end{aligned}$$

    L’area della pizza di raggio medio vale quindi:

    $$\begin{aligned}
    A(E[X])
    &= \pi(E[X])^2 \\
    &= \pi\cdot10^2 \\
    &= \boxed{100\pi\approx314.16} \;.
    \end{aligned}$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 7

La funzione $g(x)=3x-6$ è:

A) concava
B) convessa
C) concava e convessa
D) né concava né convessa

##### Risoluzione

La funzione $g(x)=3x-6$ è una funzione lineare (una retta).

Le funzioni lineari sono contemporaneamente concave e convesse, poiché vale l’uguaglianza nelle definizioni di concavità e convessità.

Quindi la risposta corretta è la:

$$
\boxed{\text{C}}
$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 8

Sia $X$ una v.a. esponenziale di parametro $3$, e sia $Y$ una gaussiana di media $1$ e varianza $4$. Quale delle seguenti affermazioni è corretta?

A) $E[1/X]\ge3,\quad E[1/Y]\ge1$
B) $E[1/X]\ge1/3,\quad E[1/Y]\le1$
C) $E[1/X]\le1/3,\quad E[1/Y]\le1$
D) $E[1/X]\le3,\quad E[1/Y]\ge1$
E) Nessuna delle precedenti

##### Risoluzione

Consideriamo la funzione

$$
g(x)=\frac1x \;.
$$

Poiché

$$
g''(x)=\frac2{x^3}>0 \qquad (x>0)
$$

allora $g$ è convessa e possiamo applicare la disuguaglianza di Jensen:

$$
E[g(X)]\ge g(E[X]) \;.
$$

- Per la variabile esponenziale $X\sim \mathrm{Exp}(3)$:

    $$
    E[X]=\frac13
    $$

    quindi

    $$
    E\!\left[\frac1X\right]\ge\frac1{E[X]}
    = \frac1{1/3}
    = 3 \;.
    $$

- Per la gaussiana $Y$:

    $$
    E[Y]= 1
    $$

    <div style="page-break-after: always;"></div>

    e quindi formalmente Jensen darebbe

    $$
    E\!\left[\frac1Y\right]\ge \frac1{E[Y]} = \frac11 = 1 \;.
    $$

    Tuttavia $Y$ può assumere anche valori negativi e inoltre la funzione $1/x$ non è definita in $0$; quindi $E[1/Y]$ non esiste.

Di conseguenza nessuna delle risposte proposte è corretta.

$$
\boxed{\text{E}}
$$

---

<div style="page-break-after: always;"></div>