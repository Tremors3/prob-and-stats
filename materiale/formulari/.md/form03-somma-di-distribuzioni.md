
# $$ \textcolor{red}{\textbf{Somme di variabili aleatorie}} $$

---

## Tabella riassuntiva delle chiusure

| Distribuzione | Condizione | Somma | Risultato |
|--------------|------------|-------|------------|
| Bernoulli | stesso $p$ | $B_1 + \dots + B_n$ | $\text{Bin}(n,p)$ |
| Binomiale | stesso $p$ | $X + Y$ | $\text{Bin}(n_1+n_2,p)$ |
| Geometrica | stesso $p$ | $G_1 + \dots + G_n$ | $\text{NegBin}(n,p)$ |
| Binomiale Negativa | stesso $p$ | $X + Y$ | $\text{NegBin}(r_1+r_2,p)$ |
| Poisson | indipendenti | $X + Y$ | $\text{Pois}(\lambda_1+\lambda_2)$ |
| Esponenziale | stesso $\lambda$ | $X_1 + \dots + X_n$ | $\Gamma(n,\lambda)$ |
| Gamma | stesso $\lambda$ | $X + Y$ | $\Gamma(k_1+k_2,\lambda)$ |
| Normale | indipendenti | $X + Y$ | $\mathcal{N}(\mu_1+\mu_2,\sigma_1^2+\sigma_2^2)$ |

---

<div style="page-break-after: always;"></div>

## $$ \textcolor{blue}{\textbf{1. Distribuzioni discrete}} $$

---

### Bernoulli $\to$ Binomiale

Somma di due Bernoulli indipendenti.

$$
X,Y \sim \text{Bern}(p)
$$

$$
X + Y \sim \text{Bin}(2, p)
$$

Somma di $n$ Bernoulli indipendenti.

$$
B_1, \dots, B_n \sim \text{Bern}(p)
$$

$$
B_1 + \dots + B_n \sim \text{Bin}(n,p)
$$

$\to$ Stesso parametro $p$.

---

### Binomiale

Somma di due Binomiali indipendenti.

$$
X \sim \text{Bin}(n_1,p), \quad Y \sim \text{Bin}(n_2,p)
$$

$$
X+Y \sim \text{Bin}(n_1+n_2,\; p)
$$

Somma di $m$ Binomiali indipendenti.

$$
X_i \sim \text{Bin}(n_i,p)
$$

$$
X_1 + \dots + X_m \sim \text{Bin}(n_1+\dots+n_m,\; p)
$$

$\to$ Stesso parametro $p$.

---

### Geometrica $\to$ Binomiale Negativa

Somma di due Geometriche indipendenti.

$$
X,Y \sim \text{Geom}(p)
$$

$$
X + Y \sim \text{NegBin}(2, p)
$$

Somma di $n$ Geometriche indipendenti.

$$
G_1, \dots, G_n \sim \text{Geom}(p)
$$

$$
G_1 + \dots + G_n \sim \text{NegBin}(n,p)
$$

$\to$ Stesso parametro $p$.

---

### Binomiale Negativa

Somma di due Binomiali Negative indipendenti.

$$
X \sim \text{NegBin}(r_1,p), \quad Y \sim \text{NegBin}(r_2,p)
$$

$$
X+Y \sim \text{NegBin}(r_1+r_2,\; p)
$$

Somma di $n$ Binomiali Negative indipendenti.

$$
X_i \sim \text{NegBin}(r_i,p)
$$

$$
X_1 + \dots + X_n \sim \text{NegBin}(r_1+\dots+r_n,\; p)
$$

$\to$ Stesso parametro $p$.

---

<div style="page-break-after: always;"></div>

### Poisson

Somma di due Poisson indipendenti.

$$
X \sim \text{Pois}(\lambda_1), \quad Y \sim \text{Pois}(\lambda_2)
$$

$$
X+Y \sim \text{Pois}(\lambda_1 + \lambda_2)
$$

Somma di $n$ Poisson indipendenti.

$$
X_i \sim \text{Pois}(\lambda_i)
$$

$$
X_1 + \dots + X_n \sim \text{Pois}(\lambda_1 + \dots + \lambda_n)
$$

---

<div style="page-break-after: always;"></div>


## $$ \textcolor{blue}{\textbf{2. Distribuzioni continue}} $$

---

### Esponenziale $\to$ Gamma

Somma di due Esponenziali indipendenti.

$$
X,Y \sim \text{Exp}(\lambda)
$$

$$
X + Y \sim \Gamma(2, \lambda)
$$

Somma di $n$ Esponenziali indipendenti.

$$
E_1, \dots, E_n \sim \text{Exp}(\lambda)
$$

$$
E_1 + \dots + E_n \sim \Gamma(n,\lambda)
$$

$\to$ Stesso parametro $\lambda$.

---

### Gamma

Somma di due Gamma indipendenti.

$$
X \sim \Gamma(k_1, \lambda), \quad Y \sim \Gamma(k_2, \lambda)
$$

$$
X+Y \sim \Gamma(k_1+k_2,\; \lambda)
$$

Somma di $m$ Gamma indipendenti.

$$
X_i \sim \Gamma(k_i,\lambda)
$$

$$
X_1 + \dots + X_m \sim \Gamma(k_1+\dots+k_m,\; \lambda)
$$

$\to$ Stesso parametro $\lambda$.

---

### Normale

Somma di due Normali indipendenti.

$$
X + Y \sim \mathcal{N}(\mu_1 + \mu_2,\; \sigma_1^2 + \sigma_2^2)
$$

Somma di $n$ Normali indipendenti.

$$
X_1 + \dots + X_n \sim \mathcal{N}(\mu_1 + \dots + \mu_n,\; \sigma_1^2 + \dots + \sigma_n^2)
$$

Trasformazione lineare:

$$
aX + bY + c \sim \mathcal{N}(a\mu_1 + b\mu_2 + c,\; a^2\sigma_1^2 + b^2\sigma_2^2)
$$

$$
a_1X_1 + \dots + a_nX_n + \gamma \sim \mathcal{N}(a_1\mu_1 + \dots + a_n\mu_n + \gamma,\; a_1^2\sigma_1^2 + \dots + a_n^2\sigma_n^2)
$$

---

### Gaussiana standard

Somma di due Normali standard indipendenti.

$$
Z_1, Z_2 \sim \mathcal{N}(0,1)
$$

$$
Z_1 + Z_2 \sim \mathcal{N}(0,2)
$$

Somma di $n$ Normali standard indipendenti.

$$
Z_1, \dots, Z_n \sim \mathcal{N}(0,1)
$$

$$
Z_1 + \dots + Z_n \sim \mathcal{N}(0,n)
$$

---

<div style="page-break-after: always;"></div>

## $$ \textcolor{blue}{\textbf{3. Formula generale (convoluzione)}} $$

---

### Caso discreto

$$
P_{X+Y}(k) = \sum_j P_X(j)\,P_Y(k-j)
$$

---

### Caso continuo

$$
f_{X+Y}(z) = \int_{-\infty}^{+\infty} f_X(x)\,f_Y(z-x)\,dx
$$

---

### Esempio applicazione

Siano

$$
X \sim \text{Exp}(\alpha)
\qquad\text{e}\qquad 
Y \sim \text{Exp}(\beta)
$$

indipendenti. Calcoliamo la densità di probabilità di $Z=X+Y$.

##### Risoluzione

> **Nota.** Nel caso particolare in cui i parametri coincidono:
>
> $$
> X,Y \sim \text{Exp}(\lambda)
> \quad\Rightarrow\quad
> X+Y \sim \text{Gamma}(\lambda, 2).
> $$
>
> Nel nostro caso però $\alpha \neq \beta$, quindi dobbiamo usare la convoluzione.

Dobbiamo applicare la formula:

$$
f_Z(z)=\int_{-\infty}^{+\infty} f_X(x)\,f_Y(z-x)\,dx.
$$

Poiché le densità sono nulle per valori negativi, l’integrale diventa:

$$\begin{aligned}
f_Z(z)
&= \int_0^z \alpha e^{-\alpha x}\,\beta e^{-\beta(z-x)}\,dx \\
&= \alpha\beta \int_0^z e^{-\alpha x} e^{-\beta(z-x)}\,dx \\
&= \alpha\beta \int_0^z e^{-\alpha x} e^{-\beta z + \beta x}\,dx \\
&= \alpha\beta e^{-\beta z} \int_0^z e^{(\beta-\alpha)x}\,dx \\
&= \alpha\beta e^{-\beta z} \left[\frac{e^{(\beta-\alpha)x}}{\beta-\alpha}\right]_0^z \\
&= \frac{\alpha\beta}{\beta-\alpha} e^{-\beta z} \left(e^{(\beta-\alpha)z}-1\right) \\
&= \frac{\alpha\beta}{\beta-\alpha} \left(e^{-\alpha z}-e^{-\beta z}\right).
\end{aligned}$$

Quindi:

$$
\boxed{
f_Z(z)
= \frac{\alpha\beta}{\beta-\alpha}
\left(
e^{-\alpha z}-e^{-\beta z}
\right)
}
\qquad z\ge 0.
$$

---

<div style="page-break-after: always;"></div>