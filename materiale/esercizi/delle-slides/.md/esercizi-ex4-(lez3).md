## $$ \textcolor{red}{\text{Esercizi Lez. 3 - Ex 4}} $$

#### Esercizio 1

Un sistema antincendio ha due congegni di attivazione. Il primo, quando c’è il fuoco, si attiva con probabilità 0.9. Il secondo, che lavora indipendentemente, si attiva con probabilità 0.95. Se almeno uno dei congegni si attiva, il sistema funziona. Se si sviluppa il fuoco, trova la probabilità:
- (a) che il sistema funzioni
- (b) che il sistema non funzioni
- (c) che ambedue i congegni si attivino
- (d) che solo il primo congegno si attivi

##### Risoluzione

$$\begin{aligned}
P(C_1) = \text{"Probabilità che il 1° sistema si attivi"} = 0.90 \\
P(C_2) = \text{"Probabilità che il 2° sistema si attivi"} = 0.95
\end{aligned}$$

- **(a)** Che il sistema funzioni

    1. **Primo metodo (*Regola del Complemento*)**

        $$\begin{aligned}
        P(\{\text{"Non Funzioni"}\}) &= P(C_1'\cap C_2') = (1-0.90)\cdot(1-0.95) = 0.005 \\
        P(\{\text{"Funzioni"}\}) &= 1 - P(\{\text{"Non Funzioni"}\}) = 1 - 0.005 = \boxed{0.995} \;.
        \end{aligned}$$

        La probabilità che il sistema funzioni è uguale al negato della probabilità che nessuno dei due congegni si attivino insieme.

    2. **Secondo metodo (*Calcolo delle singole probabilità*)**

        Calcoliamo separatamente:

        - $P(C_1\cap C_2') =$ "Solo il 1° si attiva"
        - $P(C_2\cap C_1') =$ "Solo il 2° si attiva"
        - $P(C_1\cap C_2) =$ "Entrambi si attivano"
        
        Sommiamo le componenti:

        $$
        \begin{aligned}
        P(\{\text{"Funzioni"}\})
        &= P(C_1\cap C_2') + P(C_2\cap C_1') + P(C_1\cap C_2) \\
        &= (0.90\cdot0.05)+(0.95\cdot0.10)+(0.90\cdot0.95) \\
        &= 0.045 + 0.095 + 0.855 \\
        &= \boxed{0.995}\;.
        \end{aligned}
        $$

        La probabilità che il sistema funzioni è uguale alla somma delle tre probabilità.

- **(b)** Che il sistema NON funzioni

    $$\begin{aligned}
    P(\{\text{"Non Funzioni"}\}) &= P(C_1'\cap C_2') = (1-0.90)\cdot(1-0.95) = \boxed{0.005} \\
    &= 1 - P(\{\text{Funzioni}\}) = 1 - 0.995 = \boxed{0.005} \;.
    \end{aligned}$$

    Anche in questo caso ci sono due metodi per risolvere il problema. Calcolare la probabilità che i due congegni NON si attivino oppure negare la probabilità che il sistema si attivi

- **(c)** Che ambedue i congegni si attivino

    $$
    P(C_1\cap C_2) = P(C_1)\cdot P(C_2) = 0.90\cdot 0.95 = \boxed{0.855} \;.
    $$

- **(d)** Che solo il primo congegno si attivi

    $$
    P(C_1\cap C_2') = P(C_1)\cdot P(C_2') = 0.90\cdot (1-0.95) = \boxed{0.045} \;.
    $$

---

#### Esercizio 2

Un lotto di 20 componenti ne contiene 5 difettosi. Vengono estratte senza rimessa due componenti. Sia $D_1$ l’evento “la prima è difettosa” e $D_2$ l’evento “la seconda è difettosa”. Trovare:
- (a) $P(D_2\mid D_1)$
- (b) $P(D_1\cap D_2)$
- (c) $P(D_1'\cap D_2)$
- (d) $P(D_2)$

##### Risoluzione

Gli eventi $D_1$ e $D_2$ sono **dipendenti**, poiché l’estrazione avviene senza rimessa.

La probabilità che la prima componente sia difettosa è:

$$
P(D_1)=\frac{5}{20}=\frac14
$$

- **(a)** Probabilità che la seconda sia difettosa sapendo che la prima è difettosa

    $$
    P(D_2\mid D_1)=\frac{5-1}{20-1}=\frac{4}{19}
    $$

    poiché, dopo aver estratto una difettosa, restano 4 componenti difettosi su 19.

- **(b)** Probabilità che entrambe siano difettose

    $$
    P(D_1\cap D_2)=P(D_1)\cdot P(D_2\mid D_1)
    =\frac14\cdot\frac4{19}
    =\boxed{\frac1{19}} \;.
    $$

- **(c)** Probabilità che la prima non sia difettosa e la seconda sia difettosa

    $$
    \begin{aligned}
    P(D_1^c\cap D_2)
    &=P(D_1^c)\,P(D_2\mid D_1^c) \\
    &=\frac{15}{20}\cdot\frac{5}{19} \\
    &=\frac34\cdot\frac5{19}
    =\boxed{\frac{15}{76}} \;.
    \end{aligned}
    $$

    Corrisponde alla pribabilità che la seconda componente pescata sia difettosa, assumendo che la prima pescata sia funzionante.

- **(d)** Probabilità che la seconda sia difettosa

    Usiamo la partizione rispetto a $D_1$:

    $$\begin{aligned}
    P(D_2) &= P(D_1\cap D_2)+P(D_1^c\cap D_2) \\
    &= \frac{1}{19}+\frac{15}{76}
    =\frac{4}{76}+\frac{15}{76}
    =\boxed{\frac14} \;.
    \end{aligned}$$

    > **Oss**. È naturale che:
    > 
    > $$
    > P(D_2)=P(D_1)=\frac14
    > $$
    > 
    > per simmetria: ogni posizione di estrazione ha la stessa probabilità di contenere un pezzo difettoso.

---

#### Esercizio 3

Un gene è composto di due alleli, ciascuno può essere di tipo $A$ oppure $a$. Nella popolazione vi sono 3 tipi di individui: di tipo $AA$, $Aa$, e $aa$. Ciascun genitore trasmette al figlio uno dei due alleli scelto a caso. Sapendo che inizialmente le proporzioni dei tre tipi sono:

$$
AA : \frac{2}{14}, \qquad Aa : \frac{4}{14} \qquad aa : \frac{8}{14}
$$

Quali saranno le proporzioni del tipo $AA$, del tipo $Aa$, del tipo $aa$ alla generazione successiva?

##### Risoluzione

Calcoliamo prima la probabilità che un allele trasmesso a caso sia $A$ oppure $a$. Ogni individuo:

- di tipo $AA$ trasmette sempre $A$;
- di tipo $Aa$ trasmette $A$ con probabilità $\frac12$;
- di tipo $aa$ trasmette sempre $a$.

Quindi:

$$
P(A)=P(AA)+\frac12 P(Aa)
=\frac{2}{14}+\frac12\cdot\frac{4}{14}
=\frac{4}{14}
=\frac27
$$

Di conseguenza:

$$
P(a)=1-P(A)=1-\frac27=\frac57
$$

Assumendo accoppiamento casuale e indipendenza tra i due alleli ereditati:

- **Tipo $AA$**

$$
P(AA)=P(A)^2=\left(\frac27\right)^2=\boxed{\frac{4}{49}} \;.
$$

- **Tipo $Aa$**

$$
P(Aa)=2P(A)P(a)=2\cdot\frac27\cdot\frac57=\boxed{\frac{20}{49}} \;.
$$

- **Tipo $aa$**

$$
P(aa)=P(a)^2=\left(\frac57\right)^2=\boxed{\frac{25}{49}} \;.
$$

---

#### Esercizio 4

Il gruppo sanguigno $A$ può donare il sangue ad $A$, ad $AB$. Il gruppo $B$ può donare a $B$, ad $AB$. Il gruppo $AB$ può donare ad $AB$. Il gruppo $0$ può donare a tutti. Se in una regione le proporzioni dei gruppi sono $P(A) = 0.20, P(B) = 0.50, P(AB) = 0.10, P(0) = 0.20$ inoltre se $D$ è l’evento "poter donare a un altro scelto a caso", trovare:

- (a) Le quattro seguenti probabilità condizionate:

    $$
    P(D\mid A),\;P(D\mid B),\;P(D\mid AB),\;P(D\mid 0)
    $$

- (b) La probabilità di $D$.

##### Risoluzione (*Legge della Probabilità Totale*)

- **(a)** Calcolo delle probabilità di poter donare ad un individuo a caso sapendo di apartenere al:

    1. **gruppo** $A$.

        $$
        P(D\mid A) = P(A) + P(AB) = 0.20 + 0.10  = \boxed{0.30} \;.
        $$

    2. **gruppo** $B$.

        $$
        P(D\mid B) = P(B) + P(AB) = 0.50 + 0.10  = \boxed{0.60} \;.
        $$
    
    3. **gruppo** $AB$.


        $$
        P(D\mid AB) = AB = 0.10  = \boxed{0.10} \;.
        $$

    4. **gruppo** $0$.

        $$
        P(D\mid0) = P(0) + P(A) + (B) + P(AB)  = \boxed{1.00} \;.
        $$

- **(b)** Probabilità totale di poter donare:

    Abbiamo che:

    - $P(D\cap 0) = P(D\mid 0)\cdot P(0) = 0.30\cdot0.20 = 0.06$
    - $P(D\cap A) = P(D\mid A)\cdot P(A) = 0.60\cdot0.50 = 0.30$
    - $P(D\cap B) = P(D\mid B)\cdot P(B) = 0.10\cdot0.10 = 0.01$
    - $P(D\cap AB) = P(D\mid AB)\cdot P(AB) = 1.0\cdot0.20 = 0.20$

    Somma ponderata della probabilità di donare ad un individuo a caso in base al gruppo sanguigno. Usiamo la **legge della probabilità totale**:

    $$\begin{aligned}
    P(D) &= P(D\cap A) + P(D\cap B) + P(D\cap AB) + P(D\cap 0) \\
    &= 0.06+0.30+0.01+0.20 \\
    &= \boxed{0.57} \;.
    \end{aligned}$$

---

#### Esercizio 5

In una scuola il $15$% degli alunni porta occhiali. Se uno non porta occhiali, allora pratica uno sport con probabilità $0.7$; se uno porta occhiali, pratica uno sport con probabilità $0.45$. Trova la probabilità che un alunno scelto a caso pratichi uno sport.

##### Risoluzione (*Legge della Probabilità Totale*)

Definiamo

$$\begin{aligned}
P(O) &= \text{"Probabilità occhiali"} = 0.15 \\
P(S\mid O) &= \text{"Probabilità sport se porta occhiali"} = 0.45 \\
P(S\mid O') &= \text{"Probabilità sport se NON porta occhiali"} = 0.70 \\
\end{aligned}$$

Allora calcoliamo le seguenti probabilità:

$$\begin{aligned}
P(S\cap O) &= P(O)\cdot P(S\mid O) = 0.15 \cdot 0.45 = 0.0675 \\
P(S\cap O') &= P(O')\cdot P(S\mid O') = 0.85 \cdot 0.70 = 0.595 \\
\end{aligned}$$

Usiamo la **legge della probabilità totale**:

$$\begin{aligned}
P(S) &= P(S\cap O) + P(S\cap O') \\
&= 0.0675 + 0.595 \\
&= \boxed{0.6625} \;.
\end{aligned}$$

> **Nota**. Dati $A_1,A_2,\dots,A_n$ eventi **disgiunti due a due** ($A_i\cap A_j=\emptyset$) che compongono una **partizione** di $\Omega$ ($A_1\cup\dots\cup A_n = \Omega$). La formula della legge della probabilità totale dice che:
>
> $$\begin{aligned}
> P(D) &= P(D\cap A_1) + \dots + P(D\cap A_n) \\
> &= P(D\mid A_1)\cdot P(A_1) + \dots + P(D\mid A_n)\cdot P(A_n)
> \end{aligned}$$

---