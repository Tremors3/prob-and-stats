## $$ \textcolor{red}{\text{Esercizi Lez. 8 - Ex 7}} $$

#### Esercizio 1

Certe particelle, usate come catalizzatori di un processo, hanno masse comprese tra 10 e 70 $\mu g$. Sia $X$ la massa di una particella. $X$ ha densità di probabilità

$$
f(x) = \begin{cases}
\frac{x-10}{1800} & 10<x<70 \\
0 & \text{altrove}
\end{cases}
$$

Trova:
- (a) la proporzione di particelle che hanno massa inferiore a 50.
- (b) la funzione ripartizione di $X$.
- (c) la mediana di $X$.

##### Risoluzione

- **(a)** Calcoliamo la proporzione di particelle che hanno massa inferiore a 50. Si tratta della seguente probabilità:

    $$\begin{aligned}
    P(X \le 50) = F(50)
    &= \int_{-\infty}^{50} f(x)\cdot dx
    \\&= \int_{10}^{50} \frac{x-10}{1800}\cdot dx 
    \\&= \frac1{1800}\int_{10}^{50} x\cdot dx - \frac{10}{1800}\int_{10}^{50} dx 
    \\&= \frac1{1800}\left[\frac{x^2}{2}\right]_{10}^{50} - \frac{10}{1800}(50-10) 
    \\&= \frac23 - \frac29 = \frac49 \approx \boxed{0.4444} \;.
    \end{aligned}$$

- **(b)** Calcoliamo la funzione ripartizione (distribuzione) di $X$.

    - Caso $x<10$:

        $$
        F(x) = 0
        $$

    - Caso $x>70$:

        $$
        F(x) = 1
        $$

    - Caso $10\le x\le70$:

        $$\begin{aligned}
        F(x) &= \int_{-\infty}^x f(y)\cdot dy
        \\&= \int_{10}^x \frac{y-10}{1800}\cdot dy
        \\&= \frac1{1800}\int_{10}^x (y - 10)\cdot dy
        \\&= \frac1{1800}\left[ \frac{(y-10)^2}{2} \right]_{10}^x
        \\&= \frac1{3600}(x-10)^2
        \end{aligned}$$

    La funzione di ripartizione completa è quindi

    $$\boxed{
    F(x) = \begin{cases}
    0 & x<10 \\
    \frac1{3600}(x-10)^2 & 10\le x\le70 \\
    1 & x>70
    \end{cases}
    } \;.$$

- **(c)** La mediana di $X$ corrisponde al quantile di livello $0.5$, quindi devo trovare il valore $x$ tale che:

    $$
    F(x) = 0.5
    $$

    Utilizziamo la funzione di ripartizione ottenuta al punto (b) e la imponiamo uguale a $0.5$

    $$
    \frac1{3600}(x-10)^2 = 0.5
    $$

    Troviamo le due soluzioni:

    $$\begin{aligned}
    (x-10)^2 &= 1800 \\
    x-10 &= \pm\sqrt{1800} \\
    x &= 10 \pm\sqrt{1800}
    \end{aligned}$$

    $$
    x = -32.43 \qquad\text{e}\qquad x = 52.43
    $$

    La mediana è la soluzione che appartiene al supporto della densità $[10, 70]$, cioè $\boxed{x = 52.43}\;.$

---

#### Esercizio 2

Per le nevicate in una certa regione, il numero $X$ di cm di neve è una v.a. con densità di probabilità del tipo:

$$
f(x) = \begin{cases}
cx & 0\le x\le5 \\
-c(x-10) & 5<x\le 10 \\
0 & \text{altrove}
\end{cases}
$$

Trova:

(a) il fattore $c$ di normalizzazione;
(b) la funzione di ripartizione di $X$;
(c) il $40-$mo percentile di $X$.

##### Risoluzione

- **(a)** Per trovare il fattore di normalizzazione $c$, imponiamo che la probabilità totale sia uguale a 1:

    $$
    \int_{-\infty}^{+\infty} f(x)\cdot dx = 1
    $$

    Dato che la densità è diversa da zero solo negli intervalli $[0,5]$ e $(5,10]$, otteniamo:

    $$
    \int_0^5 cx\cdot dx \quad+\quad \int_5^{10} -c(x-10)\cdot dx = 1
    $$

    Calcoliamo il primo integrale:

    $$
    \int_0^5 cx\cdot dx = c\int_0^5 x\cdot dx = c\left[\frac{x^2}2\right]_0^5 = \frac{25}2c
    $$

    Calcoliamo il secondo integrale:

    $$\begin{aligned}
    \int_5^{10} -c(x-10)\cdot dx
    &= -c \int_5^{10} (x-10) \cdot dx \\
    &= -c\left[\frac{(x-10)^2}2\right]_5^{10} \\
    &= -c\left(0-\frac{25}2\right) = \frac{25}2c
    \end{aligned}$$

    Sommiamo i due contributi:

    $$
    \frac{25}2c + \frac{25}2c = 1
    \quad\Rightarrow\quad 25c = 1
    \quad\Rightarrow\quad \boxed{c = \frac1{25}} \;.
    $$

    Riscriviamo quindi la densità di probabilità sostituendo $c=\frac1{25}$:

    $$\boxed{
    f(x) = \begin{cases}
    \frac{1}{25}x & 0\le x\le5 \\
    -\frac{1}{25}(x-10) & 5<x\le 10 \\
    0 & \text{altrove}
    \end{cases}
    } \;.$$

- **(b)** Calcoliamo la funzione di ripartizione di $X$.

    - Caso $0\le x\le5$:

        $$\begin{aligned}
        F(x) &= \int_0^x \frac1{25}y\cdot dy \\
        &= \frac1{25}\left[\frac{y^2}2\right]_0^x
        = \frac1{50}x^2
        \end{aligned}$$

    - Caso $5\le x\le10$:

        $$\begin{aligned}
        F(x) &= \int_0^5 \frac1{25}y\cdot dy \space+\space \int_5^x -\frac{1}{25}(y-10)\cdot dy
        \end{aligned}$$

        Calcoliamo il primo integrale:

        $$\begin{aligned}
        \int_0^5 \frac1{25}y\cdot dy
        = \frac1{25}\left[\frac{y^2}2\right]_0^5
        = \frac12
        \end{aligned}$$

        Calcoliamo il secondo integrale:

        $$\begin{aligned}
        \int_5^x -\frac{1}{25}(y-10)\cdot dy &= -\frac1{25}\left[\frac{(y-10)^2}2\right]_5^x \\
        &= -\frac1{50}(x-10)^2 + \frac12
        \end{aligned}$$

        Sommiamo le due componenti:

        $$\begin{aligned}
        F(x) &= \frac12 - \frac1{50}(x-10)^2 + \frac12 \\
        &= 1 - \frac1{50}(x-10)^2
        \end{aligned}$$

    La funzione di ripartizione completa è quindi

    $$\boxed{
    F(x) = \begin{cases}
    0 & x\le 0 \\
    \frac1{50}x^2 & 0\le x\le5 \\
    1 - \frac1{50}(x-10)^2 & 5\le x\le 10 \\
    1 & x\ge 10
    \end{cases}
    } \;.$$

- **(c)** il $40-$mo percentile di $X$. Corrisponde al valore dell'ascissa $x$ tale che:

    $$
    F(x) = 0.40
    $$

    Utilizziamo la funzione di ripartizione ottenuta al punto (b). In particolare usiamo la funzione di ripartizione definita nell'intervallo $0\le x\le 5$:

    $$\begin{aligned}
    \frac1{50}x^2 &= 0.40 \\
    x^2 &= 20 \\
    x &= \pm\sqrt{20}
    \end{aligned}$$

    $$
    x \approx -4.47 \qquad\text{e}\qquad x \approx 4.47
    $$

    Il quantile di livello $0.40$ è la soluzione che appartiene al supporto della densità $[0, 10]$, cioè $\boxed{x = 4.47}\;.$

---

#### Esercizio 3

Data la densità di $X$

$$
f(x) = \begin{cases}
1+x & -1\le x<0 \\
1-x & 0\le x<1 \\
0 & \text{altrove}
\end{cases}
$$

calcolare:
- (a) $P(X > 0.6)$;
- (b) la funzione distribuzione $F(x)$;

##### Risoluzione

- **(a)** Calcolare $P(X > 0.6)$. Ci sono due strate che possiamo scegliere:

    - **Prima strada** (diretta):

        $$\begin{aligned}
        P(X > 0.6) &= \int_{0.6}^1 (1-y)\cdot dy
        = \int_{0.6}^1 -(y-1)\cdot dy \\
        &= -\left[\frac{(y-1)^2}2\right]_{0.6}^1
        = 0-\frac{(-0.4)^2}2 = \boxed{0.08} \;.
        \end{aligned}$$

    - **Seconda strada** (più lunga):

        $$
        P(X > 0.6) = 1 - P(X < 0.6) = 1 - F(0.6)
        $$

        In questo caso è richiesto il calcolo della funzione di distribuzione. Una volta calcolata al punto (b) possiamo risolvere:

        $$\begin{aligned}
        P(X > 0.6) = 1 - F(0.6) &= 1 - \frac12 + 0.6 - \frac{(0.6)^2}2 \\ &= 1 - 0.92 = \boxed{0.08} \;.
        \end{aligned}$$

- **(b)** Calcolare la funzione distribuzione $F(x)$:

    - Caso $-1\le x<0$:

        $$\begin{aligned}
        F(x) &= \int_{-1}^x (1+y)\cdot dy \\
        &= \left[\frac{(1+y)^2}2\right]_{-1}^x
        = \frac{(1+x)^2}2 \\
        &= \frac12 + x + \frac{x^2}2
        \end{aligned}$$

    - Caso $0\le x<1$:

        $$\begin{aligned}
        F(x) &= \int_{-1}^0 (1+y)\cdot dy
        \quad+\quad
        \int_0^x (1-y)\cdot dy \\
        \end{aligned}$$

        Calcolo il primo integrale:

        $$
        \int_{-1}^0 (1+y)\cdot dy
        = \left[\frac{(1+y)^2}2\right]_{-1}^0
        = \frac12
        $$

        Calcoliamo il secondo integrale:

        $$
        \begin{aligned}
        \int_0^x (1-y)\cdot dy
        &= \int_0^x -(y-1)\cdot dy \\
        &= -\left[\frac{(y-1)^2}2\right]_0^x \\
        &= -\left(
        \frac{(x-1)^2}2 - \frac12
        \right) \\
        &= -\frac{(x-1)^2}2 + \frac12
        \end{aligned}
        $$

        Sommiamo le due componenti:

        $$\begin{aligned}
        F(x) &= \frac12 - \frac{(x-1)^2}2 + \frac12 \\
        &= 1 - \frac{(x-1)^2}2 \\
        &= 1 - \frac12(x^2-2x+1) \\
        &= \frac12 + x - \frac{x^2}2
        \end{aligned}$$

    La funzione di ripartizione completa è quindi:

    $$\boxed{
    F(x) = \begin{cases}
    0 & x<-1 \\
    \frac12 + x + \frac{x^2}2 & -1\le x<0 \\
    \frac12 + x - \frac{x^2}2 & 0\le x<1 \\
    1 & x\ge 1
    \end{cases}
    } \;.$$

---

#### Esercizio 4

Sia $X$ una v.a. (assolutamente) continua con densità di probabilità

$$
f(x) = \begin{cases}
\frac54(1-x^4) & 0<x<1 \\
0 & \text{altrove}
\end{cases}
$$

trova:
(a) $P(X > 0.8)$;
(b) la funzione distribuzione $F(x)$.

##### Risoluzione

- **(a)** Calcolare $P(X > 0.8)$. Ci sono due strate che possiamo scegliere:

    - **Prima strada** (diretta):

        $$\begin{aligned}
        P(X>0.8) &= \int_{0.8}^1 \frac54(1-y^4)\cdot dy \\
        &= \frac54\left[y-\frac{y^5}5\right]_{0.8}^1 \\
        &= \frac54\left( 1-\frac15 - 0.8 + \frac{(0.8)^5}5 \right) \\
        &= \boxed{0.08192} \;.
        \end{aligned}$$

    - **Seconda strada** (più lunga):

        $$
        P(X > 0.8) = 1 - P(X < 0.8) = 1 - F(0.8)
        $$

        In questo caso è richiesto il calcolo della funzione di distribuzione. Una volta calcolata al punto (b) possiamo risolvere:

        $$\begin{aligned}
        P(X > 0.8) = 1 - F(0.8) &= 1 - \frac54\left(0.8-\frac{0.8^5}5\right) \\ &= 1 - 0.91808 = \boxed{0.08192} \;.
        \end{aligned}$$

- **(b)** Calcolare la funzione distribuzione $F(x)$:

    - Caso $0\le x<1$:

        $$\begin{aligned}
        F(x) = \int_0^x \frac54(1-y^4)\cdot dy
        = \frac54\left[ y - \frac{y^5}5 \right]_0^x
        = \frac54\left(x-\frac{x^5}5\right)
        \end{aligned}$$

    La funzione di ripartizione completa è quindi:

    $$\boxed{
    F(x) = \begin{cases}
    0 & x<0 \\
    \frac54\left(x-\frac{x^5}5\right) & 0\le x<1 \\
    1 & x\ge 1
    \end{cases}
    } \;.$$

---

> ### Funzione di ripartizione e intervalli separati
>
> **Nota.** Può capitare che la densità di probabilità di una variabile aleatoria sia definita su intervalli separati tra loro. In tali casi, negli intervalli in cui la densità vale $0$, la funzione di ripartizione rimane costante.
>
> Questo accade perché, se $f(x)=0$ in un certo intervallo, non viene accumulata nuova probabilità.
>
> Ad esempio, se:
>
> $$
> f(x)=\begin{cases}
> f_1(x) & -3\le x\le-2 \\
> 0 & -2<x<2 \\
> f_2(x) & 2\le x\le3
> \end{cases}
> $$
>
> allora la funzione di ripartizione:
>
> $$
> F(x)=\int_{-\infty}^{x} f(y)\,dy
> $$
>
> cresce nel primo intervallo $[-3,-2]$, rimane costante nell'intervallo $(-2,2)$ e ricomincia a crescere nell'intervallo $[2,3]$.
>
> In particolare:
>
> $$
> F(x)=F(-2)
> \qquad\text{per } -2<x<2
> $$
>
> perché in quell'intervallo la densità è nulla e quindi non si accumula ulteriore probabilità.

> **Nota.** Se una variabile aleatoria è assolutamente continua e si conosce la funzione di ripartizione $F(x)$, allora la densità di probabilità si ottiene derivando $F(x)$:
>
> $$f(x)=F'(x)$$
>
> Se $F(x)$ è definita a tratti, la derivata va calcolata separatamente in ciascun intervallo.

---

> ### Trovare il fattore $\mathbf c$ di normalizzazione
>
> **Nota.** Per trovare il fattore di normalizzazione $c$ di una densità di probabilità si impone sempre che la probabilità totale sia uguale a $1$:
>
> $$
> \int_{-\infty}^{+\infty} f(x)\,dx = 1
> $$
>
> Esistono però due casi comuni.
>
> ---
>
> #### Caso 1 — $f(x)=c\cdot g(x)$
>
> Se la costante $c$ può essere raccolta direttamente dalla densità, allora:
>
> $$
> \int_{-\infty}^{+\infty} c\,g(x)\,dx = 1
> $$
>
> e quindi:
>
> $$
> c\int_{-\infty}^{+\infty} g(x)\,dx = 1
> $$
>
> Da cui:
>
> $$
> c =
> \frac{1}{
> \int_{-\infty}^{+\infty} g(x)\,dx
> }
> $$
>
> ---
>
> #### Caso 2 — densità definita a tratti
>
> Se la densità è definita su più intervalli e $c$ non è immediatamente estraibile in un'unica forma, allora bisogna sommare i contributi di tutti gli intervalli:
>
> $$
> \int_{a_1}^{b_1} f_1(x)\,dx +
> \int_{a_2}^{b_2} f_2(x)\,dx + \dots = 1
> $$
>
> Si calcolano quindi separatamente gli integrali e si sostituiscono i risultati nell'equazione precedente. In questo modo si ottiene un'equazione contenente $c$, che può essere risolta normalmente.
>
> Ad esempio:
>
> $$
> \frac{25}{2}c + \frac{25}{2}c = 1
> \quad\Rightarrow\quad 25c = 1
> \quad\Rightarrow\quad c=\frac1{25} 
> $$
> 

---

> ### Calcolo della funzione di ripartizione
>
> **Nota.** Quando si calcola la funzione di ripartizione di una variabile aleatoria assolutamente continua, bisogna sempre accumulare tutta la probabilità fino al punto $x$:
>
> $$
> F(x)=\int_{-\infty}^{x} f(y)\,dy
> $$
>
> Se la densità è definita a tratti, allora nel calcolo di $F(x)$ occorre sommare anche i contributi degli intervalli precedenti. Ad esempio, se:
>
> $$
> f(x)=\begin{cases}
> f_1(x) & a\le x\le b \\
> f_2(x) & b\le x\le c
> \end{cases}
> $$
>
> allora, per $b\le x\le c$,
>
> $$
> F(x) = \int_a^b f_1(y)\,dy + \int_b^x f_2(y)\,dy
> $$
>
> perché la funzione di ripartizione rappresenta sempre la probabilità totale accumulata fino a $x$.

---