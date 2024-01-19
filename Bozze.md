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

Sia $(G,\cdot)$ un gruppo e $H\le G.$ $H$ è detto ciclico se $\exists h\in H$ tale che $H=\langle h \rangle.$ In particolare $G$ è ciclico se $\exists g\in G | G=\langle g \rangle.$ Se $G$ è ciclico $\implies$ è commutativo perché $g^{s}\cdot g^{t}=g^{s+t}.$

Esempio: $(\mathbb{Z},+)$ è ciclico, perché generato da $\langle 1 \rangle$ oppure da $\langle -1 \rangle$
Esempio: $(\mathbb{Z}_{n},+)$ è ciclico, perché generato da $\langle [1] \rangle$
### Classi Laterali modulo un sottogruppo e teorema di Lagrange
Sia $(G,\star)$ un gruppo e sia $H$ un suo sottogruppo. Definiamo in $G$ la seguente relazione:$$a\space\rho\space b\iff a\star b^{-1}\in H.$$
Se l'operazione di $G$ fosse l'addizione, la relazione sarebbe $$a\space\rho\space b\iff a+(-b)\in H.$$ Per questo motivo la relazione 