
# Approfondimento sul Teorema di Bayes

## 1 · Richiami fondamentali

### 1.1 Probabilità condizionata
Per eventi $A$ e $B$ con $P(B)>0$ vale

$$
P(A\mid B)=\frac{P(A\cap B)}{P(B)}.
$$

Questa formula esprime la probabilità che si verifichi $A$, dato che è noto che si è verificato $B$.

## 2 · Teorema di Bayes e derivazione passo‑passo

### 2.1 Caso di una singola spiegazione
La probabilità di $A$ dato $B$ è pari alla probabilità di $B$ dato $A$ per la probabilità di $A$, diviso la probabilità di $B$.

Per $P(B)>0$:
$$
\boxed{\,P(A\mid B)=\dfrac{P(B\mid A)\,P(A)}{P(B)}\,}
$$

### 2.1.1 Come la si può ottenere?
1. **Definizioni di condizionata**
   $$
   P(A\mid B)=\frac{P(A\cap B)}{P(B)},\qquad P(B\mid A)=\frac{P(A\cap B)}{P(A)}.
   $$
2. **Eguagliamo** il termine comune $P(A\cap B)$:
   $$
   P(A\cap B)=P(A\mid B)P(B)=P(B\mid A)P(A).
   $$
3. **Isoliamo** $P(A\mid B)$ dividendo per $P(B)$:
   $$
   P(A\mid B)=\frac{P(B\mid A)P(A)}{P(B)}.
   $$


### 2.2 Caso di due spiegazioni alternative

$$
P(A\mid B)=\frac{P(B\mid A)P(A)}{P(B\mid A)P(A) + P(B\mid \overline{A})P(\overline{A})}.
$$

### 2.3  Caso di più spiegazioni alternative
$$
   P(A_j\mid B)=\frac{P(B\mid A_j)P(A_j)}{\sum_{i=1}^mP(B\mid A_i)P(A_i)}, \quad j=1,\dots,m
$$

---
## 3.1 Forma pronostica

Considerando il rapporto tra l'ipotesi che $A$ si verifichi data l'evidenza $B$ e l'ipotesi che $A$ non si verifichi data l'evidenza $B$, si ottiene:


$$odds = \frac{P(A \mid B)}{P(\overline{A} \mid B)} = \frac{P(B \mid A)}{P(B \mid \overline{A})} \times \frac{P(A)}{P(\overline{A})}$$

**Interpretazione dei termini della regola di Bayes**

Dove il membro a sinistra è il pronostico finale (posterior odds) di $A$, il primo fattore nel membro di destra è il rapporto di verosimiglianza (likelihood ratio) tra $A$ e $\overline{A}$, il secondo fattore nel membro di destra è il pronostico iniziale (prior odds) di $A$ 

- Prior ($P(A)$): è la probabilità iniziale assegnata all’evento prima di osservare il dato.
Rappresenta la nostra conoscenza pregressa o il nostro grado iniziale di fiducia nell’ipotesi $A$.

- Likelihood (verosomiglianza) ($P(B \mid A)$): è la probabilità di osservare il dato $B$ nell’ipotesi che $A$ sia vera.
Indica quanto il dato sia compatibile con l’ipotesi.

- Posterior ($P(A \mid B)$): è la probabilità aggiornata, cioè la nostra nuova credenza sull’evento dopo aver osservato il dato $B$.

Ora possiamo calcolare la probabilità avendo l'odds come 
$$p = \dfrac{odds}{1+odds}$$

Si usa la forma pronostica (odds ratio) se ti interessa confrontare direttamente solo due ipotesi (ad esempio, malato vs sano, colpevole vs innocente), oppure se vuoi aggiornare facilmente le odds per più dati osservati uno dopo l’altro.

---
## 3.2 · Forma moltiplicativa

La si può riscrivere in forma moltiplicativa sostituendo l'uguaglianza con la proporzionalità e scrivendo assieme le formule per A e $\overline{A}$ con il vincolo $P(A \mid B ) + P(\overline{A} \mid B ) = 1$

$$
\boxed{\,P(A\mid B)\;\propto\;P(B\mid A)\,\times\,P(A)\,}
$$
$$
\boxed{\,P( \overline{A}\mid B)\;\propto\;P(B\mid \overline{A})\,\times\,P(\overline{A})\,}
$$

Ovvero che 
> $Posterior \propto Likelihood \times Prior$  

Si usa la forma moltiplicativa quando vuoi calcolare le probabilità a posteriori di ciascuna tra più ipotesi e vuoi che la somma sia 1. È perfetta per problemi a più di due alternative, ti da direttamente la probabilità.

---

## 4 · Esempi applicativi
### 4.1 Test diagnostico medico

Nell’ambito di una campagna di screening che mira a identificare
precocemente una malattia rara, della quale si sa che colpisce
il 2% della popolazione, un nostro amico è risultato positivo al test.
Il test funziona correttamente sul 99.9% dei soggetti malati e sul 97.5%
dei soggetti sani. Ci chiediamo quale sia la probabilità che il nostro amico sia malato.

- **Prevalenza della malattia**: $P(M)=0.02$.
- **Sensibilità del test**: $P(T\mid M)=0.999$ (verosomiglianza dell'ipotesi di malattia).
- **Specificità del test**: $P(\overline{T}\mid \overline{M})=0.975$
Otteniamo che:

- la **verosomiglianza dell'ipotesi di salute** è:  $P(\overline{T}\mid \overline{M})=0.025$
- la **probabilità di salute** è:  $P(\overline{M}) = 1 - P(M) = 1 - 0.02 = 0.98$

Si vuole calcolare la probabilità finale di malattia ovvero $P(M \mid T)$

Calcolo:

$$
P(M \mid T) = \frac{P(T \mid M) P(M)}{P(T \mid M) P(M) + P(T \mid \overline{M}) P(\overline{M})} = \frac{0.999 \times 0.02}{0.999 \times 0.02 + 0.025 \times 0.98} = \frac{1998}{4448} = 45\%
$$

Come si concilia questo risultato con le ottime prestazioni del test?
La rarità della malattia attenua la verosimiglianza $P(T \mid M)$ ovvero riduce la probabilità di essere malato e allo stesso tempo amplifica la verosimiglianza $P(T \mid \overline{M})$ ovvero la probabilità di essere sano.

Il test fornisce comunque un segnale forte: la probabilità di malattia
passa dal 2% al 45% e ciò suggerisce un approfondimento clinico

A partire da (faccio notare che si stanno usando i valori espressi in percentuali)
$$
P(M)/P(\overline{M}) = \frac{2}{98} = \frac{1}{49} \simeq 0.0204
$$

$$
P(T \mid M)/P(T \mid \overline{M}) = \frac{999}{25} \simeq 40.0
$$
troviamo
$$
\frac{P(M \mid T)}{P(\overline{M} \mid T)} =
\frac{P(T \mid M)}{P(T \mid \overline{M})} \times \frac{P(M)}{P(\overline{M})}
= \frac{999}{25} \times \frac{1}{49}
\simeq 40 \times 0.0204 = 0.816
$$
con la formula di Bayes sulla scala dei pronostici e confermiamo che
$$
P(M \mid T) = \frac{0.816}{1 + 0.816} = \frac{1}{1.816} \simeq 0.45 = 45\%.
$$
### 4.2 Classificatore Multinomial Naive Bayes

#### Cos'è il Multinomial Naive Bayes?

Il **Multinomial Naive Bayes** è un algoritmo di classificazione che si basa sul Teorema di Bayes.

1. **Indipendenza tra le feature:**  
   Il modello assume che tutte le feature (ad esempio, le parole di una mail) siano indipendenti tra loro, dato che conosciamo la classe. Questo semplifica i calcoli e rende il modello molto veloce.

2. **Distribuzione multinomiale delle feature:**  
   Il modello tiene conto di quante volte ogni parola compare nel testo, cioè usa la frequenza delle parole come conteggio.

---

#### Esempio pratico: filtraggio spam

Supponiamo di voler costruire un filtro antispam per le email:

- **Classi:** {spam, non-spam}
- **Feature:** le parole contenute in ciascuna email

---

#### Fase di addestramento

Per ciascuna parola $w_k$, stimiamo la probabilità che appaia nella classe C

$$
P(w_k \mid \text{C}) = \frac{\text{count}(w_k, \text{C}) + 1}{N_{\text{C}} + V}
$$

- $\text{count}(w_k, \text{C})$: numero di volte che $w_k$ appare nel documento "C"
- $N_{\text{spam}}$: totale delle parole nel documento "C"
- $V$: numero di parole nel vocabolario

---

### Calcolo per la mail "compra ora compra ora"

Immaginiamo di avere questi 4 messaggi di addestramento:

| Messaggio | Testo            | Classe     |
|-----------|------------------|-----------|
| M1        | compra ora è gratis       | Spam      |
| M2        | offerta limitata | Spam      |
| M3        | ci vediamo ora   | Non Spam  |
| M4        | andiamo a cena   | Non Spam  |

Supponiamo:

- Vocabolario: 12 parole
- Totale parole in spam: 6
- Totale parole in non-spam: 6

---

#### Calcolo finale (mail: "compra ora compra ora")

La mail contiene:

- "compra": 2 volte
- "ora": 2 volte

Si applica la formula del Multinomial Naive Bayes:

$$
P(C \mid \text{mail}) \propto P(C) \cdot \prod_{k=1}^V P(w_k \mid C)^{f_k}
$$

dove $f_k$ rappresenta la frequenza della parola $w_k$ nella mail.

Con Prior:

$$ P(\text{spam})=0.5, \quad P(\text{not-spam})=0.5 $$ 

Spam class:
$$
P(\text{compra} \mid \text{spam}) = \frac{1 + 1}{6 + 12} = \frac{2}{18}
$$
$$
P(\text{ora} \mid \text{spam}) = \frac{2 + 1}{6 + 12} = \frac{3}{18}
$$

$$
P(\text{spam} \mid \text{mail}) \propto P(\text{spam}) \cdot [P(\text{compra} \mid \text{spam})]^2 \cdot [P(\text{ora} \mid \text{spam})]^2

= \frac{1}{2} \cdot \left( \frac{2}{18} \right)^2 \cdot \left( \frac{3}{18} \right)^2 = \frac{9}{18^4}
$$


Per "non-spam":

$$
P(\text{compra} \mid \text{spam}) = \frac{0 + 1}{6 + 10} = \frac{1}{18}
$$
$$
P(\text{ora} \mid \text{spam}) = \frac{1 + 1}{6 + 10} = \frac{2}{18}
$$

$$
P(\text{non-spam} \mid \text{mail}) \propto P(\text{non-spam}) \cdot [P(\text{compra} \mid \text{non-spam})]^2 \cdot [P(\text{ora} \mid \text{non-spam})]^2

= \frac{1}{2} \cdot \left( \frac{1}{18} \right)^2 \cdot \left( \frac{2}{18} \right)^2 = \frac{1}{18^4}
$$

---

#### Classificazione finale

$$P(\text{spam} \mid \text{mail}) = \frac{9}{18^4} > \frac{1}{18^4} =  P(\text{not-spam} \mid \text{mail})$$

Quindi la mail viene classificata come spam.


#### 4.2.4 Prestazioni e limiti

- **Vantaggi**: estramemente veloce e leggero
- **Svantaggi**: l’assunzione di indipendenza non è sempre realistica; ad esempio, le parole di una frase sono spesso collegate tra loro, ma per il modello non lo sono.
---


## 5 · Conclusioni

La regola di Bayes fornisce uno schema formale e razionale per integrare informazioni pregresse con nuove osservazioni. Questa capacità di aggiornare continuamente le nostre credenze rappresenta il cuore del ragionamento probabilistico e rende l’approccio bayesiano uno strumento fondamentale in molte discipline scientifiche e applicazioni pratiche.

