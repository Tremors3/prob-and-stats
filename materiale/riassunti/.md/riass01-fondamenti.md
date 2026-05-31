# Formulario Probabilità
$$\textbf{Fondamenti}$$

### Impostazione del problema

Si considera uno **spazio campionario**:

$$
\Omega = \{\text{tutti gli esiti possibili}\}
$$

Un **evento** è un sottoinsieme di $\Omega$:

$$
A \subseteq \Omega
$$

La probabilità di un evento $A$ è:

$$
P(A)
$$

con:

$$
0 \leq P(A) \leq 1
$$

e:

$$
P(\Omega)=1
$$

---

## Eventi e Operazioni

### Complementare

Evento “non $A$”:

$$
A^c
$$

con:

$$
A \cup A^c = \Omega
$$

$$
A \cap A^c = \emptyset
$$

---

### Unione

Evento “$A$ oppure $B$”:

$$
A \cup B
$$

---

### Intersezione

Evento “$A$ e $B$”:

$$
A \cap B
$$

---

### Eventi incompatibili (disgiunti)

Due eventi sono incompatibili se:

$$
A \cap B = \emptyset
$$

quindi non possono verificarsi insieme.

---

### Eventi indipendenti

Due eventi sono indipendenti se:

$$
P(A \cap B)=P(A)P(B)
$$

e:

$$
P(A|B)=P(A)\quad\text{o}\quad P(B|A)=P(B)
$$

Il verificarsi di uno non influenza l’altro.

---

### Eventi dipendenti

Gli eventi sono dipendenti se:

$$
P(A \cap B)\neq P(A)P(B)
$$

oppure:

$$
P(A|B)\neq P(A)\quad\text{o}\quad P(B|A)\neq P(B)
$$

Il verificarsi di uno influenza l'altro

---

## Regole fondamentali

### Regola del Complemento

$$
P(A^c)=1-P(A)
$$

---

### Regola della Somma

$$
P(A \cup B)=P(A)+P(B)-P(A \cap B)
$$

Il termine $P(A \cap B)$ viene sottratto per evitare il doppio conteggio.

---

### Somma di eventi disgiunti

Se:

$$
A \cap B=\emptyset
$$

allora:

$$
P(A \cup B)=P(A)+P(B)
$$

---

## Probabilità Condizionata

### Formula principale

Probabilità di $A$ sapendo che $B$ è avvenuto:

$$
P(A|B)=\frac{P(A \cap B)}{P(B)}
\qquad \text{con } P(B)>0
$$

---

### Regola dell’Intersezione (Prodotto)

Ricavata dalla probabilità condizionata:

$$
P(A \cap B)=P(A|B)P(B)
$$

oppure, per simmetria:

$$
P(A \cap B)=P(B|A)P(A)
$$

---

### Caso di eventi indipendenti

Se $A$ e $B$ sono indipendenti:

$$
P(A \cap B)=P(A)P(B)
$$

perchè:

$$
P(A\mid B) = P(A),\qquad P(B\mid A) = P(B)
$$

---

## Legge della Probabilità Totale

Sia $B_1,B_2,\dots,B_n$ un sistema completo di eventi:

- disgiunti due a due $(B_i \cap B_j=\emptyset \quad (i\neq j))$
- insieme formano una partizione di $\Omega$ $(\bigcup_i B_i=\Omega)$

allora:

$$
P(A)=\sum_i P(A|B_i)P(B_i)
$$

---

### Caso con due eventi

Se $B$ e $B^c$ partizionano lo spazio:

$$
P(A)=P(A|B)P(B)+P(A|B^c)P(B^c)
$$

---

## Teorema di Bayes

### Formula generale

$$
P(B_i|A)=
\frac{P(A|B_i)P(B_i)}
{\sum_j P(A|B_j)P(B_j)}
$$

Serve per “invertire” una probabilità condizionata.

---

### Caso con due eventi

$$
P(B|A)=\frac{P(A|B)P(B)}{P(A)}
$$

---

## Formule Utili con Eventi Indipendenti

### Complementari indipendenti

Se $A$ e $B$ sono indipendenti:

$$
A^c \text{ e } B
$$

sono indipendenti, così come:

$$
A^c \text{ e } B^c
$$

---

### Unione di eventi indipendenti

$$
P(A \cup B)=P(A)+P(B)-P(A)P(B)
$$

ottenuta usando:

$$
P(A \cap B)=P(A)P(B)
$$

---

## Proprietà Importanti

### Evento impossibile

$$
P(\emptyset)=0
$$

---

### Monotonia

Se:

$$
A \subseteq B
$$

allora:

$$
P(A)\leq P(B)
$$

---

### Differenza di eventi

$$
P(A\setminus B)=P(A)-P(A\cap B)
$$

---

## Riassunto Rapidissimo

| Formula | Espressione |
|---|---|
| Complemento | $P(A^c)=1-P(A)$ |
| Somma | $P(A\cup B)=P(A)+P(B)-P(A\cap B)$ |
| Condizionata | $P(A\mid B)=\frac{P(A\cap B)}{P(B)}$ |
| Intersezione | $P(A\cap B)=P(A\mid B)P(B)$ |
| Indipendenza | $P(A\cap B)=P(A)P(B)$ |
| Probabilità totale | $P(A)=\sum_i P(A\mid B_i)P(B_i)$ |
| Bayes | $P(B\mid A)=\frac{P(A\mid B)P(B)}{P(A)}$ |