###### Proposizione - Ordine di un gruppo $G$ e di un elemento di $G$
Sia $G$ un gruppo finito, l'ordine di $G,$ indicato con $|G|,$ è la sua cardinalità.

L'ordine (o periodo) di un elemento $g\in G$ del gruppo $(G,\star)$ è un numero intero positivo $h$ tale che l'operazione $\star$ compiuta $h$ volte sull'elemento $g$ dà come risultato l'elemento neutro $e$ del gruppo $g^{h}=e$

Se non esiste un intero h, l'elemento g ha un *periodo infinito*. Se esiste un intero h, l'elemento g ha un *periodo finito* e il sottogruppo $\langle g \rangle$ generato da $g$ è uguale a

$\langle g \rangle={e,g,g1,g2,...,gn−1}$



###### Proposizione
Se $G$ ha cardinalità finita allora **l'ordine** di $G$ è la sua cardinalità (l'ordine di $H_{2}$ è 6).

Per i gruppi finiti ha interesse considerare la tabella moltiplicativa 

Sia $g\in G,$ allora $\{g^{t},t\in\mathbb{Z}\}$ è un sottogruppo di $G.$
Applico il criterio: ho $g^{t_{1}}$ e $g^{t_{2}}\in\{g^{t},t\in\mathbb{Z} \}$ e considero $g^{t_{1}}\cdot (g^{t_{2}})^{-1}=g^{t_{1}}\cdot g^{-t_{2}}=g^{t_{1}-t_{2}}\in \{g^{t},t\in\mathbb{Z} \}$ Per il criterio di prima, $\{g^{t},t\in\mathbb{Z}\}$ è un sottogruppo di $G$ ed è detto **sottogruppo generato** da $g,$ ed è indicato con $\langle g \rangle.$

Sia $(G,\cdot)$ un gruppo e $H\le G.$ $H$ è detto ciclico se $\exists h\in H$ tale che $H=\langle h \rangle.$ In particolare $G$ è ciclico se $\exists g\in G | G=\langle g \rangle.$ Se $G$ è ciclico $\implies$ è commutativo perché $g^{s}\cdot g^{t}=g^{s+t}.$ Un gruppo non commutativo non può essere ciclico

Esempio: $(\mathbb{Z},+)$ è ciclico, perché generato da $\langle 1 \rangle$ oppure da $\langle -1 \rangle$
Esempio: $(\mathbb{Z}_{n},+)$ è ciclico, perché generato da $\langle [1] \rangle$

### Classi Laterali modulo un sottogruppo e Teorema di Lagrange

### Teorema di Lagrange
$G$ finito, $H\le G$
Allora l'ordine di $H$ divide la cardinalità di $G,$ ovvero $|H|\space|\space|G|$ (l'ordine di $H$ è un divisore dell'ordine di $G$)
###### Dimostrazione
Osservazione: Per ogni fissato $a,\exists$ una biiezione $H\longrightarrow aH,$ $h\longrightarrow ah$. 

Quindi $|H|=|aH|\ \forall a\in G.$
Siano $\mathcal{L}_{s}(H)=\{a_{1}H,a_{2}H,...a_{i}H \}$ le classi laterali sinistre distinte e disgiunte (costituiscono una partizione di $G$) . 
Allora se $|G|=n\implies n=\displaystyle{\sum\limits_{j=1}^{i}}|a_{j}H|$ perché $\mathcal{L}_{s}(H)$ è una partizione di $G$, in particolare $$G=\displaystyle{\bigcup_{j=1}^{i}(a_{j}H)}$$
Per l'osservazione $|a_{j}H|=|H|,$ ma allora $n=i|H|$ (ovvero la cardinalità di $H$ per $i$ insiemi) 
Dato che $|G|=n,$ allora $|H|\space|\space|G|.$

Classi laterali sinistre $\longrightarrow\mathcal{L}_{s}(H)\longrightarrow \rho_{s}$ $a\ \rho_{s}\ b\iff a^{-1}b\in H$
Classi laterali sinistre $\longrightarrow\mathcal{L}_{d}(H)\longrightarrow \rho_{s}$ $a\ \rho_{d}\ b\iff a^{-1}b\in H$

In generale $\rho_{s}\ne\rho_{d}.$ Rivediamo il controesempio di prima: $$\begin{align}\begin{pmatrix}1&2&3\\2&1&3\end{pmatrix} \ \rho_{s}\ \begin{pmatrix}1&2&3\\2&3&1\end{pmatrix}\\ \begin{pmatrix}1&2&3\\2&1&3\end{pmatrix}\ \cancel{\rho_{d}}\ \begin{pmatrix}1&2&3\\2&3&1\end{pmatrix}\end{align}.$$

###### Proposizione 
$\rho_{s}=\rho_{d}\iff aH=Ha\forall a\in G$
Definizione: $H$ è un sottogruppo normale se $l_{s}=l_{d}$
Notazione $H\trianglelefteq G$ è normale $\iff aha^{-1}\in G$ (di $aH=Ha$)
è una riscrittura di $aH=Ha$





# TODO
Scrivere la dimostrazione di essere ben definita