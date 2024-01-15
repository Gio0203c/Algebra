

### Funzione $\varphi$ di Eulero
La **funzione $\varphi$ di Eulero** è definita sugli interi positivi e $\forall n$ ci dice quanti sono gli interi tra $1$ e $n$ coprimi con $n$.

Ad esempio $\varphi(10)=4,$ perché tra $1$ e $10$ ci sono $4$ interi coprimi con $10:1,3,7,9.$

Come si calcola $\varphi(n)?$
- Caso particolare 1: se $p$ numero primo $\varphi(p)=p-1$
	- Esempio: $\varphi(7)=7-1=6:\{1,2,3,4,5,6 \}$
- Caso particolare 2: se $p^k$ è una potenza di un numero primo si può dimostrare che $\varphi(p^k)=(p-1)(p^{k-1})$
	- Esempio: $\varphi(64)=\varphi(2^{6})=(2-1)\cdot2^{5}=32$
- Caso generale: se ho un numero $n$ lo scompongo in fattori primi: $n=p_{1}^{k_{1}}\cdot p_{2}^{k_{2}} \cdot...\cdot p_{r}^{k_{r}},$ dopodiché risaliamo ai casi particolari: $\varphi(n)=\varphi(p_{1}^{k_{1}})\cdot\varphi(p_{2}^{k_{2}})\cdot...\cdot\varphi(p_{r}^{k_{r}})=$ $(p_{1}-1)p_{1}^{k_{1}-1}\cdot(p_{2}-1)p_{2}^{k_{2}-1}\cdot...\cdot(p_{1}-1)p_{r}^{k_{r}-1}=$ $n\cdot \bigg[ \bigg(1-\frac{1}{p_1}\bigg)\cdot\bigg(1-\frac{1}{p_2}\bigg)\cdot ...\cdot\bigg(1-\frac{1}{p_r}\bigg)\bigg]$
###### Osservazione - $\varphi$ moltiplicativa
Si può dimostrare che $\varphi$ è moltiplicativa, infatti se $MCD(a,b)=1,$ $\varphi(ab)=\varphi(a)\cdot\varphi(b)$
###### Esempio - Esercizio sulla funzione $\varphi$ di Eulero
Quanti sono gli interi tra 1 e 2020 coprimi con 2020 stesso?

Per risolvere questo esercizio possiamo utilizzare la funzione $\varphi$ di Eulero. Iniziamo scomponendo 2020 in fattori primi:$$2020=2^{2}\cdot 5\cdot 101$$Usando la formula generale, avremo che:$$\varphi(2020)=2020\cdot\left[\bigg(1-\frac{1}{2}\bigg)\cdot\bigg(1-\frac{1}{5}\bigg)\cdot\bigg(1-\frac{1}{101}\bigg)\right]=800$$Oppure posso scriverlo utilizzando l'altra formula (prodotto di casi particolari):$$\varphi(2020)=\varphi(2^2)\cdot \varphi(5)\cdot \varphi(101)=2\cdot 4\cdot 100=800$$Questo conferma il fatto che tra 1 e 2020 ci sono 800 numeri coprimi con 2020.

La funzione $\varphi$ di Eulero ha molte applicazioni, ad esempio permette di calcolare l'*inverso modulo $n$* di un numero.
##### Applicazioni di $\varphi$ - Inverso modulo $n$
Si dice che un intero $a$ è **invertibile modulo n** $\iff MCD(a,n)=1.$ Sotto questa ipotesi, un valore possibile dell'inverso si ottiene elevando $a^{\varphi(n-1)}.$ 

Per dimostrarlo, è necessario conoscere un teorema di Eulero, che afferma che se $MCD(a,n)=1$ allora:$$a^{\varphi(n)}\equiv1(\text{mod }n)$$
Per cui, se ho un equazione del tipo $ax\equiv b\text{ (mod }n),$ se moltiplico tutto per $a^{\varphi(n)-1}$ ottengo:$$\underset{a^{\varphi(n)}\equiv 1\text{ (mod }n)}{\underbrace{a^{\varphi(n)-1}a}x}\equiv a^{\varphi(n)-1}b\text{ (mod }n)$$
###### Esempio - calcolo di inverso modulo $n$ tramite $\varphi$ di Eulero
$$\begin{align} 3x\equiv 2\text{ (mod }5)\longrightarrow x& \equiv 3^{\varphi(5)-1}\cdot 2\text{ (mod }5)\stackrel{\varphi(5)=4}{\longrightarrow} \\ x\equiv 54\text{ (mod 5}) &\longrightarrow x\equiv 4\text{ (mod }5)\end{align}$$

### Il Piccolo Teorema di Fermat
Sia $a$ un intero e $p$ un numero primo. Allora:$$a^{p}\equiv a\text{ (mod }p)$$Dimostrazione:
Supponiamo $a\ge0$ per cui possiamo procedere per induzione prendendo come variabile di induzione $a$ stessa. Se $a=0$ il risultato è *banale* ($0^{p}\equiv 0\text{ (mod }p)$. 

Supponiamo allora vero il risultato per $a,$ cioè: $$a^{p}\equiv a\text{ (mod }p)$$e dimostriamolo per $a+1,$ infatti:$$(a+1)^{p}\equiv a^p+1^p\text{ (mod }p)$$
- come è giustificato? (Opzionale)
	applicando il teorema del binomio a $(a+1)^p$, otteniamo:$$(a+1)^p = \sum_{k=0}^{p} {p \choose k} a^{p-k} 1^k = a^p + \sum_{k=1}^{p-1} {p \choose k} a^{p-k} + 1^p$$Ora, per ogni $1 \leq k \leq p-1$, il coefficiente binomiale ${p \choose k}$ è divisibile per $p.$ Quindi, tutti i termini intermedi della somma sono congruenti a $0\text{ (mod }p)$. 
	
	Pertanto, otteniamo $(a+1)^p \equiv a^p + 1^p \mod p$. Questo è un passaggio


Ma $1^p\equiv1$ e $a^{p}\equiv a$ per l'ipotesi induttiva, quindi $$(a+1)^{p}\equiv a+1$$che è la nostra tesi.
