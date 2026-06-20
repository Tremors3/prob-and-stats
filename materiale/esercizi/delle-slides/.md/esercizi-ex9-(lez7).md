## $$ \textcolor{red}{\text{Esercizi Lez. 7 - Ex 9}} $$

#### Esercizio 1

Si getta 12 volte una coppia di dadi equi e si osserva la somma delle due facce. Trova la probabilità di ottenere la somma uguale ad 8:

- (a) esattamente 4 volte;
- (b) di un numero di volte minore di 4.

##### Risoluzione

- Definiamo la variabile aleatoria

    $$
    M=\{\text{somma ottenuta nel lancio di una coppia di dadi}\},
    \quad
    S_M=\{2,3,\ldots,12\}.
    $$

    Lo spazio campionario del singolo lancio è

    $$
    \Omega=\{(1,1),\ldots,(6,6)\},
    \qquad
    |\Omega|=36,
    \qquad
    \text{equiprobabile}.
    $$

    Calcoliamo la probabilità che, in un singolo lancio, la somma sia uguale ad 8:

    $$\begin{aligned}
    p = p_M(8) = P(M=8)
    = P(\{(2,6),(3,5),(4,4),(5,3),(6,2)\})
    = \frac{5}{36}.
    \end{aligned}$$

- Definiamo la variabile aleatoria

    $$
    X=\{\text{numero di volte in cui compare la somma }8\text{ in 12 lanci}\}.
    $$

    $$
    X\sim\mathrm{Bin}\!\left(12,5/36\right).
    $$

    dove $n=12$ è il numero di prove, $p=\frac5{36}$ è la probabilità di successo e $k$ è il numero di successi osservati.

<div style="page-break-after: always;"></div>

- **(a)** Calcoliamo la probabilità di ottenere esattamente 4 successi.

    $$\begin{aligned}
    p_X(4)
    &= P(X=4) \\
    &= \binom{12}{4}p^4(1-p)^8 \\
    &= \frac{12!}{4!8!}
    \left(\frac5{36}\right)^4
    \left(1-\frac5{36}\right)^8 \\
    &= \boxed{0.05568}\;.
    \end{aligned}$$

- **(b)** Calcoliamo la probabilità che il numero di successi sia strettamente minore di 4.

    - Calcoliamo le singole probabilità per $k\in\{0,1,2,3\}$:

    $$\begin{aligned}
    p_X(0)&=\binom{12}{0}p^0(1-p)^{12}\approx0.1662,
    &\qquad
    p_X(1)&=\binom{12}{1}p(1-p)^{11}\approx0.3217,\\
    p_X(2)&=\binom{12}{2}p^2(1-p)^{10}\approx0.2854,
    &\qquad
    p_X(3)&=\binom{12}{3}p^3(1-p)^9\approx0.1534.
    \end{aligned}$$

    - Sommiamo ora le quattro componenti:

    $$\begin{aligned}
    P(X<4)
    &= F(4^-) \\
    &= p_X(0)+p_X(1)+p_X(2)+p_X(3) \\
    &= 0.1662+0.3217+0.2854+0.1534 \\
    &\approx \boxed{0.9267}\;.
    \end{aligned}$$

> **Nota**. La funzione di probabilità della binomiale è:
>
> $$ p_X(k)=P(X=k)=\binom{n}{k}p^k(1-p)^{n-k} $$

> **Nota**. In una variabile aleatoria discreta,
>
> $$ F(4^-)=P(X<4) $$
>
> cioè la probabilità cumulata fino al valore immediatamente precedente a $4$.

---

<div style="page-break-after: always;"></div>

#### Esercizio 2

Un'urna contiene 6 palline bianche e 10 rosse. Si estraggono 5 palline. Trovare la probabilità che 2 o 3 siano rosse:

- (a) se l’estrazione è con rimessa;
- (b) se l’estrazione è senza rimessa.

##### Risoluzione

Definiamo la variabile aleatoria

$$
X=\{\text{numero di palline rosse estratte}\},
\qquad
S_X=\{0,1,\ldots,5\}.
$$

- **(a) Estrazione con rimessa**

    Poiché dopo ogni estrazione la pallina viene reinserita nell'urna, le estrazioni sono indipendenti e la probabilità di successo rimane costante:

    $$
    p=P(\text{rossa})=\frac{10}{16}=\frac58.
    $$

    Il numero di palline rosse estratte segue quindi una distribuzione binomiale:

    $$
    X\sim \mathrm{Bin}\!\left(5,5/8\right).
    $$

    > **Nota**. La funzione di probabilità della binomiale è
    > 
    > $$ p_X(k)=\binom{n}{k}p^k(1-p)^{n-k} $$

    Calcoliamo le probabilità per $k\in\{2,3\}$.

    $$\begin{aligned}
    p_X(2)=P(X=2)
    &=\binom52\left(\frac58\right)^2\left(\frac38\right)^3 \\
    &=10\left(\frac58\right)^2\left(\frac38\right)^3 \\
    &\approx 0.20599.
    \end{aligned}$$

    $$\begin{aligned}
    p_X(3)=P(X=3)
    &=\binom53\left(\frac58\right)^3\left(\frac38\right)^2 \\
    &=10\left(\frac58\right)^3\left(\frac38\right)^2 \\
    &\approx 0.34332.
    \end{aligned}$$

    Sommiamo ora le due componenti.

    $$\begin{aligned}
    P(X\in\{2,3\})
    &=P(X=2)+P(X=3) \\
    &\approx 0.20599+0.34332 \\
    &=\boxed{0.54931}.
    \end{aligned}$$

- **(b) Estrazione senza rimessa**

    In questo caso le estrazioni **non** sono indipendenti, poiché la composizione dell'urna cambia dopo ogni pescata.

    Si utilizza quindi la distribuzione ipergeometrica:

    $$
    X\sim\mathrm{Hyper}(r,b,n),
    $$

    dove

    $$
    r=10,\qquad b=6,\qquad n=5.
    $$

    > **Nota**. La funzione di probabilità dell'ipergeometrica è
    > 
    > $$ p_X(k)= \frac{\binom{r}{k}\binom{b}{n-k}}{\binom{r+b}{n}} $$

    Calcoliamo le probabilità per $k\in\{2,3\}$.

    $$\begin{aligned}
    p_X(2)=P(X=2)
    &=\frac{\binom{10}{2}\binom{6}{3}}
            {\binom{16}{5}} \\
    &=\frac{45\cdot20}{4368} \\
    &\approx 0.20604.
    \end{aligned}$$

    $$\begin{aligned}
    p_X(3)=P(X=3)
    &=\frac{\binom{10}{3}\binom{6}{2}}
            {\binom{16}{5}} \\
    &=\frac{120\cdot15}{4368} \\
    &\approx 0.41209.
    \end{aligned}$$

    Sommiamo ora le due componenti.

    $$\begin{aligned}
    P(X\in\{2,3\})
    &=P(X=2)+P(X=3) \\
    &\approx 0.20604+0.41209 \\
    &=\boxed{0.61813}.
    \end{aligned}$$

> **Osservazione**. 
> Nel caso con rimessa il modello corretto è la **Binomiale**, perché ogni estrazione è indipendente e la probabilità di successo resta costante.
>
> Nel caso senza rimessa il modello corretto è la **Ipergeometrica**, perché le estrazioni sono dipendenti e la probabilità di successo varia ad ogni pescata.

---

<div style="page-break-after: always;"></div>

#### Esercizio 3
 
Un messaggio di 10 bit arriva o dalla sorgente A (con probabilità 1/3) o dalla sorgente B (con probabilità 2/3); non puo’ venire in parte da A in parte da B.

A manda i messaggi in modo che 1 ha probabilità 1/2 e 0 ha probabilità 1/2. Invece B manda i messaggi in modo che 1 ha probabilità 4/7 e 0 ha probabilità 3/7.

Trova:
- (a) la probabilità che in un messaggio ci siano 6 bit uguali ad 1;
- (b) la probabilità che il messaggio venga da A, se il messaggio ricevuto contiene 6 bit uguali ad 1.
 
*Suggerimento: combina le due leggi binomiali (quella di A e quella di B) con la formula delle probabilità totali (a) e poi con la formula di Bayes (b).*

##### Risoluzione

- **Dati utili del problema**

    $$
    P(A)=\frac13,
    \qquad
    P(B)=\frac23.
    $$

    $$
    P(1\mid A)=\frac12,
    \qquad
    P(1\mid B)=\frac47.
    $$

- **Definizione dell'evento di interesse**

    $$
    E=\{\text{il messaggio contiene esattamente 6 bit uguali a }1\}.
    $$

    Vogliamo quindi determinare

    $$
    P(E).
    $$

    Per la formula delle probabilità totali:

    $$
    P(E)=P(E\mid A)P(A)+P(E\mid B)P(B).
    $$

<div style="page-break-after: always;"></div>

- **Calcolo di $P(E\mid A)$**

    Condizionatamente alla sorgente A, ogni bit ha probabilità $1/2$ di essere uguale a 1 e i 10 bit sono indipendenti.

    Pertanto

    $$
    X\mid A \sim \mathrm{Bin}\!\left(10,\frac12\right),
    $$

    dove:

    - $n=10$ è la lunghezza del messaggio;
    - $p=\frac12$ è la probabilità che un bit sia uguale a 1;
    - $k=6$ è il numero di bit uguali a 1 richiesto.

    Quindi

    $$\begin{aligned}
    P(E\mid A)
    &= \binom{10}{6}\left(\frac12\right)^6\left(\frac12\right)^4 \\
    &= \binom{10}{6}\left(\frac12\right)^{10} \\
    &= \frac{210}{1024} \\
    &\approx 0.20508.
    \end{aligned}$$

- **Calcolo di $P(E\mid B)$**

    Analogamente, condizionatamente alla sorgente B:

    $$
    X\mid B \sim \mathrm{Bin}\!\left(10,\frac47\right),
    $$

    con:

    - $n=10$;
    - $p=\frac47$;
    - $k=6$.

    Pertanto

    $$\begin{aligned}
    P(E\mid B)
    &= \binom{10}{6}
    \left(\frac47\right)^6
    \left(\frac37\right)^4 \\
    &\approx 0.24799.
    \end{aligned}$$

- **(a) Probabilità che il messaggio contenga esattamente 6 bit uguali a 1**

    Applichiamo la formula delle probabilità totali:

    $$\begin{aligned}
    P(E)
    &= P(E\mid A)P(A)+P(E\mid B)P(B) \\
    &= \frac13\cdot0.20508+\frac23\cdot0.24799 \\
    &\approx \boxed{0.23369} \;.
    \end{aligned}$$

- **(b) Probabilità che il messaggio provenga da A sapendo che contiene 6 bit uguali a 1**

    Applichiamo la formula di Bayes:

    $$\begin{aligned}
    P(A\mid E)
    &= \frac{P(E\mid A)P(A)}{P(E)} \\
    &= \frac{0.20508\cdot\frac13}{0.23369} \\
    &\approx \boxed{0.2925} \;.
    \end{aligned}$$

> **Osservazione.** Un errore frequente consiste nel calcolare
>
> $$\begin{aligned}
> P(1)&=P(1\mid A)P(A)+P(1\mid B)P(B) \\
> &= \frac12\cdot\frac13+\frac47\cdot\frac23
> = \frac{23}{42},
> \end{aligned}$$
>
> e concludere che
>
> $$
> X\sim\mathrm{Bin}\!\left(10,\frac{23}{42}\right).
> $$
>
> Questo ragionamento non è corretto. La sorgente viene scelta una sola volta all'inizio e tutti i 10 bit sono poi generati dalla stessa sorgente. Di conseguenza il modello corretto è una **miscela di due distribuzioni binomiali**, da combinare tramite la formula delle probabilità totali.

<div style="page-break-after: always;"></div>

> **Ripasso - Formule utili**
>
> Formula delle probabilità totali:
>
> $$
> P(A)=P(A\mid C)P(C)+P(A\mid C^c)P(C^c).
> $$
>
> Definizione di probabilità condizionata:
>
> $$
> P(A\mid B)=\frac{P(A\cap B)}{P(B)}.
> $$
>
> Formula di Bayes:
>
> $$
> P(B\mid A)
> =\frac{P(A\mid B)P(B)}{P(A)}.
> $$

---

<div style="page-break-after: always;"></div>

#### Esercizio 4

Una compagnia concede uno sconto sugli ordini che vengono pagati entro 30 giorni. Su tutti gli ordini il 10% riceve uno sconto. Si estraggono a caso 12 ordini. Approssimando i calcoli con l’ipotesi di un altissimo numero di ordini, trova la probabilità che ricevano uno sconto:

- (a) meno di 4 sui 12;
- (b) più di 1 ordine sui 12.

##### Risoluzione

Definiamo la variabile aleatoria

$$
X=\{\text{numero di ordini che ricevono lo sconto}\}.
$$

Poiché:

- ogni ordine può ricevere oppure non ricevere lo sconto;
- la probabilità di ricevere lo sconto è costante;
- il numero di ordini osservati è fissato ($n=12$);
- l'ipotesi di un numero molto grande di ordini rende ragionevole assumere indipendenza tra le osservazioni,

la variabile aleatoria $X$ segue una distribuzione binomiale con parametri

$$
n=12,
\qquad
p=\frac{1}{10}=0.1.
$$

Pertanto

$$
X\sim\mathrm{Bin}(12,0.1).
$$

> Ricordiamo la funzione di probabilità della distribuzione binomiale:
> 
> $$ P(X=k)=\binom{n}{k}p^k(1-p)^{n-k} $$

- **(a)** Calcolare la probabilità che "meno di 4 ordini su 12 ricevano lo sconto".

    $$
    P(X<4)=P(X=0)+P(X=1)+P(X=2)+P(X=3).
    $$

    Calcoliamo le singole probabilità:

    $$\begin{aligned}
    P(X=0)
    &= \binom{12}{0}(0.1)^0(0.9)^{12} \\
    &= (0.9)^{12} \\
    &\approx 0.2824
    \end{aligned}$$

    $$\begin{aligned}
    P(X=1)
    &= \binom{12}{1}(0.1)^1(0.9)^{11} \\
    &= 12\cdot0.1\cdot(0.9)^{11} \\
    &\approx 0.3766
    \end{aligned}$$

    $$\begin{aligned}
    P(X=2)
    &= \binom{12}{2}(0.1)^2(0.9)^{10} \\
    &= 66\cdot0.01\cdot(0.9)^{10} \\
    &\approx 0.2301
    \end{aligned}$$

    $$\begin{aligned}
    P(X=3)
    &= \binom{12}{3}(0.1)^3(0.9)^9 \\
    &= 220\cdot0.001\cdot(0.9)^9 \\
    &\approx 0.0852
    \end{aligned}$$

    Sommiamo le quattro probabilità:

    $$\begin{aligned}
    P(X<4)
    &= P(X=0)+P(X=1)+P(X=2)+P(X=3) \\
    &= 0.2824+0.3766+0.2301+0.0852 \\
    &\approx \boxed{0.9743}\;.
    \end{aligned}$$

- **(b)** Calcolare la probabilità che "più di un ordine su 12 riceva lo sconto". Conviene utilizzare l'evento complementare:

    $$
    P(X>1)=1-P(X\le1)=1-F(1).
    $$

    Pertanto

    $$\begin{aligned}
    P(X>1)
    &= 1-\bigl(P(X=0)+P(X=1)\bigr) \\
    &= 1-0.2824-0.3766 \\
    &\approx \boxed{0.3410}\;.
    \end{aligned}$$

> **Osservazione.** Nel punto (a) è più naturale scrivere
>
> $$
> P(X<4)=P(X=0)+P(X=1)+P(X=2)+P(X=3),
> $$
>
> mentre nel punto (b) conviene sfruttare il complemento
>
> $$
> P(X>1)=1-P(X\le1),
> $$
>
> evitando di calcolare tutte le probabilità da $2$ a $12$.

---

<div style="page-break-after: always;"></div>