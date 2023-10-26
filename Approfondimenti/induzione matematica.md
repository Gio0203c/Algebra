# Induzione Matematica

Il principio di induzione matematica afferma che se una proprietà $P$ vale per $0$ e se si può dimostrare che, ammesso che valga per il numero $n$, vale anche per $n+1$, allora P vale per qualunque numero $n$. Insiemisticamente valgono 2 proprietà: 
- $(i)$ $1\in X$
- $(ii)$ Per un generico $n ≥ 1:$ se $n ∈ X$ allora $n + 1 ∈ X$.

Allora è legittimo concludere che $N \subseteq X$, ossia che $X$ contiene tutti i numeri naturali.
###### Esempio
Proviamo a verificare che, $\forall n \ge 1:$$$1+2+3+...+(n-1)=\frac{n(n+1)}{2}$$
- Verifichiamo quindi il caso **base** $p_1$, ossia $n = 1$ $$1 = \frac{1(1 + 1)}{2} = \frac{2}{2} \space \space \space \space \triangle$$che risulta essere vero
• A questo punto, assumiamo per **ipotesi induttiva** che $p_n$ sia vera.
• Impostiamo quindi il **passo induttivo**, ossia $p_{n+1}:$ $$1 + 2 + 3 + . . . + n+(n+1)=\frac{(n+1)\cdot(n+1+1)}{2}$$• Notiamo come il passo induttivo contenga al suo interno *l’ipotesi induttiva stessa*, che abbiamo affermato **essere vera:** $$\begin{align} \underset{\text{Ipotesi induttiva}}{\underbrace{1 + 2 + 3 + . . . + n}} + (n + 1)  = \frac{(n + 1)(n + 1 + 1)}{2}  &\iff \\ \frac{n(n+1)}{2} + (n+1) = \frac{(n+1)(n+2)}{2}  &\iff \\ \frac{n(n+1)+2(n+2)}{2} =\frac{(n+1)(n+2)}{2} &\iff \\ \frac{(n+1)(n+2)}{2}
 = \frac{(n+1)(n+2)}{2} \space \space \space \space  &\square\end{align}$$Anche il passo induttivo risulta essere vero, concludendo che la pro-
posizione $p_{n}$) sia valida $\forall n \ge 1$.

Un teorema equivalente a quello dell'induzione è il *principio del buon ordinamento*.
##### Principio del Buon Ordinamento
Il **principio del buon ordinamento** (o principio del valore minimo) afferma che ogni sottoinsieme non vuoto $T\subset \mathbb{N}$ contiene un elemento minimo, cioè esiste un elemento $t \in T |t\le x \forall x\in T$.
###### Dimostrazione
Consideriamo un insieme $X\subseteq\mathbb{N}$ che soddisfa le due proprietà: $(i):$ $1 ∈ X$ e $(ii):$ per un generico $n ≥ 1$, se $n ∈ X$ allora $n + 1 ∈ X$. 

Supponiamo per assurdo che non valga la conclusione del Principio di Induzione, ossia supponiamo che non è vero che $X\subseteq{\mathbb{N}}$. Dunque l’insieme $A = (N\space\backslash\space X)$ è un sottoinsieme non-vuoto di $\mathbb{N}$. 

Per il Principio del Minimo Numero $A$ contiene un minimo. Sia $m$ il minimo di $A$. Si osserva che $m$ non può essere $1$, dato che $1 \in X$ e $m \notin X$. Dunque $m > 1$ e pertanto $m − 1 \ge 1$ (ossia è ancora un numero naturale). Inoltre dato che $m$ è scelto come il minimo in $\mathbb{N}$ ma non in $X$, necessariamente $m - 1 \in X$. 

Ma $X$ soddisfa la proprietà $(ii)$ e dunque se $m − 1 \in X$ allora $m \in X$. Abbiamo raggiunto una contraddizione: $m \in X$ e $m \notin X$.