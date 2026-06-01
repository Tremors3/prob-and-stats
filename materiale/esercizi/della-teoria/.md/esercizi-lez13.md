## $$ \textcolor{red}{\text{Esercizi Lez. 13 - Teoria}} $$

#### Esercizio 1 $-$ Calcolo FGM $-$ caso discreto

Calcolare la FGM e i momenti primo e secondo delle seguenti variabili aleatorie:

1. $X \in \{1, 2, 3, 4, 5, 6\}$ Uniforme Discreta
2. $Y \sim \text{Ber}(p)$
3. $Z \sim \text{Geom}(p)$

##### Risoluzione

1. **Calcolare la FGM e i momenti di $X$**.

    $$
    X \in \{1,2,3,4,5,6\}
    \qquad
    \text{Uniforme Discreta}
    $$

    Si tratta di una distribuzione uniforme discreta e quindi equiprobabile sui punti del supporto.

    $$
    p_X(k)=\frac16,
    \qquad
    k\in S_X=\{1,2,3,4,5,6\}.
    $$

    - **Calcoliamo la FGM:**

        $$\begin{aligned}
        G_X(t)
        &=E[e^{tk}]\\
        &=\sum_{k\in S_X} e^{tk}\,p_X(k)\\
        &=\sum_{k\in S_X}\frac16 e^{tk}\\
        &=\boxed{\frac16\left(e^t+e^{2t}+e^{3t}+e^{4t}+e^{5t}+e^{6t}\right)} \;.
        \end{aligned}$$

    - **Primo momento:**

        $$\begin{aligned}
        G'_X(t)
        &=\frac16\left(e^t+2e^{2t}+3e^{3t}+4e^{4t}+5e^{5t}+6e^{6t}\right).
        \end{aligned}$$

        <div style="page-break-after: always;"></div>

        Sostituiamo $t=0$ e otteniamo il momento primo:

        $$\begin{aligned}
        E[X]
        =G'_X(0)
        &=\frac16\left(1+2+3+4+5+6\right)\\
        &=\frac{6(6+1)}{6\cdot2}\\
        &=\boxed{\frac72=3.5} \;.
        \end{aligned}$$

    - **Secondo momento:**

        $$\begin{aligned}
        G''_X(t)
        &=\frac16\left(e^t+2^2e^{2t}+3^2e^{3t}+4^2e^{4t}+5^2e^{5t}+6^2e^{6t}\right).
        \end{aligned}$$

        Sostituiamo $t=0$ e otteniamo il momento secondo:

        $$\begin{aligned}
        E[X^2]
        =G''_X(0)
        &=\frac16\left(1+2^2+3^2+4^2+5^2+6^2\right)\\
        &=\boxed{\frac{91}{6}\approx15.17} \;.
        \end{aligned}$$

<div style="page-break-after: always;"></div>

2. **Calcolare la FGM e i momenti di $Y$**.

    $$
    Y\sim\text{Ber}(p)
    $$

    - **Calcoliamo la FGM:**

        $$\begin{aligned}
        G_Y(t)
        &=E[e^{tk}]\\
        &=\sum_{k\in S_Y} e^{tk}\,p_Y(k)\\
        &=\sum_{k\in\{0,1\}} e^{tk}\,p^k(1-p)^{1-k}\\
        &=1\cdot(1-p)+e^t p\\
        &=\boxed{pe^t+(1-p)} \;.
        \end{aligned}$$

    - **Primo momento:**

        $$\begin{aligned}
        G'_Y(t)
        &=pe^t.
        \end{aligned}$$

        Sostituiamo $t=0$ e otteniamo il momento primo:

        $$\begin{aligned}
        E[Y]
        =G'_Y(0)
        &=pe^0\\
        &=\boxed{p} \;.
        \end{aligned}$$

    - **Secondo momento:**

        $$\begin{aligned}
        G''_Y(t)
        &=pe^t.
        \end{aligned}$$

        Sostituiamo $t=0$ e otteniamo il momento secondo:

        $$\begin{aligned}
        E[Y^2]
        =G''_Y(0)
        &=pe^0\\
        &=\boxed{p} \;.
        \end{aligned}$$

    > **Nota**. In generale, per una Bernoulli vale $Y^n=Y$ per ogni $n\ge1$, quindi tutti i momenti non nulli coincidono con $p$.

<div style="page-break-after: always;"></div>

3. **Calcolare la FGM e i momenti di $Z$**.

    $$
    Z\sim\text{Geom}(p)
    $$

    Assumiamo la convenzione

    $$
    P(Z=k)=p(1-p)^{k-1},
    \qquad
    k=1,2,\ldots
    $$

    - **Calcoliamo la FGM:**

        $$\begin{aligned}
        G_Z(t)
        &=E[e^{tk}]\\
        &=\sum_{k=1}^{\infty} e^{tk}\,p_Z(k)\\
        &=p\sum_{k=1}^{\infty} e^{tk}(1-p)^{k-1}\\
        &=p\sum_{k=1}^{\infty}(e^t)^{k-1+1}(1-p)^{k-1}\\
        &=pe^t\sum_{k=1}^{\infty}(e^t)^{k-1}(1-p)^{k-1}\\
        &=pe^t\sum_{k=1}^{\infty}\left(e^t(1-p)\right)^{k-1}\\
        &=pe^t\sum_{n=0}^{\infty}\left(e^t(1-p)\right)^n.
        \end{aligned}$$

        La serie geometrica converge se

        $$
        e^t(1-p)<1
        \qquad\Longleftrightarrow\qquad
        t<\log\frac1{1-p}.
        $$

        Quindi

        $$\begin{aligned}
        G_Z(t)
        &=pe^t\cdot\frac1{1-e^t(1-p)}\\
        &=\boxed{
        \begin{cases}
        \dfrac{pe^t}{1-e^t(1-p)}
        &
        t<\log\frac1{1-p}
        \\[8pt]
        \infty
        &
        t\ge\log\frac1{1-p}
        \end{cases}}
        \;.
        \end{aligned}$$

    - **Primo momento:**

        $$\begin{aligned}
        G'_Z(t)
        &=\frac{pe^t(1-e^t(1-p))-pe^t(-e^t(1-p))}
        {(1-e^t(1-p))^2}\\
        &=\frac{pe^t\big(1-e^t(1-p)+e^t(1-p)\big)}
        {(1-e^t(1-p))^2}\\
        &=\frac{pe^t}{(1-e^t(1-p))^2}.
        \end{aligned}$$

        Sostituiamo $t=0$ e otteniamo il momento primo:

        $$\begin{aligned}
        E[Z]
        =G'_Z(0)
        &=\frac{pe^0}{(1-e^0(1-p))^2}\\
        &=\frac{p}{(1-(1-p))^2}\\
        &=\frac{p}{p^2}\\
        &=\boxed{\frac1p} \;.
        \end{aligned}$$

    - **Secondo momento:**

        $$\begin{aligned}
        G''_Z(t) &= \frac{pe^t(1-e^t(1-p))^2 - pe^t\Big[2(1-e^t(1-p))(-e^t(1-p))\Big] }{(1-e^t(1-p))^4} \\
        &= \frac{pe^t(1-e^t(1-p))\Big[1 - e^t(1-p) + 2e^t(1-p) \Big]}{(1-e^t(1-p))^4} \\
        &= \frac{pe^t(1-e^t(1-p))\Big[1 + e^t(1-p) \Big]}{(1-e^t(1-p))^4} \\
        &= \frac{pe^t (1 + e^t(1-p)) }{(1-e^t(1-p))^3} \\
        \end{aligned}$$

        <div style="page-break-after: always;"></div>

        Sostituiamo $t=0$ e otteniamo il momento secondo:

        $$\begin{aligned}
        E[Z^2] = G''_Z(0) &= \frac{pe^0 (1 + e^0(1-p)) }{(1-e^0(1-p))^3} \\
        &= \frac{p(1+(1-p))}{(1-(1-p))^3} \\
        &= \frac{2p-p^2}{p^3}
        = \frac{p(2-p)}{p^3}
        = \boxed{
            \frac{2-p}{p^2}
        } \;.
        \end{aligned}$$

> **Nota**. Non era necessario calcolare esplicitamente questi momenti dato che sulla tabella che potremo usare all'esame la prof ci fornisce già aspettazione e varianza. Tuttavia è un esercizio utile perché mostra come ricavare i momenti direttamente dalla FGM.

> **Nota**. Formule da ricordare per FGM e momenti:
>
> - La **funzione generatrice dei momenti** (FGM) di una variabile aleatoria $X$ è definita come
>
> $$
> G_X(t)=E[e^{tX}].
> $$
>
> - Se la FGM esiste in un intorno di $t=0$, il momento $n$-esimo si ottiene derivando $n$ volte la FGM e valutando in $t=0$:
>
> $$
> E[X^n]=G_X^{(n)}(0).
> $$
>
> In particolare:
>
> $$
> E[X]=G_X'(0),
> $$
>
> $$
> E[X^2]=G_X''(0).
> $$
>
> - Una volta ottenuti i primi due momenti, la varianza si calcola tramite
>
> $$
> \operatorname{Var}(X)
> =E[X^2]-\big(E[X]\big)^2.
> $$
>
> - Se $X$ e $Y$ hanno la stessa FGM in un intorno di $t=0$, allora hanno la stessa distribuzione.

---

<div style="page-break-after: always;"></div>

#### Esercizio 2 $-$ Calcolo FGM $-$ caso continuo

Calcolare la FGM e i momenti delle seguenti variabili aleatorie:

4. $Z \sim N(0,1)$
5. $X \sim \text{Exp}(\lambda)$
6. $Y \sim \text{Par}(\alpha)$, per quali valori di $t$, $G_X(t)$ è finita?

##### Risoluzione

4. **Calcolare la FGM e i momenti di $Z$**.

    $$
    Z \sim N(0,1)
    $$

    La cui densità di probabilità è

    $$
    f_Z(x) = \frac{1}{\sqrt{2\pi}} e^{-\frac{x^2}{2}}
    $$

    per 

    $$
    \mu=0, \qquad \sigma^2=1
    $$

    - **Calcoliamo la FGM di $Z$:**

        $$\begin{aligned}
        G_Z(t) = E[e^{tZ}]
        &= \int_{-\infty}^{+\infty} e^{tx}\,f_Z(x)\,dx \\
        &= \int_{-\infty}^{+\infty} e^{tx}\frac{1}{\sqrt{2\pi}} e^{-\frac{x^2}{2}}\,dx \\
        &= \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{+\infty} e^{tx-\frac{x^2}{2}}\,dx
        \end{aligned}$$

        Completiamo il quadrato nell’esponente:

        $$
        tx-\frac{x^2}{2}
        = -\frac{1}{2}(x^2-2tx)
        = -\frac{1}{2}\big[(x-t)^2 - t^2\big]
        $$

        quindi:

        $$
        tx-\frac{x^2}{2}
        = -\frac{(x-t)^2}{2} + \frac{t^2}{2}
        $$

        Sostituendo nell’integrale:

        $$\begin{aligned}
        G_Z(t)
        &= \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{+\infty}
        e^{-\frac{(x-t)^2}{2}} \cdot e^{\frac{t^2}{2}}\,dx \\
        &= e^{\frac{t^2}{2}} \cdot \frac{1}{\sqrt{2\pi}}
        \int_{-\infty}^{+\infty} e^{-\frac{(x-t)^2}{2}}\,dx
        \end{aligned}$$

        Con il cambio di variabile $u=x-t$, $du=dx$:

        $$\begin{aligned}
        G_Z(t)
        &= e^{\frac{t^2}{2}} \cdot
        \frac{1}{\sqrt{2\pi}}
        \int_{-\infty}^{+\infty} e^{-\frac{u^2}{2}}\,du \\
        &= e^{\frac{t^2}{2}}
        \underbrace{
        \int_{-\infty}^{+\infty} 
        \frac{1}{\sqrt{2\pi}} e^{-\frac{u^2}{2}}\,du
        }_{N(0,1) = 1}
        \end{aligned}$$

        L’integrale vale 1, quindi:

        $$
        G_Z(t) = \boxed{e^{\frac{t^2}{2}}} \;.
        $$

    - **Primo momento:**

        $$
        G_Z'(t) = t e^{\frac{t^2}{2}}
        $$

        $$
        E[Z] = G_Z'(0) = \boxed{0} \;.
        $$

    - **Secondo momento:**

        $$\begin{aligned}
        G_Z''(t)
        &= \frac{d}{dt}\left(t e^{\frac{t^2}{2}}\right) \\
        &= e^{\frac{t^2}{2}} + t^2 e^{\frac{t^2}{2}} \\
        &= (1+t^2)e^{\frac{t^2}{2}}
        \end{aligned}$$

        $$
        E[Z^2] = G_Z''(0) = \boxed{1} \;.
        $$

<div style="page-break-after: always;"></div>

5. **Calcolare la FGM e i momenti di $X$**.

    Sia $X \sim \text{Exp}(\lambda)$ con densità:

    $$
    f(x)=\lambda e^{-\lambda x}, \quad x\ge 0
    $$

    - **Calcoliamo la FGM:**

        $$\begin{aligned}
        G_X(t) = E[e^{tX}]
        &= \int_0^{+\infty} e^{tx}\, \lambda e^{-\lambda x}\, dx \\
        &= \lambda \int_0^{+\infty} e^{tx-\lambda x}\, dx \\
        &= \lambda \int_0^{+\infty} e^{-(\lambda - t)x}\, dx
        \end{aligned}$$

        - **Caso $\lambda - t > 0$ (cioè $t < \lambda$):**

            $$\begin{aligned}
            G_X(t)
            &= \lambda \int_0^{+\infty} e^{-(\lambda - t)x}\, dx \\
            &= \lambda \cdot \frac{1}{\lambda - t}
            \underbrace{
            \int_0^{+\infty} (\lambda-t)e^{-(\lambda - t)x}\, dx
            }_1 \\
            &= \lambda \cdot \frac{1}{\lambda - t}, \quad t<\lambda
            \end{aligned}$$

        - **Caso $\lambda - t \le 0$ (cioè $t \ge \lambda$):**

            l’integrale diverge, quindi:

            $$
            G_X(t)=+\infty
            $$

        In generale abbiamo:

        $$
        G_X(t)=
        \boxed{\begin{cases}
        \frac{\lambda}{\lambda-t} & t<\lambda \\
        +\infty & t\ge \lambda
        \end{cases}} \;.
        $$

<div style="page-break-after: always;"></div>

- **Primo momento:**

    $$\begin{aligned}
    G'_X(t)
    &= \lambda \cdot (\lambda-t)^{-1} \\
    &= \lambda \cdot \big[-1(\lambda-t)^{-2}\cdot(-1)\big] \\
    &= \lambda (\lambda-t)^{-2} \\
    &= \frac{\lambda}{(\lambda-t)^2}
    \end{aligned}$$

    $$
    E[X]=G'_X(0)=\frac{\lambda}{\lambda^2}=\frac{1}{\lambda}
    $$

- **Secondo momento:**

    $$\begin{aligned}
    G''_X(t)
    &= \lambda \cdot (-2)(\lambda-t)^{-3}\cdot(-1) \\
    &= 2\lambda (\lambda-t)^{-3} \\
    &= \frac{2\lambda}{(\lambda-t)^3}
    \end{aligned}$$

    $$
    E[X^2]=G''_X(0)=\frac{2\lambda}{\lambda^3}=\frac{2}{\lambda^2}
    $$

6. **Calcolare i momenti di $Y$**.

    Sia

    $$
    Y \sim \text{Par}(\alpha)
    $$

    con densità:

    $$
    f(x)=\frac{\alpha}{x^{\alpha+1}}, \quad x\ge 1
    $$

    - **Calcoliamo la FGM:**

        $$\begin{aligned}
        G_Y(t)
        &= \int_1^{+\infty} e^{tx}\frac{\alpha}{x^{\alpha+1}}dx
        = +\infty
        \end{aligned}$$

    > **Nota**. La FGM non esiste per $t>0$ perché l’integrale diverge. Quindi:
    > $$ G_Y(t) \text{ esiste solo per } t \le 0 $$

---

<div style="page-break-after: always;"></div>

#### Esercizio 3 $-$ Calcolo dei momenti

Tramite il metodo della FGM calcolare

7. il momento terzo di $Z \sim N(0,1)$  
8. il momento terzo di $Y \sim \text{Exp}(\lambda)$  
9. il valore atteso di $X \sim U(0,1)$  

##### Risoluzione

7. **Momento terzo di $Z \sim N(0,1)$.**

    La FGM della normale standard è:

    $$
    G_Z(t)=e^{\frac{t^2}{2}}
    $$

    Calcoliamo le derivate successive:

    $$\begin{aligned}
    G'_Z(t) &= t e^{\frac{t^2}{2}} \\
    G''_Z(t) &= 1\cdot e^{\frac{t^2}{2}} + t\left(t e^{\frac{t^2}{2}}\right) \\
    &= (1 + t^2)e^{\frac{t^2}{2}} \\
    G'''_Z(t) &= (0+2t)e^{\frac{t^2}{2}} + (1+t^2)\cdot t e^{\frac{t^2}{2}} \\
    &= 2t e^{\frac{t^2}{2}} + (t+t^3)e^{\frac{t^2}{2}} \\
    &= (3t+t^3)e^{\frac{t^2}{2}}
    \end{aligned}$$

    Valutiamo in $t=0$:

    $$
    E[Z^3] = G'''_Z(0) = \boxed{0} \;.
    $$

8. **Momento terzo di $Y \sim \text{Exp}(\lambda)$.**

    La FGM dell'esponenziale:

    $$
    G_Y(t)=\frac{\lambda}{\lambda - t} = \lambda(\lambda - t)^{-1}
    $$

    <div style="page-break-after: always;"></div>

    Calcoliamo le derivate successive:

    $$\begin{aligned}
    G'_Y(t) 
    &= \lambda \cdot (-1)(\lambda - t)^{-2}\cdot(-1) \\
    &= \lambda(\lambda - t)^{-2}
    \\
    G''_Y(t)
    &= \lambda \cdot (-2)(\lambda - t)^{-3}\cdot(-1) \\
    &= 2\lambda(\lambda - t)^{-3}
    \\
    G'''_Y(t)
    &= \lambda \cdot (-3)(-2)(\lambda - t)^{-4}\cdot(-1) \\
    &= 6\lambda(\lambda - t)^{-4}
    \end{aligned}$$

    Valutiamo in $t=0$:

    $$
    E[Y^3] = G'''_Y(0)
    = \frac{6\lambda}{\lambda^4}
    = \boxed{
    \frac{6}{\lambda^3}
    } \;.
    $$

9. **Valore atteso di $X \sim U(0,1)$.**

    $$\begin{aligned}
    G_X(t) = E[e^{tX}]
    &= \int_0^1 e^{tx}\,dx
    = \left[\frac{e^{tx}}{t}\right]_0^1
    = \frac{e^t - 1}{t}
    \end{aligned}$$

    Derivata:

    $$\begin{aligned}
    G'_X(t)
    &= \frac{t e^t - (e^t - 1)}{t^2}
    \end{aligned}$$

    Valutiamo il limite per $t\to 0$:

    $$
    E[X] = G'_X(0)
    = \lim_{t\to0}
    \frac{t e^t-(e^t-1)}{t^2}
    $$

    Usiamo lo sviluppo di Taylor di $e^t$ attorno a $0$:

    $$
    e^t = 1+t+\frac{t^2}{2}+o(t^2)
    $$

    <div style="page-break-after: always;"></div>

    Sostituendo nel numeratore:

    $$\begin{aligned}
    t e^t-(e^t-1)
    &= t\left(1+t+\frac{t^2}{2}+o(t^2)\right)
    -\left(t+\frac{t^2}{2}+o(t^2)\right) \\
    &= t+t^2+\frac{t^3}{2}
    -t-\frac{t^2}{2}+o(t^2) \\
    &= \frac{t^2}{2}+o(t^2)
    \end{aligned}$$

    Quindi

    $$\begin{aligned}
    E[X]
    &= \lim_{t\to0} \frac{\frac{t^2}{2}+o(t^2)}{t^2}
    = \frac{\frac{t^2}2}{t^2}
    = \boxed{\frac12} \;.
    \end{aligned}$$

---

<div style="page-break-after: always;"></div>