## $$ \textcolor{red}{\text{Esercizi Lez. 10 - Teoria}} $$

#### Esercizio 1

Sia $Z\sim N(0,1)$ la normale standard. Calcolare:

$$
P(Z>0), \quad P(Z\ge1.07), \quad P(Z<-1.45), \quad P(Z>-0.06), \quad P(Z\le-2)
$$

##### Risoluzione

1. $$\begin{aligned}
P(Z>0) &= 1 - P(Z\le0) = 1 - \Phi(0) \\
&= 1 - 0.5 = \boxed{0.5} \;.
\end{aligned}$$

2. $$\begin{aligned}
P(Z\ge1.07) &= 1 - P(Z<1.07) = 1 - \Phi(1.07) \\
&= 1 - 0.85769 = \boxed{0.14231} \;.
\end{aligned}$$

3. $$\begin{aligned}
P(Z<-1.45) &= \Phi(-1.45) = 1 - \Phi(1.45) \\
&= 1 - 0.92647 = \boxed{0.07353} \;.
\end{aligned}$$

4. $$\begin{aligned}
P(Z>-0.06) &= 1 - \Phi(-0.06) \\
&= 1 - (1-\Phi(0.06)) \\
&= \Phi(0.06) = \boxed{0.52392} \;.
\end{aligned}$$

5. $$\begin{aligned}
P(Z\le-2) &= \Phi(-2) = 1 - \Phi(2) \\
&= 1 - 0.97725 = \boxed{0.02275} \;.
\end{aligned}$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 2

Sia $X\sim N(4,25)$, calcolare:

$$
P(X\le5), \space P(X\ge2)
$$

##### Risoluzione

Abbiamo $\mu=4$ e $\sigma=5$:

1. $$\begin{aligned}
P(X\le 5) &= \Phi\left(\frac{5 - \mu}{\sigma}\right) = \Phi\left(\frac{5 - 4}{5}\right) \\
&= \Phi\left(0.20\right) = \boxed{0.57926} \;.
\end{aligned}$$

2. $$\begin{aligned}
P(X\ge2) &= 1 - \Phi\left(\frac{2-4}{5}\right) = 1 - \Phi\left(-\frac25\right) = 1 - \left(1 - \Phi(0.40)\right) \\
&= \Phi(0.40) = \boxed{0.65542} \;.
\end{aligned}$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 3

Determinare il $10^{\text{mo}}$ percentile di

$$
Z \sim N(0,1), \qquad X \sim N(21,3)
$$

##### Risoluzione

1. Per $Z\sim N(0,1)$:

    $$\begin{aligned}
    \Phi(q_{0.10}) &= 0.10 \\
    \Phi(-q_{0.10}) &= 1-0.10 = 0.90 \approx 0.89973 \\
    -q_{0.10} &= \Phi'(0.89973) \approx 1.28 \\
    q_{0.10} &= \boxed{-1.28} \;.
    \end{aligned}$$

2. Per $X\sim N(21,3)$:

    $$\begin{aligned}
    \Phi\left(\frac{q_{0.10}-21}{\sqrt3}\right) &= 0.10 \\
    \Phi\left(-\frac{q_{0.10}-21}{\sqrt3}\right) &= 1-0.10 = 0.90 \approx 0.89973 \\
    -\frac{q_{0.10}-21}{\sqrt3} &= \Phi'(0.89973) \approx 1.28 \\
    q_{0.10} &= -1.28\sqrt3 + 21 = \boxed{18.78} \;.
    \end{aligned}$$

---