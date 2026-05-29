## $$ \textcolor{red}{\text{Esercizi Lez. 12 - Ex 8}} $$

#### Esercizio 1

Il numero $X$ di difetti di un certo prodotto può assumere i valori $0,1,2,3$ con rispettive probabilità

$$
P(X=0)=0.38,\quad
P(X=1)=0.29,\quad
P(X=2)=0.20,\quad
P(X=3)=0.13
$$

Trovare:

- (a) la varianza di $X$;
- (b) i valori della standardizzata di $X$.

##### Risoluzione

Calcoliamo innanzitutto $E[X]$ ed $E[X^2]$.

$$\begin{aligned}
E[X]
&= \sum_{x\in S_X} x\cdot p_X(x) \\
&= 0\cdot0.38 + 1\cdot0.29 + 2\cdot0.20 + 3\cdot0.13 \\
&= 0 + 0.29 + 0.40 + 0.39 \\
&= 1.08
\end{aligned}$$

$$\begin{aligned}
E[X^2]
&= \sum_{x\in S_X} x^2\cdot p_X(x) \\
&= 0^2\cdot0.38 + 1^2\cdot0.29 + 2^2\cdot0.20 + 3^2\cdot0.13 \\
&= 0 + 0.29 + 0.80 + 1.17 \\
&= 2.26
\end{aligned}$$

- **(a)** Calcolo della varianza:

    $$\begin{aligned}
    \mathrm{Var}(X)
    &= E[X^2] - (E[X])^2 \\
    &= 2.26 - (1.08)^2 \\
    &= \boxed{1.0936} \;.
    \end{aligned}$$

- **(b)** Calcolo della standardizzata di $X$.

    Ricordiamo che:

    $$
    z_k=\frac{x_k-\mu}{\sigma},\qquad\text{con } k\in S_X
    $$

    dove

    $$
    \mu = E[X]=1.08,
    \qquad
    \sigma=\sqrt{\mathrm{Var}(X)}=\sqrt{1.0936}\approx1.0458
    $$

    Quindi:

    $$\boxed{
    \begin{gathered}
    \begin{aligned}
    z_0 &= \frac{0-1.08}{1.0458} \approx -1.03
    &\qquad
    z_1 &= \frac{1-1.08}{1.0458} \approx -0.076
    \\
    z_2 &= \frac{2-1.08}{1.0458} \approx 0.88
    &\qquad
    z_3 &= \frac{3-1.08}{1.0458} \approx 1.84
    \end{aligned}
    \\[25pt]
    Z \sim
    \begin{pmatrix}
    -1.03 & -0.076 & 0.88 & 1.84 \\
    0.38 & 0.29 & 0.20 & 0.13
    \end{pmatrix}
    \end{gathered}
    }\;.
    $$

---

<div style="page-break-after: always;"></div>

#### Esercizio 2

Una ditta chimica vende un certo solvente in fusti da $10$ kg. Il numero $X$ di fusti acquistati da un cliente a caso è una v.a. discreta con la seguente funzione di ripartizione:

$$
F(x) : \quad
\begin{pmatrix}
1 & 2 & 3 & 4 & 5 \\
4/10 &
6/10 &
8/10 &
9/10 &
1
\end{pmatrix}
$$

Inoltre, sia $Y$ il numero di kg acquistati. Trovare:

- (a) il numero medio di fusti acquistati;
- (b) la varianza del numero di kg acquistati.

##### Risoluzione

Ricaviamo prima la funzione di probabilità partendo dalla funzione di ripartizione:

$$\begin{aligned}
p_X(1) &= F(1)=\frac4{10} \\
p_X(2) &= F(2)-F(1)=\frac{6-4}{10}=\frac2{10} \\
p_X(3) &= F(3)-F(2)=\frac{8-6}{10}=\frac2{10} \\
p_X(4) &= F(4)-F(3)=\frac{9-8}{10}=\frac1{10} \\
p_X(5) &= F(5)-F(4)=\frac{10-9}{10}=\frac1{10}
\end{aligned}$$

Quindi:

$$
p_X(x) : \quad
\begin{pmatrix}
1 & 2 & 3 & 4 & 5 \\
4/10 &
2/10 &
2/10 &
1/10 &
1/10
\end{pmatrix}
$$

- **(a)** Calcolo del numero medio di fusti acquistati:

    $$\begin{aligned}
    E[X]
    &= \sum_{x\in S_X} x\cdot p_X(x) \\
    &= 1\cdot\frac4{10} +
    2\cdot\frac2{10} +
    3\cdot\frac2{10} +
    4\cdot\frac1{10} +
    5\cdot\frac1{10} \\
    &= 0.4 + 0.4 + 0.6 + 0.4 + 0.5 \\
    &= \boxed{2.3} \;.
    \end{aligned}$$

- **(b)** Calcolo della varianza del numero di kg acquistati.

    Poiché ogni fusto contiene $10$ kg:

    $$
    Y=10X
    $$

    Calcoliamo prima $\mathrm{Var}(X)$.

    $$\begin{aligned}
    E[X^2]
    &= \sum_{x\in S_X} x^2\cdot p_X(x) \\
    &= 1^2\cdot\frac4{10} +
    2^2\cdot\frac2{10} +
    3^2\cdot\frac2{10} +
    4^2\cdot\frac1{10} +
    5^2\cdot\frac1{10} \\
    &= 0.4 + 0.8 + 1.8 + 1.6 + 2.5 \\
    &= 7.1
    \end{aligned}$$

    $$\begin{aligned}
    \mathrm{Var}(X)
    &= E[X^2]-(E[X])^2 \\
    &= 7.1-(2.3)^2 \\
    &= 7.1-5.29 \\
    &= 1.81
    \end{aligned}$$

    Infine:

    $$\begin{aligned}
    \mathrm{Var}(Y)
    &= \mathrm{Var}(10X) \\
    &= 10^2\mathrm{Var}(X) \\
    &= 100\cdot1.81 \\
    &= \boxed{181} \;.
    \end{aligned}$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 3

La funzione di distribuzione $F(x)$ di una variabile aleatoria discreta $X$ assume i valori:

$$
F(x) : \quad
\begin{pmatrix}
20 & 25 & 30 & 44 & 51 \\
0.10 & 0.40 & 0.70 & 0.80 & 1
\end{pmatrix}
$$

Trovare:

- (a) media e varianza di $X$;
- (b) i valori della v.a. standardizzata di $X$.

##### Risoluzione

Ricaviamo prima la funzione di probabilità partendo dalla funzione di distribuzione:

$$\begin{aligned}
p_X(20) &= F(20)=0.10 \\
p_X(25) &= F(25)-F(20)=0.40-0.10=0.30 \\
p_X(30) &= F(30)-F(25)=0.70-0.40=0.30 \\
p_X(44) &= F(44)-F(30)=0.80-0.70=0.10 \\
p_X(51) &= F(51)-F(44)=1.00-0.80=0.20
\end{aligned}$$

Quindi:

$$
p_X(x) : \quad
\begin{pmatrix}
20 & 25 & 30 & 44 & 51 \\
0.10 & 0.30 & 0.30 & 0.10 & 0.20
\end{pmatrix}
$$

- **(a)** Calcolo di media e varianza di $X$.

    $$\begin{aligned}
    E[X]
    &= \sum_{x\in S_X} x\cdot p_X(x) \\
    &= 20\cdot0.1 +
    25\cdot0.3 +
    30\cdot0.3 +
    44\cdot0.1 +
    51\cdot0.2 \\
    &= 2 + 7.5 + 9 + 4.4 + 10.2 \\
    &= \boxed{33.1} \;.
    \end{aligned}$$

    $$\begin{aligned}
    E[X^2]
    &= \sum_{x\in S_X} x^2\cdot p_X(x) \\
    &= 20^2\cdot0.1 +
    25^2\cdot0.3 +
    30^2\cdot0.3 +
    44^2\cdot0.1 +
    51^2\cdot0.2 \\
    &= 40 + 187.5 + 270 + 193.6 + 520.2 \\
    &= 1211.3
    \end{aligned}$$

    $$\begin{aligned}
    \mathrm{Var}(X)
    &= E[X^2]-(E[X])^2 \\
    &= 1211.3-(33.1)^2 \\
    &= 1211.3-1095.61 \\
    &= \boxed{115.69} \;.
    \end{aligned}$$

- **(b)** Calcolo dei valori della standardizzata di $X$.

    Ricordiamo che:

    $$
    z_k=\frac{x_k-\mu}{\sigma},\qquad\text{con } k\in S_X
    $$

    dove

    $$
    \mu=E[X]=33.1,
    \qquad
    \sigma=\sqrt{\mathrm{Var}(X)}=\sqrt{115.69}\approx10.756 \;.
    $$

    Quindi:

    $$
    \boxed{
    \begin{gathered}
    \begin{aligned}
    z_{20} &= \frac{20-33.1}{10.756} \approx -1.22
    &\qquad
    z_{25} &= \frac{25-33.1}{10.756} \approx -0.75
    \\
    z_{30} &= \frac{30-33.1}{10.756} \approx -0.29
    &\qquad
    z_{44} &= \frac{44-33.1}{10.756} \approx 1.01
    \\
    z_{51} &= \frac{51-33.1}{10.756} \approx 1.66
    \end{aligned}
    \\[35pt]
    Z \sim
    \begin{pmatrix}
    -1.22 & -0.75 & -0.29 & 1.01 & 1.66 \\
    0.10 & 0.30 & 0.30 & 0.10 & 0.20
    \end{pmatrix}
    \end{gathered}
    }\;.
    $$

---

<div style="page-break-after: always;"></div>