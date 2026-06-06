## $$ \textcolor{red}{\text{Esercizi Lez. 15 - Teoria}} $$

#### Esercizio 1

Siano $S$ e $M$ variabili aleatorie discrete. $S$ modella la somma dei valori ottenuti dal lancio di due dadi; mentre $M$ modella il massimo valore ottenuto dal lancio di due dadi.

Calcolare:
- $p_{S,M}(s,m)$;
- $p_{S,M}(2,1)$;
- $p_{S,M}(3,2)$;
- $p_S(7)$;
- $p_M(5)$;
- $F(3,2)$.

##### Risoluzione

La distribuzione congiunta è:

| $s \backslash m$ | 1 | 2 | 3 | 4 | 5 | 6 |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| 2  | $\frac1{36}$ | 0 | 0 | 0 | 0 | 0 |
| 3  | 0 | $\frac2{36}$ | 0 | 0 | 0 | 0 |
| 4  | 0 | $\frac1{36}$ | $\frac2{36}$ | 0 | 0 | 0 |
| 5  | 0 | 0 | $\frac2{36}$ | $\frac2{36}$ | 0 | 0 |
| 6  | 0 | 0 | $\frac1{36}$ | $\frac2{36}$ | $\frac2{36}$ | 0 |
| 7  | 0 | 0 | 0 | $\frac2{36}$ | $\frac2{36}$ | $\frac2{36}$ |
| 8  | 0 | 0 | 0 | $\frac1{36}$ | $\frac2{36}$ | $\frac2{36}$ |
| 9  | 0 | 0 | 0 | 0 | $\frac2{36}$ | $\frac2{36}$ |
| 10 | 0 | 0 | 0 | 0 | $\frac1{36}$ | $\frac2{36}$ |
| 11 | 0 | 0 | 0 | 0 | 0 | $\frac2{36}$ |
| 12 | 0 | 0 | 0 | 0 | 0 | $\frac1{36}$ |

- **Calcolo di $p_{S,M}(s,m)$**

    $$
    p_{S,M}(s,m)=
    \begin{cases}
    \dfrac1{36} & s=2m \\[6pt]
    \dfrac2{36} & m<s<2m \\[6pt]
    0 & \text{altrimenti}
    \end{cases}
    $$

- **Calcolo di $p_{S,M}(2,1)$**

    $$
    p_{S,M}(2,1)=\frac1{36}.
    $$

- **Calcolo di $p_{S,M}(3,2)$**

    $$
    p_{S,M}(3,2)=\frac2{36}=\frac1{18}.
    $$

- **Calcolo di $p_S(7)$**

    $$\begin{aligned}
    p_S(7)
    &= \sum_m p_{S,M}(7,m) \\
    &= \frac2{36}+\frac2{36}+\frac2{36} \\
    &= \frac6{36}
    = \boxed{\frac16}.
    \end{aligned}$$

- **Calcolo di $p_M(5)$**

    $$\begin{aligned}
    p_M(5)
    &= \sum_s p_{S,M}(s,5) \\
    &= \frac2{36}+\frac2{36}+\frac2{36}+\frac2{36}+\frac1{36} \\
    &= \frac9{36}
    = \boxed{\frac14}.
    \end{aligned}$$

- **Calcolo di $F(3,2)$**

    $$\begin{aligned}
    F(3,2)
    &= P(S\le3,M\le2) \\
    &= \frac1{36}+\frac1{36}+\frac1{36} \\
    &= \frac3{36}
    = \boxed{\frac1{12}}.
    \end{aligned}$$

> **Nota.**
>
> $$
> p_S(s)=\sum_m p_{S,M}(s,m),
> \qquad
> p_M(m)=\sum_s p_{S,M}(s,m).
> $$
>
> $$
> F(s,m)=P(S\le s,\,M\le m).
> $$
>
> La funzione di ripartizione congiunta corrisponde alla somma delle probabilità contenute nella “sottotabella” formata dalle righe con $S \le s$ e dalle colonne con $M \le m$ della tabella della distribuzione congiunta.

---

<div style="page-break-after: always;"></div>

#### Esercizio 2

Sia data la seguente distribuzione congiunta:

| $x \backslash y$ | 1 | 2 | 3 | 4 | $p_X(x)$ |
|:-:|:-:|:-:|:-:|:-:|:-:|
| 1 | $\frac{16}{136}$ | $\frac{3}{136}$ | $\frac{2}{136}$ | $\frac{13}{136}$ | $\to\frac{34}{136}$ |
| 2 | $\frac{5}{136}$ | $\frac{10}{136}$ | $\frac{11}{136}$ | $\frac{8}{136}$ | $\to\frac{34}{136}$ |
| 3 | $\frac{9}{136}$ | $\frac{6}{136}$ | $\frac{7}{136}$ | $\frac{12}{136}$ | $\to\frac{34}{136}$ |
| 4 | $\frac{4}{136}$ | $\frac{15}{136}$ | $\frac{14}{136}$ | $\frac{1}{136}$ | $\to\frac{34}{136}$ |
| $p_Y(y)$ | $\substack{\downarrow\\[3pt]\frac{34}{136}}$ | $\substack{\downarrow\\[3pt]\frac{34}{136}}$ | $\substack{\downarrow\\[3pt]\frac{34}{136}}$ | $\substack{\downarrow\\[3pt]\frac{34}{136}}$ | 1 |

##### Risoluzione

- **Marginali**

    Le marginali si ottengono sommando per righe e colonne:

    $$
    p_X(x)=\sum_y p_{X,Y}(x,y),
    \qquad
    p_Y(y)=\sum_x p_{X,Y}(x,y).
    $$

    Dalla tabella:

    $$\begin{aligned}
    p_X(1)=p_X(2)=p_X(3)=p_X(4)&=\boxed{\frac{34}{136}} \;.
    \\
    p_Y(1)=p_Y(2)=p_Y(3)=p_Y(4)&=\boxed{\frac{34}{136}} \;.
    \end{aligned}$$

- **Calcolo di $P(X=Y)$**

    $$\begin{aligned}
    P(X=Y)
    &= \frac{16}{136}+\frac{10}{136}+\frac{7}{136}+\frac{1}{136} \\
    &= \boxed{\frac{34}{136}} \;.
    \end{aligned}$$

<div style="page-break-after: always;"></div>

- **Calcolo di $P(1<X\le3,\;1<Y\le3)$**

    Righe $X=2,3$ e colonne $Y=1,2,3$:

    $$\begin{aligned}
    P
    &= \frac{10}{136}+\frac{11}{136}+\frac{6}{136}+\frac{7}{136} \\
    &= \boxed{\frac{34}{136}} \;.
    \end{aligned}$$

- **Calcolo di $P((X,Y)\in\{1,4\}\times\{1,4\})$**

    $$\begin{aligned}
    P
    &= p(1,1)+p(1,4)+p(4,1)+p(4,4) \\
    &= \frac{16}{136}+\frac{13}{136}+\frac{4}{136}+\frac{1}{136} \\
    &= \boxed{\frac{34}{136}.} \;.
    \end{aligned}$$

> **Nota.**
>
> Le marginali si leggono direttamente come somme di righe/colonne della tabella congiunta.
>
> Le probabilità su sottoinsiemi si ottengono sommando le celle corrispondenti alla regione richiesta.

---

#### Esercizio 3

È possibile determinare la funzione di probabilità congiunta $p_{X,Y}$ conoscendo solo le marginali $p_X$ e $p_Y$?

##### Risoluzione

$$
\boxed{\text{NO}}
$$

Infatti, conoscere le marginali significa sapere soltanto:

$$
p_X(x)=\sum_y p_{X,Y}(x,y),
\qquad
p_Y(y)=\sum_x p_{X,Y}(x,y),
$$

ma queste condizioni **non determinano univocamente** i valori della congiunta.

<div style="page-break-after: always;"></div>
