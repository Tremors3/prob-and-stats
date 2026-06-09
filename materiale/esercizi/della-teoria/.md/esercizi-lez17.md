## $$ \textcolor{red}{\text{Esercizi Lez. 17 - Teoria}} $$

### $$ \textcolor{blue}{\text{Esercizi Indipendenza e Correlazione}} $$

#### Esercizio 1

Siano $X$ ed $Y$ due variabili aleatorie discrete la cui funzione di probabilità congiunta è data dalla tabella di seguito. Quale delle seguenti affermazioni è vera?

|$Y$ \ $X$| 0 | 1 | 2 |
|:-:|:-:|:-:|:-:|
| -1 | $\frac16$ | $\frac16$ | $\frac16$ |
|  1 | $0$ | $\frac12$ | $0$ |

A) $X$ ed $Y$ sono scorrelate e dipendenti
B) $X$ ed $Y$ sono scorrelate e indipendenti
C) $X$ ed $Y$ sono positivamente correlate e dipendenti
D) $X$ ed $Y$ sono negativamente correlate e indipendenti

##### Risoluzione

1. **Studiamo l'indipendenza tra $X$ e $Y$.**

    Calcoliamo le marginali.

    |$Y$ \ $X$| 0 | 1 | 2 | $p_Y(y)$ |
    |:-:|:-:|:-:|:-:|:-:|
    | -1 | $\frac16$ | $\frac16$ | $\frac16$ | $\frac12$ |
    |  1 | $0$ | $\frac12$ | $0$ | $\frac12$ |
    | $p_X(x)$ | $\frac16$ | $\frac23$ | $\frac16$ | $1$ |

    Verifichiamo la condizione di indipendenza sulla coppia $(0,-1)$.

    $$
    p_{X,Y}(0,-1)
    = \frac16
    \neq
    p_X(0)\,p_Y(-1)
    = \frac16\cdot\frac12
    = \frac1{12}
    $$

    La condizione non è soddisfatta. Quindi $X$ ed $Y$ sono **dipendenti**.

    <div style="page-break-after: always;"></div>

2. **Studiamo la correlazione tra $X$ e $Y$.**

    Calcoliamo la covarianza.

    $$
    \operatorname{Cov}(X,Y)
    = E[XY]-E[X]E[Y]
    $$

    Calcoliamo le tre aspettazioni necessarie.

    $$\begin{aligned}
    E[X]
    &= \sum_{x\in\{0,1,2\}} x\,p_X(x) \\
    &= 0\cdot\frac16 + 1\cdot\frac23 + 2\cdot\frac16 \\
    &= 1
    \end{aligned}$$

    $$\begin{aligned}
    E[Y]
    &= \sum_{y\in\{-1,1\}} y\,p_Y(y) \\
    &= -1\cdot\frac12 + 1\cdot\frac12 \\
    &= 0
    \end{aligned}$$

    $$\begin{aligned}
    E[XY]
    &= \sum_{(x,y)\in\{0,1,2\}\times\{-1,1\}}
    xy\,p_{X,Y}(x,y) \\
    &=
    (0\cdot(-1))\frac16
    +(1\cdot(-1))\frac16
    +(2\cdot(-1))\frac16 \\
    &\quad +
    (0\cdot1)0
    +(1\cdot1)\frac12
    +(2\cdot1)0 \\
    &= -\frac16-\frac13+\frac12 \\
    &= 0
    \end{aligned}$$

    Calcoliamo quindi la covarianza.

    $$\begin{aligned}
    \operatorname{Cov}(X,Y)
    &= E[XY]-E[X]E[Y] \\
    &= 0-1\cdot0 \\
    &= 0
    \end{aligned}$$

    Poiché la covarianza è nulla, le variabili sono **scorrelate**.

Quindi:

$$
\boxed{
X \text{ e } Y
\text{ sono \textbf{dipendenti} e \textbf{scorrelate}}
}
\;.
$$

> **Nota.** Conviene controllare prima l'indipendenza. Infatti, se due variabili sono indipendenti, allora sono automaticamente scorrelate. Se invece risultano dipendenti, occorre calcolare la covarianza per stabilire se sono correlate oppure scorrelate.

> **Nota.** Formule essenziali:
>
> $$
> p_{X,Y}(x,y)=p_X(x)\,p_Y(y)
> \qquad \forall (x,y)
> $$
>
> $$
> \operatorname{Cov}(X,Y)
> = E[XY]-E[X]E[Y]
> $$
>
> $$
> \operatorname{Cov}(X,Y)=0
> \;\Longrightarrow\;
> X \text{ e } Y \text{ sono scorrelate}.
> $$
>
> $$
> X \text{ e } Y \text{ indipendenti}
> \;\Longrightarrow\;
> \operatorname{Cov}(X,Y)=0.
> $$
>
> L'implicazione inversa, in generale, non è vera.

---

<div style="page-break-after: always;"></div>

#### Esercizio 2

Siano

$$
X \sim \mathcal N(0,1)
\qquad\text{e}\qquad
Y=X^2
$$

Quale delle seguenti affermazioni è vera?

A) $X$ ed $Y$ sono scorrelate e dipendenti
B) $X$ ed $Y$ sono scorrelate e indipendenti
C) $X$ ed $Y$ sono positivamente correlate e dipendenti
D) $X$ ed $Y$ sono negativamente correlate e indipendenti

##### Risoluzione

1. **Studiamo l'indipendenza tra $X$ e $Y$.**

    Osserviamo che

    $$
    Y=X^2.
    $$

    Quindi il valore di $Y$ è completamente determinato dal valore di $X$.

    $\;$

    Di conseguenza $Y$ è una funzione di $X$ e le due variabili **non** possono essere indipendenti.

    $\;$

2. **Studiamo la correlazione tra $X$ e $Y$.**

    Calcoliamo la covarianza.

    $$
    \operatorname{Cov}(X,Y)
    = E[XY]-E[X]E[Y].
    $$

    Poiché $Y=X^2$, si ha

    $$
    \operatorname{Cov}(X,Y)
    = E[X^3]-E[X]E[X^2].
    $$

    Essendo $X\sim\mathcal N(0,1)$, la distribuzione è simmetrica rispetto a $0$. Pertanto

    $$
    E[X]=0
    \qquad\text{e}\qquad
    E[X^3]=0
    $$

    poiché $X^3$ è una funzione dispari.

    <div style="page-break-after: always;"></div>

    Calcoliamo la covarianza.

    $$\begin{aligned}
    \operatorname{Cov}(X,Y)
    &= E[X^3]-E[X]E[X^2] \\
    &= 0-0\cdot E[X^2] \\
    &= 0
    \end{aligned}$$

    La covarianza è nulla, quindi $X$ ed $Y$ sono scorrelate.

Conclusione:

$$
\boxed{
X \text{ ed } Y
\text{ sono \textbf{scorrelate} e \textbf{dipendenti}}
}
\;.
$$

> **Nota.** Questo è un classico esempio che mostra come la scorrelazione non implichi l'indipendenza. Infatti:
>
> $$
> \operatorname{Cov}(X,Y)=0
> $$
>
> ma
>
> $$
> Y=X^2
> $$
>
> dipende completamente da $X$.

---

<div style="page-break-after: always;"></div>

#### Esercizio 3

Siano $X$ ed $Y$ due variabili aleatorie la cui covarianza è uguale a $-2.5$.

Calcolare $\text{Cov}(-2X+7,\,5Y-2)$.

##### Risoluzione

Per la proprietà di linearità della covarianza abbiamo che

$$
\text{Cov}(aX+b,\;cY+d)=ac\,\text{Cov}(X,Y).
$$

Applicandola al nostro caso:

$$\begin{aligned}
\text{Cov}(-2X+7,\;5Y-2)
&=(-2)\cdot5\cdot\text{Cov}(X,Y) \\
&=(-2)\cdot5\cdot(-2.5) \\
&=25.
\end{aligned}$$

Pertanto

$$
\boxed{\text{Cov}(-2X+7,\;5Y-2)=25} \;.
$$

> **Nota.** Proprietà di linearità della covarianza:
>
> $$
> \text{Cov}(aX+b,\;cY+d)=ac\,\text{Cov}(X,Y).
> $$
>
> Proprietà di linearità della varianza:
>
> $$
> \text{Var}(aX + bY + c) = a^2X + b^2Y + 2ab\,\text{Cov}(X,Y)
> $$
>

---

<div style="page-break-after: always;"></div>

#### Esercizio 4

Siano $X$ ed $Y$ due variabili aleatorie tali che

$$
\text{Cov}(X,Y) = -2.4
\qquad
\text{Var}(X)=4
\qquad
\text{Var}(Y)=9.
$$

Calcolare $\rho(-6X+2,\,-3Y)$.

##### Risoluzione

> **Nota.** Ricordiamo che il **coefficiente di correlazione** $\rho$ è definito come
>
> $$
> \rho(X,Y)
> = \frac{\text{Cov}(X,Y)}
> {\sqrt{\text{Var}(X)}\,\sqrt{\text{Var}(Y)}}.
> $$
>
> Inoltre vale la seguente proprietà:
>
> $$
> \rho(aX+b,\;cY+d)
> = \operatorname{sgn}(ac)\,\rho(X,Y).
> $$
>
> In particolare, se $a$ e $c$ hanno lo stesso segno, allora
>
> $$
> \rho(aX+b,\;cY+d)=\rho(X,Y).
> $$

Nel nostro caso $a=-6$ e $c=-3$, quindi $ac>0$.

Pertanto

$$
\rho(-6X+2,\,-3Y)=\rho(X,Y).
$$

Calcoliamo quindi $\rho(X,Y)$.

$$\begin{aligned}
\rho(X,Y)
&=
\frac{\text{Cov}(X,Y)}
{\sqrt{\text{Var}(X)}\,\sqrt{\text{Var}(Y)}} \\
&=
\frac{-2.4}{\sqrt{4}\,\sqrt{9}} \\
&=
\frac{-2.4}{2\cdot 3} \\
&=
\frac{-2.4}{6} \\
&=
\boxed{-0.4}.
\end{aligned}$$

<div style="page-break-after: always;"></div>

Quindi

$$
\boxed{\rho(-6X+2,\,-3Y)=-0.4}.
$$

Sfruttare questa proprietà permette di semplificare notevolmente i calcoli.

---

<div style="page-break-after: always;"></div>

#### Esercizio 5

Siano $X$ e $Y$ due v.a. la cui funzione di probabilità congiunta è data nella tabella seguente:

| $X$ \ $Y$ | 0 | 1 | 2 |
|:-:|:-:|:-:|:-:|
| 0 | $\frac14$ | 0 | $\frac14$ |
| 1 | 0 | $\frac12$ | 0 |

Calcolare:

- $\text{Cov}(X,Y)$,
- $\rho(X,Y)$.

##### Risoluzione

1. **Calcoliamo la covarianza di $X$ e $Y$.**

    Calcoliamo le marginali.

    | $X$ \ $Y$ | 0 | 1 | 2 | $p_X(x)$ |
    |:-:|:-:|:-:|:-:|:-:|
    | 0 | $\frac14$ | 0 | $\frac14$ | $\frac12$ |
    | 1 | 0 | $\frac12$ | 0 | $\frac12$ |
    | $p_Y(y)$ | $\frac14$ | $\frac12$ | $\frac14$ | 1 |

    Calcoliamo le aspettazioni necessarie.

    $$\begin{aligned}
    E[X]
    &= \sum_{x\in\{0,1\}} x \cdot p_X(x) \\
    &= 0\cdot\frac12 + 1\cdot\frac12 \\
    &= \frac12
    \end{aligned}$$

    $$\begin{aligned}
    E[Y]
    &= \sum_{y\in\{0,1,2\}} y \cdot p_Y(y) \\
    &= 0\cdot\frac14 + 1\cdot\frac12 + 2\cdot\frac14 \\
    &= 1
    \end{aligned}$$

    $$\begin{aligned}
    E[XY]
    &= \sum_{(x,y)\in\{0,1\}\times\{0,1,2\}} xy \cdot p_{X,Y}(x,y) \\
    &= (0\cdot0)\frac14 + (0\cdot1)0 + (0\cdot2)\frac14 \\
    &\quad + (1\cdot0)0 + (1\cdot1)\frac12 + (1\cdot2)0 \\
    &= \frac12
    \end{aligned}$$

    Calcoliamo la covarianza.

    $$\begin{aligned}
    \text{Cov}(X,Y)
    &= E[XY] - E[X]\cdot E[Y] \\
    &= \frac12 - \frac12\cdot1 \\
    &= \boxed{0} \;.
    \end{aligned}$$

    Le due variabili sono quindi scorrelate.

2. **Calcoliamo il coefficiente di correlazione.**

    $$\begin{aligned}
    \rho(X,Y)
    &= \frac{\text{Cov}(X,Y)}
    {\sqrt{\text{Var}(X)}\,\sqrt{\text{Var}(Y)}} \\
    &= \frac{0}
    {\sqrt{\text{Var}(X)}\,\sqrt{\text{Var}(Y)}} \\
    &= \boxed{0} \;.
    \end{aligned}$$

    Poiché la covarianza è nulla, anche il coefficiente di correlazione è nullo.

---

<div style="page-break-after: always;"></div>

#### Esercizio 6

Siano $X$ ed $Y$ due v.a. con densità di probabilità congiunta data da

$$
f_{X,Y}(x,y) =
\begin{cases}
\frac{12}5 xy(1+y) & \text{per } (x,y)\in[0,1]^2 \\
0 & \text{altrimenti}
\end{cases}
$$

Calcolare $\text{Cov}(X,Y)$ e $\rho(X,Y)$.

##### Risoluzione

1. **Calcoliamo la covarianza.**

    Come prima cosa ricaviamo le densità marginali di $X$ e $Y$.

    $$\begin{aligned}
    f_X(x)
    &= \int_{-\infty}^{+\infty} f_{X,Y}(x,y)\,dy \\
    &= \int_0^1 \frac{12}5 xy(1+y)\,dy \\
    &= \frac{12}5 x \int_0^1 (y+y^2)\,dy \\
    &= \frac{12}5 x \left[\frac{y^2}{2}+\frac{y^3}{3}\right]_0^1 \\
    &= \frac{12}5 x \left(\frac12+\frac13\right) \\
    &= 2x,
    \qquad 0\le x\le 1
    \end{aligned}$$

    $$\begin{aligned}
    f_Y(y)
    &= \int_{-\infty}^{+\infty} f_{X,Y}(x,y)\,dx \\
    &= \int_0^1 \frac{12}5 xy(1+y)\,dx \\
    &= \frac{12}5 y(1+y)\int_0^1 x\,dx \\
    &= \frac{12}5 y(1+y)\left[\frac{x^2}{2}\right]_0^1 \\
    &= \frac{12}5 y(1+y)\frac12 \\
    &= \frac65\,y(1+y),
    \qquad 0\le y\le 1
    \end{aligned}$$

    Prima di procedere con ulteriori calcoli, conviene verificare se $X$ ed $Y$ sono indipendenti.

    $$\begin{aligned}
    f_X(x)\,f_Y(y)
    &= 2x\cdot\frac65\,y(1+y) \\
    &= \frac{12}5xy(1+y) \\
    &= f_{X,Y}(x,y)
    \end{aligned}$$

    La condizione di indipendenza è soddisfatta per ogni $(x,y)\in[0,1]^2$. Pertanto $X$ ed $Y$ sono **indipendenti** e quindi anche **scorrelate**.

    $$
    \boxed{\text{Cov}(X,Y)=0} \;.
    $$

2. **Calcoliamo il coefficiente di correlazione.**

    Poiché la covarianza è nulla, si ha immediatamente

    $$
    \rho(X,Y)
    = \frac{\text{Cov}(X,Y)}
    {\sqrt{\text{Var}(X)}\,\sqrt{\text{Var}(Y)}}
    = 0
    $$

    Pertanto

    $$
    \boxed{\rho(X,Y)=0} \;.
    $$

---

<div style="page-break-after: always;"></div>

#### Esercizio 7

Siano $X$ ed $Y$ due v.a. la cui funzione di probabilità congiunta è data nella tabella in alto.

|$Y$ \ $X$| 0 | 1 | 2 |
|:-:|:-:|:-:|:-:|
| 0 | $\frac16$ | $\frac16$ | $\frac16$ |
| 1 | $0$ | $\frac12$ | $0$ |

- calcolare $E[XY]$,
- determinare se $X$ ed $Y$ sono indipendenti,
- determinare se $X$ ed $Y$ sono scorrelate,
- calcolare $\text{Var}(X-Y)$.

##### Risoluzione

1. **Calcoliamo $E[XY]$.**

    $$\begin{aligned}
    E[XY]
    &= \sum_{(x,y)\in\{0,1,2\}\times\{0,1\}} xy\,p_{X,Y}(x,y) \\
    &= (0\cdot0)\frac16 + (1\cdot0)\frac16 + (2\cdot0)\frac16 \\
    &\quad + (0\cdot1)0 + (1\cdot1)\frac12 + (2\cdot1)0 \\
    &= \boxed{\frac12} \;.
    \end{aligned}$$

2. **Determinare se $X$ ed $Y$ sono indipendenti.**

    Calcoliamo le marginali.

    |$Y$ \ $X$| 0 | 1 | 2 | $p_Y(y)$ |
    |:-:|:-:|:-:|:-:|:-:|
    | 0 | $\frac16$ | $\frac16$ | $\frac16$ | $\frac12$ |
    | 1 | $0$ | $\frac12$ | $0$ | $\frac12$ |
    | $p_X(x)$ | $\frac16$ | $\frac23$ | $\frac16$ | 1 |

    <div style="page-break-after: always;"></div>

    Scegliamo la coppia $(0,0)$ e verifichiamo la condizione di indipendenza.

    $$\begin{aligned}
    p_X(0)\,p_Y(0)
    &= \frac16\cdot\frac12 \\
    &= \frac1{12}
    \neq
    p_{X,Y}(0,0)
    = \frac16
    \end{aligned}$$

    La condizione di indipendenza non è soddisfatta.

    $$
    \boxed{X \text{ e } Y \text{ sono tra loro \textbf{dipendenti}}} \;.
    $$

3. **Determinare se $X$ ed $Y$ sono scorrelate.**

    Calcoliamo le aspettazioni necessarie.

    $$\begin{aligned}
    E[X]
    &= \sum_{x\in\{0,1,2\}} x\,p_X(x) \\
    &= 0\frac16 + 1\frac23 + 2\frac16 \\
    &= 1
    \end{aligned}$$

    $$\begin{aligned}
    E[Y]
    &= \sum_{y\in\{0,1\}} y\,p_Y(y) \\
    &= 0\frac12 + 1\frac12 \\
    &= \frac12
    \end{aligned}$$

    $$
    E[XY] = \frac12
    \qquad \text{(già calcolata).}
    $$

    Calcoliamo la covarianza.

    $$\begin{aligned}
    \text{Cov}(X,Y)
    &= E[XY] - E[X]E[Y] \\
    &= \frac12 - 1\cdot\frac12 \\
    &= 0
    \end{aligned}$$

    La covarianza è nulla.

    $$
    \boxed{X \text{ e } Y \text{ sono tra loro \textbf{scorrelate}}} \;.
    $$

    <div style="page-break-after: always;"></div>

4. **Calcolare $\text{Var}(X-Y)$.**

    Poiché $X$ e $Y$ sono scorrelate, risulta $\text{Cov}(X,Y)=0$.

    > **Nota.** Per $X$ e $Y$ correlate:
    >
    > $$
    > \text{Var}(aX+bY+c)
    > = a^2\text{Var}(X) + b^2\text{Var}(Y) + 2ab\text{Cov}(X,Y)
    > $$
    >
    > **Nota.** Mentre per $X$ e $Y$ scorrelate:
    >
    > $$
    > \text{Var}(aX+bY+c)
    > = a^2\text{Var}(X) + b^2\text{Var}(Y)
    > $$

    Nel nostro caso:

    $$\begin{aligned}
    \text{Var}(X-Y)
    &= \text{Var}(X) + (-1)^2\text{Var}(Y) \\
    &= \text{Var}(X) + \text{Var}(Y) \\
    \end{aligned}$$

    Calcoliamo le aspettazioni necessarie.

    $$\begin{aligned}
    E[X^2]
    &= \sum_{x\in\{0,1,2\}} x^2\,p_X(x) \\
    &= 0^2\frac16 + 1^2\frac23 + 2^2\frac16 \\
    &= \frac43
    \end{aligned}$$

    $$\begin{aligned}
    E[Y^2]
    &= \sum_{y\in\{0,1\}} y^2\,p_Y(y) \\
    &= 0^2\frac12 + 1^2\frac12 \\
    &= \frac12
    \end{aligned}$$

    $$
    E[X] = 1
    \qquad \text{(già calcolata).}
    $$

    $$
    E[X] = \frac12
    \qquad \text{(già calcolata).}
    $$

    <div style="page-break-after: always;"></div>

    Calcoliamo le varianze.

    $$\begin{aligned}
    \text{Var}(X)
    &= E[X^2] - (E[X])^2 \\
    &= \frac43 - 1^2 \\
    &= \frac13
    \end{aligned}$$

    $$\begin{aligned}
    \text{Var}(Y)
    &= E[Y^2] - (E[Y])^2 \\
    &= \frac12 - \left(\frac12\right)^2 \\
    &= \frac14
    \end{aligned}$$

    Infine:

    $$\begin{aligned}
    \text{Var}(X-Y)
    &= \text{Var}(X) + \text{Var}(Y) \\
    &= \frac13 + \frac14 \\
    &= \boxed{\frac7{12}} \;.
    \end{aligned}$$

---

<div style="page-break-after: always;"></div>

> Mini formulario su **varianza, covarianza e correlazione**.
>
> **Varianza**
>
> $$
> \text{Var}(X) = E[X^2] - (E[X])^2
> $$
>
> $$
> \text{Var}(aX+b) = a^2\text{Var}(X)
> $$
>
> **Covarianza**
>
> $$
> \text{Cov}(X,Y)
> = E[XY] - E[X]E[Y]
> $$
>
> $$
> \text{Cov}(aX+b,\; rY+s)
> = ar\,\text{Cov}(X,Y)
> $$
>
> In particolare:
>
> $$
> \text{Cov}(X,X)=\text{Var}(X)
> $$
>
> $$
> \text{Cov}(X,c)=0
> $$
>
> **Varianza di combinazioni lineari**
>
> $$
> \text{Var}(aX+bY+c)
> = a^2\text{Var}(X) +
> b^2\text{Var}(Y) +
> 2ab\,\text{Cov}(X,Y)
> $$
>
> Casi particolari:
>
> $$
> \text{Var}(X+Y)
> = \text{Var}(X) +
> \text{Var}(Y) +
> 2\text{Cov}(X,Y)
> $$
>
> $$
> \text{Var}(X-Y)
> = \text{Var}(X) +
> \text{Var}(Y) -
> 2\text{Cov}(X,Y)
> $$
>
> **Variabili scorrelate**
>
> $$
> \text{Cov}(X,Y)=0
> $$
>
> Se $X$ e $Y$ sono scorrelate:
>
> $$
> \text{Var}(aX+bY+c)
> = a^2\text{Var}(X) +
> b^2\text{Var}(Y)
> $$
>
> e quindi:
>
> $$
> \text{Var}(X\pm Y)
> = \text{Var}(X) +
> \text{Var}(Y)
> $$

<div style="page-break-after: always;"></div>

> **Variabili indipendenti**
>
> $$
> X \perp Y
> \quad\Longrightarrow\quad
> \text{Cov}(X,Y)=0
> $$
>
> cioè:
>
> $$
> \text{indipendenti}
> \;\Longrightarrow\;
> \text{scorrelate}
> $$
>
> Il viceversa **non è in generale vero**.
>
> Inoltre, se $X$ e $Y$ sono indipendenti:
>
> $$
> E[XY]=E[X]E[Y]
> $$
>
> **Coefficiente di correlazione**
>
> $$
> \rho(X,Y)
> = \frac{\text{Cov}(X,Y)}
> {\sqrt{\text{Var}(X)}\sqrt{\text{Var}(Y)}}
> $$
>
> Proprietà:
>
> $$
> -1 \le \rho(X,Y) \le 1
> $$
>
> $$
> \rho(X,Y)=0
> \quad\Longleftrightarrow\quad
> X,Y \text{ scorrelate}
> $$
>
> Per trasformazioni lineari:
>
> $$
> \rho(aX+b,\; rY+s)
> = \frac{ar}{|a||r|}
> \rho(X,Y)
> $$
>
> quindi:
>
> $$
> ar>0
> \;\Longrightarrow\;
> \rho(aX+b,\; rY+s)=\rho(X,Y)
> $$
>
> $$
> ar<0
> \;\Longrightarrow\;
> \rho(aX+b,\; rY+s)=-\rho(X,Y)
> $$
>
> **Regola pratica**
>
> $$
> \text{Indipendenza}
> \;\Rightarrow\;
> \text{Cov}=0
> \;\Rightarrow\;
> \rho=0
> $$
>
> ma
>
> $$
> \rho=0
> \;\not\Rightarrow\;
> \text{Indipendenza}.
> $$

<div style="page-break-after: always;"></div>