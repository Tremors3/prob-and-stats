## $$ \textcolor{red}{\text{Esercizi Ex. 13 - Lez. 9}} $$

#### Esercizio 1

La durata di un circuito integrato ha una distribuzione esponenziale con media pari a due anni.

- (a) Trova la probabilità che il circuito abbia durata di almeno ($\ge$) 3 anni.
- (b) Dimostra che la probabilità $P(X>7\mid X>4)$ è uguale alla precedente.

##### Risoluzione

Definiamo la variabile aleatoria

$$
X=\{\text{durata di un circuito integrato (in anni)}\}.
$$

Poiché il problema ci dice che la durata segue una distribuzione esponenziale con media pari a 2 anni, ricordiamo che

$$
E[X]=\frac1\lambda
$$

Pertanto

$$
\frac1\lambda=2
\qquad\Longrightarrow\qquad
\lambda=\frac12
$$

La variabile aleatoria è quindi distribuita come

$$
X\sim\text{Exp}\!\left(\lambda=\frac12\right)
$$

> Ricordiamo che:
> 
> $$
> f_X(x)=
> \begin{cases}
> \lambda e^{-\lambda x}, & x\ge0,\\
> 0, & x<0,
> \end{cases}
> $$
> 
> e che la funzione di ripartizione vale
> 
> $$
> F(x)=P(X\le x)=1-e^{-\lambda x},
> \qquad x\ge0
> $$

Nel nostro caso

$$
f_X(x)=\frac12 e^{-x/2},
\qquad
F(x)=1-e^{-x/2}.
$$

- **(a)** Calcoliamo la probabilità che il circuito duri almeno 3 anni:

    $$\begin{aligned}
    P(X\ge3)
    &=1-P(X<3) \\
    &=1-F(3) \\
    &=1-\left(1-e^{-3/2}\right) \\
    &=e^{-3/2} \\
    &\approx \boxed{0.2231}\;.
    \end{aligned}$$

    In alternativa si può integrare direttamente la densità:

    $$\begin{aligned}
    P(X\ge3)
    &=\int_3^{+\infty}\frac12 e^{-x/2}\,dx \\
    &=\left[-e^{-x/2}\right]_3^{+\infty} \\
    &=0-(-e^{-3/2}) \\
    &=e^{-3/2}
    \end{aligned}$$

- **(b)** Dimostriamo che

    $$
    P(X>7\mid X>4)=P(X>3)
    $$

    Per definizione di probabilità condizionata:

    $$\begin{aligned}
    P(X>7\mid X>4)
    &=\frac{P(X>4\mid X>7)P(x>7)}{P(X>4)} \\
    &=\frac{1\cdot P(X>7)}{P(X>4)}
    \end{aligned}$$

    Per una variabile esponenziale vale

    $$
    P(X>t)=e^{-\lambda t}
    $$

    <div style="page-break-after: always;"></div>

    Quindi

    $$\begin{aligned}
    P(X>7\mid X>4)
    &=\frac{e^{-7/2}}{e^{-4/2}} \\
    &=e^{-7/2+2} \\
    &=e^{-3/2} = P(X>3)
    \end{aligned}$$

    Pertanto

    $$\boxed{
    P(X>7\mid X>4)=P(X>3)
    }
    $$

    e abbiamo verificato la proprietà di **assenza di memoria** della distribuzione esponenziale.

> **Nota.** La distribuzione esponenziale gode della proprietà di assenza di memoria:
>
> $$ P(X>s+t\mid X>s)=P(X>t) $$
>
> In altre parole, se il circuito ha già funzionato per $s$ anni, la probabilità che continui a funzionare per altri $t$ anni non dipende dalla sua età attuale. Questa è l'analoga continua della proprietà di assenza di memoria della distribuzione geometrica.

---

<div style="page-break-after: always;"></div>