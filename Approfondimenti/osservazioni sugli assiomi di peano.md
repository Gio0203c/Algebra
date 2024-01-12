# Osservazioni sugli Assiomi di Peano
### Definizione 1
Si chiama **terna di Peano** una terna $(\mathbb{N},0,\sigma)$ dove:
1) $\mathbb{N}$ è un insieme non vuoto;
2) $0$ è un elemento di $\mathbb{N}$;
3) $\sigma:\mathbb{N}\rightarrow\mathbb{N}$ è un'applicazione verificante i tre assiomi, detti *assiomi di Peano:*
	- $(P_1)$ $\sigma$ è iniettiva;
	- ($P_2$) $0\notin Im(\sigma)$;
	- $(P_3)$ Per ogni $U\subseteq \mathbb{N}$ tale che $(f(x) = \begin{cases} (a) & 0 \in U, \\ (b) & \sigma(U)\in U, \end{cases}$ risulta $U = \mathbb{N}$.
L'applicazione $\sigma$ è detta *applicazione del successivo*, per cui dato un elemento $n\in \mathbb{N}$, $\sigma(n)$ viene definito *successivo* di $n$. Il terzo assioma di Peano $(P_3)$ è detto **[[induzione matematica|principio d'induzione matematica]].**
###### Postilla
Nell'approfondimento sugli [[assiomi di peano|assiomi di Peano]] c'è scritto che gli assiomi sono 5, perché qui sono 3? Sono semplicemente una riformulazione di quei 5. Nello specifico:
- $(2)$ corrisponde al primo assioma
- $(1)$ corrisponde al secondo assioma
- $(P_1)$ corrisponde al terzo assioma
- $(P_2)$ corrisponde al quarto assioma
- $(P_3)$ corrisponde al quinto assioma
#### Osservazione
Dall'assioma $(P_{3})$ segue subito che:
1) $n = \sigma(\sigma(... \sigma(0))),\forall n\in\mathbb{N} := \mathbb{N}-\{ 0\}$ .
   Ogni numero $n \in \mathbb{N}$ (tranne lo zero) è semplicemente il risultato dell'**applicazione $\sigma$ su $0$ $n$ volte**. Per questo $0$ *non è il successivo di nessuno* e non appartiene ad $Im(\sigma)$.
2) $n \ne \sigma(\sigma(...\sigma(n))), \forall n\in\mathbb{N}$. 
   In base a $(P_{2}),0\ne \sigma(\sigma(...\sigma(0)))$. Sia $n\in\mathbb{N}$ e in base a $_{(1)}$ $n=\sigma(\sigma(...\sigma(0)))$. Se per assurdo fosse $n=\sigma(\sigma(...\sigma(n)))$, allora applicando l'iniettività di $\sigma$ avremo che $0 = \sigma(\sigma(...\sigma(0)))$, ma *ricordiamo che $0\notin Im(\sigma)$ per ipotesi* si arriva ad un assurdo.
### Definizione 2
In $\mathbb{N}$ è definita la seguente relazione di diseguaglianza stretta $<$ : $\forall n,m \in \mathbb{N},n<m \iff m=\sigma(\sigma(...\sigma(n)))$, cioè che se $n<m$ se e solo se $m$ è un *successivo* di $n$.
#### Proposizione 
$(N,\le)$ è un insieme totalmente ordinato, con primo elemento $0$.
##### Dimostrazione
La relazione $≤$ è *riflessiva* per definizione. 

Verifichiamo che $\le$ sia *transitiva*: se $n<m$ e $m<p$, allora $m =σ(σ( ... σ(n)))$, $p = σ(σ(...σ(m)))$, quindi $p=\sigma\big(\sigma(...(\sigma(\sigma(\sigma(n)))))\big)$. Allora $n<p$ .

Verifichiamo che $≤$ sia *antisimmetrica*. Sia $n ≤ m, m ≤ n$ e, per assurdo, $n \ne m$. Allora $m = σ(σ(... σ(n)))$ e $n = σ(σ(... σ(m)))$, da cui $m = σ\big(σ( ... σ(σ(σ( ... σ(m)))))\big)$. Ciò e assurdo in base a $_{(2)}$. 

Quindi è una **relazione d'ordine**.

Verifichiamo ora che $≤$ sia **totale**. Siano $n, m ∈ N$, con $n\ne m$. Da $_{(1)}$, se $n = σ( σ( ... σ(0)))$ ed $m = σ (σ( ... σ(0) ))$, segue subito che $n = σ(σ( ... σ(m)))$ oppure $m = σ(σ( ... σ(n)))$, cioè $n<m$ oppure $m<n$. 

Infine, che 0 sia il primo elemento di N è ovvio.

