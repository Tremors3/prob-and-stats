## $$ \textcolor{red}{\text{Esercizi Lez. 18 - Teoria}} $$

#### Esercizio 1

Siano $X$ ed $Y$ due v.a. indipendenti con $X\sim N(2,5)$ ed $Y\sim N(5,9)$. Definiamo

$$
Z = 3X-2Y+1.
$$

- calcolare $E[Z]$ e $\text{Var}(Z)$,
- determinare la distribuzione di $Z$,
- calcolare $P(Z\le6)$.

##### Risoluzione

1. **Calcoliamo l'aspettazione della variabile $Z$.**

    Per la linearità dell'aspettazione possiamo esprimere l'aspettazione di $Z$ in funzione delle aspettazioni di $X$ e $Y$.

    $$\begin{aligned}
    E[Z]
    &= E[3X -2Y + 1] \\
    &= 3E[X] -2E[Y] + 1 \\
    &= 3\cdot2 - 2\cdot5 + 1 \\
    &= 6 - 10 + 1 \\
    &= \boxed{-3} \;.
    \end{aligned}$$

    <div style="page-break-after: always;"></div>

2. **Calcoliamo la varianza della variabile $Z$.**

    Poiché $X$ e $Y$ sono indipendenti, risulta:

    $$
    \text{Cov}(X,Y)=0.
    $$

    Possiamo quindi utilizzare la formula della varianza di una combinazione lineare.

    $$\begin{aligned}
    \text{Var}(Z)
    &= \text{Var}(3X - 2Y + 1) \\
    &= 3^2\text{Var}(X) + (-2)^2\text{Var}(Y) \\
    &= 9\cdot5 + 4\cdot9 \\
    &= 45 + 36 \\
    &= \boxed{81} \;.
    \end{aligned}$$

3. **Determinare la distribuzione di $Z$.**

    Una combinazione lineare di variabili gaussiane indipendenti è ancora una variabile gaussiana.

    $$
    aX + bY + c
    \sim
    N\!\left(
    a\mu_X + b\mu_Y + c,\;
    a^2\sigma_X^2 + b^2\sigma_Y^2
    \right).
    $$

    Pertanto:

    $$
    \boxed{
    Z = 3X - 2Y + 1 \sim N(-3,\;81)
    } \;.$$

4. **Calcolare $P(Z\le6)$.**

    Standardizziamo la variabile:

    $$\begin{aligned}
    P(Z\le6)
    &= \Phi\!\left(
    \frac{6-E[Z]}{\sqrt{\text{Var}(Z)}}
    \right) \\
    &= \Phi\!\left(
    \frac{6-(-3)}{\sqrt{81}}
    \right) \\
    &= \Phi(1).
    \end{aligned}$$

    Dalle tavole della normale standard:

    $$
    \boxed{P(Z\le6)\approx 0.84134} \;.
    $$

---

<div style="page-break-after: always;"></div>

#### Esercizio 2

Siano $X$ ed $Y$ due v.a. indipendenti ed identicamente distribuite $\sim U(0,1)$. Calcolare la densità di probabilità di $Z=X+Y$.

##### Risoluzione

> Ricordiamo la formula di convoluzione per la somma di due variabili aleatorie indipendenti:
> 
> $$
> f_Z(z)
> = \int_{-\infty}^{+\infty}
> f_X(z-y)\,f_Y(y)\,dy.
> $$

Poiché

$$
X,Y \sim U(0,1),
$$

abbiamo

$$
f_X(x)=
\begin{cases}
1 & 0\le x\le 1\\
0 & \text{altrimenti}
\end{cases}
\qquad
f_Y(y)=
\begin{cases}
1 & 0\le y\le 1\\
0 & \text{altrimenti}
\end{cases}
$$

Pertanto

$$
f_Z(z)
= \int_{-\infty}^{+\infty}
f_X(z-y)\,f_Y(y)\,dy.
$$

Affinché l'integrando sia diverso da zero devono valere contemporaneamente le condizioni

$$
0\le y\le 1
\qquad\text{e}\qquad
0\le z-y\le 1.
$$

Quest'ultima equivale a

$$
z-1\le y\le z.
$$

L'intervallo di integrazione è quindi l'intersezione tra

$$
[0,1]
\qquad\text{e}\qquad
[z-1,z].
$$

Distinguiamo ora i possibili valori di $z$.

1. **Caso $0\le z\le 1$.**

    In questo caso l'intersezione è

    $$
    0\le y\le z.
    $$

    Quindi

    $$\begin{aligned}
    f_Z(z)
    &= \int_0^z 1\,dy \\
    &= \left[y\right]_0^z \\
    &= z.
    \end{aligned}$$

2. **Caso $1<z\le 2$.**

    In questo caso l'intersezione è

    $$
    z-1\le y\le 1.
    $$

    Quindi

    $$\begin{aligned}
    f_Z(z)
    &= \int_{z-1}^{1} 1\,dy \\
    &= \left[y\right]_{z-1}^{1} \\
    &= 1-(z-1) \\
    &= 2-z.
    \end{aligned}$$

3. **Caso $z<0$ oppure $z>2$.**

    L'intersezione è vuota e quindi

    $$
    f_Z(z)=0.
    $$

Concludiamo che la densità di probabilità di $Z=X+Y$ è

$$
\boxed{
f_Z(z)=
\begin{cases}
z & \text{se } 0\le z\le 1, \\[2mm]
2-z & \text{se } 1<z\le 2, \\[2mm]
0 & \text{altrimenti}.
\end{cases}
} \;.
$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 3

Siano $X \sim \text{Pois}(\alpha)$ e $Y \sim \text{Pois}(\beta)$ indipendenti. Calcolare la funzione di probabilità di $Z=X+Y$.

##### Risoluzione

> **Nota.** La somma di due variabili aleatorie di Poisson indipendenti è ancora una variabile aleatoria di Poisson:
>
> $$
> X \sim \text{Pois}(\alpha),
> \qquad
> Y \sim \text{Pois}(\beta)
> $$
>
> $$
> X+Y \sim \text{Pois}(\alpha+\beta).
> $$

Poiché

$$
Z=X+Y,
$$

segue immediatamente che

$$
Z \sim \text{Pois}(\alpha+\beta).
$$

La funzione di probabilità di $Z$ è quindi

$$
p_Z(k)
= P(Z=k)
= e^{-(\alpha+\beta)}
\frac{(\alpha+\beta)^k}{k!},
\qquad
k=0,1,2,\ldots
$$

Pertanto:

$$
\boxed{
p_Z(k)
= e^{-(\alpha+\beta)}
\frac{(\alpha+\beta)^k}{k!}
}
\qquad
k=0,1,2,\ldots
$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 4

Siano $X \sim \text{Exp}(\alpha)$ e $Y \sim \text{Exp}(\beta)$ indipendenti. Calcolare la densità di probabilità di $Z=X+Y$.

##### Risoluzione

> **Nota.** Nel caso particolare in cui i parametri coincidono:
>
> $$
> X,Y \sim \text{Exp}(\lambda)
> $$
>
> allora
>
> $$
> X+Y \sim \text{Gamma}(\lambda, 2).
> $$
>
> Nel nostro caso però $\alpha \neq \beta$, quindi dobbiamo usare la convoluzione.

Dobbiamo applicare la formula:

$$
f_Z(z)=\int_{-\infty}^{+\infty} f_X(x)\,f_Y(z-x)\,dx.
$$

Poiché le densità sono nulle per valori negativi, l’integrale diventa:

$$\begin{aligned}
f_Z(z)
&= \int_0^z \alpha e^{-\alpha x}\,\beta e^{-\beta(z-x)}\,dx \\
&= \alpha\beta \int_0^z e^{-\alpha x} e^{-\beta(z-x)}\,dx \\
&= \alpha\beta \int_0^z e^{-\alpha x} e^{-\beta z + \beta x}\,dx \\
&= \alpha\beta e^{-\beta z} \int_0^z e^{(\beta-\alpha)x}\,dx \\
&= \alpha\beta e^{-\beta z} \left[\frac{e^{(\beta-\alpha)x}}{\beta-\alpha}\right]_0^z \\
&= \frac{\alpha\beta}{\beta-\alpha} e^{-\beta z} \left(e^{(\beta-\alpha)z}-1\right) \\
&= \frac{\alpha\beta}{\beta-\alpha} \left(e^{-\alpha z}-e^{-\beta z}\right).
\end{aligned}$$

<div style="page-break-after: always;"></div>

Quindi:

$$
\boxed{
f_Z(z)
= \frac{\alpha\beta}{\beta-\alpha}
\left(
e^{-\alpha z}-e^{-\beta z}
\right)
}
\qquad z\ge 0.
$$

> **Nota finale.**
>
> Caso speciale:
>
> $$
> \alpha=\beta=\lambda \Rightarrow
> f_Z(z)=\lambda^2 z e^{-\lambda z},\quad z\ge0
> $$
>
> Caso generale:
>
> $$
> \alpha\neq\beta \Rightarrow
> f_Z(z)=\frac{\alpha\beta}{\beta-\alpha}(e^{-\alpha z}-e^{-\beta z})
> $$

---

<div style="page-break-after: always;"></div>
