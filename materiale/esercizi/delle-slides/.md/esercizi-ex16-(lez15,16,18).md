## $$ \textcolor{red}{\text{Esercizi Ex. 16 - Lez. 15,16,18}} $$

#### Esercizio 1

Un componente è composto da due sottocomponenti. La durata $X$ del primo, misurata in ore, è normale di media $900$ e varianza $20000$. La durata $Y$ dell’altro è normale di media $1000$ e varianza $30000$. Le durate sono linearmente correlate, con $\rho = -0.6$.

Trova la probabilità che il secondo duri almeno ($\ge$) $300$ ore più del primo.

##### Risoluzione

Abbiamo le variabili aleatorie:

$$\begin{aligned}
X &\sim N(\mu=900,\; \sigma^2=20000) \\
Y &\sim N(\mu=1000,\; \sigma^2=30000)
\end{aligned}$$

Il coefficiente di correlazione vale $\rho = -0.6$, quindi le due variabili sono negativamente correlate.

La probabilità richiesta è:

$$
P(Y \ge X + 300)
$$

che può essere riscritta come:

$$
P(Y - X \ge 300)
$$

Definiamo una nuova variabile aleatoria:

$$
Z = Y - X
$$

Poiché una combinazione lineare di variabili gaussiane è ancora una variabile gaussiana, possiamo scrivere:

$$
aX + bY + c \sim N\left(a\mu_X + b\mu_Y + c,\; a^2\sigma_X^2 + b^2\sigma_Y^2 + 2ab\,\text{Cov}(X,Y)\right)
$$

Per applicare la formula dobbiamo prima calcolare la covarianza.

Sfruttando la relazione tra correlazione e covarianza:

$$\begin{aligned}
\text{Cov}(X,Y)
&= \rho \sqrt{\sigma_X^2}\sqrt{\sigma_Y^2} \\
&= -0.6 \cdot \sqrt{20000}\cdot\sqrt{30000} \\
&\approx -14696.94
\end{aligned}$$

Calcoliamo ora media e varianza di $Z$.

$$
\mu_Z = E[Z] = E[Y] - E[X] = 1000 - 900 = 100
$$

$$\begin{aligned}
\sigma_Z^2
&= \sigma_Y^2 + (-1)^2\sigma_X^2 + 2\cdot1\cdot(-1)\,\text{Cov}(X,Y) \\
&= 30000 + 20000 - 2(-14696.94) \\
&= 50000 + 29393.88 \\
&= 79393.88
\end{aligned}$$

Pertanto:

$$
Z \sim N(100,\; 79393.88)
$$

La probabilità richiesta diventa:

$$
P(Z \ge 300)
$$

Standardizzando:

$$\begin{aligned}
P(Z \ge 300)
&= 1 - P(Z < 300) \\
&= 1 - \Phi\left(\frac{300 - 100}{\sqrt{79393.88}}\right) \\
&\approx 1 - \Phi(0.71) \\
&\approx 1 - 0.76115 \\
&= \boxed{0.23885} \;.
\end{aligned}$$

<div style="page-break-after: always;"></div>

> **Nota.**
>
> Se $X$ e $Y$ sono variabili aleatorie gaussiane congiunte, allora ogni loro combinazione lineare è ancora una variabile gaussiana:
>
> $$
> aX + bY + c \sim N\left(a\mu_X + b\mu_Y + c,\; a^2\sigma_X^2 + b^2\sigma_Y^2 + 2ab\,\text{Cov}(X,Y)\right)
> $$
>
> La covarianza può essere ricavata dal coefficiente di correlazione:
>
> $$
> \text{Cov}(X,Y)
> = \rho\,\sqrt{\sigma_X^2}\sqrt{\sigma_Y^2}
> = \rho\,\sigma_X\sigma_Y
> $$
>
> In particolare:
>
> $$
> E(aX+bY+c)
> = aE(X)+bE(Y)+c
> $$
>
> $$
> \mathrm{Var}(aX+bY)
> = a^2\mathrm{Var}(X)+b^2\mathrm{Var}(Y)+2ab\,\mathrm{Cov}(X,Y)
> $$
>
> Una volta ottenuta la nuova variabile gaussiana, la probabilità richiesta si calcola tramite standardizzazione:
>
> $$
> Z = \frac{X-\mu}{\sigma}
> $$
>
> e quindi utilizzando la funzione di ripartizione della normale standard:
>
> $$
> P(X \le x)
> = \Phi\!\left(\frac{x-\mu}{\sigma}\right)
> $$
>
> $$
> P(X \ge x)
> = 1-\Phi\!\left(\frac{x-\mu}{\sigma}\right)
> $$
>
> In questo esercizio è conveniente definire:
>
> $$
> Z = Y - X
> $$
>
> nella probabilità equivalente
>
> $$
> P(Z \ge 300)
> $$
>
> che può essere calcolata direttamente sulla nuova distribuzione normale.

---

<div style="page-break-after: always;"></div>

#### Esercizio 2

Due atleti arrivano al traguardo di una corsa in istanti $X$, $Y$ indipendenti. L’uno arriva in un istante casuale $X$ fra le $16$ e le $17$. L’altro arriva in un istante casuale $Y$ fra le $15.30$ e le $17$.

Trova:
- (a) la probabilità che sia $Y \ge X$
- (b) la probabilità che sia $Y \le X + 15$ minuti

##### Risoluzione

Modelliamo le variabili aleatorie come distribuzioni uniformi indipendenti:

$$
X \sim U(16,17)
\qquad
Y \sim U(15.5,17)
$$

Le rispettive densità sono:

$$
f_X(x)
= \frac{1}{17-16}
= 1
\qquad
16 \le x \le 17
$$

$$
f_Y(y)
= \frac{1}{17-15.5}
= \frac{2}{3}
\qquad
15.5 \le y \le 17
$$

Poiché $X$ e $Y$ sono indipendenti, la densità congiunta è:

$$
f_{X,Y}(x,y)
= f_X(x)f_Y(y)
= \frac{2}{3}
$$

per

$$
16 \le x \le 17,
\qquad
15.5 \le y \le 17
$$

<div style="page-break-after: always;"></div>

- **(a) Calcolare la probabilità che sia $Y \ge X$.**

    La probabilità richiesta è:

    $$
    P(Y \ge X)
    $$

    Integrando la densità congiunta sulla regione definita da $y \ge x$:

    $$\begin{aligned}
    P(Y \ge X)
    &=
    \int_{16}^{17}
    \int_x^{17}
    f_{X,Y}(x,y)
    \,dy\,dx \\
    &=
    \int_{16}^{17}
    \int_x^{17}
    \frac23
    \,dy\,dx \\
    &=
    \int_{16}^{17}
    \frac23(17-x)
    \,dx \\
    &=
    \frac23
    \int_{16}^{17}
    (17-x)
    \,dx \\
    &=
    \frac23
    \left[
    17x-\frac{x^2}{2}
    \right]_{16}^{17} \\
    &=
    \frac23
    \left(
    \frac{289}{2}-144
    \right) \\
    &=
    \frac23\cdot\frac12 \\
    &=
    \boxed{\frac23}
    \;\approx\;
    0.6667
    \;.
    \end{aligned}$$

<div style="page-break-after: always;"></div>

- **(b) Calcolare la probabilità che sia $Y \le X + 15$ minuti.**

    Poiché $15$ minuti corrispondono a:

    $$
    \frac{15}{60}=0.25
    $$

    la probabilità richiesta è:

    $$
    P(Y \le X+0.25)
    $$

    Integrando la densità congiunta sulla regione definita da $y \le x+0.25$:

    $$\begin{aligned}
    P(Y \le X+0.25)
    &=
    \int_{16}^{17}
    \int_{15.5}^{x+0.25}
    f_{X,Y}(x,y)
    \,dy\,dx \\
    &=
    \int_{16}^{17}
    \int_{15.5}^{x+0.25}
    \frac23
    \,dy\,dx \\
    &=
    \int_{16}^{17}
    \frac23
    \Bigl((x+0.25)-15.5\Bigr)
    \,dx \\
    &=
    \frac23
    \int_{16}^{17}
    (x-15.25)
    \,dx \\
    &=
    \frac23
    \left[
    \frac{x^2}{2}-15.25x
    \right]_{16}^{17} \\
    &=
    \frac23
    (1.40625) \\
    &=
    0.9375 \\
    &=
    \boxed{\frac{15}{16}}
    \;.
    \end{aligned}$$

<div style="page-break-after: always;"></div>

> **Nota.**
>
> Se $X$ e $Y$ sono variabili aleatorie continue indipendenti con densità $f_X$ e $f_Y$, allora la densità congiunta è:
>
> $$
> f_{X,Y}(x,y)=f_X(x)\,f_Y(y)
> $$
>
> La probabilità di un evento descritto da una regione $A$ del piano $(x,y)$ si ottiene integrando la densità congiunta su tale regione:
>
> $$
> P((X,Y)\in A)
> = \iint_A f_{X,Y}(x,y)\,dx\,dy
> $$
>
> Il procedimento generale è:
>
> 1. determinare il supporto delle variabili
> 2. calcolare la densità congiunta
> 3. individuare la regione che soddisfa la condizione richiesta
> 4. impostare e calcolare l'integrale doppio sulla regione favorevole

---

<div style="page-break-after: always;"></div>

#### Esercizio 3

Un componente elettronico è formato da due elementi in serie (cioè non funziona se almeno uno dei due non funziona), il primo dei quali ha un tempo di vita distribuito esponenzialmente con parametro $1/2$. Il secondo elemento è a sua volta formato da due elementi in parallelo (cioè non funziona se ambedue non funzionano), aventi tempo di vita esponenziale rispettivamente con parametro $5/2$ e $7/2$. Si suppone l’indipendenza.

Sia $U$ il tempo di vita globale. Trova la funzione di distribuzione di $U$.

##### Risoluzione

**Variabili aleatorie**

$$
X \sim \text{Exp}\left(\frac12\right),
\qquad
Y \sim \text{Exp}\left(\frac52\right),
\qquad
Z \sim \text{Exp}\left(\frac72\right)
$$

Il sistema è composto da:

- un elemento in serie con durata $X$
- un blocco in parallelo formato da $Y$ e $Z$

**Struttura del sistema**

Nel blocco in parallelo il sistema funziona finché almeno uno dei due elementi funziona, quindi il tempo di vita del blocco è:

$$
V = \max(Y,Z)
$$

Il sistema totale è in serie tra $X$ e $V$, quindi si guasta quando si guasta il primo dei due:

$$
U = \min(X,V)
$$

**Funzione di distribuzione**

Calcoliamo la funzione di distribuzione tramite la funzione di sopravvivenza:

$$
F_U(u) = P(U \le u) = 1 - P(U > u)
$$

<div style="page-break-after: always;"></div>

Per avere $U > u$ devono essere verificate entrambe le condizioni:

$$
X > u,
\qquad
V > u
$$

quindi:

$$
P(U>u) = P(X>u)\,P(V>u)
$$

per indipendenza.

**Calcolo dei singoli termini**

Per la variabile esponenziale:

$$
P(X>u) = e^{-\frac12 u}
$$

Per il blocco in parallelo:

$$
P(V \le u) = P(Y \le u,\; Z \le u)
$$

per indipendenza:

$$
P(V \le u) = P(Y \le u)\,P(Z \le u)
$$

quindi:

$$
P(V>u) = 1 - (1 - e^{-\frac52 u})(1 - e^{-\frac72 u})
$$

**Sopravvivenza del sistema**

$$\begin{aligned}
P(U>u)
&= e^{-\frac12 u}
\left[
1 - (1 - e^{-\frac52 u})(1 - e^{-\frac72 u})
\right]
\end{aligned}$$

**Sviluppo del termine nel parallelo**

$$\begin{aligned}
(1 - e^{-\frac52 t})(1 - e^{-\frac72 t})
&= 1 - e^{-\frac52 t} - e^{-\frac72 t} + e^{-6t}
\end{aligned}$$

$$\begin{aligned}
1 - (1 - e^{-\frac52 t} - e^{-\frac72 t} + e^{-6t})
&= e^{-\frac52 t} + e^{-\frac72 t} - e^{-6t}
\end{aligned}$$

**Moltiplicazione con il ramo in serie**

$$\begin{aligned}
e^{-\frac12 t}
\left(
e^{-\frac52 t} + e^{-\frac72 t} - e^{-6t}
\right)
&= e^{-3t} + e^{-4t} - e^{-\frac{13}{2}t}
\end{aligned}$$

**Funzione di distribuzione finale**

$$\begin{aligned}
F_U(t)
&= 1 - \left(
e^{-3t} + e^{-4t} - e^{-\frac{13}{2}t}
\right) \\
&= 1 - e^{-3t} - e^{-4t} + e^{-\frac{13}{2}t}
\end{aligned}$$

$$
\boxed{
F_U(t) = 1 - e^{-\frac62t} - e^{-\frac82t} + e^{-\frac{13}2t}
} \;.
$$

---

<div style="page-break-after: always;"></div>