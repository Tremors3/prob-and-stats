## $$ \textcolor{red}{\text{Esercizi Lez. 5 - Ex 6}} $$

#### Esercizio 1

Sia $X$ = "La somma dei due numeri uscenti dal lancio di due dadi equi". Descrivere:

- (a) La funzione di probabilità $p_X(x)=P(X=x)$;

- (b) La funzione di distribuzione $F_X(x)=P(X\le x)$.

##### Risoluzione

Lo spazio di probabilità è *equiprobabile*. Definisco lo spazio campionario:

$$
\Omega = \{(1,1),\dots,(6,6)\},\quad |\Omega| = 36
$$

Definisco il supporto della variabile aleatoria $X$:

$$
S_X = \{ 2,3,\dots,12 \}
$$


- **(a)** Calcoliamo la funzione di probabilità $p_X(x)$ per ciascun punto nel supporto di $X$:
        
    $$\begin{aligned}
    p_X(2) &= P(X=2) = P({(1,1)}) = \frac{1}{36} \\
    p_X(3) &= P(X=3) = P({(1,2),(2,1)}) = \frac{2}{36} \\
    p_X(4) &= P(X=4) = P({(1,3),(2,2),(3,1)}) = \frac{3}{36} \\
    p_X(5) &= P(X=5) = P({(1,4),(2,3),(3,2),(4,1)}) = \frac{4}{36} \\
    p_X(6) &= P(X=6) = P({(1,5),(2,4),(3,3),(4,2),(5,1)}) = \frac{5}{36} \\
    p_X(7) &= P(X=7) = P({(1,6),(2,5),(3,4),(4,3),(5,2),(6,1)}) = \frac{6}{36} \\
    \end{aligned}$$

    $$\begin{aligned}
    p_X(8) &= P(X=8) = P(\{(2,6),(3,5),(4,4),(5,3),(6,2)\}) = \frac{5}{36} \\
    p_X(9) &= P(X=9) = P(\{(3,6),(4,5),(5,4),(6,3)\}) = \frac{4}{36} \\
    p_X(10) &= P(X=10) = P(\{(4,6),(5,5),(6,4)\}) = \frac{3}{36} \\
    p_X(11) &= P(X=11) = P(\{(5,6),(6,5)\}) = \frac{2}{36} \\
    p_X(12) &= P(X=12) = P(\{(6,6)\}) = \frac{1}{36}
    \end{aligned}$$

    Quindi, in generale:

    $$
    p_X(x) = \begin{cases}
    \frac{x-1}{36} & 2\le x\le7 \\
    \frac{13 - x}{36} &  8\le x\le12 \\
    0 & \text{altrimenti}
    \end{cases}
    $$


- **(b)** Calcoliamo la funzione di distribuzione $F_X$:

    $$
    F_X(x)=
    \begin{cases}
    0 & x<2 \\[6pt]
    \frac{1}{36} & 2\le x<3 \\[6pt]
    \frac{1+2}{36}=\frac{3}{36} & 3\le x<4 \\[6pt]
    \frac{1+2+3}{36}=\frac{6}{36} & 4\le x<5 \\[6pt]
    \frac{1+2+3+4}{36}=\frac{10}{36} & 5\le x<6 \\[6pt]
    \frac{1+2+3+4+5}{36}=\frac{15}{36} & 6\le x<7 \\[6pt]
    \frac{1+2+3+4+5+6}{36}=\frac{21}{36} & 7\le x<8 \\[6pt]
    \frac{26}{36} & 8\le x<9 \\[6pt]
    \frac{30}{36} & 9\le x<10 \\[6pt]
    \frac{33}{36} & 10\le x<11 \\[6pt]
    \frac{35}{36} & 11\le x<12 \\[6pt]
    1 & x\ge12
    \end{cases}
    $$

---

#### Esercizio 2

Una v.a. $X$ = "numero di sportivi tra 5 adulti di città" ha la funzione distribuzione $F(x)$ tale che

$$
F (0) = 0.08,\; F (1) = 0.34,\; F (2) = 0.68, \\ F (3) = 0.91,\; F (4) = 0.99,\; F (5) = 1
$$

Trova la funzione di probabilità.

##### Risoluzione

Calcoliamo la funzione di probabilità $p_X(x)$ nei vari intervalli a partire dai valori della funzione di distribuzione $F_X(x)$:

$$\begin{aligned}
p_X(0) &= 0.08 - 0 = 0.08 \\
p_X(1) &= 0.34 - 0.08 = 0.26 \\
p_X(2) &= 0.68 - 0.34 = 0.34 \\
p_X(3) &= 0.91 - 0.68 = 0.23 \\
p_X(4) &= 0.99 - 0.91 = 0.08 \\
p_X(5) &= 1.00 - 0.99 = 0.01
\end{aligned} \Rightarrow
p_X(x) = \begin{cases}
0.08 & x=0 \\
0.26 & x=1 \\
0.34 & x=2 \\
0.23 & x=3 \\
0.08 & x=4 \\
0.01 & x=5
\end{cases}
$$

Verifichiamo che la somma delle singole probabilità faccia uno:

$$
0.08+0.26+0.34+0.23+0.08+0.01 = 1.0\quad\text{ok}
$$

> **Nota**. La regola per passare da $F(x)$ a $p(x)$ per una variabile discreta:
>
> $$ p(x) = \nabla F(x) = F(x) - F(x^-) $$
>
> cioè il "salto" della funzione di distribuzione nel punto $x$. 

---