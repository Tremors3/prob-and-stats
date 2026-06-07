## $$ \textcolor{red}{\text{Esercizi Lez. 15 - Teoria}} $$

### $$ \textcolor{blue}{\text{Casi Discreti}} $$

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

<div style="page-break-after: always;"></div>

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

### $$ \textcolor{blue}{\text{Casi Continui}} $$

#### Esercizio 4

Siano $X$ ed $Y$ due v.a. a.c. la cui distribuzione congiunta è

$$
F_{X,Y}(x,y) =
\begin{cases}
1-e^{-2x}-e^{-y}+e^{-(2x+y)} & \text{per } x>0 \text{ e } y>0 \\
0 & \text{altrimenti}
\end{cases}
$$

Determinare:

1. le funzioni di distribuzione marginali di $X$ ed $Y$,
2. la funzione di densità congiunta di $X$ ed $Y$,
3. le funzioni di densità marginali di $X$ ed $Y$.

##### Risoluzione

1. **Calcolare le funzioni di distribuzione marginali di $X$ e $Y$.**

    Esistono due modi per ottenere le funzioni di distribuzione marginali.
    $\;$
    1. **Primo metodo (a partire da $F_{X,Y}$)**

        Fissata una delle due variabili, si fa tendere l'altra a $+\infty$ nella funzione di distribuzione congiunta.

        $$\begin{aligned}
        F_X(x) = P(X\le x)
        &= \lim_{y\to+\infty} F_{X,Y}(x,y) \\
        &= \lim_{y\to+\infty}
        \left(
        1-e^{-2x}-e^{-y}+e^{-2x}e^{-y}
        \right) \\
        &= 1-e^{-2x}-\underbrace{e^{-y}}_{0}
        +e^{-2x}\underbrace{e^{-y}}_{0} \\
        &= \boxed{1-e^{-2x}}
        \qquad \text{per } x>0 \;.
        \end{aligned}$$

        $$\begin{aligned}
        F_Y(y) = P(Y\le y)
        &= \lim_{x\to+\infty} F_{X,Y}(x,y) \\
        &= \lim_{x\to+\infty}
        \left(
        1-e^{-2x}-e^{-y}+e^{-2x}e^{-y}
        \right) \\
        &= 1-\underbrace{e^{-2x}}_{0}
        -e^{-y}
        +\underbrace{e^{-2x}}_{0}e^{-y} \\
        &= \boxed{1-e^{-y}}
        \qquad \text{per } y>0 \;.
        \end{aligned}$$

        Se una delle due variabili è fissata superiormente (ad esempio $Y\le y_0$), invece di fare il limite basta sostituire il valore fissato nella funzione di distribuzione congiunta.

        $\;$

    2. **Secondo metodo (a partire da $f_{X,Y}$)**

        Prima si calcolano le densità marginali $f_X$ e $f_Y$ (punto 3), poi si integrano per ottenere le rispettive funzioni di distribuzione.

        $\;$

        Dalle densità marginali ottenute al punto 3:

        $$
        f_X(x)=2e^{-2x},
        \qquad
        f_Y(y)=e^{-y}
        $$

        ricaviamo:

        $$\begin{aligned}
        F_X(x)
        &= \int_{-\infty}^{x} f_X(u)\,du \\
        &= \int_0^x 2e^{-2u}\,du \\
        &= -\left[e^{-2u}\right]_0^x \\
        &= -(e^{-2x}-1) \\
        &= \boxed{1-e^{-2x}}
        \qquad \text{per } x>0 \;.
        \end{aligned}$$

        $$\begin{aligned}
        F_Y(y)
        &= \int_{-\infty}^{y} f_Y(v)\,dv \\
        &= \int_0^y e^{-v}\,dv \\
        &= -\left[e^{-v}\right]_0^y \\
        &= -(e^{-y}-1) \\
        &= \boxed{1-e^{-y}}
        \qquad \text{per } y>0 \;.
        \end{aligned}$$

    Notiamo che i due metodi conducono agli stessi risultati.

    $\;$

2. **Calcolare la funzione di densità congiunta di $X$ ed $Y$.**

    Per ottenere la densità congiunta dalla funzione di distribuzione congiunta bisogna derivare rispetto a entrambe le variabili:

    $$
    f_{X,Y}(x,y)
    = \frac{\partial^2}{\partial x\,\partial y}
    F_{X,Y}(x,y)
    $$

    Calcoliamo quindi:

    $$\begin{aligned}
    f_{X,Y}(x,y)
    &=
    \frac{\partial^2}{\partial x\,\partial y}
    \left(
    1-e^{-2x}-e^{-y}+e^{-2x}e^{-y}
    \right) \\
    &=
    \frac{\partial}{\partial y}
    \left(
    0+2e^{-2x}-0-2e^{-2x}e^{-y}
    \right) \\
    &=
    0+0+0+2e^{-2x}e^{-y} \\
    &=
    \boxed{2e^{-(2x+y)}}
    \qquad \text{per } x>0,\;y>0 \;.
    \end{aligned}$$

    In questo caso abbiamo derivato prima rispetto a $x$ e poi rispetto a $y$, ma l'ordine può essere invertito.

    $\;$

3. **Calcolare le funzioni di densità marginali di $X$ ed $Y$.**

    Le densità marginali si ottengono integrando la densità congiunta rispetto all'altra variabile.

    $$\begin{aligned}
    f_X(x)
    &= \int_{-\infty}^{+\infty} f_{X,Y}(x,y)\,dy \\
    &= \int_0^{+\infty} 2e^{-2x}e^{-y}\,dy \\
    &= -2e^{-2x}\left[e^{-y}\right]_0^{+\infty} \\
    &= -2e^{-2x}(0-1) \\
    &= \boxed{2e^{-2x}}
    \qquad \text{per } x>0 \;.
    \end{aligned}$$

    $$\begin{aligned}
    f_Y(y)
    &= \int_{-\infty}^{+\infty} f_{X,Y}(x,y)\,dx \\
    &= \int_0^{+\infty} 2e^{-2x}e^{-y}\,dx \\
    &= -e^{-y}\left[e^{-2x}\right]_0^{+\infty} \\
    &= -e^{-y}(0-1) \\
    &= \boxed{e^{-y}}
    \qquad \text{per } y>0 \;.
    \end{aligned}$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 5

Siano $X$ ed $Y$ due v.a. a.c. la cui densità congiunta è

$$
f_{X,Y}(x,y) =
\begin{cases}
\frac{12}{5}xy(1+y) & \text{per } (x,y)\in[0,1]^2
\\[4pt]
0 & \text{altrimenti}
\end{cases}
$$

Determinare:
1. $P\!\left(\frac14 \le X \le \frac12,\; \frac13 \le Y \le \frac23\right)$
2. la funzione di distribuzione congiunta di $X$ ed $Y$ per $(x,y)\in[0,1]^2$,
3. la funzione di distribuzione marginale di $X$ per $x \in [0,1]$,
4. la funzione di densità marginale di $X$.

##### Risoluzione

Vedi prossima pagina.

<div style="page-break-after: always;"></div>

1. **Calcolare la probabilità congiunta richiesta.**

    $$\begin{aligned}
    P\left(\frac14\le X\le\frac12,\;\frac13\le Y\le\frac23\right)
    &= \int_{\frac14}^{\frac12}\int_{\frac13}^{\frac23}
    f_{X,Y}(x,y)\,dy\,dx \\
    &= \int_{\frac14}^{\frac12}\int_{\frac13}^{\frac23}
    \frac{12}{5}xy(1+y)\,dy\,dx \\
    &= \frac{12}{5}\int_{\frac14}^{\frac12}
    x\int_{\frac13}^{\frac23}(y+y^2)\,dy\,dx \\
    &= \frac{12}{5}\int_{\frac14}^{\frac12}
    x\left[\frac{y^2}{2}+\frac{y^3}{3}\right]_{\frac13}^{\frac23}\,dx \\
    &= \frac{12}{5}\int_{\frac14}^{\frac12}
    x\left(
    \frac{2}{9}+\frac{8}{81}
    -\frac{1}{18}-\frac{1}{81}
    \right)\,dx \\
    &= \frac{12}{5}\int_{\frac14}^{\frac12}
    x\cdot\frac{41}{162}\,dx \\
    &= \frac{82}{135}\int_{\frac14}^{\frac12}x\,dx \\
    &= \frac{82}{135}
    \left[\frac{x^2}{2}\right]_{\frac14}^{\frac12} \\
    &= \frac{82}{135}
    \left(
    \frac18-\frac{1}{32}
    \right) \\
    &= \frac{82}{135}\cdot\frac{3}{32}
    = \boxed{\frac{41}{720}} \;.
    \end{aligned}$$

<div style="page-break-after: always;"></div>

2. **Calcolare la funzione di distribuzione congiunta di $X$ ed $Y$ per $(x,y)\in[0,1]^2$.**

    $$\begin{aligned}
    F_{X,Y}(x,y)
    &= \int_{-\infty}^x \int_{-\infty}^y f_{X,Y}(u,v)\,dv\,du \\
    &= \int_0^x \int_0^y \frac{12}{5}uv(1+v)\,dv\,du \\
    &= \frac{12}{5}\int_0^x u \int_0^y (v+v^2)\,dv\,du \\
    &= \frac{12}{5}\int_0^x u
    \left[\frac{v^2}{2}+\frac{v^3}{3}\right]_0^y\,du \\
    &= \frac{12}{5}\int_0^x u
    \left(\frac{y^2}{2}+\frac{y^3}{3}\right)\,du \\
    &= \frac{12}{5}
    \left(\frac{y^2}{2}+\frac{y^3}{3}\right)
    \int_0^x u\,du \\
    &= \frac{12}{5}
    \left(\frac{y^2}{2}+\frac{y^3}{3}\right)
    \left[\frac{u^2}{2}\right]_0^x \\
    &= \frac{12}{5}
    \left(\frac{y^2}{2}+\frac{y^3}{3}\right)
    \frac{x^2}{2} \\
    &= \frac{6}{5}x^2
    \left(\frac{y^2}{2}+\frac{y^3}{3}\right) \\
    &= \frac{3}{5}x^2y^2+\frac{2}{5}x^2y^3.
    \end{aligned}$$

    Quindi

    $$\boxed{
    F_{X,Y}(x,y)=
    \begin{cases}
    \frac35x^2y^2+\frac25x^2y^3 & \text{per } (x,y)\in[0,1]^2
    \\[4pt]
    0 & \text{altrimenti}.
    \end{cases}
    } \;.$$

<div style="page-break-after: always;"></div>

3. **Calcolare la funzione di distribuzione marginale di $X$ per $x\in[0,1]$.**

    Esistono due modi per ottenere una funzione di distribuzione marginale.

    $\;$

    1. **Primo metodo (a partire da $F_{X,Y}$)**

        Fissata una delle due variabili, si porta l'altra al valore massimo del suo supporto.

        $$\begin{aligned}
        F_X(x)
        &= \lim_{y\to+\infty}F_{X,Y}(x,y) \\
        &= F_{X,Y}(x,1) \\
        &= \frac35x^2(1)^2+\frac25x^2(1)^3 \\
        &= \boxed{x^2} \;.
        \end{aligned}$$

        Poiché $Y$ assume valori soltanto nell'intervallo $[0,1]$, invece di calcolare il limite è sufficiente sostituire $y=1$.

        $\;$

    2. **Secondo metodo (a partire da $f_X$)**

        Dalla densità marginale di $X$ ottenuta al punto 4:

        $$
        f_X(x)=2x,
        \qquad 0\le x\le1
        $$

        otteniamo la distribuzione marginale integrando:

        $$\begin{aligned}
        F_X(x)
        &= \int_{-\infty}^{x}f_X(u)\,du \\
        &= \int_0^x 2u\,du \\
        &= \left[u^2\right]_0^x \\
        &= \boxed{x^2} \;.
        \end{aligned}$$

    I due metodi forniscono lo stesso risultato, come previsto.

<div style="page-break-after: always;"></div>

4. **Calcolare la funzione di densità marginale di $X$.**

    Per ottenere la densità marginale di $X$ integriamo la densità congiunta rispetto a $y$:

    $$\begin{aligned}
    f_X(x)
    &= \int_{-\infty}^{+\infty} f_{X,Y}(x,y)\,dy \\
    &= \int_0^1 \frac{12}{5}xy(1+y)\,dy \\
    &= \frac{12}{5}x\int_0^1 (y+y^2)\,dy \\
    &= \frac{12}{5}x
    \left[\frac{y^2}{2}+\frac{y^3}{3}\right]_0^1 \\
    &= \frac{12}{5}x
    \left(\frac12+\frac13\right) \\
    &= \frac{12}{5}x\cdot\frac56 \\
    &= \boxed{2x}
    \qquad \text{per } 0\le x\le1 \;.
    \end{aligned}$$

---

<div style="page-break-after: always;"></div>

#### Formule per distribuzioni congiunte assolutamente continue

> **Da funzione di distribuzione congiunta a densità congiunta**
>
> $$
> f_{X,Y}(x,y) =
> \frac{\partial^2}{\partial x\,\partial y}
> F_{X,Y}(x,y)
> $$
>
> Solitamente prima si deriva per $x$ e poi per $y$.
>
> ---
>
> **Da densità congiunta a distribuzione congiunta**
>
> $$
> F_{X,Y}(x,y) =
> \int_{-\infty}^{x}
> \int_{-\infty}^{y}
> f_{X,Y}(u,v)\,dv\,du
> $$
>
> Solitamente prima si integra per $v$ (y) e poi per $u$ (x).
>
> ---
>
> **Densità marginali dalla densità congiunta**
>
> $$
> f_X(x) =
> \int_{-\infty}^{+\infty}
> f_{X,Y}(x,y)\,dy
> $$
>
> $$
> f_Y(y) =
> \int_{-\infty}^{+\infty}
> f_{X,Y}(x,y)\,dx
> $$
>
> ---
>
> **Distribuzioni marginali dalla distribuzione congiunta**
>
> $$
> F_X(x) =
> \lim_{y\to+\infty}
> F_{X,Y}(x,y)
> $$
>
> $$
> F_Y(y) =
> \lim_{x\to+\infty}
> F_{X,Y}(x,y)
> $$
>
> ---

<div style="page-break-after: always;"></div>

> **Distribuzioni marginali dalle densità marginali**
>
> $$
> F_X(x) =
> \int_{-\infty}^{x}
> f_X(u)\,du
> $$
>
> $$
> F_Y(y) =
> \int_{-\infty}^{y}
> f_Y(v)\,dv
> $$
>
> ---
>
> **Procedura 1 (partendo da $F_{X,Y}$)**
>
> $$
> F_{X,Y}
> \longrightarrow
> F_X,F_Y
> \longrightarrow
> f_X,f_Y
> $$
>
> tramite limiti e successiva derivazione.
>
> ---
>
> **Procedura 2 (partendo da $F_{X,Y}$)**
>
> $$
> F_{X,Y}
> \longrightarrow
> f_{X,Y}
> \longrightarrow
> f_X,f_Y
> \longrightarrow
> F_X,F_Y
> $$
>
> tramite derivazione, marginalizzazione e integrazione.
>
> Entrambe le procedure devono produrre le stesse marginali.
