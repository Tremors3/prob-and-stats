## $$ \textcolor{red}{\text{Esercizi Lez. 14 - Teoria}} $$

### $\textcolor{blue}{\text{Caso Discreto}}$

---

#### Esercizio 1

Sia $X$ una v.a. discreta Uniforme a valori nell'insieme $\{-1,0,1,2\}$. Qual è la funzione di probabilità $p_Y$ di $Y = X^2$?

##### Risoluzione

La funzione di probabilità di $X$ è:

$$
p_X : \quad
\begin{pmatrix}
-1 & 0 & 1 & 2 \\
\frac14 & \frac14 & \frac14 & \frac14
\end{pmatrix}
$$

1) Calcoliamo il supporto di $Y$:

    $$
    Y = X^2
    $$

    Applicando la trasformazione ai punti del supporto di $X$ otteniamo:

    $$
    (-1)^2 = 1,
    \qquad
    0^2 = 0,
    \qquad
    1^2 = 1,
    \qquad
    2^2 = 4.
    $$

    Quindi

    $$
    S_Y = \{0,1,4\}.
    $$

2) Calcoliamo la funzione di probabilità di $Y$ nei punti del supporto:

    $$\begin{aligned}
    p_Y(0)
    = P(Y=0)
    = P(X^2=0)
    = P(X=0)
    = \frac14
    \end{aligned}$$

    $$\begin{aligned}
    p_Y(1)
    = P(Y=1)
    = P(X^2=1)
    &= P(X\in\{-1,1\}) \\
    &= P(X=-1)+P(X=1) \\
    &= \frac14+\frac14
    = \frac24
    \end{aligned}$$

    $$\begin{aligned}
    p_Y(4)
    = P(Y=4)
    = P(X^2=4)
    &= P(X\in\{-2,2\}) \\
    &= P(X=-2)+P(X=2) \\
    &= 0+\frac14
    = \frac14
    \end{aligned}$$

    Abbiamo quindi:

    $$\boxed{
    p_Y : \quad
    \begin{pmatrix}
    0 & 1 & 4 \\
    \frac14 & \frac12 & \frac14
    \end{pmatrix}
    } \;.$$

> **Nota.** Quando la trasformazione non è iniettiva (come nel caso di $g(x)=x^2$), più valori di $X$ possono produrre lo stesso valore di $Y$. In tal caso bisogna sommare le probabilità di tutti i valori di $X$ che vengono trasformati nello stesso valore di $Y$.

---

<div style="page-break-after: always;"></div>

### $\textcolor{blue}{\text{Casi Continui}}$

---

#### Esercizio 2

Sia $X$ una v.a. continua $\sim N(0,1)$. Qual è la densità di probabilità $f_Y$ di $Y=X^2$?

##### Risoluzione

> Ricordiamo che la densità di probabilità per una normale standard è:
> 
> $$
> f_X(x) = \frac1{\sqrt{2\pi}}e^{-\frac{x^2}2}
> $$

Notiamo subito che la funzione

$$
g(x) = x^2
$$

è una parabola e quindi non è strettamente crescente o decrescente. Per questo motivo non possiamo applicare direttamente il teorema.

1) Scriviamo $F_Y$ in termini di $F_X$:

    $$\begin{aligned}
    F_Y(y) = P(Y\le y) = P(X^2\le y)
    &= P(-\sqrt y\le X\le \sqrt y) \\
    &= P(X\le \sqrt y) - P(X<-\sqrt y) \\
    &= F_X(\sqrt y) - F_X(-\sqrt y)
    \end{aligned}$$

<div style="page-break-after: always;"></div>

2) Calcoliamo $f_Y$ in termini di $F_Y$:

    $$\begin{aligned}
    f_Y(y)
    &= \frac{d}{dy}\Big\{ F_X(\sqrt y) - F_X(-\sqrt y) \Big\} \\
    &= \frac{d}{dy}\Big\{ F_X(\sqrt y)\Big\} -
    \frac{d}{dy}\Big\{ F_X(-\sqrt y)\Big\} \\
    &= f_X(\sqrt y)\cdot\frac1{2\sqrt y} + 
    f_X(-\sqrt y)\cdot\frac1{2\sqrt y} \\
    &= \frac1{2\sqrt y}\left(f_X(\sqrt y) + f_X(-\sqrt y)\right) \\
    &= \frac1{2\sqrt y}2f_X(\sqrt y) \\
    &= \frac1{\sqrt y}f_X(\sqrt y)
    \end{aligned}$$

    Questo perchè la normale standard è una funzione pari:

    $$
    f_X(x) = f_X(-x)
    $$

3) Calcoliamo il supporto di $Y$:

    $$
    Y \ge 0
    $$

4) La densità di probabilità di $Y$ è:

    $$\begin{aligned}
    f_Y(y)= \frac1{\sqrt y}f_X(\sqrt y)
    &= \frac1{\sqrt y}\frac1{\sqrt{2\pi}}e^{-\frac{(\sqrt y)^2}2} \\
    &= 
    \boxed{
    \frac1{\sqrt{2\pi y}}e^{-\frac{y}2}
    \cdot \mathbf{1}_{(0,\,\infty)}(y)
    } \;.
    \end{aligned}$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 3

Sia $X\sim \text{Par}(\alpha)$, determinare la densità di probabilità di $Y = \ln X$.

##### Risoluzione

> Ricordiamo che la densità di probabilità di una variabile aleatoria di Pareto di parametro $\alpha$ è:
> 
> $$
> f_X(x) = \frac{\alpha}{x^{\alpha+1}}, \quad x \ge 1
> $$
>
> (supporto tipico della Pareto standard: $x \ge 1$)

Notiamo subito che la funzione

$$
g(x) = \ln(x)
$$

è strettamente crescente su $(0,+\infty)$, quindi possiamo applicare direttamente il teorema di trasformazione per variabili monotone.

> Teorema di trasformazione per variabili monotone:
>
> $$
> f_Y(y) = f_X\!\big(g^{-1}(y)\big)\cdot \left|\frac{d}{dy}g^{-1}(y)\right|
> $$

1) Calcoliamo l’inversa della funzione $g(x)$:

    $$\begin{aligned}
    y = \ln x \quad &\Longrightarrow \quad x = e^y
    \end{aligned}$$

    quindi:

    $$
    g^{-1}(y) = e^y
    $$

2) Applichiamo il teorema e otteniamo $f_Y$:

    $$\begin{aligned}
    f_Y(y)
    &= f_X(e^y)\cdot \left|\frac{d}{dy}e^y\right| \\
    &= f_X(e^y)\cdot e^y
    \end{aligned}$$

<div style="page-break-after: always;"></div>

3) Calcoliamo il supporto di $Y$:

    Poiché $X \ge 1$, allora:

    $$
    Y = \ln X \ge \ln 1 = 0
    $$

    quindi:

    $$
    y \ge 0
    $$

4) La densità di probabilità di $Y$ è:

    $$\begin{aligned}
    f_Y(y)
    &= f_X(e^y)\cdot e^y \\
    &= \frac{\alpha}{(e^y)^{\alpha+1}} \cdot e^y \\
    &= \frac{\alpha}{(e^y)^{\alpha}\cancel{e^y}} \cdot \cancel{e^y} \\
    &= \alpha e^{-\alpha y}
    \end{aligned}$$

    quindi:

    $$\boxed{
    f_Y(y) = \alpha e^{-\alpha y}\cdot\mathbf{1}_{[0,+\infty)}(y)
    } \;.$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 4

Sia $X\sim\text{Exp}(1)$, e siano $\alpha,\lambda > 0$, determinare la densità di probabilità di $Y = \frac{X^{1/\alpha}}{\lambda}$.

##### Risoluzione

> Ricordiamo che la densità di probabilità di una variabile aleatoria esponenziale di parametro $1$ è:
> 
> $$
> f_X(x) = e^{-x}, \quad x \ge 0
> $$

Notiamo subito che la funzione

$$
g(x) = \frac{x^{1/\alpha}}{\lambda}
$$

è strettamente crescente su $x \ge 0$, quindi possiamo applicare direttamente il teorema di trasformazione per variabili monotone.

> Teorema di trasformazione per variabili monotone:
>
> $$
> f_Y(y) = f_X\!\big(g^{-1}(y)\big)\cdot \left|\frac{d}{dy}g^{-1}(y)\right|
> $$

1) Calcoliamo l’inversa della funzione $g(x)$:

    $$\begin{aligned}
    y &= \frac{x^{1/\alpha}}{\lambda} \\
    \lambda y &= x^{1/\alpha} \\
    (\lambda y)^\alpha &= x = g^{-1}(y)
    \end{aligned}$$

2) Applichiamo il teorema e otteniamo $f_Y$:

    $$\begin{aligned}
    f_Y(y)
    &= f_X\big((\lambda y)^\alpha\big)\cdot \left|\frac{d}{dy}(\lambda y)^\alpha\right| \\
    &= e^{-(\lambda y)^\alpha}\cdot \alpha(\lambda y)^{\alpha-1}\cdot \lambda^\alpha
    \end{aligned}$$

<div style="page-break-after: always;"></div>

3) Calcoliamo il supporto di $Y$:

    Poiché $X \ge 0$ e la trasformazione è crescente:

    $$
    Y \ge 0
    $$

4) La densità di probabilità di $Y$ è:

    $$
    \begin{aligned}
    f_Y(y)
    &= e^{-(\lambda y)^\alpha}\cdot \alpha(\lambda y)^{\alpha-1}\lambda^\alpha \\
    &= \alpha \lambda^\alpha (\lambda y)^{\alpha-1} e^{-(\lambda y)^\alpha}
    \end{aligned}
    $$

    quindi:

    $$\boxed{
    f_Y(y)
    = \alpha \lambda^\alpha (\lambda y)^{\alpha-1} e^{-(\lambda y)^\alpha}
    \cdot \mathbf{1}_{[0,+\infty)}(y)
    } \;.$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 5

Sia $X$ una v.a. continua $\sim\text{Exp}(5)$. Qual è la densità di probabilità $f_Y$ di $Y=X^2$?

##### Risoluzione

> Ricordiamo che la densità di probabilità di una variabile aleatoria esponenziale di parametro $5$ è:
> 
> $$
> f_X(x) = 5e^{-5x}, \quad x \ge 0
> $$

Notiamo subito che la funzione

$$
g(x) = x^2
$$

è una parabola e quindi non è strettamente crescente o decrescente su $\mathbb{R}$. Per questo motivo non possiamo applicare direttamente il teorema di trasformazione per funzioni monotone.

1) Scriviamo $F_Y$ in termini di $F_X$:

    $$\begin{aligned}
    F_Y(y) = P(Y\le y) = P(X^2\le y)
    &= P(-\sqrt y\le X\le \sqrt y) \\
    &= P(X\le \sqrt y) - P(X<-\sqrt y) \\
    &= F_X(\sqrt y) - F_X(-\sqrt y)
    \end{aligned}$$

2) Calcoliamo $f_Y$ in termini di $F_Y$:

    $$\begin{aligned}
    f_Y(y)
    &= \frac{d}{dy}\Big\{ F_X(\sqrt y) - F_X(-\sqrt y) \Big\} \\
    \end{aligned}$$

    Poiché $X\sim \text{Exp}(5)$ ha supporto $[0,+\infty)$, si ha:

    $$
    F_X(-\sqrt y)=0 \quad \text{per ogni } y \ge 0
    $$

    quindi:

    $$
    \begin{aligned}
    f_Y(y)
    &= \frac{d}{dy}F_X(\sqrt y) \\
    &= \frac{1}{2\sqrt y} f_X(\sqrt y)
    \end{aligned}
    $$

<div style="page-break-after: always;"></div>

3) Calcoliamo il supporto di $Y$:

    Poiché $Y=X^2$ e $X\ge 0$:

    $$
    Y \ge 0
    $$

4) La densità di probabilità di $Y$ è:

    $$
    \begin{aligned}
    f_Y(y)
    &= \frac{1}{2\sqrt y}\, 5e^{-5\sqrt y} \\
    &= \frac{5}{2\sqrt y} e^{-5\sqrt y}
    \end{aligned}
    $$

    quindi:

    $$\boxed{
    f_Y(y)
    = \frac{5}{2\sqrt y} e^{-5\sqrt y}
    \cdot \mathbf{1}_{[0,+\infty)}(y)
    } \;.$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 6

Sia $X\sim N(0,3)$, calcolare la densità di probabilità di $Y=\arctan(X)$.

##### Risoluzione

> Ricordiamo che la densità di probabilità di una variabile aleatoria normale $N(0,3)$ è:
> 
> $$
> f_X(x) = \frac{1}{\sqrt{6\pi}}e^{-\frac{x^2}{6}}
> $$

Notiamo subito che la funzione

$$
g(x) = \arctan(x)
$$

è strettamente crescente su $\mathbb{R}$, quindi possiamo applicare direttamente il teorema di trasformazione per variabili monotone.

> Teorema di trasformazione per variabili monotone:
>
> $$
> f_Y(y) = f_X\!\big(g^{-1}(y)\big)\cdot \left|\frac{d}{dy}g^{-1}(y)\right|
> $$

1) Calcoliamo l’inversa della funzione $g(x)$:

    $$\begin{aligned}
    g(x) = y &= \arctan(x) \\
    g^{-1}(y) = x &= \tan(y)
    \end{aligned}$$

2) Applichiamo il teorema:

    $$\begin{aligned}
    f_Y(y)
    &= f_X(\tan y)\cdot \left|\frac{d}{dy}\tan y\right| \\
    &= f_X(\tan y)\cdot \frac1{cos^2(y)}
    \end{aligned}$$

3) Calcoliamo il supporto di $Y$:

    Poiché $\arctan(x)$ mappa $\mathbb{R}$ in $(-\frac{\pi}{2},\frac{\pi}{2})$, si ha:

    $$
    y \in \left(-\frac{\pi}{2},\frac{\pi}{2}\right)
    $$

<div style="page-break-after: always;"></div>

4) La densità di probabilità di $Y$ è:

    $$\begin{aligned}
    f_Y(y)
    &= \frac{1}{\sqrt{6\pi}}e^{-\frac{\tan^2 y}{6}}
    \frac1{\cos^2(y)}
    \end{aligned}$$

    quindi:

    $$\boxed{
    f_Y(y)=\frac{1}{\sqrt{6\pi}\cos^2(y)}\,e^{-\frac{\tan^2(y)}{6}}
    \cdot \mathbf{1}_{\left(-\frac{\pi}{2},\frac{\pi}{2}\right)}(y)
    } \;.$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 7

Sia $X\sim N(0,5)$, calcolare la densità di probabilità di $Y=X^2$.

##### Risoluzione

> Ricordiamo che la densità di probabilità di una variabile aleatoria normale $N(0,5)$ è:
> 
> $$
> f_X(x) = \frac1{\sqrt{10\pi}}e^{-\frac{x^2}{10}}
> $$

Notiamo subito che la funzione

$$
g(x) = x^2
$$

è una parabola e quindi non è strettamente crescente o decrescente su $\mathbb{R}$. Per questo motivo non possiamo applicare direttamente il teorema di trasformazione per funzioni monotone.

1) Scriviamo $F_Y$ in termini di $F_X$:

    $$\begin{aligned}
    F_Y(y) = P(Y\le y) = P(X^2\le y)
    &= P(-\sqrt y\le X\le \sqrt y) \\
    &= P(X\le \sqrt y) - P(X<-\sqrt y) \\
    &= F_X(\sqrt y) - F_X(-\sqrt y)
    \end{aligned}$$

2) Calcoliamo $f_Y$ in termini di $F_Y$:

    $$\begin{aligned}
    f_Y(y)
    &= \frac{d}{dy}\Big\{ F_X(\sqrt y) - F_X(-\sqrt y) \Big\} \\
    &= \frac{d}{dy}F_X(\sqrt y) - \frac{d}{dy}F_X(-\sqrt y) \\
    &= f_X(\sqrt y)\cdot\frac1{2\sqrt y} + 
    f_X(-\sqrt y)\cdot\frac1{2\sqrt y} \\
    &= \frac1{2\sqrt y}\left(f_X(\sqrt y)+f_X(-\sqrt y)\right) \\
    &= \frac1{2\sqrt y}\cdot 2f_X(\sqrt y) \\
    &= \frac1{\sqrt y}f_X(\sqrt y)
    \end{aligned}$$

    Poiché la normale è una funzione pari:

    $$
    f_X(x)=f_X(-x)
    $$

3) Calcoliamo il supporto di $Y$:

    Poiché $Y=X^2$:

    $$
    Y \ge 0
    $$

4) La densità di probabilità di $Y$ è:

    $$
    \begin{aligned}
    f_Y(y)
    &= \frac1{\sqrt y}f_X(\sqrt y) \\
    &= \frac1{\sqrt y}\cdot \frac1{\sqrt{10\pi}}e^{-\frac{(\sqrt y)^2}{10}} \\
    &= \frac1{\sqrt{10\pi y}}e^{-\frac{y}{10}}
    \end{aligned}
    $$

    quindi:

    $$\boxed{
    f_Y(y)= \frac1{\sqrt{10\pi y}}e^{-\frac{y}{10}}
    \cdot \mathbf{1}_{(0,+\infty)}(y)
    } \;.$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 8

Sia $X\sim U(0,9)$, calcolare la densità di probabilità di $Y=1/X$.

##### Risoluzione

> Ricordiamo che la densità di probabilità di una variabile aleatoria uniforme su $(0,9)$ è:
> 
> $$
> f_X(x) = \frac1{9}, \quad x\in(0,9)
> $$

Notiamo subito che la funzione

$$
g(x)=\frac1x
$$

è strettamente decrescente su $(0,9)$ (quindi invertibile), per cui possiamo applicare il teorema di trasformazione per variabili monotone.

> Teorema di trasformazione per variabili monotone:
>
> $$
> f_Y(y) = f_X\!\big(g^{-1}(y)\big)\cdot \left|\frac{d}{dy}g^{-1}(y)\right|
> $$

1) Calcoliamo l’inversa della funzione $g(x)$:

    $$\begin{aligned}
    y = \frac1x \quad \Longrightarrow \quad x = \frac1y
    \end{aligned}$$

    quindi:

    $$
    g^{-1}(y)=\frac1y
    $$

2) Applichiamo il teorema:

    $$\begin{aligned}
    f_Y(y)
    &= f_X\!\left(\frac1y\right)\cdot \left|\frac{d}{dy}\frac1y\right| \\
    &= f_X\!\left(\frac1y\right)\cdot \frac1{y^2}
    \end{aligned}$$

<div style="page-break-after: always;"></div>

3) Calcoliamo il supporto di $Y$:

    Poiché $X\in(0,9)$:

    - per $x\to 9$ si ha $y\to \frac19$
    - per $x\to 0^+$ si ha $y\to +\infty$

    quindi:

    $$
    y \in \left[\frac19,+\infty\right)
    $$

4) La densità di probabilità di $Y$ è:

    $$\begin{aligned}
    f_Y(y)
    &= \frac1{9}\cdot \frac1{y^2} \\
    &= \frac1{9y^2}
    \end{aligned}$$

    quindi:

    $$\boxed{
    f_Y(y)= \frac1{9y^2}\cdot \mathbf{1}_{\left[\frac19,+\infty\right)}(y)
    } \;.$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 9

Sia $X\sim U(0,11)$, calcolare la densità di probabilità di $Y=\max\{X, 11-X\}$.

##### Risoluzione

> Ricordiamo che la densità di probabilità di una variabile aleatoria uniforme su $(0,11)$ è:
> 
> $$
> f_X(x)=\frac1{11}, \quad x\in(0,11)
> $$

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
