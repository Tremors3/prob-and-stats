## $$ \textcolor{red}{\text{Esercizi Lez. 7 - Ex 10}} $$

#### Esercizio 1

Un corpo ha 5000 atomi di una sostanza radioattiva. Ogni atomo decade in un minuto con probabilità $0.0004$. Sia $X$ il numero di atomi che decadono in un minuto. Trovare la probabilità che decadano almeno 3 atomi.

##### Risoluzione

Definiamo la variabile aleatoria

$$
X=\{\text{numero di atomi che decadono in un minuto}\}.
$$

Ogni atomo decade indipendentemente dagli altri con probabilità

$$
p=0.0004.
$$

Poiché il numero di atomi è molto grande ($n=5000$) e la probabilità di decadimento è molto piccola, possiamo approssimare la distribuzione binomiale con una distribuzione di Poisson di parametro

$$
\mu=np=5000\cdot0.0004=2.
$$

Quindi

$$
X\sim\mathrm{Pois}(2).
$$

> Ricordiamo che la funzione di probabilità della distribuzione di Poisson è
> 
> $$ p_X(k)=P(X=k)=e^{-\mu}\frac{\mu^k}{k!} $$

Nel nostro caso:

$$
p_X(k)=e^{-2}\frac{2^k}{k!}.
$$

Calcoliamo le probabilità necessarie:

$$\begin{aligned}
P(X=0)
&=e^{-2}\frac{2^0}{0!}
=e^{-2}
\approx 0.1353,
\\[4pt]
P(X=1)
&=e^{-2}\frac{2^1}{1!}
=2e^{-2}
\approx 0.2707,
\\[4pt]
P(X=2)
&=e^{-2}\frac{2^2}{2!}
=2e^{-2}
\approx 0.2707.
\end{aligned}$$

Dobbiamo trovare la probabilità che decadano **almeno 3 atomi**, cioè

$$\begin{aligned}
P(X\ge 3)
&=1-P(X\le 2) \\
&=1-\bigl(P(X=0)+P(X=1)+P(X=2)\bigr) \\
&=1-(0.1353+0.2707+0.2707) \\
&\approx \boxed{0.3233}.
\end{aligned}$$

Quindi la probabilità che in un minuto decadano almeno 3 atomi è

$$
\boxed{P(X\ge 3)\approx 0.3233}.
$$

> **Nota.** In alternativa all’approssimazione di Poisson, era possibile modellare direttamente il problema con una distribuzione binomiale:
>
> $$ X \sim \mathrm{Bin}(n=5000,\; p=0.0004) $$
>
> In questo caso la probabilità richiesta si calcola come
>
> $$ P(X \ge 3)=1-\bigl(P(X=0)+P(X=1)+P(X=2)\bigr) $$
>
> usando la formula binomiale.
>
> Tuttavia, dato che $n$ è molto grande e $p$ molto piccolo, l’approssimazione di Poisson con parametro $\mu=np=2$ è spesso preferita perché semplifica i calcoli mantenendo un’ottima accuratezza.

---

<div style="page-break-after: always;"></div>

#### Esercizio 2

Il numero medio di nascite all’anno in un paese è 7. Trova:
- (a) la probabilità di avere esattamente 6 neonati;
- (b) la probabilità condizionata di avere 6 neonati sapendo che il numero di nascite è almeno 4.

##### Risoluzione

Definiamo la variabile aleatoria

$$
X=\{\text{numero di neonati nati nel corso di un anno}\}.
$$

Il problema fornisce direttamente il valore medio:

$$
\mu = 7 \text{ nascite/anno}
$$

Assumiamo quindi un modello di Poisson:

$$
X \sim \mathrm{Pois}(7).
$$

> Ricordiamo la funzione di probabilità della Poisson:
> 
> $$ P(X=k)=e^{-\mu}\frac{\mu^k}{k!} $$

Nel nostro caso:

$$
P(X=k)=e^{-7}\frac{7^k}{k!}.
$$

- **(a)** Probabilità "di avere esattamente 6 nascite":

$$\begin{aligned}
P(X=6)
&= e^{-7}\frac{7^6}{6!}
\approx \boxed{0.1490} \;.
\end{aligned}$$

- **(b)** Probabilità condizionata "di avere 6 neonati sapendo che essi sono almeno 4":

    $$
    P(X=6 \mid X \ge 4)
    $$

    Per definizione:

    $$
    P(X=6 \mid X \ge 4)=\frac{P(X\ge4\mid X=6)P(X=6)}{P(X \ge 4)}.
    $$

    La probabilità di avere almeno quattro neonati quando se ne hanno esattamente sei è 1. Cioè l’evento \(X=6\) implica automaticamente \(X \ge 4\), allora:

    $$
    P(X\ge4\mid X=6) = 1
    $$

    Quindi:

    $$
    P(X=6 \mid X \ge 4)=\frac{1\cdot P(X=6)}{P(X \ge 4)}.
    $$

    - Calcoliamo \(P(X \ge 4)\) tramite complemento:

        $$\begin{aligned}
        P(X \ge 4)
        &= 1 - P(X \le 3) \\
        &= 1 - \bigl(P(0)+P(1)+P(2)+P(3)\bigr).
        \end{aligned}$$

        Calcoliamo i singoli termini:

        $$\begin{aligned}
        P(0) &= e^{-7}\frac{7^0}{0!} \approx 0.000911 \\
        P(1) &= e^{-7}\frac{7^1}{1!} \approx 0.006338 \\
        P(2) &= e^{-7}\frac{7^2}{2!} \approx 0.022183 \\
        P(3) &= e^{-7}\frac{7^3}{3!} \approx 0.051753
        \end{aligned}$$

        Quindi:

        $$\begin{aligned}
        P(X \ge 4)
        &\approx 1 - (0.000911 + 0.006338 + 0.022183 + 0.051753) \\
        &= 1 - 0.081185 \\
        &= 0.918815.
        \end{aligned}$$

    Infine calcoliamo la probabilità richiesta:

    $$\begin{aligned}
    P(X=6 \mid X \ge 4)
    &= \frac{0.1490}{0.918815}
    \approx \boxed{0.1622}.
    \end{aligned}$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 3

Un'assicurazione ha 1000 assicurati contro un sinistro che ha probabilità $0.006$ di verificarsi, per ogni persona in un anno.

- (a) Trova la probabilità che si verifichino almeno 5 sinistri.
- (b) Detto $X$ il numero dei sinistri in un anno, se ognuno dei mille assicurati paga un premio di 100 euro, e l’assicurazione deve pagare 9000 euro per ogni sinistro, trova la media e la deviazione standard del beneficio annuale della compagnia

$$
Y = 1000\cdot100 - 9000X.
$$

##### Risoluzione

Definiamo la variabile aleatoria

$$
X=\{\text{numero di sinistri che si verificano durante l'anno}\}.
$$

- **(a)** Calcolare la probabilità che si verifichino almeno 5 sinistri.

    Vogliamo determinare

    $$
    P(X\ge 5)=1-P(X\le 4).
    $$

    Si possono seguire due approcci.

    1. **Modello Binomiale (esatto)**

        Ogni assicurato può avere oppure non avere un sinistro durante l'anno, indipendentemente dagli altri. Pertanto:

        $$
        X\sim\mathrm{Bin}(1000,0.006).
        $$

        In linea teorica si potrebbe calcolare

        $$
        P(X\ge5)=1-P(X\in\{0,1,2,3,4\}).
        $$

        Tuttavia i coefficienti binomiali coinvolti sono molto grandi e i calcoli risultano poco pratici.

    2. **Approssimazione di Poisson**

        Poiché il numero di prove è molto grande ($n=1000$) e la probabilità di successo è molto piccola ($p=0.006$), possiamo approssimare la binomiale con una Poisson di parametro

        $$
        \mu=np=1000\cdot0.006=6.
        $$

        Quindi:

        $$
        X\sim\mathrm{Pois}(6).
        $$

        > Ricordiamo che la funzione di probabilità della Poisson è
        > 
        > $$ P(X=k)=e^{-\mu}\frac{\mu^k}{k!} $$

        Nel nostro caso:

        $$
        P(X=k)=e^{-6}\frac{6^k}{k!}.
        $$

        Calcoliamo le probabilità necessarie:

        $$\begin{aligned}
        P(X=0) &= e^{-6}\frac{6^0}{0!} \approx 0.002478 \\
        P(X=1) &= e^{-6}\frac{6^1}{1!} \approx 0.014873 \\
        P(X=2) &= e^{-6}\frac{6^2}{2!} \approx 0.044618 \\
        P(X=3) &= e^{-6}\frac{6^3}{3!} \approx 0.089235 \\
        P(X=4) &= e^{-6}\frac{6^4}{4!} \approx 0.133853
        \end{aligned}$$

        Pertanto:

        $$\begin{aligned}
        P(X\ge5)
        &= 1-P(X\le4) \\
        &= 1-\bigl(P(X=0)+P(X=1)+P(X=2)+P(X=3)+P(X=4)\bigr) \\
        &\approx 1-(0.002478+0.014873+0.044618+0.089235+0.133853) \\
        &\approx 1-0.285057 \\
        &\approx \boxed{0.7149}.
        \end{aligned}$$

- **(b)** Calcolare la media e la deviazione standard del beneficio annuale

    $$
    Y=1000\cdot100-9000X.
    $$

    > **Nota.** Per risolvere questo punto occorre conoscere le proprietà dell'aspettazione e della varianza delle trasformazioni lineari di una variabile aleatoria (capitoli 10,11 della teoria).

    - Calcolo della media $\mu_Y=E[Y]$.

        $$\begin{aligned}
        E[Y]
        &= E[1000\cdot100-9000X] \\
        &= 100000-9000E[X].
        \end{aligned}$$

        Per una variabile di Poisson vale:

        $$
        E[X]=\mu=6.
        $$

        Quindi:

        $$\begin{aligned}
        E[Y]
        &=100000-9000\cdot6 \\
        &=100000-54000 \\
        &=\boxed{46000\text{ euro}} \;.
        \end{aligned}$$

    - Calcolo della deviazione standard $\sigma_Y$.

        > Ricordiamo che:
        > 
        > $$ \mathrm{Var}(aX+b)=a^2\mathrm{Var}(X) $$

        Pertanto:

        $$\begin{aligned}
        \mathrm{Var}(Y)
        &=\mathrm{Var}(100000-9000X) \\
        &=(-9000)^2\mathrm{Var}(X).
        \end{aligned}$$

        Per una Poisson vale:

        $$
        \mathrm{Var}(X)=\mu=6.
        $$

        Quindi:

        $$\begin{aligned}
        \mathrm{Var}(Y)
        &=(-9000)^2\cdot6 \\
        &=486\,000\,000.
        \end{aligned}$$

        Infine:

        $$\begin{aligned}
        \sigma_Y
        &=\sqrt{\mathrm{Var}(Y)} \\
        &=\sqrt{486\,000\,000} \\
        &\approx \boxed{22045\text{ euro}}.
        \end{aligned}$$

> **Nota.** Anche se nel punto (a) abbiamo usato la Poisson come approssimazione della Binomiale, nel punto (b) il risultato per media e varianza coincide praticamente con quello ottenuto usando direttamente
>
> $$
> X\sim\mathrm{Bin}(1000,0.006),
> $$
>
> poiché per la Binomiale vale
>
> $$
> E[X]=np=6,
> \qquad
> \mathrm{Var}(X)=np(1-p)=5.964 \approx 6.
> $$

---

<div style="page-break-after: always;"></div>