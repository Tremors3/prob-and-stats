
#### Esercizio 1

Un segnale $X$ normalmente distribuito, $X \sim N(1.7; 16)$, entra in un dispositivo che lo azzera se $X \le 0$, e lo lascia immutato se $X > 0$. Se il segnale uscente è $Y$, trova:

- (a) la probabilità $P(Y = 0)$;
- (b) la funzione distribuzione $F_Y(t)$ nei tre casi $t < 0$, $t = 0$ e $t > 0$.

##### Risoluzione

Dal testo del problema abbiamo:

$$
Y =
\begin{cases}
0 & \text{se } X \le 0 \\
X & \text{se } X > 0
\end{cases}
$$

- **(a) Calcolare la probabilità $P(Y = 0)$.**

    $$\begin{aligned}
    P(Y = 0)
    &= P(X \le 0) \\
    &= \Phi\left(\frac{0 - 1.7}{\sqrt{16}}\right) \\
    &= \Phi\left(-0.425\right) \\
    &= 1 - \Phi\left(0.425\right) \\
    &\approx 1 - 0.6640 \\
    &\approx \boxed{0.3360} \;.
    \end{aligned}$$

- **(b) Calcolare la funzione distribuzione $F_Y(t)$ nei tre casi $t < 0$, $t = 0$ e $t > 0$.**

    Ricordiamo che:

    $$
    F_Y(t) = P(Y \le t)
    $$

    - Caso $t < 0$:

        $\;$

        Poiché $Y$ può assumere soltanto valori non negativi, risulta:

        $$
        F_Y(t) = 0
        $$

    <div style="page-break-after: always;"></div>

    - Caso $t = 0$:

        $$\begin{aligned}
        F_Y(0)
        &= P(Y \le 0) \\
        &= P(Y = 0) \\
        &= P(X \le 0) \\
        &\approx 0.3360
        \end{aligned}$$

    - Caso $t > 0$:

        $\;$

        In questo caso:

        $$\begin{aligned}
        F_Y(t)
        &= P(Y \le t) \\
        &= P(X \le 0) + P(0 < X \le t) \\
        &= P(X \le t) \\
        &= F_X(t) \\
        &= \Phi\left(\frac{t - 1.7}{\sqrt{16}}\right)
        \end{aligned}$$

    Quindi:

    $$
    \boxed{
    F_Y(t) =
    \begin{cases}
    0 & \text{se } t < 0 \\[6pt]
    0.3360 & \text{se } t = 0 \\[6pt]
    \Phi\left(\dfrac{t - 1.7}{\sqrt{16}}\right) & \text{se } t > 0
    \end{cases}
    }
    \;.
    $$

---

<div style="page-break-after: always;"></div>

#### Esercizio 2

Se $X \sim U[-3, 7]$ e

$$
X^+ =
\begin{cases}
0, & X \le 0 \\
X, & X > 0
\end{cases}
$$

trova la funzione distribuzione di $Y = X^+$.

##### Risoluzione

- **Caso $t < 0$.**

    Poiché $X^+$ assume soltanto valori non negativi:

    $$
    F_{X^+}(t) = P(X^+ \le t) = 0
    $$

- **Caso $t = 0$.**

    $$\begin{aligned}
    F_{X^+}(0)
    &= P(X^+ \le 0) \\
    &= P(X^+ = 0) \\
    &= P(X \le 0) \\
    &= \int_{-3}^{0} f_X(x)\,dx \\
    &= \frac1{7-(-3)}(0-(-3)) \\
    &= \frac3{10} \\
    &= 0.3
    \end{aligned}$$

    <div style="page-break-after: always;"></div>

- **Caso $t > 0$.**

    $$\begin{aligned}
    F_{X^+}(t)
    &= P(X^+ \le t) \\
    &= P(X \le 0) + P(0 < X \le t) \\
    &= P(X \le t) \\
    &= \int_{-3}^{t} f_X(x)\,dx \\
    &= \frac1{7-(-3)}(t-(-3)) \\
    &= \frac{t+3}{10}
    \end{aligned}$$

    Questa espressione è valida finché $0 < t < 7$.

    Per $t \ge 7$ risulta:

    $$
    F_{X^+}(t) = 1
    $$

Quindi:

$$
\boxed{
F_{X^+}(t)=
\begin{cases}
0 & t < 0 \\[6pt]
0.3 & t = 0 \\[6pt]
\dfrac{t+3}{10} & 0 < t < 7 \\[8pt]
1 & t \ge 7
\end{cases}
}
\;.
$$

---

<div style="page-break-after: always;"></div>

#### Esercizio 3

Sia $X \sim U (0, 3)$. Trova:

- (a) la densità di probabilità di $Y = \min(X, 3 − X)$;
- (b) la varianza di $Y$. 

##### Risoluzione

La funzione $g(x) = \min(X, 3-X)$ non è strettamente crescente o decrescente, quindi non possiamo applicare direttamente il teorema di trasformazione.

- **(a) Calcoliamo la densità di probabilità di $Y = \min(X, 3 − X)$.**

    Troviamo prima la funzione di ripartizione $F_Y$ in termini di $F_X$.

    $$\begin{aligned}
    F_Y(y)
    &= P(Y \le y) \\
    &= P(\min(X,3-X) \le y) \\
    &= P(3-y \le X \le y) \\
    &= P(X \le y) - P(X < 3-y) \\
    &= F_X(y) - F_X(3-y)
    \end{aligned}$$

    Troviamo $f_Y$ in termini di $F_Y$.

    $$\begin{aligned}
    f_Y(y)
    &= \frac{d}{dy}\left\{ F_Y(y) \right\} \\
    &= \frac{d}{dy}\left\{ F_X(y) - F_X(3-y) \right\} \\
    &= f_X(y) - (-f_X(3-y)) \\
    &= f_X(y) + f_X(3-y) \\
    &= 2 f_X(y) \\
    &= 2\cdot\frac1{3-0} \\
    &= \frac23
    \end{aligned}$$

    Determiniamo ora il supporto di $Y$. Dal disegno:

    $$
    0 \le Y \le \frac32
    $$

    Quindi:

    $$
    \boxed{
    f_Y(y) =
    \begin{cases}
    \frac23 & 0 \le y \le \frac32 \\
    0 & \text{altrimenti}
    \end{cases}
    }
    \;.
    $$

- **(b) Calcoliamo la varianza di $Y$.**

    Calcoliamo prima l'aspettazione:

    $$\begin{aligned}
    E[Y]
    &= \int_0^{\frac32} y\,f_Y(y)\,dy \\
    &= \frac23 \int_0^{\frac32} y\,dy \\
    &= \frac23 \left[\frac{y^2}{2}\right]_0^{\frac32} \\
    &= \frac34
    \end{aligned}$$

    Calcoliamo poi il secondo momento:

    $$\begin{aligned}
    E[Y^2]
    &= \int_0^{\frac32} y^2\,f_Y(y)\,dy \\
    &= \frac23 \int_0^{\frac32} y^2\,dy \\
    &= \frac23 \left[\frac{y^3}{3}\right]_0^{\frac32} \\
    &= \frac34
    \end{aligned}$$

    Infine:

    $$\begin{aligned}
    \text{Var}(Y)
    &= E[Y^2] - (E[Y])^2 \\
    &= \frac34 - \left(\frac34\right)^2 \\
    &= \boxed{ \frac{3}{16} } \;.
    \end{aligned}$$
---

<div style="page-break-after: always;"></div>