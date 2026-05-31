## $$ \textcolor{red}{\text{Esercizi Lez. 4 - Ex 5}} $$

#### Esercizio 1

Uno studente studia con probabilità $\frac{1}{2}$. Gli viene presentato un quiz con 4 risposte possibili. Se ha studiato da certamente la risposta esatta, se non ha studiato sceglie a caso una delle 4 risposte. Supponiamo che abbia dato risposta esatta: con che probabilità ha studiato davvero?

##### Risoluzione

Definiamo i due eventi:

$\begin{aligned}
E &= \{\text{"Lo studente ha dato la risposta esatta}"\} \\
S &= \{\text{"Lo studente ha studiato"}\}
\end{aligned}$

Calcoliamo $P(E)$ con la **legge della Probabilità Totale**:

$$\begin{aligned}
P(S) &= P(S') = 0.50 \\
P(E\cap S) &= P(E\mid S)\cdot P(S) = 1\cdot0.50 = 0.50 \\
P(E\cap S') &= P(E\mid S')\cdot P(S') = \frac{1}{4}\cdot0.50 = 0.125 \\
P(E) &= P(E\cap S) + P(E\cap S') = 0.50 + 0.125 = 0.625
\end{aligned}$$

Calcoliamo $P(S\mid E)$ tramite l'applicazione della **legge di Bayes**:

$$\begin{aligned}
P(S\mid E) &= \frac{P(E\mid S)\cdot P(S)}{P(E)} \\
&= \frac{0.50}{0.625} = \boxed{0.8} \;.
\end{aligned}$$

> **Nota**. Dati $A_1,A_2,\dots,A_n$ eventi **disgiunti due a due** ($A_i\cap A_j=\emptyset$) che compongono una **partizione** di $\Omega$ ($A_1\cup\dots\cup A_n = \Omega$). La formula della legge della probabilità totale dice che:
>
> $$\begin{aligned}
> P(D) &= P(D\cap A_1) + \dots + P(D\cap A_n) \\
> &= P(D\mid A_1)\cdot P(A_1) + \dots + P(D\mid A_n)\cdot P(A_n) \\
> &= \sum_{i=1}^n P(D\mid A_i)\cdot P(A_i)
> \end{aligned}$$

> **Nota**. Se voglio **invertire il condizionamento** degli eventi posso sfruttare la proprietà di simmetria. La formula della legge di Bayes dice che:
>
> $$\begin{aligned}
> P(B\mid A) &= \frac{P(A\mid B)\cdot P(B)}{P(A)}
> \end{aligned}$$
>
> Unendo la legge di Bayes con la probabilità totale otteniamo:
>
> $$\begin{aligned}
> P(C_i\mid D) &= \frac{P(D\mid C_i)\cdot P(C_i)}{\sum_{k=1}^n P(D\mid C_k)\cdot P(C_k)}
> \end{aligned}$$

---

#### Esercizio 2

In una regione una malattia colpisce il 5 per mille della popolazione. Un test è affidabile con probabilità 0.99 tanto sui sani quanto sui malati. *Cioè: per un malato il test è postivo con probabilità 0.99; per un sano il test è negativo con probabilità 0.99*.
- (a) Se il risultato di una persona è positivo, trova la probabilità che la persona sia realmente malata.
- (b) Se il risultato è negativo, trova la probabilità che la persona sia in realtà malata.

##### Risoluzione

Definiamo gli eventi:

$\begin{aligned}
M &= \{\text{"La persona ha contratto la malattia"}\} \\
N &= \{\text{"L'esito del test è risultato negativo"}\}
\end{aligned}$

Abbiamo che:

$\begin{aligned}
P(M) = 0.005, &\qquad P(M') = 0.995 \\
P(N'\mid M) = 0.99, &\qquad P(N'\mid M') = 0.01 \\
P(N\mid M') = 0.99, &\qquad P(N\mid M) = 0.01  
\end{aligned}$

- **(a)** Calcoliamo $P(M\mid N')$ applicando la **legge di Bayes**:

    $$\begin{aligned}
    P(M\mid N') &= \frac{P(N'\mid M)\cdot P(M)}{P(N'\mid M)\cdot P(M) + P(N'\mid M')\cdot P(M')} \\
    &= \frac{0.99\cdot 0.005}{0.99\cdot 0.005 + 0.01\cdot 0.995} = \boxed{33.22\%} \;.
    \end{aligned}$$

- **(b)** Calcolare $P(M\mid N)$ applicando la **legge di Bayes**:

    $$\begin{aligned}
    P(M\mid N) &= \frac{P(N\mid M)\cdot P(M)}{P(N\mid M)\cdot P(M) + P(N\mid M')\cdot P(M')} \\
    &= \frac{0.01\cdot 0.005}{0.01\cdot 0.005 + 0.99\cdot 0.995} \approx \boxed{5.075\times 10^{-5}} \;.
    \end{aligned}$$

---

#### Esercizio 3

In una regione una malattia colpisce il 4 per mille della popolazione. Un test è affidabile con probabilità 0.94 sui sani e 0.88 sui malati. Cioè: per un malato il test è postivo con probabilità 88%; per un sano il test è negativo con probabilità 0.94. Assumiamo che i test ripetuti siano indipendenti. Se due test su una persona sono risultati positivi, trova la probabilità che la persona sia malata.

##### Risoluzione

Definisco gli eventi:

$\begin{aligned}
M &= \{\text{"La persona ha contratto la malattia"}\} \\
N_i &= \{\text{"L'esito dell'}i\text{-esimo test è risultato negativo"}\}
\end{aligned}$

Il problema ci dice che:

$\begin{aligned}
P(M) = 0.004, &\qquad P(M') = 0.996 \\
P(N_i\mid M') = 0.94, &\qquad P(N_i'\mid M') = 0.06 \\
P(N_i'\mid M) = 0.88, &\qquad P(N_i\mid M) = 0.12 \\
\end{aligned}$

e che i test sono tra loro indipendenti.

Siamo interessati a calcolare $P(M\mid N_1'\cap N_2')$, cioè *"la probabilità che la persona sia malata dato che i due test hanno dato esito positivo"*.

Dato che $N_1$ e $N_2$ sono **indipendenti**:

$
P(N_1'\cap N_2'\mid M) = P(N_1'\mid M)\cdot P(N_2'\mid M) = 0.88^2 = 0.7744 \\
P(N_1'\cap N_2'\mid M') = P(N_1'\mid M')\cdot P(N_2'\mid M') = 0.06^2 = 0.0036
$

Calcoliamo la probabilità richiesta applicando la **legge di Bayes** e della **probabilità totale**:

$$\begin{aligned}
P(M\mid N_1'\cap N_2') &= \frac{P(N_1'\cap N_2'\mid M)\cdot P(M)}{P(N_1'\cap N_2'\mid M)\cdot P(M) + P(N_1'\cap N_2'\mid M')\cdot P(M')} \\
&= \frac{0.7744\cdot 0.004}{0.7744\cdot 0.004 + 0.0036\cdot 0.996} \approx \boxed{46.35\%} \;.
\end{aligned}$$

Il trucco sta nel formulare correttamente la probabilità richiesta e ricordarsi che i due test sono tra loro indipendenti.

> **Nota**. Se $A$ e $B$ sono indipendenti, allora
> $$ P(A\cap B)=P(A)\cdot P(B) $$
>
> Se inoltre $A$ e $B$ sono indipendenti **condizionatamente a $M$**, allora
> $$ P(A\cap B\mid M)=P(A\mid M)\cdot P(B\mid M) $$

---

#### Esercizio 4

L’urna $I$ contiene 5 palline bianche e 9 palline rosse. L’urna $II$ contiene 7 palline bianche e 4 rosse. Una pallina è estratta dall’urna $I$ e, senza osservare il colore, viene messa nell’urna $II$. Poi viene estratta una pallina dall’urna $II$. Trova la probabilità che la prima estratta sia rossa, sapendo che la seconda estratta sia bianca.

##### Risoluzione

Definiamo l'evento:

$
R_i = \{\text{"La pallina estratta all'}i\text{-esima estrazione è Rossa"}\}
$

Abbiamo che:

$\begin{aligned}
P(R_1)=\frac{9}{14},\qquad P(R_1')=\frac{5}{14}
\end{aligned}$

$\begin{aligned}
\textit{1° rossa, 2° bianca:}&\qquad\textit{1° bianca, 2° bianca:} \\
P(R_2'\mid R_1) = \frac{7}{11+1},&\qquad P(R_2'\mid R_1') = \frac{7+1}{11+1}
\end{aligned}$

Siamo interessati a calcolare $P(R_1\mid R_2')$ cioè *"la probabilità che la prima pallina estratta sia Rossa, dato che la seconda estratta è Bianca"*.

Calcoliamo la probabilità richiesta applicando la **legge di Bayes** e la **probabilità totale**:

$$\begin{aligned}
P(R_1\mid R_2') &= \frac{P(R_2'\mid R_1)\cdot P(R_1)}{P(R_2'\mid R_1)\cdot P(R_1) + P(R_2'\mid R_1')\cdot P(R_1')} \\
&= \frac{\frac{7}{12}\cdot\frac{9}{14}}{\frac{7}{12}\cdot\frac{9}{14} + \frac{8}{12}\cdot\frac{5}{14}} \approx \boxed{61.17\%} \;.
\end{aligned}$$

---

#### Esercizio 5

Il gruppo sanguigno $A$ può donare ai gruppi $A$, $AB$. Il gruppo $B$ può donare ai gruppi $B$, $AB$. Il gruppo $AB$ può donare solo al gruppo $AB$. Il gruppo $O$ può donare a tutti. Supponiamo che in una regione le proporzioni siano: per il gruppo $A$ il 21%; per il gruppo $B$ il 43%; per il gruppo $AB$ il 10%; per il gruppo $O$ il 26%. Trova:

(a) La probabilità che un donatore a caso possa donare il sangue a una persona a caso.
(b) La probabilità che, se un donatore puo’ donare a un altro, allora quel donatore sia del gruppo B.

##### Risoluzione

Definiamo l'evento

$$
D = \{\text{"Un donatore può donare ad un ricevente"}\}
$$

Abbiamo che:

$
P(D\mid O) = P(O) + P(A) + P(B) + P(AB) = 1.00 \\
P(D\mid A) = P(A) + P(AB) = 0.21 + 0.10 = 0.31 \\
P(D\mid B) = P(B) + P(AB) = 0.43 + 0.10 = 0.53 \\
P(D\mid AB) = P(AB) = 0.10 \\
$

- **(a)** Siamo interessati a calcolare $P(D)$, cioè *"La probabilità che un donatore a caso possa donare il sangue a una persona a caso"*.

    Calcoliamo la probabilità richiesta applicando la legge della **probabilità totale**:

    $$\begin{aligned}
    P(D) &= \sum_{x\in\{O,A,B,AB\}} P(D\mid x)\cdot P(x) \\
    &= 1.00\cdot0.26 + 0.31\cdot0.21 + 0.53\cdot0.43 + 0.10\cdot0.10 \\
    &= \boxed{0.563} \;.
    \end{aligned}$$

- **(b)** Siamo interessati a calcolare $P(B\mid D)$, cioè *"La probabilità che, se un donatore puo’ donare a un altro, allora quel donatore sia del gruppo B"*.

    Calcoliamo la probabilità richiesta applicando la **legge di Bayes**:

    $$\begin{aligned}
    P(B\mid D) &= \frac{P(D\mid B)\cdot P(B)}{P(D)} \\
    &= \frac{0.53\cdot0.43}{0.563} \approx \boxed{40.48\%} \;.
    \end{aligned}$$

---