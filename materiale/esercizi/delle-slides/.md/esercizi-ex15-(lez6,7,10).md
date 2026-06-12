## $$ \textcolor{red}{\text{Esercizi Ex. 15 - Lez. 6,7,10}} $$

#### Esercizio 1

Un corpo ha 5000 atomi di una sostanza radioattiva. Ogni atomo decade in un minuto con probabilità $0.0004$. Sia $X$ il numero di atomi che decadono in un minuto.

- (a) Trova la probabilità che decadano almeno 3 atomi.
- (b) Se il corpo ha $5 \times 10^6$ atomi della sostanza radioattiva, trova la probabilità che decadano da 1980 a 2020 atomi.

##### Risoluzione

- **(a) Calcolare la probabilità che decadano almeno 3 atomi.**

   Abbiamo due possibili modelli.

   $\;$

   1. Modellare $X$ come una distribuzione Binomiale.

      $$
      X \sim \text{Bin}(n=5000,\; p=0.0004)
      $$

      Tuttavia, dato che $n$ è molto grande e $p$ è molto piccolo, i calcoli risultano poco pratici. Conviene quindi utilizzare l'approssimazione di Poisson.

   $\;$

   2. Modellare $X$ come una distribuzione di Poisson.

      Calcoliamo il parametro:

      $$
      \mu = np = 5000\cdot0.0004 = 2
      $$

      Quindi:

      $$
      X \sim \text{Pois}(\mu=2)
      $$

      <div style="page-break-after: always;"></div>

      Calcoliamo la probabilità richiesta.

      $$\begin{aligned}
      P(X\ge3)
      &= 1 - P(X<3) \\
      &= 1 - \left(P(X=0)+P(X=1)+P(X=2)\right) \\
      &= 1 - \left(
      e^{-2} + 2e^{-2} + \frac{2^2}{2!}e^{-2}
      \right) \\
      &= 1 - \left(
      e^{-2} + 2e^{-2} + 2e^{-2}
      \right) \\
      &= 1 - 5e^{-2} \\
      &\approx \boxed{0.3233}\;.
      \end{aligned}$$

- **(b) Se il corpo ha $5 \times 10^6$ atomi della sostanza radioattiva, trova la probabilità che decadano da 1980 a 2020 atomi.**

   Anche in questo caso modelliamo il problema con una distribuzione di Poisson.

   $\;$

   Calcoliamo il parametro:

   $$
   \mu = np
   = (5\times10^6)\cdot0.0004
   = 2000
   $$

   Quindi:

   $$
   X \sim \text{Pois}(\mu=2000)
   $$

   Notiamo però che il parametro $\mu$ è molto grande. Possiamo quindi utilizzare l'approssimazione normale, ricordando che per una variabile di Poisson vale:

   $$
   E[X]=\mu,
   \qquad
   \text{Var}(X)=\mu
   $$

   Pertanto:

   $$
   X \approx N(\mu=2000,\;\sigma^2=2000)
   $$

   La probabilità richiesta è:

   $$
   P(1980 \le X \le 2020)
   $$

   <div style="page-break-after: always;"></div>

   Standardizziamo rispetto alla normale standard.

   $$\begin{aligned}
   P(1980 \le X \le 2020)
   &= P(X\le2020)-P(X<1980) \\
   &= \Phi\!\left(\frac{2020-\mu}{\sigma}\right) - \Phi\!\left(\frac{1980-\mu}{\sigma}\right) \\
   &= \Phi\!\left(\frac{2020-2000}{\sqrt{2000}}\right) - \Phi\!\left(\frac{1980-2000}{\sqrt{2000}}\right) \\
   &= \Phi\!\left(\frac{\sqrt5}{5}\right) - \Phi\!\left(-\frac{\sqrt5}{5}\right) \\
   &= \Phi\!\left(\frac{\sqrt5}{5}\right) - \left(1-\Phi\!\left(\frac{\sqrt5}{5}\right)\right) \\
   &= 2\cdot\Phi\!\left(\frac{\sqrt5}{5}\right)-1 \\
   &\approx 2\cdot\Phi(0.4472)-1 \\
   &\approx 2\cdot0.67264-1 \\
   &\approx \boxed{0.3453} \;.
   \end{aligned}$$

> **Approssimazioni utili tra distribuzioni.**
>
> $$
> \text{Bin}(n,p)
> \xrightarrow[\;n\text{ grande},\,p\text{ piccolo}\;]{\mu=np}
> \text{Pois}(\mu)
> \xrightarrow[\;\mu\text{ grande}\;]{}
> N(\mu,\mu)
> $$
>
> In molti esercizi conviene quindi procedere nel seguente modo:
>
> $$
> \text{Binomiale}
> \;\longrightarrow\;
> \text{Poisson}
> \;\longrightarrow\;
> \text{Normale}
> $$
>
> In realtà si ottiene una stima più accurata approssimando direttamente:
>
> $$
> \text{Binomiale}
> \;\longrightarrow\;
> \text{Normale}
> $$
>
> Vedi esercizi 3,4,5,6.

---

<div style="page-break-after: always;"></div>

#### Esercizio 2

Una certa lotteria istantanea ha probabilità di vincita $0.01$ per singolo biglietto. Si domanda:

- (a) la probabilità che fra 300 biglietti tale vincita si verifichi 2 o 3 volte;
- (b) la probabilità che fra 30000 biglietti quella vincita si verifichi da 295 a 310 volte (estremi inclusi).

##### Risoluzione

- **(a) Calcolare la probabilità che fra 300 biglietti tale vincita si verifichi 2 o 3 volte.**

   Modelliamo il problema con una distribuzione Binomiale.

   $$
   X \sim \text{Bin}(n=300,\; p=0.01)
   $$

   Tuttavia, dato che $n$ è grande e $p$ è piccolo, conviene utilizzare l'approssimazione di Poisson.

   $$
   \mu = np = 300\cdot0.01 = 3
   $$

   Quindi:

   $$
   X \sim \text{Pois}(\mu=3)
   $$

   Calcoliamo la probabilità richiesta.

   $$\begin{aligned}
   P(X\in\{2,3\})
   &= P(X=2)+P(X=3) \\
   &= e^{-3}\frac{3^2}{2!}
      + e^{-3}\frac{3^3}{3!} \\
   &= \frac92 e^{-3}
      + \frac{27}{6}e^{-3} \\
   &= 9e^{-3} \\
   &\approx \boxed{0.4481}\;.
   \end{aligned}$$

   <div style="page-break-after: always;"></div>

- **(b) Calcolare la probabilità che fra 30000 biglietti quella vincita si verifichi da 295 a 310 volte (estremi inclusi).**

   Modelliamo inizialmente il problema con una distribuzione Binomiale.

   $$
   X \sim \text{Bin}(n=30000,\; p=0.01)
   $$

   Dato che $n$ è molto grande e $p$ è piccolo, utilizziamo l'approssimazione di Poisson.

   $$
   \mu = np = 30000\cdot0.01 = 300
   $$

   Quindi:

   $$
   X \sim \text{Pois}(\mu=300)
   $$

   Notiamo però che il parametro $\mu$ è molto grande. Possiamo quindi applicare l'approssimazione normale, ricordando che per una variabile di Poisson vale:

   $$
   E[X]=\mu,
   \qquad
   \text{Var}(X)=\mu
   $$

   Pertanto:

   $$
   X \approx N(\mu=300,\;\sigma^2=300)
   $$

   Calcoliamo la probabilità richiesta.

   $$\begin{aligned}
   P(295\le X\le310)
   &= P(X\le310)-P(X<295) \\
   &= \Phi\left(\frac{310-\mu}{\sigma}\right)
      - \Phi\left(\frac{295-\mu}{\sigma}\right) \\
   &= \Phi\left(\frac{310-300}{\sqrt{300}}\right)
      - \Phi\left(\frac{295-300}{\sqrt{300}}\right) \\
   &= \Phi\left(\frac{1}{\sqrt3}\right)
      - \Phi\left(-\frac{1}{2\sqrt3}\right) \\
   &= \Phi\left(\frac{1}{\sqrt3}\right)
      - \left(1-\Phi\left(\frac{1}{2\sqrt3}\right)\right) \\
   &= \Phi\left(\frac{1}{\sqrt3}\right)
      + \Phi\left(\frac{1}{2\sqrt3}\right)
      - 1 \\
   &\approx \Phi(0.5774)+\Phi(0.2887)-1 \\
   &\approx 0.7181 + 0.6136 - 1
   \approx \boxed{0.3317} \;.
   \end{aligned}$$

<div style="page-break-after: always;"></div>

> **Approssimazioni utili tra distribuzioni.**
>
> $$
> \text{Bin}(n,p)
> \xrightarrow[\;n\text{ grande},\,p\text{ piccolo}\;]{\mu=np}
> \text{Pois}(\mu)
> \xrightarrow[\;\mu\text{ grande}\;]{}
> N(\mu,\mu)
> $$
>
> oppure direttamente:
>
> $$
> \text{Bin}(n,p)
> \xrightarrow[\;np,\;n(1-p)\text{ grandi}\;]{}
> N\!\big(np,\;np(1-p)\big)
> $$
>
> In molti esercizi conviene quindi procedere nel seguente modo:
>
> $$
> \text{Binomiale}
> \;\longrightarrow\;
> \text{Poisson}
> \;\longrightarrow\;
> \text{Normale}
> $$
>
> oppure, quando possibile:
>
> $$
> \text{Binomiale}
> \;\longrightarrow\;
> \text{Normale}
> $$
>
> scegliendo l'approssimazione più conveniente in base ai parametri del problema.
>
> ---
>
> La **correzione di continuità** migliora sensibilmente l’approssimazione nei casi come questo.
>
> Le regole corrette sono:
>
> $$
> P(X \ge k) \approx P(N \ge k - 0.5),
> $$
>
> $$
> P(X > k) \approx P(N \ge k + 0.5),
> $$
>
> $$
> P(X \le k) \approx P(N \le k + 0.5),
> $$
>
> $$
> P(X < k) \approx P(N \le k - 0.5).
> $$

---

<div style="page-break-after: always;"></div>

#### Esercizio 3

Viene lanciata 100 volte una coppia di dadi equi contando quante volte esce la somma sette.

Trova:

- (a) la probabilità che esca più di 20 volte;
- (b) la probabilità che esca da 14 a 20 volte (estremi compresi).

##### Risoluzione

Definiamo la variabile aleatoria:

$$
S = \text{"Numero di volte che esce la somma 7"}.
$$

Lo spazio campionario relativo a un singolo lancio della coppia di dadi è equiprobabile e contiene $36$ esiti.

La probabilità che la somma dei due dadi sia uguale a $7$ è:

$$
p
= \frac{|\{(1,6),(2,5),(3,4),(4,3),(5,2),(6,1)\}|}{36}
= \frac{6}{36}
= \frac{1}{6}
$$

Poiché ripetiamo l’esperimento 100 volte in modo indipendente, possiamo modellare il numero di successi con una distribuzione binomiale:

$$
S \sim \text{Bin}(n=100,\;p=\tfrac{1}{6})
$$

Possiamo utilizzare l’approssimazione normale:

$$
S \approx N(\mu,\sigma^2)
$$

con

$$
\mu = np = 100 \cdot \frac{1}{6} \approx 16.67
$$

$$
\sigma^2 = np(1-p) = 100 \cdot \frac{1}{6} \cdot \frac{5}{6} \approx 13.89
$$

<div style="page-break-after: always;"></div>

- **(a) Calcolare la probabilità che esca più di 20 volte.**

   La probabilità richiesta è:

   $$
   P(S > 20)
   $$

   Utilizzando la **correzione di continuità**:

   $$
   P(S > 20) \approx P(N > 20.5)
   $$

   Standardizzando:

   $$\begin{aligned}
   P(S > 20)
   &\approx 1 - \Phi\!\left(\frac{20.5 - 16.67}{\sqrt{13.89}}\right) \\
   &\approx 1 - \Phi(1.03) \\
   &\approx 1 - 0.8485 \\
   &\approx \boxed{0.1515} \;.
   \end{aligned}$$

- **(b) la probabilità che esca da 14 a 20 volte (estremi compresi).**

   La probabilità richiesta è:

   $$
   P(14 \le S \le 20)
   $$

   Applicando la **correzione di continuità**:

   $$
   P(14 \le S \le 20) \approx P(13.5 \le N \le 20.5)
   $$

   Quindi:

   $$\begin{aligned}
   P(14 \le S \le 20)
   &\approx P(N\le20.5) - P(N<13.5) \\
   &\approx \Phi\!\left(\frac{20.5 - 16.67}{\sqrt{13.89}}\right)
      - \Phi\!\left(\frac{13.5 - 16.67}{\sqrt{13.89}}\right) \\
   &\approx \Phi(1.03) - \Phi(-0.85) \\
   &\approx 0.8485 - 0.1977 \\
   &\approx \boxed{0.6508} \;.
   \end{aligned}$$

<div style="page-break-after: always;"></div>

> **Approssimazione utile tra Binomiale e Gaussiana**
>
> $$
> \text{Bin}(n,p)
> \xrightarrow[\;np,\;n(1-p)\text{ grandi}\;]{}
> N\!\big(np,\;np(1-p)\big)
> $$
>
> La differenza rispetto al valore ottenuto senza correzione di continuità è dovuta al fatto che stiamo approssimando una variabile discreta (binomiale) con una continua (normale).
>
> La **correzione di continuità** migliora sensibilmente l’approssimazione nei casi come questo.
>
> Le regole corrette sono:
>
> $$
> P(X \ge k) \approx P(N \ge k - 0.5),
> $$
>
> $$
> P(X > k) \approx P(N \ge k + 0.5),
> $$
>
> $$
> P(X \le k) \approx P(N \le k + 0.5),
> $$
>
> $$
> P(X < k) \approx P(N \le k - 0.5).
> $$

---

<div style="page-break-after: always;"></div>

#### Esercizio 4

Il 20% di componenti prodotti è difettoso. Ogni spedizione comprende 400 pezzi. Se una spedizione contiene più di 90 pezzi difettosi, può essere restituita.

Trova:
- (a) la probabilità che una data spedizione venga restituita;
- (b) se in un particolare giorno vengono fatte 500 spedizioni, la probabilità che 60 o più di queste spedizioni vengano restituite.

##### Risoluzione

Modelliamo il numero di pezzi difettosi in una spedizione come una variabile aleatoria binomiale:

$$
X \sim \text{Bin}(n=400,\; p=0.2)
$$

Approssimiamo $X$ con una distribuzione normale:

$$
X \approx N(\mu,\sigma^2)
$$

con

$$
\mu = np = 400 \cdot 0.2 = 80
$$

$$
\sigma^2 = np(1-p) = 400 \cdot 0.2 \cdot 0.8 = 64
$$

- **(a) Calcolare la probabilità che una data spedizione venga restituita.**

   Una spedizione viene restituita se contiene più di 90 pezzi difettosi:

   $$
   P(X > 90)
   $$

   Poiché stiamo approssimando una variabile discreta con una continua, applichiamo la **correzione di continuità**:

   $$
   P(X > 90) \approx P(N > 90.5)
   $$

   <div style="page-break-after: always;"></div>

   Standardizzando:

   $$\begin{aligned}
   P(X > 90)
   &\approx 1 - \Phi\!\left(\frac{90.5 - 80}{\sqrt{64}}\right) \\
   &\approx 1 - \Phi(1.31) \\
   &\approx 1 - 0.9049 \\
   &\approx \boxed{0.0951} \;.
   \end{aligned}$$

- **(b) Se in un particolare giorno vengono fatte 500 spedizioni, calcolare la probabilità che 60 o più di queste spedizioni vengano restituite.**

   Sia $Y$ il numero di spedizioni restituite in una giornata. Ogni spedizione è un evento con probabilità di successo (restituzione) pari a $p \approx 0.0951$, quindi:

   $$
   Y \sim \text{Bin}(n=500,\; p=0.0951)
   $$

   Approssimiamo con una distribuzione normale:

   $$
   Y \approx N(\mu,\sigma^2)
   $$

   con

   $$\begin{aligned}
   \mu &= np = 500 \cdot 0.0951 = 47.55 \\
   \sigma^2 &= np(1-p) = 500 \cdot 0.0951 \cdot (1 - 0.0951) \approx 43.03 \\
   \end{aligned}$$

   La probabilità richiesta è:

   $$
   P(Y \ge 60)
   $$

   Poiché stiamo approssimando una variabile discreta con una continua, applichiamo la **correzione di continuità**:

   $$
   P(Y \ge 60) \approx P(Y > 59.5)
   $$

   Standardizzando:

   $$\begin{aligned}
   P(Y \ge 60)
   &\approx 1 - \Phi\!\left(\frac{59.5 - 47.55}{\sqrt{43.03}}\right) \\
   &\approx 1 - \Phi(1.82) \\
   &\approx 1 - 0.96562
   \approx \boxed{0.0344} \;.
   \end{aligned}$$

<div style="page-break-after: always;"></div>

> **Approssimazione utile tra Binomiale e Gaussiana**
>
> $$
> \text{Bin}(n,p)
> \xrightarrow[\;np,\;n(1-p)\text{ grandi}\;]{}
> N\!\big(np,\;np(1-p)\big)
> $$
>
> La differenza rispetto al valore ottenuto senza correzione di continuità è dovuta al fatto che stiamo approssimando una variabile discreta (binomiale) con una continua (normale).
>
> La **correzione di continuità** migliora sensibilmente l’approssimazione nei casi come questo.
>
> Le regole corrette sono:
>
> $$
> P(X \ge k) \approx P(N \ge k - 0.5),
> $$
>
> $$
> P(X > k) \approx P(N \ge k + 0.5),
> $$
>
> $$
> P(X \le k) \approx P(N \le k + 0.5),
> $$
>
> $$
> P(X < k) \approx P(N \le k - 0.5).
> $$

---

<div style="page-break-after: always;"></div>

#### Esercizio 5

La compagnia aerea VOLAREBASSO stima che il 5% dei passeggeri prenotati non si presenti all'imbarco. Decide quindi di adottare una politica di overbooking: per un volo di 300 posti accetta 310 prenotazioni.

Con che probabilità resteranno delle persone a terra?

##### Risoluzione

Modelliamo il problema considerando il numero di passeggeri che si presentano all’imbarco. Ogni passeggero si presenta con probabilità $p = 0.95$, quindi il numero di presenti segue una distribuzione binomiale:

$$
X \sim \text{Bin}(n=310,\; p=0.95)
$$

Approssimiamo la distribuzione binomiale con una normale:

$$
X \approx N(\mu,\sigma^2)
$$

dove:

$$\begin{aligned}
\mu &= np = 310 \cdot 0.95 = 294.5 \\
\sigma^2 &= np(1-p) = 310 \cdot 0.95 \cdot 0.05 = 14.725
\end{aligned}$$

La compagnia ha 300 posti, quindi restano persone a terra se si presentano più di 300 passeggeri:

$$
P(X > 300)
$$

Poiché stiamo approssimando una variabile discreta con una continua, applichiamo la **correzione di continuità**:

$$
P(X > 300) \approx P(X > 300.5)
$$

Standardizzando:

$$\begin{aligned}
P(X > 300)
&\approx 1 - \Phi\left(\frac{300.5 - 294.5}{\sqrt{14.725}}\right) \\
&\approx 1 - \Phi(1.56) \\
&\approx 1 - 0.9406
\approx \boxed{0.0594} \;.
\end{aligned}$$

> **Approssimazione utile tra Binomiale e Gaussiana**
>
> $$
> \text{Bin}(n,p)
> \xrightarrow[\;np,\;n(1-p)\text{ grandi}\;]{}
> N\!\big(np,\;np(1-p)\big)
> $$
>
> La **correzione di continuità** migliora sensibilmente l’approssimazione nei casi come questo.
>
> Le regole corrette sono:
>
> $$
> P(X \ge k) \approx P(N \ge k - 0.5),
> $$
>
> $$
> P(X > k) \approx P(N \ge k + 0.5),
> $$
>
> $$
> P(X \le k) \approx P(N \le k + 0.5),
> $$
>
> $$
> P(X < k) \approx P(N \le k - 0.5).
> $$

---

<div style="page-break-after: always;"></div>

#### Esercizio 6

Ogni giorno una ditta guadagna 1 punto con probabilità $1/2$, perde 1 punto con probabilità $1/4$, mentre resta stazionaria con probabilità $1/4$. Se questa tendenza perdura per $100$ giorni, con quale probabilità avrà guadagnato almeno $28$ punti?

*Suggerimento: all’istante $0$ poniamo $S_0 = 0$; per ogni $j \in N$ sia*

$$
X_j = \textit{"incremento (positivo o nullo o negativo) nel j-esimo giorno"}.
$$

*Quanto valgono $\mu$ e $\sigma^2$ di $X_j$? Come si comporta, per $n$ grande, il guadagno cumulativo $S_n$ fino al giorno $n$? Quanto vale $P (S_{100} \ge 28)$?*


##### Risoluzione

Definiamo la variabile aleatoria che rappresenta l’incremento giornaliero:

$$
X_j =
\begin{cases}
+1 & \text{con probabilità } \frac{1}{2} \\
0 & \text{con probabilità } \frac{1}{4} \\
-1 & \text{con probabilità } \frac{1}{4}
\end{cases}
$$

Il guadagno totale dopo $n$ giorni è:

$$
S_n = \sum_{j=1}^{n} X_j
$$

Calcoliamo media e varianza di $X_j$.

- **Valore atteso**

$$
\mu = \mathbb{E}[X_j]
= 1 \cdot \frac{1}{2} + 0 \cdot \frac{1}{4} - 1 \cdot \frac{1}{4}
= \frac{1}{4}
$$

- **Secondo momento**

    $$
    \mathbb{E}[X_j^2]
    = 1^2 \cdot \frac{1}{2} + 0^2 \cdot \frac{1}{4} + (-1)^2 \cdot \frac{1}{4}
    = \frac{3}{4}
    $$

- **Varianza**

    $$
    \sigma^2 = \mathbb{E}[X_j^2] - (\mathbb{E}[X_j])^2
    = \frac{3}{4} - \frac{1}{16}
    = \frac{11}{16}
    $$

Per $n=100$ giorni, per linearità di media e varianza:

$$
S_{100} \approx N(\mu_{100}, \sigma_{100}^2)
$$

con

$$\begin{aligned}
\mu_{100} &= 100 \cdot \frac{1}{4} = 25 \\
\sigma_{100}^2 &= 100 \cdot \frac{11}{16} = 68.75
\end{aligned}$$

Approssimiamo con la distribuzione normale:

$$
S_{100} \approx N(25,\; 68.75)
$$

- **Calcolo della probabilità**

    $$
    P(S_{100} \ge 28)
    $$

    Poiché stiamo approssimando una variabile discreta con una continua, applichiamo la **correzione di continuità**:

    $$
    P(S_{100} \ge 28) \approx P(S \ge 27.5)
    $$

    Standardizzando:

    $$\begin{aligned}
    P(S_{100} \ge 28)
    &\approx 1 - \Phi\left(\frac{27.5 - 25}{\sqrt{68.75}}\right) \\
    &\approx 1 - \Phi(0.30) \\
    &\approx 1 - 0.61791 \\
    &\approx \boxed{0.38209} \;.
    \end{aligned}$$

<div style="page-break-after: always;"></div>

> **Approssimazione utile tra Binomiale e Gaussiana**
>
> $$
> \text{Bin}(n,p)
> \xrightarrow[\;np,\;n(1-p)\text{ grandi}\;]{}
> N\!\big(np,\;np(1-p)\big)
> $$
>
> La differenza rispetto al valore ottenuto senza correzione di continuità è dovuta al fatto che stiamo approssimando una variabile discreta (binomiale) con una continua (normale).
>
> La **correzione di continuità** migliora sensibilmente l’approssimazione nei casi come questo.
>
> Le regole corrette sono:
>
> $$
> P(X \ge k) \approx P(N \ge k - 0.5),
> $$
>
> $$
> P(X > k) \approx P(N \ge k + 0.5),
> $$
>
> $$
> P(X \le k) \approx P(N \le k + 0.5),
> $$
>
> $$
> P(X < k) \approx P(N \le k - 0.5).
> $$

---

<div style="page-break-after: always;"></div>