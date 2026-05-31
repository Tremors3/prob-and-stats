## $$ \textcolor{red}{\text{Esercizi Lez. 3 - Ex 3}} $$

#### Esercizio 1

Trova la probabilità che, nel lancio di due dadi equi, escano due numeri dispari.

##### Risoluzione

- Spazio di probabilità è *Equiprobabile*.
- Gli eventi sono *Indipendenti* $\Rightarrow P(A\cap B)=P(A)\cdot P(B)$.

$$\begin{aligned}
P(D_i) &= P(\{\text{"Tiro i-esimo risulta dispari"}\}) = \frac{3}{6} = \frac{1}{2} \\
P(D_1\cap D_2) &= P(D_1)\cdot P(D_2) = \frac{1}{2}\cdot\frac{1}{2} = \boxed{\frac{1}{4} = 0.25} \;.
\end{aligned}$$

---

#### Esercizio 2

Fra 12 persone, trova la probabilità che almeno due abbiano lo stesso compleanno.

##### Risoluzione (*Probabilità Combinatoria*)

$$\begin{aligned}
|\Omega| &= D^R(365, 12) = \text{"Disposizioni totali dei compleanni"}. \\
|A'| &= D(365,12) = \text{"Disposizioni senza compleanni coincidenti"}.
\end{aligned}$$

$$
P(A) = \frac{D^R(365,12)-D(365,12)}{D^R(365,12)} = \boxed{1 - \frac{D(365,12)}{D^R(365,12)} \approx 0.17} \;.
$$

##### Risoluzione (*Probabilità Condizionata*)

$$
P(A') = \frac{365}{365}\cdot\frac{364}{365}\cdots\frac{365-(12-1)}{365}
 = \prod_{k=0}^{12-1} \frac{365-k}{365}
$$

$$
P(A) = 1 - P(A') = \boxed{1 - \prod_{k=0}^{12-1} \frac{365-k}{365} \approx 0.17} \;.
$$

---

#### Esercizio 3

Da un mazzo ben mescolato di 52 carte (12 “figure” e 40 carte “numeriche”), trovare la probabilità che ci siano 4 carte numeriche in una mano di 7 carte.

##### Risoluzione (*Probabilità Combinatoria*)

Spazio campionario:

$$\begin{aligned}
|\Omega| = C(52, 7) = \text{"Numero totale di pescate possibili"}.
\end{aligned}$$

I casi favorevoli si ottengono scegliendo:

- 4 carte numeriche tra le 40 disponibili;
- 3 figure tra le 12 disponibili.

$$
P(N_4) = \frac{\binom{40}{4}\cdot\binom{12}{7-4}}{\binom{52}{7}} = \frac{\frac{40!}{4!\cdot 36!}\cdot\frac{12!}{3!\cdot 9!}}{\frac{52!}{7!\cdot 45!}} \approx \boxed{0.15} \;.
$$

> **Nota**. Questo è un caso di distribuzione ipergeometrica:
> 
> $$
> P(A)=\frac{\binom{r}{k}\binom{b}{n-k}}{\binom{r+b}{n}}
> $$
> 
> dove:
> 
> - $r$ = numero di elementi del primo tipo;
> - $b$ = numero di elementi del secondo tipo;
> - $n$ = numero totale di estrazioni;
> - $k$ = numero desiderato di elementi del primo tipo.

---

#### Esercizio 4

Un programma deve collocare 7 variabili in 80 celle di memoria, mettendo ogni variabile in una cella a caso. Se c’è un conflitto (due variabili nella stessa cella), l’assegnazione deve ripetersi.

Trovare la probabilità che non ci sia alcun conflitto.

##### Risoluzione (*Probabilità Combinatoria*)

Spazio di probabilità *equiprobabile*; spazio campionario:

$$
|\Omega| = D^R(80,7) = \text{"Numero totale di disposizioni possibili"} \;.
$$

I casi favorevoli (nessun conflitto) sono le assegnazioni iniettive:

$$
|A| = D(80,7)=80\cdot79\cdot78\cdot77\cdot76\cdot75\cdot74
$$

Quindi:

$$\begin{aligned}
P(A) &= \frac{|A|}{|\Omega|} = \frac{D(80,7)}{D^R(80,7)} = \frac{80\cdot79\cdot78\cdot77\cdot76\cdot75\cdot74}{80^7}
\approx \boxed{0.763} \;.
\end{aligned}$$

> **Nota**. Forma equivalente tramite complementazione
> 
> Se $C$ è l’evento “almeno un conflitto”, allora:
> 
> $$
> P(A)=1-P(C)
> $$
> 
> ma è più semplice calcolare direttamente $P(A)$ come sopra.

---