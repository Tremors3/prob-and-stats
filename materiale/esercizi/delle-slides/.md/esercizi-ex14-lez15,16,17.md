## $$ \textcolor{red}{\text{Esercizi Ex. 14 - Lez. 15,16,17}} $$

#### Esercizio 1

Sia $(X,Y)$ un vettore aleatorio discreto con funzione di probabilità:

$$\begin{aligned}
f(0,3) = 0.10 &\qquad& f(0,7) = 0.05 \\
f(1,3) = 0.20 &\qquad& f(1,7) = 0.15 \\
f(2,3) = 0.20 &\qquad& f(2,7) = 0.30
\end{aligned}$$

- (a) Trovare le medie e le varianze delle marginali.
- (b) Trovare la covarianza.
- (c) Calcolare la varianza della somma $X+Y$.

##### Risoluzione

- **(a) Calcolare medie e varianze delle marginali.**

    Come prima cosa calcoliamo le distribuzioni marginali.

    $$\begin{aligned}
    f_X(0) &= 0.10 + 0.05 = 0.15 \\
    f_X(1) &= 0.20 + 0.15 = 0.35 \\
    f_X(2) &= 0.20 + 0.30 = 0.50
    \end{aligned}$$

    $$\begin{aligned}
    f_Y(3) &= 0.10 + 0.20 + 0.20 = 0.50 \\
    f_Y(7) &= 0.05 + 0.15 + 0.30 = 0.50
    \end{aligned}$$

    Calcoliamo ora le aspettazioni delle marginali.

    $$\begin{aligned}
    E[X]
    &= \sum_{x\in\{0,1,2\}} x\,f_X(x) \\
    &= 0\cdot0.15 + 1\cdot0.35 + 2\cdot0.50
    = \boxed{1.35}\;.
    \\[6pt]
    E[Y]
    &= \sum_{y\in\{3,7\}} y\,f_Y(y) \\
    &= 3\cdot0.50 + 7\cdot0.50 \\
    &= 1.5 + 3.5
    = \boxed{5}\;.
    \end{aligned}$$

    Calcoliamo i momenti secondi.

    $$\begin{aligned}
    E[X^2]
    &= \sum_{x\in\{0,1,2\}} x^2\,f_X(x) \\
    &= 0^2\cdot0.15 + 1^2\cdot0.35 + 2^2\cdot0.50 \\
    &= 0 + 0.35 + 2 \\
    &= 2.35
    \end{aligned}$$

    $$\begin{aligned}
    E[Y^2]
    &= \sum_{y\in\{3,7\}} y^2\,f_Y(y) \\
    &= 3^2\cdot0.50 + 7^2\cdot0.50 \\
    &= 4.5 + 24.5 \\
    &= 29
    \end{aligned}$$

    Calcoliamo infine le varianze.

    $$\begin{aligned}
    \text{Var}(X)
    &= E[X^2] - (E[X])^2 \\
    &= 2.35 - (1.35)^2 \\
    &= 2.35 - 1.8225 \\
    &= \boxed{0.5275}\;.
    \end{aligned}$$

    $$\begin{aligned}
    \text{Var}(Y)
    &= E[Y^2] - (E[Y])^2 \\
    &= 29 - 5^2 \\
    &= \boxed{4}\;.
    \end{aligned}$$

- **(b) Calcolare la covarianza.**

    Per prima cosa calcoliamo l'ultima aspettazione necessaria.

    $$\begin{aligned}
    E[XY]
    &= \sum_{(x,y)\,\in\,\{0,1,2\}\times\{3,7\}} xy\,f_{X,Y}(x,y) \\
    &= (0\cdot3)0.10 + (0\cdot7)0.05 \\
    &\quad + (1\cdot3)0.20 + (1\cdot7)0.15 \\
    &\quad + (2\cdot3)0.20 + (2\cdot7)0.30 \\
    &= 0 + 0 + 0.60 + 1.05 + 1.20 + 4.20 \\
    &= 7.05
    \end{aligned}$$

    Calcoliamo quindi la covarianza.

    $$\begin{aligned}
    \text{Cov}(X,Y)
    &= E[XY] - E[X]E[Y] \\
    &= 7.05 - 1.35\cdot5 \\
    &= 7.05 - 6.75 \\
    &= \boxed{0.30}\;.
    \end{aligned}$$

    La covarianza è positiva, quindi $X$ e $Y$ sono positivamente correlate.

    $\;$

- **(c) Calcolare la varianza della somma $X+Y$.**

    Utilizziamo la formula

    $$
    \text{Var}(X+Y)
    = \text{Var}(X) + \text{Var}(Y) + 2\text{Cov}(X,Y).
    $$

    Sostituendo i valori ottenuti:

    $$\begin{aligned}
    \text{Var}(X+Y)
    &= 0.5275 + 4 + 2(0.30) \\
    &= 0.5275 + 4 + 0.6 \\
    &= \boxed{5.1275}\;.
    \end{aligned}$$

> **Nota.** Formule utilizzate:
>
> $$
> E[X] = \sum_x x\,p_X(x)
> $$
>
> $$
> E[X^2] = \sum_x x^2\,p_X(x)
> $$
>
> $$
> \text{Var}(X)
> = E[X^2] - (E[X])^2
> $$
>
> $$
> \text{Cov}(X,Y)
> = E[XY] - E[X]E[Y]
> $$
>
> $$
> \text{Var}(aX+bY + c)
> = a^2\text{Var}(X) + b^2\text{Var}(Y) + 2ab\text{Cov}(X,Y).
> $$

---

<div style="page-break-after: always;"></div>

#### Esercizio 2

Una lampada è composta da 2 lampadine. La durata $X$ di una lampadina, misurata in ore, è normale di media 1000 e varianza 20000. La durata $Y$ dell’altra lampadina è normale di media 800 e varianza 30000. La covarianza tra $X$ e $Y$ è nulla.

- (a) Trovare la probabilità che la prima duri almeno 300 ore più della seconda.
- (b) Si decide di usare la prima lampadina e, quando questa brucia, di usare la seconda: trovare la probabilità che la durata totale sia maggiore di 2000 ore.

##### Risoluzione

- **(a) Trovare la probabilità che la prima duri almeno 300 ore più della seconda.**

    Il problema richiede di calcolare:

    $$\begin{aligned}
    P(X \ge Y + 300)
    &= P(X - Y \ge 300).
    \end{aligned}$$

    Definiamo quindi una nuova variabile aleatoria:

    $$
    Z = X - Y.
    $$

    Per calcolare la probabilità richiesta dobbiamo determinare media e varianza di $Z$.

    $$\begin{aligned}
    E[Z]
    &= E[X-Y] \\
    &= E[X]-E[Y] \\
    &= 1000-800 \\
    &= 200.
    \end{aligned}$$

    $$\begin{aligned}
    \text{Var}(Z)
    &= \text{Var}(X-Y) \\
    &= \text{Var}(X)+(-1)^2\text{Var}(Y)
       +2(1)(-1)\text{Cov}(X,Y) \\
    &= 20000+30000-2\text{Cov}(X,Y) \\
    &= 20000+30000-2\cdot0 \\
    &= 50000
    \end{aligned}$$

    Poiché $X$ e $Y$ sono scorrelate $\text{Cov}(X,Y)=0$.

    $\;$

    Inoltre, essendo $X$ e $Y$ gaussiane con covarianza nulla, la variabile $Z=X-Y$ è ancora gaussiana: $Z \sim N(200,50000)$.

    $\;$

    Possiamo quindi standardizzare:

    $$\begin{aligned}
    P(Z\ge300)
    &= 1-P(Z<300) \\
    &= 1-\Phi\!\left(
    \frac{300-200}{\sqrt{50000}}
    \right) \\
    &= 1-\Phi(0.4472) \\
    &\approx 1-0.67264 \\
    &= \boxed{0.32736}\;.
    \end{aligned}$$

- **(b) Si decide di usare la prima lampadina e, quando questa brucia, di usare la seconda: trovare la probabilità che la durata totale sia maggiore di 2000 ore.**

    In questo caso la durata totale è data dalla somma delle due durate.

    $$\begin{aligned}
    P(X+Y>2000).
    \end{aligned}$$

    Definiamo quindi una nuova variabile aleatoria:

    $$
    Z=X+Y.
    $$

    Calcoliamo media e varianza di $Z$.

    $$\begin{aligned}
    E[Z]
    &= E[X+Y] \\
    &= E[X]+E[Y] \\
    &= 1000+800 \\
    &= 1800.
    \end{aligned}$$

    $$\begin{aligned}
    \text{Var}(Z)
    &= \text{Var}(X+Y) \\
    &= \text{Var}(X)+\text{Var}(Y)
       +2\text{Cov}(X,Y) \\
    &= 20000+30000+2\cdot0 \\
    &= 50000.
    \end{aligned}$$

    Quindi

    $$
    Z \sim N(1800,50000).
    $$

    Calcoliamo la probabilità richiesta.

    $$\begin{aligned}
    P(Z>2000)
    &= 1-P(Z\le2000) \\
    &= 1-\Phi\!\left(
    \frac{2000-1800}{\sqrt{50000}}
    \right) \\
    &= 1-\Phi(0.8944) \\
    &\approx 1-0.81445 \\
    &= \boxed{0.18555}\;.
    \end{aligned}$$

> **Nota.** Se $X$ e $Y$ sono variabili gaussiane con covarianza nulla, allora:
>
> $$
> X\pm Y \sim N\!\left(
> E[X]\pm E[Y],\;
> \text{Var}(X)+\text{Var}(Y)
> \right).
> $$
>
> Inoltre:
>
> $$
> \text{Var}(X\pm Y)
> = \text{Var}(X) + \text{Var}(Y) \pm 2\text{Cov}(X,Y).
> $$

---

<div style="page-break-after: always;"></div>

#### Esercizio 3

Siano $X$, $Y$ v.a. discrete con funzione di probabilità

$$\begin{aligned}
f(1,10)=\frac6{13} &\qquad& f(1,20)=\frac1{13} \\
f(2,10)=\frac3{13} &\qquad& f(2,20)=\frac3{13}
\end{aligned}$$

- (a) calcolare la covarianza di $X$ e $Y$;
- (b) calcolare le varianze di $X$ e di $Y$;
- (c) calcolare la varianza di $3X+Y$.

##### Risoluzione

- **(a) Calcolare la covarianza di $X$ e $Y$.**

    Come prima cosa calcoliamo le marginali di $X$ e di $Y$.

    $$\begin{aligned}
    f_X(1) &= \frac6{13}+\frac1{13}=\frac7{13} \\
    f_X(2) &= \frac3{13}+\frac3{13}=\frac6{13}
    \end{aligned}
    \qquad\qquad
    \begin{aligned}
    f_Y(10) &= \frac6{13}+\frac3{13}=\frac9{13} \\
    f_Y(20) &= \frac1{13}+\frac3{13}=\frac4{13}
    \end{aligned}$$

    Calcoliamo ora le aspettazioni di $X$ e di $Y$.

    $$\begin{aligned}
    E[X]
    &= \sum_{x\in\{1,2\}} x\,f_X(x) \\
    &= 1\cdot\frac7{13}+2\cdot\frac6{13} \\
    &= \frac{19}{13}.
    \end{aligned}$$

    $$\begin{aligned}
    E[Y]
    &= \sum_{y\in\{10,20\}} y\,f_Y(y) \\
    &= 10\cdot\frac9{13}+20\cdot\frac4{13} \\
    &= \frac{170}{13}.
    \end{aligned}$$

    <div style="page-break-after: always;"></div>

    Calcoliamo inoltre:

    $$\begin{aligned}
    E[XY]
    &= \sum_{(x,y)\in\{1,2\}\times\{10,20\}} xy\,f_{X,Y}(x,y) \\
    &= (1\cdot10)\frac6{13}+(1\cdot20)\frac1{13} \\
    &\quad +(2\cdot10)\frac3{13}+(2\cdot20)\frac3{13} \\
    &= \frac{260}{13}.
    \end{aligned}$$

    Possiamo quindi calcolare la covarianza.

    $$\begin{aligned}
    \text{Cov}(X,Y)
    &= E[XY]-E[X]E[Y] \\
    &= \frac{260}{13}
       -\frac{19}{13}\cdot\frac{170}{13} \\
    &= \frac{3380-3230}{169} \\
    &= \boxed{\frac{150}{169}}.
    \end{aligned}$$

    La covarianza è positiva, quindi $X$ e $Y$ risultano positivamente correlate.

    $\;$

- **(b) Calcolare le varianze di $X$ e di $Y$.**

    Calcoliamo innanzitutto i momenti secondi.

    $$\begin{aligned}
    E[X^2]
    &= \sum_{x\in\{1,2\}} x^2\,f_X(x) \\
    &= (1)^2\frac7{13}+(2)^2\frac6{13} \\
    &= \frac{31}{13}.
    \end{aligned}$$

    $$\begin{aligned}
    E[Y^2]
    &= \sum_{y\in\{10,20\}} y^2\,f_Y(y) \\
    &= (10)^2\frac9{13}+(20)^2\frac4{13} \\
    &= \frac{2500}{13}.
    \end{aligned}$$

    <div style="page-break-after: always;"></div>

    Calcoliamo ora le varianze.

    $$\begin{aligned}
    \text{Var}(X)
    &= E[X^2]-(E[X])^2 \\
    &= \frac{31}{13}
       -\left(\frac{19}{13}\right)^2 \\
    &= \boxed{\frac{42}{169}}.
    \end{aligned}$$

    $$\begin{aligned}
    \text{Var}(Y)
    &= E[Y^2]-(E[Y])^2 \\
    &= \frac{2500}{13}
       -\left(\frac{170}{13}\right)^2 \\
    &= \boxed{\frac{3600}{169}}.
    \end{aligned}$$

    $\;$

- **(c) Calcolare la varianza di $3X+Y$.**

    Utilizziamo la formula:

    $$
    \text{Var}(aX+bY)
    = a^2\text{Var}(X) + b^2\text{Var}(Y) + 2ab\,\text{Cov}(X,Y).
    $$

    Nel nostro caso:

    $$\begin{aligned}
    \text{Var}(3X+Y)
    &= 3^2\text{Var}(X) + \text{Var}(Y) + 2\cdot3\cdot1\,\text{Cov}(X,Y) \\
    &= 9\cdot\frac{42}{169} + \frac{3600}{169} + 6\cdot\frac{150}{169} \\
    &= \frac{378+3600+900}{169} \\
    &= \boxed{\frac{4878}{169}}.
    \end{aligned}$$

> **Nota.** Formule utilizzate:
>
> $$
> \text{Cov}(X,Y)=E[XY]-E[X]E[Y]
> $$
>
> $$
> \text{Var}(X)=E[X^2]-(E[X])^2
> $$
>
> $$
> \text{Var}(aX+bY)
> =a^2\text{Var}(X)
> +b^2\text{Var}(Y)
> +2ab\,\text{Cov}(X,Y).
> $$

---

<div style="page-break-after: always;"></div>

#### Esercizio 4

La densità congiunta di $X$ e $Y$ è

$$
f(x,y)=
\begin{cases}
c(x+y^4) & \text{per } 0\le x,y\le1 \\
0 & \text{altrove}
\end{cases}
$$

Trovare:

- (a) il fattore di normalizzazione $c$ in modo che $f$ sia una densità di probabilità;
- (b) la densità marginale di $Y$.

##### Risoluzione

- **(a) Trovare il fattore di normalizzazione $c$.**

    Affinché $f(x,y)$ sia una densità di probabilità deve valere:

    $$
    \int_{-\infty}^{+\infty}
    \int_{-\infty}^{+\infty}
    f(x,y)\,dy\,dx = 1
    $$

    Poiché

    $$
    f(x,y)=c\cdot g(x,y)
    \qquad\text{con}\qquad
    g(x,y)=x+y^4
    $$

    si ha:

    $$\begin{aligned}
    c
    \int_{-\infty}^{+\infty}
    \int_{-\infty}^{+\infty}
    g(x,y)\,dy\,dx
    &= 1 \\
    c
    &= \frac{1}{
    \displaystyle
    \int_{-\infty}^{+\infty}
    \int_{-\infty}^{+\infty}
    g(x,y)\,dy\,dx}
    \end{aligned}$$

    <div style="page-break-after: always;"></div>

    Calcoliamo quindi l'integrale.

    $$\begin{aligned}
    \int_{-\infty}^{+\infty}
    \int_{-\infty}^{+\infty}
    g(x,y)\,dy\,dx
    &= \int_0^1\int_0^1 (x+y^4)\,dy\,dx \\
    &= \int_0^1
    \left(
    x\int_0^1 dy
    +
    \int_0^1 y^4\,dy
    \right)dx \\
    &= \int_0^1
    \left(
    x+\frac15
    \right)dx \\
    &= \int_0^1 x\,dx
    +
    \frac15\int_0^1 dx \\
    &= \frac12+\frac15 \\
    &= \frac7{10}
    \end{aligned}$$

    Pertanto:

    $$
    c
    = \frac{1}{7/10}
    = \boxed{\frac{10}{7}} \;.
    $$

    La densità congiunta diventa quindi:

    $$
    \boxed{
    f(x,y)=
    \begin{cases}
    \frac{10}{7}(x+y^4) & \text{per } 0\le x,y\le1 \\
    0 & \text{altrove}
    \end{cases}
    } \;.
    $$

    <div style="page-break-after: always;"></div>

- **(b) Calcolare la densità marginale di $Y$.**

    La densità marginale di $Y$ si ottiene integrando la densità congiunta rispetto a $x$.

    $$\begin{aligned}
    f_Y(y)
    &= \int_{-\infty}^{+\infty}
    f_{X,Y}(x,y)\,dx \\
    &= \int_0^1
    \frac{10}{7}(x+y^4)\,dx \\
    &= \frac{10}{7}
    \left(
    \int_0^1 x\,dx
    +
    y^4\int_0^1 dx
    \right) \\
    &= \frac{10}{7}
    \left(
    \left[\frac{x^2}{2}\right]_0^1
    +
    y^4[x]_0^1
    \right) \\
    &= \frac{10}{7}
    \left(
    \frac12+y^4
    \right),
    \qquad 0\le y\le1
    \end{aligned}$$

    La densità marginale di $Y$ è quindi:

    $$
    \boxed{
    f_Y(y)=
    \begin{cases}
    \frac{10}{7}\left(\frac12+y^4\right)
    & \text{per } 0\le y\le1 \\[4pt]
    0
    & \text{altrove}
    \end{cases}
    }.
    $$

---

<div style="page-break-after: always;"></div>