## $$ \textcolor{red}{\text{Esercizi Ex. 12 - Lez. 10}} $$

#### Esercizio 1

Sia $X\sim N(0.6;3)$. Trovare

- (a) $P(X\le -0.53)$
- (b) $P(X\ge 1)$
- (c) $P(0<X<2)$

##### Risoluzione

La variabile aleatoria è distribuita normalmente con

$$
\mu=0.6,
\qquad
\sigma^2=3,
\qquad
\sigma=\sqrt3
$$

Per utilizzare le tavole della normale standard usiamo la variabile standardizzata

$$
Z=\frac{X-\mu}{\sigma}
=\frac{X-0.6}{\sqrt3},
\qquad
Z\sim N(0,1)
$$

> Ricordiamo che
> 
> $$ P(X\le x) = \Phi\!\left(\frac{x-\mu}{\sigma}\right) $$
>
> dove $\Phi$ è la funzione di ripartizione della normale standard.

- **(a)** Calcoliamo $P(X\le -0.53)$:

    $$\begin{aligned}
    P(X\le-0.53)
    &= \Phi\!\left(\frac{-0.53-0.6}{\sqrt3}\right) \\
    &= \Phi(-0.6524) \\
    &\approx \Phi(-0.65) \\
    &= 1-\Phi(0.65) \\
    &= 1-0.74215 \\
    &= \boxed{0.25785}\;.
    \end{aligned}$$

- **(b)** Calcoliamo $P(X\ge1)$:

    $$\begin{aligned}
    P(X\ge1)
    &= 1-P(X\le1) \\
    &= 1-\Phi\!\left(\frac{1-0.6}{\sqrt3}\right) \\
    &= 1-\Phi(0.2309) \\
    &\approx 1-\Phi(0.23) \\
    &= 1-0.59095 \\
    &= \boxed{0.40905}\;.
    \end{aligned}$$

- **(c)** Calcoliamo $P(0<X<2)$:

    $$\begin{aligned}
    P(0<X<2)
    &= P(X<2)-P(X\le0) \\
    &= \Phi\!\left(\frac{2-0.6}{\sqrt3}\right)
       -\Phi\!\left(\frac{0-0.6}{\sqrt3}\right) \\
    &= \Phi(0.8083)-\Phi(-0.3464) \\
    &\approx \Phi(0.81)-\Phi(-0.35) \\
    &= \Phi(0.81)-\bigl(1-\Phi(0.35)\bigr) \\
    &= 0.79103-(1-0.63683) \\
    &= 0.79103-0.36317 \\
    &= \boxed{0.42786}\;.
    \end{aligned}$$

> **Nota.** A seconda della tavola utilizzata si possono ottenere valori leggermente diversi per effetto degli arrotondamenti.

---

<div style="page-break-after: always;"></div>

#### Esercizio 2

Sia $X\sim N(-1;0.36)$. Trovare $c\in\mathbb{R}$ tale che:

- (a) $P(X>c)=0.40$
- (b) $P(X<c)=0.38$

##### Risoluzione

La variabile aleatoria è distribuita normalmente con

$$
\mu=-1,
\qquad
\sigma^2=0.36,
\qquad
\sigma=\sqrt{0.36}=0.6
$$

Per utilizzare le tavole della normale standard introduciamo la variabile standardizzata

$$
Z=\frac{X-\mu}{\sigma}
=\frac{X-(-1)}{0.6},
\qquad
Z\sim N(0,1).
$$

Ricordiamo che

$$
P(X\le x)
= \Phi\!\left(\frac{x-\mu}{\sigma}\right),
$$

dove $\Phi$ è la funzione di ripartizione della normale standard.

- **(a)** Calcolare $P(X>c)=0.40$:

    $$\begin{aligned}
    P(X>c)
    = 1-P(X\le c)
    &= 1-\Phi\!\left(\frac{c+1}{0.6}\right)
    =0.40 \\
    &\Rightarrow
    \Phi\!\left(\frac{c+1}{0.6}\right)
    =0.60 \\
    &\Rightarrow
    \frac{c+1}{0.6}
    \approx \Phi^{-1}(0.60) \\
    &\Rightarrow
    \frac{c+1}{0.6}
    \approx 0.25 \\
    &\Rightarrow
    c
    \approx 0.25\cdot0.6-1 \\
    &\Rightarrow
    \boxed{c\approx -0.85}\;.
    \end{aligned}$$

<div style="page-break-after: always;"></div>

- **(b)** Calcolare $P(X<c)=0.38$:

    $$\begin{aligned}
    P(X<c)
    &= P(X\le c) \\
    &= \Phi\!\left(\frac{c+1}{0.6}\right)
    =0.38
    \end{aligned}$$

    Poiché $0.38<0.5$, usiamo la simmetria della normale standard:

    $$\begin{aligned}
    \Phi\!\left(\frac{c+1}{0.6}\right)
    &=0.38 \\
    \Rightarrow\;
    \Phi\!\left(-\frac{c+1}{0.6}\right)
    &=1-0.38 \\
    &=0.62.
    \end{aligned}$$

    Dalle tavole della normale standard:

    $$
    \Phi^{-1}(0.62)\approx 0.31.
    $$

    Quindi

    $$\begin{aligned}
    -\frac{c+1}{0.6}
    &\approx 0.31 \\
    \frac{c+1}{0.6}
    &\approx -0.31 \\
    c+1
    &\approx -0.31\cdot0.6 \\
    c
    &\approx -0.186-1 \\
    &\approx \boxed{-1.186}\;.
    \end{aligned}$$

> **Nota.** Per la normale standard vale la proprietà di simmetria
>
> $$
> \Phi(-z)=1-\Phi(z),
> $$
>
> che permette di trasformare probabilità inferiori a $0.5$ in probabilità superiori a $0.5$, più facili da leggere sulle tavole.

---

<div style="page-break-after: always;"></div>

#### Esercizio 3

Sia $X\sim N(\mu;\sigma^2)$. Trovare con che probabilità la variabile si discosta dalla media al più per i primi tre multipli della deviazione standard; dimostrare che:

$$\begin{aligned}
P(\mu-\sigma\le X\le\mu+\sigma) &= 0.68 \\
P(\mu-2\sigma\le X\le\mu+2\sigma) &= 0.955 \\
P(\mu-3\sigma\le X\le\mu+3\sigma) &= 0.997
\end{aligned}$$

##### Risoluzione

Per utilizzare le tavole della normale standard introduciamo la variabile standardizzata

$$
Z=\frac{X-\mu}{\sigma},
\qquad
Z\sim N(0,1).
$$

Ricordiamo inoltre che

$$
P(X\le x)
= \Phi\!\left(\frac{x-\mu}{\sigma}\right),
$$

dove $\Phi$ è la funzione di ripartizione della normale standard.

- **Primo multiplo della deviazione standard**

    $$\begin{aligned}
    P(\mu-\sigma\le X\le\mu+\sigma)
    &= P(X\le\mu+\sigma)-P(X<\mu-\sigma) \\
    &= \Phi\!\left(\frac{\mu+\sigma-\mu}{\sigma}\right)
       -\Phi\!\left(\frac{\mu-\sigma-\mu}{\sigma}\right) \\
    &= \Phi(1)-\Phi(-1) \\
    &= \Phi(1)-\bigl(1-\Phi(1)\bigr) \\
    &= 2\Phi(1)-1 \\
    &= 2(0.84134)-1 \\
    &= 0.68268 \\
    &\approx \boxed{0.68}\;.
    \end{aligned}$$

<div style="page-break-after: always;"></div>

- **Secondo multiplo della deviazione standard**

    $$\begin{aligned}
    P(\mu-2\sigma\le X\le\mu+2\sigma)
    &= P(X\le\mu+2\sigma)-P(X<\mu-2\sigma) \\
    &= \Phi(2)-\Phi(-2) \\
    &= \Phi(2)-\bigl(1-\Phi(2)\bigr) \\
    &= 2\Phi(2)-1 \\
    &= 2(0.97725)-1 \\
    &= 0.95450 \\
    &\approx \boxed{0.955}\;.
    \end{aligned}$$

- **Terzo multiplo della deviazione standard**

    $$\begin{aligned}
    P(\mu-3\sigma\le X\le\mu+3\sigma)
    &= P(X\le\mu+3\sigma)-P(X<\mu-3\sigma) \\
    &= \Phi(3)-\Phi(-3) \\
    &= \Phi(3)-\bigl(1-\Phi(3)\bigr) \\
    &= 2\Phi(3)-1 \\
    &= 2(0.99865)-1 \\
    &= 0.99730 \\
    &\approx \boxed{0.997}\;.
    \end{aligned}$$

> **Nota (Regola del 68-95-99.7).** Per una variabile normale:
>
> $$
> \begin{aligned}
> P(\mu-\sigma\le X\le\mu+\sigma) &\approx 68\% \\
> P(\mu-2\sigma\le X\le\mu+2\sigma) &\approx 95\% \\
> P(\mu-3\sigma\le X\le\mu+3\sigma) &\approx 99.7\%
> \end{aligned}
> $$
>
> Questa proprietà è molto importante perché permette di stimare rapidamente quanto una variabile normale tende a concentrarsi attorno alla propria media.

---

<div style="page-break-after: always;"></div>

#### Esercizio 4

I punteggi di un test di ammissione sono normalmente distribuiti, con media 480 e varianza 8100.

- (a) Se il peggior 25% dei candidati sarà escluso, trova il minimo punteggio per essere ammessi.
- (b) Se il miglior 12% dei candidati avrà una borsa di studio, trova il minimo punteggio per avere la borsa di studio.

##### Risoluzione

La variabile aleatoria è distribuita normalmente con

$$
\mu=480,
\qquad
\sigma^2=8100,
\qquad
\sigma=\sqrt{8100}=90
$$

Per standardizzare introduciamo

$$
Z=\frac{X-\mu}{\sigma}
=\frac{X-480}{90},
\qquad
Z\sim N(0,1)
$$

Ricordiamo che

$$
P(X\le x)
= \Phi\!\left(\frac{x-\mu}{\sigma}\right),
$$

dove $\Phi$ è la funzione di ripartizione della normale standard.

<div style="page-break-after: always;"></div>

- **(a)** Il peggior 25% viene escluso $\Rightarrow$ cerchiamo il quantile $0.25$:

    $$\begin{aligned}
    P(X\le x)=0.25
    &\Rightarrow \Phi\!\left(\frac{x-480}{90}\right)=0.25 \\
    &\Rightarrow \Phi\!\left(-\frac{x-480}{90}\right)=1-0.25 \\
    &\Rightarrow \Phi\!\left(-\frac{x-480}{90}\right)=0.75 \\
    &\Rightarrow -\frac{x-480}{90}=\Phi^{-1}(0.75)\approx 0.674 \\
    &\Rightarrow \frac{x-480}{90}=-0.674 \\
    &\Rightarrow x=480-90\cdot 0.674 \\
    &\Rightarrow x\approx 419.3 \approx \boxed{420}.
    \end{aligned}$$

- **(b)** Il miglior 12% riceve la borsa $\Rightarrow P(X\ge x)=0.12$:

    $$\begin{aligned}
    P(X\ge x)=0.12
    &\Rightarrow 1-\Phi\!\left(\frac{x-480}{90}\right)=0.12 \\
    &\Rightarrow \Phi\!\left(\frac{x-480}{90}\right)=0.88 \\
    &\Rightarrow \frac{x-480}{90}=\Phi^{-1}(0.88) \approx 1.175 \\
    &\Rightarrow x\approx 480+90\cdot 1.175 \\
    &\Rightarrow x\approx 585.8 \approx \boxed{586} \;.
    \end{aligned}$$

> **Nota.** I quantili della normale si leggono sempre come:
>
> $$
> x = \mu + \sigma z_p
> \quad \text{dove } z_p=\Phi^{-1}(p).
> $$

---

<div style="page-break-after: always;"></div>

#### Esercizio 5

La concentrazione di zucchero per coltivare il penicillium deve essere circa 4.9 mg/ml e, se eccede 6.0 mg/ml, il fungo muore e il processo deve essere fermato quel giorno.

Trova la probabilità che il processo sia fermato se la concentrazione di zucchero é:
- (a) normale con media 4.9 e varianza 0.36
- (b) normale con media 5.2 e deviazione standard 0.4.

##### Risoluzione

La probabilità che il processo sia fermato è

$$
P(X>6)
$$

- **(a)** La variabile aleatoria è distribuita normalmente con

    $$
    \mu=4.9,
    \qquad
    \sigma^2=0.36,
    \qquad
    \sigma=0.6
    $$

    Calcoliamo la probabilità richiesta:

    $$\begin{aligned}
    P(X>6)
    &= 1 - P(X\le 6) \\
    &= 1 - \Phi\!\left(\frac{6-4.9}{0.6}\right) \\
    &= 1 - \Phi(1.8333) \\
    &\approx 1 - 0.96638
    = \boxed{0.03362}\;.
    \end{aligned}$$

- **(b)** La variabile aleatoria è distribuita normalmente con

    $$
    \mu=5.2,
    \qquad
    \sigma=0.4
    $$

    Calcoliamo la probabilità richiesta:

    $$\begin{aligned}
    P(X>6)
    &= 1 - P(X\le 6) \\
    &= 1 - \Phi\!\left(\frac{6-5.2}{0.4}\right) \\
    &= 1 - \Phi(2) \\
    &\approx 1 - 0.97725
    = \boxed{0.02275}\;.
    \end{aligned}$$

<div style="page-break-after: always;"></div>