## $$ \textcolor{red}{\text{Esercizi Lez. 9 - Teoria}} $$

#### Esercizio 1

Sia $X \sim \mathrm{Exp}(2)$. Calcolare $P(X>1)$ e il $40\%$-percentile di $X$.

##### Risoluzione

Per una distribuzione esponenziale di parametro $\lambda = 2$, la funzione di distribuzione è:

$$
F(x)=1-e^{-2x}, \qquad x \ge 0
$$

1. Riscriviamo la probabilità richiesta nel seguente modo:

    $$
    \begin{aligned}
    P(X>1)
    &= 1 - P(X\le 1) \\
    &= 1 - F(1)
    \end{aligned}
    $$

    Calcoliamo quindi il valore della probabilità:

    $$
    \begin{aligned}
    P(X>1)
    &= 1 - \left(1-e^{-2}\right) \\
    &= e^{-2} \\
    &\approx \boxed{0.1353} \;.
    \end{aligned}
    $$

> **Nota**: per una variabile aleatoria esponenziale vale la proprietà:
>
> $$
> P(X>t)=e^{-\lambda t}
> $$

2. Calcoliamo ora il $40\%$-percentile, cioè il valore $q_{0.4}$ tale che:

    $$
    q_{0.4} = x \qquad\text{e}\qquad F(x) = 0.4
    $$

    Sostituendo la funzione di distribuzione:

    $$
    \begin{aligned}
    1-e^{-2x} &= 0.4 \\
    e^{-2x} &= 0.6
    \end{aligned}
    $$

    Applicando il logaritmo naturale:

    $$
    \begin{aligned}
    -2x &= \ln(0.6) \\
    x &= -\frac12 \ln(0.6) \approx \boxed{0.2554} \;.
    \end{aligned}
    $$

---

#### Esercizio 2

Sia $X \sim \Gamma(1,2)$. Calcolare $P(X \in [-2,2])$.

##### Risoluzione

Osserviamo che una distribuzione $\Gamma(1,\lambda)$ coincide con una distribuzione esponenziale di parametro $\lambda$. Pertanto:

$$
\Gamma(1,2) \sim \mathrm{Exp}(2)
$$

La corrispondente funzione di distribuzione è:

$$
F(x)=1-e^{-2x}, \qquad x \ge 0
$$

Riscriviamo la probabilità richiesta:

$$
\begin{aligned}
P(X\in[-2,2])
&= P(X\le 2)-P(X\le -2) \\
&= F(2)-F(-2)
\end{aligned}
$$

Poiché una variabile esponenziale assume soltanto valori non negativi, vale:

$$
F(-2)=0
$$

Quindi:

$$
\begin{aligned}
P(X\in[-2,2])
&= F(2) \\
&= 1-e^{-2\cdot 2} \\
&= 1-e^{-4}
\end{aligned}
$$

Pertanto:

$$
P(X\in[-2,2])=\boxed{1-e^{-4}} \;.
$$

> **Nota**: esiste una relazione analoga tra alcune distribuzioni discrete e continue.
>
> L'esponenziale è l'analogo continuo della geometrica, mentre la gamma è l'analogo continuo della binomiale negativa. In particolare:
>
> $$
> \begin{aligned}
> NB(1,p) &= Geo(p) \\
> \Gamma(1,\lambda) &= \mathrm{Exp}(\lambda)
> \end{aligned}
> $$

---

#### Esercizio 3

Calcolare $\lambda$ tale che la mediana di $X \sim \mathrm{Exp}(\lambda)$ sia uguale a $1$.

##### Risoluzione

La mediana corrisponde al $50\%$-percentile della distribuzione. Pertanto il testo del problema ci dice che:

$$
q_{0.5}=x, \qquad F(x)=0.5, \qquad\text{con }x=1
$$

Per una distribuzione esponenziale di parametro $\lambda$, la funzione di distribuzione è:

$$
F(x)=1-e^{-\lambda x}, \qquad x \ge 0
$$

Sostituendo $x=1$ otteniamo:

$$
F(1)=1-e^{-\lambda} = 0.5
$$

Risolviamo l'equazione ricavando il valore di $\lambda$:

$$
\begin{aligned}
1-e^{-\lambda} &= 0.5 \\
e^{-\lambda} &= 0.5 \\
-\lambda &= \ln(0.5) \\
\lambda &= -\ln(0.5) = \ln(2)
\end{aligned}
$$

concludiamo che:

$$
\lambda=\boxed{\ln(2)\approx 0.693} \;.
$$

---

#### Esercizio 4

Sia $X \sim \mathrm{Par}(1)$, e sia $a \le 5$. Calcolare il valore di $a$ tale che:

$$
P\left(X\in[a,10-a)\right)=\frac12
$$

##### Risoluzione

Per una distribuzione di Pareto con parametro $\alpha=1$, la funzione di distribuzione è:

$$
F(x)=1-\frac1x, \qquad x \ge 1
$$

Riscriviamo la probabilità richiesta utilizzando la funzione di distribuzione:

$$
\begin{aligned}
P(X\in[a,10-a))
&= P(X<10-a)-P(X<a) \\
&= F(10-a)-F(a)
\end{aligned}
$$

Sostituendo l'espressione di $F(x)$ ed imponendo la condizione richiesta dal testo:

$$\begin{aligned}
P(x\in[a,10-a))
&= 1 - \frac1{10-a} - \left( 1-\frac1{a} \right) = \frac12 \\
&\Rightarrow \frac1a - \frac1{10-a} - \frac12 = 0 \\
&\Rightarrow \frac{2(10-a)-2a-a(10-a)}{2a(10-a)} = 0 \\
&\Rightarrow a^2 -14a +20 = 0 \\
&\Rightarrow a = 7\pm\sqrt{29}
\end{aligned}$$

Poiché il testo impone $a\le5$, l'unico valore accettabile è:

$$
\boxed{a=7-\sqrt{29}} \;.
$$

---

#### Esercizio 5

Sia $X \sim \text{Par}(\alpha)$. Calcolare $\alpha$ tale che il $30\%$-percentile di $X$ sia $2$.

##### Risoluzione

Il $30\%$-percentile è il valore $q_{0.30}$ tale che:

$$
q_{0.30}=x, \qquad F(x)=0.30, \qquad \text{con } x=2
$$

Per una distribuzione di Pareto con parametro $\alpha$, la funzione di ripartizione è:

$$
F(x)=1-\left(\frac1x\right)^\alpha, \qquad x \ge 1
$$

Sostituendo $x=2$ otteniamo:

$$
\begin{aligned}
F(2) &= 0.30 \\
1-\left(\frac12\right)^\alpha &= 0.30 \\
\left(\frac12\right)^\alpha &= 0.70 \\
\alpha &= \log_{\frac12}(0.70)
\approx \boxed{0.514} \;.
\end{aligned}
$$

---


#### Esercizio 6

Mario arriva alla fermata dell’autobus in ritardo e si accorge di averlo perso per un pelo. Decide di andare a piedi se il prossimo autobus ci mette più di 5 minuti ad arrivare. L’intervallo di tempo tra l’arrivo di un autobus e l’altro è una v.a. $U(4,6)$. Chiamiamo $X$ il tempo di attesa di Mario alla fermata:

- qual è la probabilità che $X$ sia minore di 4 minuti e mezzo?
- qual è la probabilità che $X$ sia uguale a 5 minuti?
- $X$ è una v.a. discreta o assolutamente continua?

##### Risoluzione

Per una distribuzione uniforme di parametri $\alpha,\beta$, la funzione di ripartizione è:

$$
F(x)=\frac{x-\alpha}{\beta-\alpha}
$$

Nel nostro caso $X\sim U(4,6)$, quindi:

- $P(X\le4.5) = F(4.5) = \frac{4.5-4}{6-4} = \frac{0.5}{2} = \boxed{0.25} \;.$

- $P(X=5)=\boxed{0} \;.$ Poiché una variabile assolutamente continua assegna probabilità nulla ai singoli punti.

- $\boxed{X\text{ è una variabile aleatoria assolutamente continua}} \;.$

---