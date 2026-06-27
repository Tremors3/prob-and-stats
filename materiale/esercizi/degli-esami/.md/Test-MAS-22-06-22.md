## $$ \textcolor{red}{\text{Esercizi Esame Test-MAS-22-06-22}} $$

#### Esercizio 1

Si calcola che un individuo beve, in media, $2$ Litri d’acqua durante un’escursione in montagna, con una deviazione standard di $0.8$ Litri. Un gruppo di $64$ persone decide di portare $130$ Litri d'acqua alla prossima escursione. Qual è la probabilità che la riserva d’acqua non sarà sufficiente?

##### Risoluzione

Definiamo la generica variabile aleatoria associata al consumo di ciascun individuo.

$$
X_i \sim N(2, 0.8^2)
$$

La somma di variabili aleatorie Normali indipendenti è ancora una Normale, con media e varianza pari alla somma delle medie e delle varianze delle singole variabili.

$$
\begin{aligned}
X_1 + \ldots + X_{64}
&\sim N(2 \times 64, \, 0.64 \times 64) \\
&\sim N(128, \, 40.96)
\end{aligned}
$$

Calcoliamo la probabilità richiesta.

$$
\begin{aligned}
P(X > 130)
&= 1 - P(X \le 130) \\
&= 1 - \Phi\left(\frac{130 - 128}{\sqrt{40.96}}\right) \\
&= 1 - \Phi(0.3125) \\
&\approx 1 - 0.62267 \\
&= \boxed{0.37733} \;.
\end{aligned}
$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 2

Un supermercato riceve una fornitura di $20$ cartoni di latte. Si viene a sapere che $3$ di essi sono danneggiati e non possono essere venduti. Il magazziniere sceglie $5$ cartoni a caso per l’ispezione. Qual è la probabilità che tra i $5$ cartoni ispezionati ce ne sia al più uno danneggiato?

##### Risoluzione

Poiché i $5$ cartoni vengono scelti a caso senza reimmissione, modelliamo il problema mediante una distribuzione Ipergeometrica.

$$
X \sim \text{Hyper}(r = 3, \, b = 17, \, n = 5)
$$

Calcoliamo la probabilità richiesta.

$$
\begin{aligned}
P(X \le 1)
&= P(X = 0) + P(X = 1) \\
&= \frac{\binom{3}{0}\binom{17}{5}}{\binom{20}{5}} +
\frac{\binom{3}{1}\binom{17}{4}}{\binom{20}{5}} \\
&= \frac{6188 + 7140}{15504} \\
&\approx \boxed{85.96\%} \;.
\end{aligned}
$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 3

Mario ha tre monete, delle quali: la prima è equa, la seconda è truccata e dà testa con una probabilità del $75\%$ e la terza ha testa su entrambe le facce. Mario pesca una moneta a caso tra le tre e la lancia. Esce testa. Qual è la probabilità che la moneta lanciata sia quella avente testa su entrambe le facce?

##### Risoluzione

Definiamo le tre monete:

- Moneta equa $M_1$:

    $$\begin{aligned}
    P(T) = 0.5, &\quad& P(T') = 0.5
    \end{aligned}$$

- Moneta truccata $M_2$:

    $$\begin{aligned}
    P(T) = 0.75, &\quad& P(T') = 0.25
    \end{aligned}$$

- Moneta con due teste $M_3$:

    $$\begin{aligned}
    P(T) = 1.00, &\quad& P(T') = 0.00
    \end{aligned}$$

Calcoliamo la probabilità di ottenere testa, indipendentemente dalla moneta estratta, applicando la legge della probabilità totale.

$$
\begin{aligned}
P(T)
&= P(T \mid M_1)P(M_1) + P(T \mid M_2)P(M_2) + P(T \mid M_3)P(M_3) \\
&= \frac13(0.5 + 0.75 + 1.00) \\
&= \frac34
\end{aligned}
$$

Calcoliamo ora la probabilità richiesta applicando la formula di Bayes.

$$
\begin{aligned}
P(M_3 \mid T)
&= \frac{P(T \mid M_3)P(M_3)}{P(T)}
= \frac{1 \cdot \frac13}{\frac34}
= \boxed{\frac49} \;.
\end{aligned}
$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 4

Siano X e Y due variabili aleatorie la cui funzione di probabilità congiunta è data dalla tabella seguente:

| $Y \setminus X$ | -1 | 0 | 1 |
|:-:|:-:|:-:|:-:|
| -1 | $\frac3{24}$ | $\frac6{24}$ | $\frac9{24}$ |
|  1 | $\frac1{24}$ | $\frac2{24}$ | $\frac3{24}$ |

Quale delle seguenti affermazioni è vera?

1. X e Y sono indipendenti e scorrelate
2. X e Y sono dipendenti e scorrelate
3. X e Y sono indipendenti e positivamente correlate
4. X e Y sono dipendenti e positivamente correlate

##### Risoluzione

Per prima cosa calcoliamo le distribuzioni marginali.

| $Y \setminus X$ | -1 | 0 | 1 | $p_Y(y)$ |
|:-:|:-:|:-:|:-:|:-:|
| -1 | $\frac3{24}$ | $\frac6{24}$ | $\frac9{24}$ | $\frac{18}{24}$ |
|  1 | $\frac1{24}$ | $\frac2{24}$ | $\frac3{24}$ | $\frac6{24}$ |
| $p_X(x)$ | $\frac4{24}$ | $\frac8{24}$ | $\frac{12}{24}$ | $1$ |

Verifichiamo che la condizione di indipendenza sia soddisfatta per ogni coppia $(x,y)$.

$$
p_{X,Y}(x,y) = p_X(x)\,p_Y(y) \qquad \forall (x,y)\in S_X \times S_Y
$$

Poiché la relazione è verificata per tutte le coppie, le variabili $X$ e $Y$ sono indipendenti. Inoltre, l'indipendenza implica la scorrelazione.

$$
\boxed{
X \text{ e } Y \text{ sono \textbf{indipendenti} e \textbf{scorrelate}}
} \;.
$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 5

Siano $X$ ed $Y$ due variabili aleatorie indipendenti con distribuzione $X \sim U(0,1)$ e $Y \sim \text{Exp}(1)$. Calcolare la densità di probabilità $f_Z(z), \, z\in\R$ della variabile aleatoria somma $Z := X + Y$.

##### Risoluzione

Innanzitutto ricaviamo le densità delle due variabili aleatorie.

$$
f_X(x) = 1,
\qquad 0 \le x \le 1
$$

$$
f_Y(y) = e^{-y},
\qquad y \ge 0
$$

Per determinare gli estremi di integrazione, osserviamo che le densità sono non nulle se e solo se:

$$
0 \le x \le 1
\qquad\text{e}\qquad
z - x \ge 0
\iff x \le z
$$

Pertanto,

$$
x \in [0,1] \cap (-\infty, z]
= [0, \min\{1,z\}]
$$

da cui si distinguono i seguenti casi:

$$
\begin{cases}
0 < z \le 1 &\Longrightarrow x \in [0,z] \\
z > 1 &\Longrightarrow x \in [0,1]
\end{cases}
$$

Applichiamo la formula di convoluzione per ottenere la densità cercata.

$$
f_Z(z)
= \int_{-\infty}^{+\infty}
f_X(x)f_Y(z-x)\,dx
$$

<div style="page-break-after: always;"></div>

Caso $0 < z \le 1$.

$$
\begin{aligned}
f_Z(z)
&= \int_{0}^{z} 1 \cdot e^{-(z-x)} \,dx \\
&= e^{-z}\int_{0}^{z} e^x \,dx \\
&= e^{-z} \left[ e^x \right]_0^z \\
&= e^{-z} (e^z - 1) \\
&= 1 - e^{-z}
\end{aligned}
$$

Caso $z > 1$.

$$
\begin{aligned}
f_Z(z)
&= \int_{0}^{1} 1 \cdot e^{-(z-x)} \,dx \\
&= e^{-z}\int_{0}^{1} e^x \,dx \\
&= e^{-z} \left[ e^x \right]_0^1 \\
&= e^{-z} (e - 1)
\end{aligned}
$$

Pertanto,

$$
\boxed{
f_Z(z)=
\begin{cases}
0 & z \le 0 \\
1-e^{-z} & 0 < z \le 1 \\
(e-1)e^{-z} & z > 1
\end{cases}
} \;.
$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 6

Siano $A$, $B$ e $C$ tre eventi tali che $P(A) = 1/3$, $P(B) = 1/4$ e $P(C) = 1/2$, $P(A \cup B \cup C) = 1$, $P(A \cap C) = 0$, $P(B \cap C) = 0$.

Quale delle quattro affermazioni seguenti è falsa?

1. $P(B \cup C \mid A) = P(C \mid A)$
2. $A$ e $B$ sono indipendenti
3. $P(A \cup B) = P(C)$
4. $P(A \cup C) = P(A) + P(C)$

##### Risoluzione

Dalle ipotesi, gli eventi $A$ e $C$ sono incompatibili, così come $B$ e $C$. Applicando la formula dell'unione:

$$
\begin{aligned}
1
&= P(A \cup B \cup C) \\
&= P(A) + P(B) + P(C) - P(A \cap B) \\
&= \frac13 + \frac14 + \frac12 - P(A \cap B)
\end{aligned}
$$

da cui otteniamo:

$$
P(A \cap B)
= \frac13 + \frac14 + \frac12 - 1
= \frac1{12}
$$

Verifichiamo ora le quattro affermazioni.

1. Poiché $A \cap C = \varnothing$:

    $$
    P(B \cup C \mid A)
    = P(B \mid A)
    \neq 0
    = P(C \mid A)
    $$

2. Si ha:

    $$
    P(A)P(B)
    = \frac13 \cdot \frac14
    = \frac1{12}
    = P(A \cap B)
    $$

    quindi $A$ e $B$ sono indipendenti.

3. Calcoliamo:

    $$
    P(A \cup B)
    = P(A) + P(B) - P(A \cap B)
    = \frac13 + \frac14 - \frac1{12}
    = \frac12
    = P(C)
    $$

4. Poiché $A \cap C = \varnothing$:

    $$
    P(A \cup C)
    = P(A) + P(C)
    $$

Pertanto, l'unica affermazione falsa è:

$$
\boxed{
P(B \cup C \mid A) = P(C \mid A)
}
\;.
$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 7

Sia $X$ una variabile aleatoria di Pareto di parametro $11$, $X \sim \text{Par}(11)$, calcolare la varianza di

$$
Y = \frac{6X^5-7}{5}
$$

##### Risoluzione

Innanzitutto semplifichiamo la varianza richiesta.

$$
\begin{aligned}
\mathrm{Var}(Y)
&= \mathrm{Var}\left(\frac15(6X^5-7)\right) \\
&= \left(\frac15\right)^2 \mathrm{Var}(6X^5-7) \\
&= \frac1{25} \cdot 6^2 \mathrm{Var}(X^5) \\
&= \frac{36}{25}\mathrm{Var}(X^5)
\end{aligned}
$$

Per una distribuzione di Pareto con parametro $\alpha = 11$, la densità è:

$$
f_X(x) = 11x^{-12},
\qquad x \ge 1
$$

Calcoliamo il quinto e il decimo momento.

$$
\begin{aligned}
E[X^5]
&= \int_1^{+\infty} x^5 f_X(x)\,dx \\
&= \int_1^{+\infty} x^5 \cdot 11x^{-12}\,dx \\
&= 11 \int_1^{+\infty} x^{-7}\,dx \\
&= 11 \left[-\frac{x^{-6}}{6}\right]_1^{+\infty} \\
&= \frac{11}{6}
\end{aligned}
$$

$$
\begin{aligned}
E[X^{10}]
&= \int_1^{+\infty} x^{10} f_X(x)\,dx \\
&= \int_1^{+\infty} x^{10} \cdot 11x^{-12}\,dx \\
&= 11 \int_1^{+\infty} x^{-2}\,dx \\
&= 11 \left[-x^{-1}\right]_1^{+\infty} \\
&= 11
\end{aligned}
$$

Calcoliamo quindi la varianza di $X^5$.

$$
\begin{aligned}
\mathrm{Var}(X^5)
&= E[X^{10}] - (E[X^5])^2 \\
&= 11 - \left(\frac{11}{6}\right)^2 \\
&= \frac{275}{36}
\end{aligned}
$$

Infine,

$$
\begin{aligned}
\mathrm{Var}(Y)
&= \frac{36}{25}\mathrm{Var}(X^5) \\
&= \frac{36}{25} \cdot \frac{275}{36} \\
&= \boxed{11} \;.
\end{aligned}
$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 8

Sia $X$ una variabile aleatoria (assolutamente) continua la cui funzione di densità è data da

$$
f_X (x) =
\begin{cases}
\frac{6x}{a^2} - \frac{6x^2}{a^3} & \text{per } 0 < x \le a \\
0 & \text{altrimenti}
\end{cases}
$$

per qualche $a > 0$. Per quali valori di $a$ l’aspettazione di $X$ coincide con il suo momento secondo, ovvero $E[X] = E[X^2]$?

##### Risoluzione

Calcoliamo l'aspettazione e il momento secondo.

$$
\begin{aligned}
E[X]
&= \int_0^a x \cdot \left( \frac{6x}{a^2} - \frac{6x^2}{a^3} \right) \,dx \\
&= \int_0^a \left( \frac{6x^2}{a^2} - \frac{6x^3}{a^3} \right) \,dx \\
&= \frac6{a^2}\int_0^a x^2 \,dx - \frac6{a^3} \int_0^a x^3 \,dx \\
&= \frac6{a^2} \left[\frac{x^3}3\right]_0^a - \frac6{a^3} \left[\frac{x^4}4\right]_0^a \\
&= \frac2{a^2} a^3 - \frac3{2a^3} a^4 \\
&= 2a - \frac32 a \\
&= \frac12 a
\end{aligned}
$$

$$
\begin{aligned}
E[X^2]
&= \int_0^a x^2 \cdot \left( \frac{6x}{a^2} - \frac{6x^2}{a^3} \right) \,dx \\
&= \int_0^a \left( \frac{6x^3}{a^2} - \frac{6x^4}{a^3} \right) \,dx \\
&= \frac6{a^2}\int_0^a x^3 \,dx - \frac6{a^3} \int_0^a x^4 \,dx \\
&= \frac6{a^2} \left[\frac{x^4}4\right]_0^a - \frac6{a^3} \left[\frac{x^5}5\right]_0^a \\
&= \frac3{2a^2} a^4 - \frac6{5a^3} a^5 \\
&= \frac32 a^2 - \frac65 a^2 \\
&= \frac3{10} a^2
\end{aligned}
$$

Imponiamo ora la condizione richiesta.

$$
\begin{aligned}
E[X] &= E[X^2] \\
\frac12 a &= \frac3{10} a^2 \\
0 &= \frac3{10} a^2 - \frac12 a \\
0 &= a\left(\frac3{10}a - \frac12\right)
\end{aligned}
$$

Le soluzioni sono:

$$
a = 0
\qquad \text{oppure} \qquad
\frac3{10}a = \frac12
\Longrightarrow
a = \frac53
$$

Poiché per ipotesi $a > 0$, otteniamo:

$$
\boxed{a = \frac53} \;.
$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 9

Sia $X$ una variabile aleatoria (assolutamente) continua la cui densità di probabilità è data da:

$$
f_X(x) =
\begin{cases}
\frac{1}{x} & \text{per } 1 < x \le e \\
0 & \text{altrimenti}
\end{cases}
$$

Indicare come simulare $X$ a partire da una variabile aleatoria uniforme $U \sim \mathrm{Unif}[0,1]$.

##### Risoluzione

Applichiamo il metodo dell'inversione della funzione di ripartizione.

Calcoliamo innanzitutto la funzione di distribuzione di $X$.

$$
\begin{aligned}
F_X(x)
&= \int_1^x \frac{1}{t} \,dt \\
&= \left[\ln t\right]_1^x \\
&= \ln x,
\qquad (1 \le x \le e)
\end{aligned}
$$

Poniamo ora:

$$
U = F_X(X) = \ln X
$$

da cui:

$$
\boxed{X = e^U} \;.
$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 10

Sia $X$ una Gaussiana Standard, $X \sim N(0,1)$, calcolare la densità di probabilità $f_Z(z)$ della variabile aleatoria $Z=\frac1{X^2}$.

##### Risoluzione

Notiamo subito che $g(x)=\frac1{x^2}$ non è monotona su tutto $\mathbb{R}$. Non possiamo quindi applicare direttamente il teorema di trasformazione per funzioni monotone.

Calcoliamo la funzione di ripartizione di $Z$.

$$
\begin{aligned}
F_Z(z)
&= P(Z \le z) \\
&= P\left(\frac1{X^2} \le z\right) \\
&= P\left(X^2 \ge \frac1z \right) \\
&= P\left(X \le - \frac1{\sqrt{z}} \right) +
P\left(X \ge \frac1{\sqrt{z}} \right) \\
&= F_X\left(-\frac1{\sqrt{z}}\right) + 1 - F_X\left(\frac1{\sqrt{z}}\right)
\end{aligned}
$$

Dato che $X$ è una Normale Standard, vale la simmetria:

$$
F_X(-x) = 1 - F_X(x)
$$

Quindi:

$$
\begin{aligned}
F_Z(z)
&= 1 - F_X\left(\frac1{\sqrt{z}}\right) + 1 - F_X\left(\frac1{\sqrt{z}}\right) \\
&= 2\left(1 - F_X\left(\frac1{\sqrt{z}}\right)\right)
\end{aligned}
$$

<div style="page-break-after: always;"></div>

Ricaviamo ora la densità di $Z$.

$$
\begin{aligned}
f_Z(z)
&= \frac{d}{dz}\left\{2\left(1 - F_X\left(\frac1{\sqrt{z}}\right)\right)\right\} \\
&= 2\left(-f_X\left(\frac1{\sqrt{z}}\right)\left(-\frac{1}{2z^{3/2}}\right)\right) \\
&= \frac{1}{z^{3/2}} f_X\left(\frac1{\sqrt{z}}\right)
\end{aligned}
$$

Sostituendo la densità della Normale Standard:

$$
\begin{aligned}
f_Z(z)
&= \frac{1}{z^{3/2}}
\frac{1}{\sqrt{2\pi}}
e^{-\frac12\left(\frac1{\sqrt{z}}\right)^2} \\
&= \boxed{
\frac{1}{\sqrt{2\pi z^3}}
e^{-\frac{1}{2z}},
\qquad z > 0
} \;.
\end{aligned}
$$

---

<div style="page-break-after: always;"></div>