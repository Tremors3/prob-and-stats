## $$ \textcolor{red}{\text{Esercizi Lez. 16a - Teoria}} $$

### $$ \textcolor{blue}{\text{Esercizi Indipendenza - Casi Discreti}} $$

#### Esercizio 1 $-$ Ripasso indipendenza tra eventi

Siano $M$ ed $S$ due variabili aleatorie che modellano rispettivamente il massimo tra il lancio di due dadi e la somma dei valori ottenuti nei due lanci.

Sono $M$ ed $S$ indipendenti?

##### Risoluzione

> **Nota.** Due eventi $A$ e $B$ si dicono **indipendenti** se il verificarsi di uno non influenza la probabilità che si verifichi l'altro. Formalmente:
>
> $$
> P(A\cap B)=P(A)\cdot P(B).
> $$
>
> Per dimostrare che due eventi **non sono indipendenti** è sufficiente trovare una coppia di eventi per cui
>
> $$
> P(A\cap B)\neq P(A)\cdot P(B).
> $$

Consideriamo gli eventi $\{M=1\}$ e $\{S=12\}$.

- $P(M=1) = \frac{|\{M=1\}|}{|\Omega|} = \frac{|\{(1,1)\}|}{36} = \frac1{36} $

- $P(S=12) = \frac{|\{S=12\}|}{|\Omega|} = \frac{|\{(6,6)\}|}{36} = \frac1{36} $

I due eventi non possono verificarsi contemporaneamente, quindi $P(M=1,S=12)=0$.

$$
P(M=1,S=12)
= 0 \neq \frac1{36}\cdot\frac1{36}
= P(M=1)\,P(S=12)
$$

la condizione di indipendenza non è soddisfatta.

$$
\boxed{M \text{ ed } S \text{ non sono indipendenti}} \;.
$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 2 $-$ Indipendenza v.a. congiunte

$X$ ed $Y$ sono due v.a. discrete con funzione di probabilità data dalla tabella seguente. $X$ ed $Y$ sono indipendenti?

|$Y$ \ $X$| 0 | 1 | 2 |
|:-:|:-:|:-:|:-:|
| -1 | $\frac16$ | $\frac16$ | $\frac16$ |
|  1 | $0$ | $\frac12$ | $0$ |

##### Risoluzione

> Due variabili aleatorie discrete $X,Y$ sono indipendenti se
>
> $$
> p_{X,Y}(x,y)=p_X(x)\,p_Y(y)
> \qquad \forall x,y.
> $$
>
> Per mostrare che non sono indipendenti è sufficiente trovare una coppia di valori per cui tale uguaglianza non vale.

Scegliamo la coppia $(0,-1)$ e calcoliamo le rispettive marginali.

$$
p_Y(-1)
= \frac16+\frac16+\frac16
= \frac12.
$$

$$
p_X(0)
= \frac16+0
= \frac16.
$$

Confrontiamo ora la probabilità congiunta con il prodotto delle marginali:

$$
p_{X,Y}(0,-1)
= \frac16
\neq
\frac16\cdot\frac12
= p_X(0)\,p_Y(-1),
$$

la condizione di indipendenza non è soddisfatta.

$$
\boxed{X \text{ ed } Y \text{ non sono indipendenti}} \;.
$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 3 $-$ Indipendenza v.a. congiunte

Siano $X$ ed $Y$ due v.a. la cui funzione di probabilità congiunta $p_{X,Y}(x,y)$ è data dalla seguente tabella, dove $\varepsilon\in[-\frac14,\frac14]$.

|$Y$ \ $X$| 0 | 1 |
|:-:|:-:|:-:|
| 0 | $\frac14 - \varepsilon$ | $\frac14 + \varepsilon$ |
| 1 | $\frac14 + \varepsilon$ | $\frac14 - \varepsilon$ |

Determinare i valori di $\varepsilon$ per cui $X$ ed $Y$ sono indipendenti.

##### Risoluzione

Calcoliamo innanzitutto le marginali.

$$
p_X(0)=\frac12,
\qquad
p_X(1)=\frac12.
$$

$$
p_Y(0)=\frac12,
\qquad
p_Y(1)=\frac12.
$$

Se $X$ ed $Y$ sono indipendenti deve valere

$$
p_{X,Y}(x,y)
= p_X(x)\,p_Y(y)
\qquad \forall x,y.
$$

In particolare, per la coppia $(0,0)$:

$$
p_{X,Y}(0,0)
= \frac14-\varepsilon
= p_X(0)\,p_Y(0)
= \frac12\cdot\frac12
= \frac14.
$$

Abbiamo quindi che

$$
\frac14-\varepsilon=\frac14
\quad\Longrightarrow\quad
\boxed{\varepsilon=0} \;.
$$

$$
\boxed{X \text{ ed } Y \text{ sono indipendenti se e solo se } \varepsilon=0}.
$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 4 $-$ Indipendenza v.a. congiunte

Siano $X$ ed $Y$ due v.a. la cui funzione di probabilità congiunta è data dalla seguente tabella.

|$Y$ \ $X$| -1 | 0 | 1 |
|:-:|:-:|:-:|:-:|
| 4 | $\eta - \frac1{16}$ | $\frac14 - \eta$ | 0 |
| 5 | $\frac18$ | $\frac3{16}$ | $\frac18$ |
| 6 | $\eta + \frac1{16}$ | $\frac1{16}$ | $\frac14 - \eta$ |

1. Quali valori può assumere $\eta$ ?
2. Esistono dei valori di $\eta$ per i quali $X$ ed $Y$ sono indipendenti?

##### Risoluzione

1. **Determinare i valori ammissibili di $\eta$.**

    Essendo le probabilità non negative, deve valere:

    $$
    \eta-\frac1{16}\ge 0
    \qquad\text{e}\qquad
    \frac14-\eta\ge 0
    $$

    Da cui otteniamo

    $$
    \boxed{\frac1{16}\le \eta \le \frac14} \;.
    $$

2. **Verificare se esistono valori di $\eta$ per cui $X$ ed $Y$ sono indipendenti.**

    Come prima cosa calcoliamo le marginali di $X$.

    $$\begin{aligned}
    p_X(-1)
    &= \left(\eta-\frac1{16}\right)+\frac18+\left(\eta+\frac1{16}\right) \\
    &= 2\eta+\frac18
    \end{aligned}$$

    $$\begin{aligned}
    p_X(0)
    &= \left(\frac14-\eta\right)+\frac3{16}+\frac1{16} \\
    &= \frac12-\eta
    \end{aligned}$$

    $$\begin{aligned}
    p_X(1)
    &= 0+\frac18+\left(\frac14-\eta\right) \\
    &= \frac38-\eta
    \end{aligned}$$

    Calcoliamo ora le marginali di $Y$.

    $$\begin{aligned}
    p_Y(4)
    &= \left(\eta-\frac1{16}\right)+\left(\frac14-\eta\right)+0 \\
    &= \frac3{16}
    \end{aligned}$$

    $$\begin{aligned}
    p_Y(5)
    &= \frac18+\frac3{16}+\frac18 \\
    &= \frac7{16}
    \end{aligned}$$

    $$\begin{aligned}
    p_Y(6)
    &= \left(\eta+\frac1{16}\right)+\frac1{16}+\left(\frac14-\eta\right) \\
    &= \frac38
    \end{aligned}$$

    > Se $X$ ed $Y$ fossero indipendenti dovrebbe valere
    > 
    > $$
    > p_{X,Y}(x,y)=p_X(x)\,p_Y(y)
    > $$
    > 
    > per ogni coppia $(x,y)$.

    - Consideriamo la coppia $(-1,4)$:

        $$\begin{aligned}
        p_{X,Y}(-1,4)
        &= p_X(-1)\,p_Y(4) \\
        \eta-\frac1{16}
        &= \left(2\eta+\frac18\right)\frac3{16}
        \end{aligned}$$

        Risolvendo:

        $$\begin{aligned}
        16\eta-1
        &= 6\eta+\frac38 \\
        10\eta
        &= \frac{11}{8} \\
        \eta
        &= \frac{11}{80}.
        \end{aligned}$$

    - Verifichiamo ora un'altra coppia, ad esempio $(1,4)$:

        $$\begin{aligned}
        p_{X,Y}(1,4)
        &= p_X(1)\,p_Y(4) \\
        0
        &= \left(\frac38-\eta\right)\frac3{16}.
        \end{aligned}$$

        Risolvendo:

        $$
        \eta=\frac38.
        $$

    Poiché

    $$
    \frac{11}{80}\neq \frac38,
    $$

    non esiste alcun valore di $\eta$ che soddisfi contemporaneamente entrambe le condizioni.

    $$
    \boxed{\text{non esiste alcun valore di }\eta\text{ per cui }X\text{ ed }Y\text{ sono indipendenti}.}
    $$

> **Nota.** Per dimostrare che due variabili aleatorie **non** sono indipendenti è sufficiente trovare una sola coppia $(x,y)$ per cui
>
> $$
> p_{X,Y}(x,y)\neq p_X(x)\,p_Y(y).
> $$
>
> Per dimostrare invece che sono indipendenti bisogna verificare l'uguaglianza per tutte le coppie del supporto.

---

<div style="page-break-after: always;"></div>

### $$ \textcolor{blue}{\text{Esercizi Indipendenza - Casi Continui}} $$

#### Esercizio 5 $-$ Indipendenza v.a. congiunte

Siano $X$ ed $Y$ due v.a. a.c. la cui densità congiunta è

$$
f_{X,Y}(x,y) =
\begin{cases}
\frac{12}5 xy(1+y) & \text{per } (x,y)\in[0,1]^2 \\
0 & \text{altrimenti.}
\end{cases}
$$

Determinare:

1. le funzioni di densità marginali di $X$ e $Y$ per $(x,y)\in[0,1]^2$,
2. se $X$ ed $Y$ sono indipendenti.

##### Risoluzione

1. **Calcolare le funzioni di densità marginali di $X$ e $Y$.**

    $$\begin{aligned}
    f_X(x)
    &= \int_{-\infty}^{+\infty} f_{X,Y}(x,y)\,dy \\
    &= \int_0^1 \frac{12}5 xy(1+y)\,dy \\
    &= \frac{12}5 x \int_0^1 (y+y^2)\,dy \\
    &= \frac{12}5 x
    \left[\frac{y^2}{2}+\frac{y^3}{3}\right]_0^1 \\
    &= \frac{12}5 x
    \left(\frac12+\frac13\right) \\
    &= \frac{12}5 x\cdot\frac56 \\
    &= \boxed{2x}
    \qquad \text{per } 0\le x\le1 \;.
    \end{aligned}$$

    $$\begin{aligned}
    f_Y(y)
    &= \int_{-\infty}^{+\infty} f_{X,Y}(x,y)\,dx \\
    &= \int_0^1 \frac{12}5 xy(1+y)\,dx \\
    &= \frac{12}5 y(1+y)\int_0^1 x\,dx \\
    &= \frac{12}5 y(1+y)
    \left[\frac{x^2}{2}\right]_0^1 \\
    &= \frac{12}5 y(1+y)\cdot\frac12 \\
    &= \boxed{\frac65\,y(1+y)}
    \qquad \text{per } 0\le y\le1 \;.
    \end{aligned}$$

2. **Determinare se $X$ ed $Y$ sono indipendenti.**

    Verifichiamo la condizione di indipendenza:

    $$\begin{aligned}
    f_X(x)\,f_Y(y)
    &= 2x \cdot \frac65\,y(1+y) \\
    &= \frac{12}5 xy(1+y) \\
    &= f_{X,Y}(x,y).
    \end{aligned}$$

    Poiché

    $$
    f_{X,Y}(x,y)=f_X(x)\,f_Y(y)
    \qquad \forall (x,y)\in[0,1]^2,
    $$

    la condizione di indipendenza è soddisfatta.

    $$
    \boxed{X \text{ ed } Y \text{ sono indipendenti}} \;.
    $$

> **Nota.** Per variabili aleatorie assolutamente continue, $X$ ed $Y$ sono indipendenti se e solo se
>
> $$
> f_{X,Y}(x,y)=f_X(x)\,f_Y(y)
> \qquad \forall (x,y).
> $$
>
> In pratica, dopo aver calcolato le densità marginali, basta verificare che il loro prodotto coincida con la densità congiunta.

---

<div style="page-break-after: always;"></div>

#### Esercizio 6 $-$ Indipendenza v.a. congiunte

Siano $X$ ed $Y$ due v.a. a.c. la cui densità di probabilità congiunta è uguale a

$$
f_{X,Y}(x,y) = 
\frac1{10} (3x^2+8xy)
\quad\text{per}\quad
\begin{aligned}
0\le x\le1 \\
0\le y\le2
\end{aligned}
$$

e uguale a $0$ per gli altri valori di $x$ ed $y$.

Determinare se $X$ ed $Y$ sono indipendenti.

##### Risoluzione

1. **Calcolare le funzioni di densità marginali di $X$ e $Y$.**

    $$\begin{aligned}
    f_X(x)
    &= \int_{-\infty}^{+\infty} f_{X,Y}(x,y)\,dy \\
    &= \int_0^2 \frac1{10}(3x^2+8xy)\,dy \\
    &= \frac1{10}\int_0^2 (3x^2+8xy)\,dy \\
    &= \frac1{10}
    \left[
    3x^2y+4xy^2
    \right]_0^2 \\
    &= \frac1{10}(6x^2+16x) \\
    &= \boxed{\frac35x^2+\frac85x}
    \qquad \text{per } 0\le x\le1 \;.
    \end{aligned}$$

    $$\begin{aligned}
    f_Y(y)
    &= \int_{-\infty}^{+\infty} f_{X,Y}(x,y)\,dx \\
    &= \int_0^1 \frac1{10}(3x^2+8xy)\,dx \\
    &= \frac1{10}
    \left[
    x^3+4x^2y
    \right]_0^1 \\
    &= \frac1{10}(1+4y) \\
    &= \boxed{\frac1{10}+\frac25y}
    \qquad \text{per } 0\le y\le2 \;.
    \end{aligned}$$

2. **Determinare se $X$ ed $Y$ sono indipendenti.**

    Verifichiamo la condizione di indipendenza:

    $$\begin{aligned}
    f_X(x)\,f_Y(y)
    &= \left(\frac35x^2+\frac85x\right)
    \left(\frac1{10}+\frac25y\right) \\
    &= \frac3{50}x^2+\frac6{25}x^2y
    +\frac4{25}x+\frac{16}{25}xy.
    \end{aligned}$$

    Tale espressione **non coincide** con

    $$
    f_{X,Y}(x,y)
    = \frac3{10}x^2+\frac45xy.
    $$

    Pertanto

    $$
    f_{X,Y}(x,y)\neq f_X(x)\,f_Y(y),
    $$

    e la condizione di indipendenza non è soddisfatta.

    $$
    \boxed{X \text{ ed } Y \text{ non sono indipendenti}} \;.
    $$

> **Nota.** Per variabili aleatorie assolutamente continue, $X$ ed $Y$ sono indipendenti se e solo se
>
> $$
> f_{X,Y}(x,y)=f_X(x)\,f_Y(y)
> \qquad \forall (x,y).
> $$
>
> In pratica, dopo aver calcolato le densità marginali, basta verificare che il loro prodotto coincida con la densità congiunta.

---

<div style="page-break-after: always;"></div>

#### Esercizio 7 $-$ Indipendenza tra 3 v.a. congiunte

Siano $X$, $Y$ e $Z$ tre v.a. a.c. la cui densità congiunta è

$$
f_{X,Y,Z}(x,y,z) =
\begin{cases}
\frac23 (x+y+z) & \text{per } (x,y,z)\in[0,1]^3 \\
0 & \text{altrimenti}
\end{cases}
$$

1. calcolare le funzioni di densità marginali,
2. determinare se $X$, $Y$ e $Z$ sono indipendenti.

##### Risoluzione

1. **Calcolare le funzioni di densità marginali di $X$, $Y$ e $Z$.**

    $$\begin{aligned}
    f_X(x)
    &= \int_{-\infty}^{+\infty}\int_{-\infty}^{+\infty}
    f_{X,Y,Z}(x,y,z)\,dz\,dy \\
    &= \int_0^1 \left(
    \int_0^1 \frac23(x+y+z)\,dz
    \right)\,dy \\
    &= \int_0^1 \left(
    \frac23(x+y)+\frac23\int_0^1 z\,dz
    \right)\,dy \\
    &= \int_0^1 \left(
    \frac23(x+y)+\frac23\left[\frac{z^2}{2}\right]_0^1
    \right)\,dy \\
    &= \int_0^1 \left(
    \frac23(x+y)+\frac13
    \right)\,dy \\
    &= \frac23x\int_0^1dy
    +\frac23\int_0^1y\,dy
    +\frac13\int_0^1dy \\
    &= \frac23x
    +\frac23\left[\frac{y^2}{2}\right]_0^1
    +\frac13 \\
    &= \frac23x+\frac13+\frac13 \\
    &= \boxed{\frac23(x+1)}
    \qquad \text{per } 0\le x\le1 \;.
    \end{aligned}$$

    <div style="page-break-after: always;"></div>

    Per simmetria otteniamo immediatamente anche:

    $$
    f_Y(y)=\boxed{\frac23(y+1)}
    \qquad \text{per } 0\le y\le1  \;.
    $$

    $$
    f_Z(z)=\boxed{\frac23(z+1)}
    \qquad \text{per } 0\le z\le1  \;.
    $$

2. **Determinare se $X$, $Y$ e $Z$ sono indipendenti.**

    Verifichiamo la condizione di indipendenza:

    $$\begin{aligned}
    f_X(x)f_Y(y)f_Z(z)
    &= \frac23(x+1)\cdot\frac23(y+1)\cdot\frac23(z+1) \\
    &= \frac8{27}(x+1)(y+1)(z+1).
    \end{aligned}$$

    Tale espressione non coincide con

    $$
    f_{X,Y,Z}(x,y,z)=\frac23(x+y+z).
    $$

    Pertanto

    $$
    f_{X,Y,Z}(x,y,z)
    \neq
    f_X(x)f_Y(y)f_Z(z),
    $$

    e la condizione di indipendenza non è soddisfatta.

    $$
    \boxed{X,\;Y\text{ e }Z\text{ non sono indipendenti}} \;.
    $$

> **Nota.** Siano $X_1,\dots,X_n$ variabili aleatorie congiunte. Sono indipendenti se e solo se
>
> $$
> f_{X_1,\dots,X_n}(x_1,\dots,x_n)
> = \prod_{i=1}^n f_{X_i}(x_i)
> \qquad \forall (x_1,\dots,x_n).
> $$
>
> In pratica, dopo aver calcolato le marginali, basta verificare che il prodotto di tutte le densità marginali coincida con la densità congiunta.
>
> ---

<div style="page-break-after: always;"></div>

> ---
>
> La marginale di $X_i$ si ottiene integrando la densità congiunta rispetto a tutte le altre variabili:
>
> $$
> f_{X_i}(x_i)
> = \int \cdots \int
> f_{X_1,\dots,X_n}(x_1,\dots,x_n)\,
> \prod_{j\ne i} dx_j.
> $$

---

<div style="page-break-after: always;"></div>