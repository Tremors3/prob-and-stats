# Variabili Alteatorie Discrete

### Definizione

Una variabile aleatoria discreta è proprio una funzione

$$
X : \Omega \to \R
$$

che ad ogni **esito elementare** $\omega\in\Omega$ associa un numero reale.

---

### Funzione di Probabilità

La funzione di probabilità

$$
p_x(x) = P(X = x)
$$

prende un valore reale $x$ e considera

$$
\{X=x\} = \{ \omega\in\Omega : X(\omega) = x \}
$$

cioè l'insieme di tutti gli esiti che vengono mandati nel valore $x$.


Questo insieme **è un evento** dello spazio campionario $\Omega$, quindi ha una probabilità.

L'insieme $\{X=x\}$ è quindi l'*"evento che contiene tutti gli esiti associati al valore $x$ (dalla funzione $X$)"*.

---

### Riassunto Utile

- Una variabile aleatoria $X$ è una funzione che associa un numero reale ad ogni esito:

    $$
    X:\Omega\in\R
    $$

    - dato un **esito** $\to$ otteniamo un **valore reale** $X(\omega)$.

- La funzione di probabilità fa il ragionamento opposto:

    $$
    p_X(x) = P(X=x)
    $$

    - dato un **valore reale** $x$ $\to$ otteniamo la probabilità dell'evento formato da tutti gli esiti associati a quel valore.

        $$
        \{X=x\} = \{ \omega\in\Omega : X(\omega) = x \}
        $$

L’insieme dei valori reali che la variabile aleatoria può assumere con probabilità positiva prende il nome di **supporto** della variabile aleatoria $X$.

$$
S_X=\{x\in\mathbb{R} : P(X=x)>0\}
$$

---

### Funzione di Distribuzione

La funzione di distribuzione di una variabile aleatoria:

$$
F_X(x) = P(X\le x)
$$

esprime la probabilità cumulata fino al valore x.

- dato un **valore reale** $x$ $\to$ dice quanto è probabile che la funzione assuma un valore **minore o uguale** ad $x$.

---