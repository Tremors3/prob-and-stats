## $$ \textcolor{red}{\text{Domande V/F di teoria}} $$

#### Test-MAS-16-06-2021

**Vero o Falso** - Indicare se le seguenti affermazioni sono vere o false.

11. Sia $X$ una variabile aleatoria assolutamente continua, allora il $0.3\text{mo}$-quantile di $X$ è sempre minore o uguale del $60\text{mo}$-percentile di $X$.

    $\;$

    **VERA**. Il $0.3$-quantile coincide con il $30$-esimo percentile. Poiché la funzione di ripartizione è monotona crescente, il $30$-esimo percentile è sempre minore o uguale al $60$-esimo percentile.

    $\;$

12. Sia $X$ una variabile aleatoria a valori in $(−\infty, 0]$ e con $E[X] = −2$, allora $P (X < 0) = 1$.

    $\;$

    **FALSA**. Una variabile aleatoria può assumere il valore $0$ con probabilità positiva pur avendo media pari a $-2$. Ad esempio:

    $$
    P(X=0)=\frac12,
    \qquad
    P(X=-4)=\frac12
    $$

    In tal caso $E[X]=-2$, ma:

    $$
    P(X<0)=\frac12 \ne 1
    $$

    *Nota. La prof ha risposto **VERO**, probabilmente assumendo che $X$ fosse assolutamente continua. In tal caso $P(X=0)=0$ e l'affermazione sarebbe effettivamente vera*.

    $\;$

13. Sia $X$ una variabile aleatoria a valori in $(−\infty, 0]$ e con $E[X] = −2$, allora $E[X^3] \ge −8$.

    $\;$

    **FALSA**. La funzione $g(x)=x^3$ è concava in $(-\infty,0)$. Applicando la disuguaglianza di Jensen otteniamo:

    $$
    E[X^3] \le (E[X])^3
    $$

    quindi:

    $$
    E[X^3] \le (-2)^3 = -8
    $$

    L'affermazione del testo è quindi **falsa**.

    $\;$

14. Siano $A$, $B$ e $C$ tre eventi dello stesso spazio di probabilità $(\Omega, \Sigma, P)$, allora $A$, $B$ e $C$ sono elementi dello spazio campionario $\Omega$.

    $\;$

    **FALSA**. Gli eventi appartengono alla $\Sigma$, cioè:

    $$
    A,B,C \in \Sigma
    $$

    mentre $\Omega$ contiene i singoli esiti elementari.

    $\;$

15. Siano $A$, $B$ e $C$ tre eventi dello stesso spazio di probabilità $(\Omega, \Sigma, P)$. Se $A$, $B$ e $C$ sono indipendenti allora sono indipendenti a due a due.

    $\;$

    **VERA**. L'indipendenza reciproca implica sempre l'indipendenza a due a due, poiché:

    $$
    P(A\cap B)=P(A)P(B)
    $$

    e analogamente per le altre coppie.

    $\;$

16. Siano $A$ e $B$ due eventi dello stesso spazio di probabilità $(\Omega, \Sigma, P)$, allora $P(A \mid B) = P (B \mid A)$.

    $\;$

    **FALSA**. In generale:

    $$
    P(A\mid B)=\frac{P(A\cap B)}{P(B)},
    \qquad
    P(B\mid A)=\frac{P(A\cap B)}{P(A)}
    $$

    Le due probabilità coincidono solo in casi particolari, ad esempio quando $P(A)=P(B)\ne0$.

---

<div style="page-break-after: always;"></div>

#### Test-MAS-22-06-22

**Vero o Falso** - Indicare se le seguenti affermazioni sono vere o false.

11. Siano $X_1, X_2, \ldots, X_n$ delle variabili aleatorie indipendenti ed identicamente distribuite come esponenziali di parametro $2$, e sia $\bar X_n = \frac1n \sum_{i=1}^n X_i$ la loro media aritmetica. Allora:

    $$
    P\left(\left|2\bar X_n - 1\right| > 1\right) \le \frac1n
    $$

    $\;$

    **VERA**. Si ha $E[X_i]=\frac12$ e $\mathrm{Var}(X_i)=\frac14$, quindi $E[2\bar X_n]=1$ e $\mathrm{Var}(2\bar X_n)=\frac1n$. Per la disuguaglianza di Chebyshev:

    $$
    P\left(\left|2\bar X_n-1\right|>1\right)
    \le \frac{\mathrm{Var}(2\bar X_n)}{1^2}
    = \frac1n
    $$

    $\;$

12. Si estraggono contemporaneamente $5$ carte da un mazzo di carte da Poker ($52$ carte: $4$ semi, $13$ carte per ogni seme). Sia $X$ la variabile aleatoria che rappresenta il numero di cuori tra le $5$ carte estratte. Allora: $X \sim \text{Bin}(5, 1/4)$.

    $\;$

    **FALSA**. Le estrazioni avvengono senza reimmissione, quindi non sono indipendenti. La distribuzione corretta è:

    $$
    X \sim \text{Hyper}(r=13,\, b=39,\, n=5)
    $$

    $\;$

13. Siano $X$, $Y$ e $Z$ tre variabili aleatorie indipendenti. Definiamo le variabili aleatorie: $X_1 = XY,\; X_2 = YZ,\; X_3 = ZX$. Allora $X_1$, $X_2$ ed $X_3$ sono indipendenti.

    $\;$

    **FALSA**. Le tre variabili condividono fattori comuni, quindi in generale non sono indipendenti.

    $\;$

14. Siano $X$ ed $Y$ due variabili aleatorie indipendenti ed identicamente distribuite come Poisson di parametro $\alpha > 0$. Allora la loro somma $X + Y$ è anch'essa una variabile aleatoria di Poisson.

    $\;$

    **VERA**. La somma di due variabili di Poisson indipendenti è ancora una Poisson:

    $$
    X+Y \sim \mathrm{Pois}(\alpha_1 + \alpha_2)
    $$

    $\;$

15. Sia $X$ una variabile aleatoria (assolutamente) continua a valori in $\mathbb R$, allora per ogni funzione $g : \mathbb R \to \mathbb R$ la nuova variabile aleatoria $Y := g(X)$ è anch'essa (assolutamente) continua.

    $\;$

    **FALSA**. Ad esempio, se $g(x)=1$, allora $Y=1$ è una variabile degenere e quindi non assolutamente continua.

    $\;$

16. Siano $A$ e $B$ due eventi qualsiasi, allora:

    $$
    P(A) = P(A \mid B)\,P(B) + P(A \mid B^c)\,P(B^c)
    $$

    $\;$

    **VERA**. Gli eventi $B$ e $B^c$ formano sempre una partizione di $\Omega$, quindi la formula segue dalla legge della probabilità totale.

    $\;$

---

<div style="page-break-after: always;"></div>

#### Test-PS-21-01-2026

**Vero o Falso** - Indicare se le seguenti affermazioni sono vere o false.

11. Siano $A$ e $B$ due eventi indipendenti. Allora: $P(A \cap B)=0$.

    $\;$

    **FALSA**. Se $A$ e $B$ sono indipendenti, allora:

    $$
    P(A \cap B)=P(A)P(B)
    $$

    L'intersezione ha probabilità nulla solo nel caso particolare in cui almeno uno dei due eventi abbia probabilità nulla.

    $\;$

12. Siano $A$ e $B$ due eventi dello stesso spazio di probabilità $(\Omega,\Sigma,P)$. Allora: $P(A \mid B)=P(B \mid A)$.

    $\;$

    **FALSA**. In generale le due probabilità condizionate non coincidono. Ad esempio, vale:

    $$
    P(A \mid B)=\frac{P(A \cap B)}{P(B)},
    \qquad
    P(B \mid A)=\frac{P(A \cap B)}{P(A)}
    $$

    quindi sono uguali solo in casi particolari, ad esempio quando $P(A)=P(B)\neq 0$.

    $\;$

13. Sia $X$ una variabile aleatoria la cui funzione generatrice dei momenti è $G_X(t)$, con $t\in\mathbb R$. Allora la variabile aleatoria $Y=3X+1$ ha funzione generatrice dei momenti: $G_Y(t)=3G_X(t)+1$.

    $\;$

    **FALSA**. La funzione generatrice dei momenti di $Y$ è:

    $$
    G_Y(t)
    = E[e^{tY}]
    = E[e^{t(3X+1)}]
    = e^t E[e^{3tX}]
    = e^t G_X(3t)
    $$

    $\;$

14. Siano $X_1$, $X_2$ e $X_3$ tre variabili aleatorie indipendenti ed identicamente distribuite come esponenziali di parametro $5$. Allora la variabile aleatoria: $X=X_1+X_2+X_3$ ha distribuzione Gamma di parametri $5$ e $3$, cioè: $X\sim\Gamma(5,3)$.

    $\;$

    **VERA**. La somma di tre variabili esponenziali indipendenti di parametro $5$ ha distribuzione Gamma con parametri $\lambda=5$ e $n=3$.

    $\;$

15. Sia $X$ una variabile aleatoria a valori in $(-\infty,0]$ e sia $F_X(\cdot)$ la sua funzione di distribuzione. Allora: $F_X(x)=0\space\forall x\ge0$.

    $\;$

    **FALSA**. Poiché $X$ assume valori soltanto in $(-\infty,0]$, per ogni $x\ge0$ vale:

    $$
    F_X(x)=P(X\le x)=1
    $$

    $\;$

16. Sia $X_1,\ldots,X_n$ un campione casuale con distribuzione di Poisson di parametro $\lambda>0$. Lo stimatore: $T_n=\frac1n\sum_{i=1}^{n}X_i$ è consistente per $\lambda$.

    $\;$

    **VERA**. Lo stimatore coincide con la media campionaria. Poiché:

    $$
    E[T_n]=\lambda,
    \qquad
    \mathrm{Var}(T_n)=\frac{\lambda}{n}\xrightarrow[n\to\infty]{}0
    $$

    esso converge in probabilità a $\lambda$ ed è quindi consistente.

---

<div style="page-break-after: always;"></div>