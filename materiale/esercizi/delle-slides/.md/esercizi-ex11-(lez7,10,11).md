## $$ \textcolor{red}{\text{Esercizi Ex. 11 - Lez. 7,10,11}} $$

#### Esercizio 1

Si estrae più volte, con rimessa, una carta da un mazzo di carte ogni volta ben mescolato. La probabilità che esca "quadri" è $1/4$. Sia $T$ il tempo di attesa di una carta "quadri".

- (a) Trova $P(T = 4)$;
- (b) Dimostra che è uguale ad essa la probabilità condizionata $P(T = 7\mid T > 3)$.

##### Risoluzione

Definiamo la variabile aleatoria

$$
T = \{\text{numero di estrazioni necessarie per ottenere la prima carta di quadri}\}.
$$

Poiché le estrazioni avvengono **con rimessa**, ogni prova è indipendente dalle precedenti e la probabilità di successo rimane costante:

$$
p=P(\text{quadri})=\frac14
$$

Siamo quindi nel caso di una distribuzione geometrica:

$$
T\sim\mathrm{Geom}\!\left(p=1/4\right)
$$

> **Ricordiamo**. La funzione di probabilità della distribuzione geometrica è
>
> $$
> P(T=k)=p(1-p)^{k-1},
> \qquad k=1,2,\ldots
> $$

Nel nostro caso:

$$
P(T=k)=\frac14\left(\frac34\right)^{k-1}
$$

- **(a)** Calcoliamo la probabilità richiesta:

    $$\begin{aligned}
    P(T=4)
    &= \frac14\left(\frac34\right)^3
    = \frac14\cdot\frac{27}{64}
    = \frac{27}{256}
    \approx \boxed{0.1055} \;.
    \end{aligned}$$

- **(b)** Dimostriamo che

    $$
    P(T=7\mid T>3)=P(T=4)
    $$

    Utilizziamo la definizione di probabilità condizionata:

    $$\begin{aligned}
    P(T=7\mid T>3)
    &= \frac{P(T>3\mid T=7)P(T=7)}{P(T>3)}
    \end{aligned}$$

    Poiché l'evento $T=7$ implica automaticamente $T>3$, si ha

    $$
    P(T>3\mid T=7)=1
    $$

    Pertanto:

    $$\begin{aligned}
    P(T=7\mid T>3)
    &= \frac{P(T=7)}{P(T>3)} \\
    &= \frac{\frac14\left(\frac34\right)^6}
            {\left(\frac34\right)^3} \\
    &= \frac14\left(\frac34\right)^3
    = P(T=4)
    \end{aligned}$$

    Quindi

    $$
    \boxed{P(T=7\mid T>3)=P(T=4)} \;.
    $$

> **Nota.** Questo risultato è una manifestazione della **proprietà di assenza di memoria** (*memoryless property*) della distribuzione geometrica:
>
> $$ P(T>m+n\mid T>m)=P(T>n) $$
>
> In altre parole, dopo aver atteso $m$ prove senza successo, il processo "riparte da zero" e la distribuzione del tempo di attesa residuo rimane invariata.
>
> La distribuzione geometrica è l'analogo discreto della distribuzione esponenziale, che possiede la stessa proprietà nel caso continuo.

---

<div style="page-break-after: always;"></div>

#### Esercizio 2

Un calcolatore in ogni addizione assicura un errore $X$ uniformemente distribuito in $[-0.5\times10^{-10},\,0.5\times10^{-10}]$.

- (a) Trova la varianza $\sigma^2$ della variabile $X$;
- (b) Trova la probabilità $P(-\sigma < X < \sigma)$.

##### Risoluzione

Definiamo la variabile aleatoria

$$
X=\{\text{errore commesso dal calcolatore in una singola addizione}\}.
$$

Modelliamo il problema mediante una distribuzione uniforme continua:

$$
X\sim U\!\left(\alpha=-0.5\times10^{-10},\;\beta=0.5\times10^{-10}\right)
$$

> **Ricordiamo.** La densità di una variabile uniforme continua su $[\alpha,\beta]$ è
>
> $$
> f_X(x)=
> \begin{cases}
> \dfrac1{\beta-\alpha} & \alpha\le x\le\beta \\[6pt]
> 0 & \text{altrimenti.}
> \end{cases}
> $$

- **(a)** Calcolare la varianza $\sigma^2$ della variabile $X$.

    - Per prima cosa calcoliamo l'aspettazione:

        $$\begin{aligned}
        E[X]
        &= \int_\alpha^\beta x\,f_X(x)\,dx \\
        &= \int_{-0.5\times10^{-10}}^{0.5\times10^{-10}}
        x\,\frac1{0.5\times10^{-10}-(-0.5\times10^{-10})}\,dx \\
        &= \frac1{10^{-10}}
        \left[\frac{x^2}{2}\right]_{-0.5\times10^{-10}}^{0.5\times10^{-10}} \\
        &= 10^{10}\cdot
        \frac{(0.5\times10^{-10})^2-(-0.5\times10^{-10})^2}{2} \\
        &= 10^{10}\cdot 0
        = 0
        \end{aligned}$$

        Quindi

        $$
        \mu_X=E[X]=0
        $$

        > **Osservazione.** Non era necessario svolgere il calcolo integrale. Poiché l'intervallo è simmetrico rispetto a $0$, la media dell'uniforme è
        >
        > $$
        > E[X]=\frac{\alpha+\beta}{2}
        > =\frac{-0.5\times10^{-10}+0.5\times10^{-10}}{2}
        > =0
        > $$

    - Calcoliamo ora $E[X^2]$:

        $$\begin{aligned}
        E[X^2]
        &= \int_\alpha^\beta x^2\,f_X(x)\,dx \\
        &= \int_{-0.5\times10^{-10}}^{0.5\times10^{-10}}
        x^2\,\frac1{10^{-10}}\,dx \\
        &= 10^{10}
        \left[\frac{x^3}{3}\right]_{-0.5\times10^{-10}}^{0.5\times10^{-10}} \\
        &= \frac{10^{10}}{3}
        \left[
        (0.5\times10^{-10})^3
        -(-0.5\times10^{-10})^3
        \right] \\
        &= \frac{10^{10}}{3}
        \left[
        2(0.5\times10^{-10})^3
        \right] \\
        &= \frac{2}{3}\cdot10^{10}\cdot0.125\cdot10^{-30} \\
        &= \frac1{12}\cdot10^{-20}
        \end{aligned}$$

    - Infine calcoliamo la varianza:

        $$\begin{aligned}
        \mathrm{Var}(X)
        &= E[X^2]-(E[X])^2 \\
        &= \frac1{12}\cdot10^{-20}-0^2 \\
        &= \boxed{\frac1{12}\cdot10^{-20}} \;.
        \end{aligned}$$

        Equivalentemente,

        $$
        \boxed{\sigma^2
        =8.33\times10^{-22}} \;.
        $$

- **(b)** Calcolare la probabilità $P(-\sigma < X < \sigma)$.

    - Possiamo scrivere la probabilità richiesta come:

        $$\begin{aligned}
        P(-\sigma<X<\sigma)
        &= P(X<\sigma)-P(X\le-\sigma) \\
        &= F(\sigma)-F(-\sigma)
        \end{aligned}$$

        Tuttavia, essendo $X$ una variabile continua, è più comodo calcolarla direttamente come area sotto la densità nell'intervallo $[-\sigma,\sigma]$:

        $$
        P(-\sigma<X<\sigma)
        = \int_{-\sigma}^{\sigma} f_X(x)\,dx
        $$

        Dalla parte precedente sappiamo che

        $$
        \sigma=\sqrt{\frac1{12}\cdot10^{-20}}
        \approx 2.886\times10^{-11}
        $$

    - Calcoliamo quindi la probabilità richiesta:

        $$\begin{aligned}
        P(-\sigma<X<\sigma)
        &= \int_{-\sigma}^{\sigma}
        \frac1{\beta-\alpha}\,dx \\
        &= \int_{-\sigma}^{\sigma}
        \frac1{10^{-10}}\,dx \\
        &= 10^{10}\,[x]_{-\sigma}^{\sigma} \\
        &= 10^{10}\,(\sigma-(-\sigma)) \\
        &= 2\sigma\cdot10^{10} \\
        &= 2\cdot(2.886\times10^{-11})\cdot10^{10} \\
        &\approx \boxed{0.577} \;.
        \end{aligned}$$

---

<div style="page-break-after: always;"></div>