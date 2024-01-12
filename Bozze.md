###### Esempio - risoluzione di un'equazione diofantea
Avendo a disposizione soltanto strane monete da 13 euro e potendone ricevere di resto solo da 33 euro, qual è il minimo numero di monete per effettuare un pagamento di esattamente 21 euro?

Che si può formalizzare con $13x-33y=21.$ Con $x,y>0.$

Iniziamo risolvendo l'equazione associata $13x-33y=1$ tramite l'algoritmo di Euclide.$$\begin{align}33 & =2\cdot 13+7 \\ 13& =1\cdot 7+6 \\ 7& =1\cdot 6+1\\6&=6\cdot1+0\end{align}$$Per cui, essendo $1$ l'ultimo resto non nullo, $MCD(13,33)=1.$

Dopodiché dobbiamo riscrivere le nostre equazioni esplicitando i resti:$$\begin{align}1&=7-1\cdot 6 \\6&=13-1\cdot 7 \\ 7&=33-2\cdot 13\end{align}$$Andando nell'equazione dell'$1$ a sostituire $6$ e $7$ in funzione di $13$ e $33$ otterremo $1=7-1\cdot6=7-1\cdot(13-1\cdot7)=$ $2\cdot7-1\cdot 13=2\cdot(33-2\cdot 13)-1\cdot 13$

Quindi $1=2\cdot33-5\cdot13.$ Per tornare al caso iniziale, basterà moltiplicare tutto per $21:$$$\begin{align}21\cdot(2\cdot33-5\cdot13)&=21\cdot1\\ 42\cdot 33-105\cdot 13&=21 \end{align}$$L'equazione quindi diventerà $13\cdot(-105)-33(-42)=21.$ Il problema è che $x$ e $y$ devono essere maggiori di zero. Applichiamo quindi questa procedura.$$\begin{align}&13\cdot (-105)-33\cdot(-42)=21 & +\\ (13\cdot33-33\cdot 13=0) \cdot4=\ & 13\cdot132-33\cdot 52=0 &= \\ ------------- &-------------& \\ & 13\cdot 27-33\cdot 10=21\end{align}$$Adesso le $x$ e $y$ sono positivi, quindi la soluzione è accettabile. L'insieme di tutte le soluzioni si può scrivere come:$$\begin{cases} x=27+33K \\y=10+13K\end{cases}$$al variare di $k.$

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
### Teorema Cinese del Resto
Il **teorema cinese del resto** fornisce una **condizione sufficiente** affinché un sistema di congruenze lineari ammetta soluzione.

Consideriamo un sistema di congruenzze: $$\begin{cases}x\equiv &a_{1}\text{ (mod }n_{1}) \\ x\equiv &a_2\text{ (mod }n_{2}) \\...&\\ x\equiv &a_{k}\text{ (mod }n_{k})\end{cases}$$Dove gli $n_{i}$ sono degli interi a due a due coprimi, ovvero che il loro $MCD=1,$ mentre gli $a_{i}$ sono interi qualsiasi. Se ciò accade, il teorema ci garantisce che un sistema del genere ha soluzione.

Per trovare le soluzioni di sistemi come questo si applica il seguente algoritmo:
0) Controllare che gli $n_{i}$ siano a due a due coprimi
1) Calcolare il prodotto dei moduli: $N=n_{1}\cdot n_{2}\cdot n_{3}$ e il prodotto tra i moduli escluso uno per tutti i moduli presenti: $N_{1}=n_{2}\cdot n_{3},$ $N_{2}=n_{1}\cdot n_{3},$ $N_{3}=n_{1}\cdot n_{2}.$
2) Risolvere le congruenze $N_iy_i\equiv 1\text{ (mod }n_i),$ ovvero cercare l'inverso modulo $n_{i}$ per ogni $N_{i}$ (si può fare con l'identità di Bézout)
3) La soluzione del sistema è: $$x\equiv a_1N_1y_1+a_2N_2y_2+a_3N_3y_3\text{ (mod }N).$$
La soluzione è espressa modulo $N,$ e ciò significa che data una soluzione particolare tutte le altre soluzioni si otterranno sommando o sottraendo multipli di $N.$

###### Esempio - Esercizio sul teorema cinese del resto
Prendiamo questo sistema:$$\begin{cases}x\equiv &2\text{ (mod }5) \\ x\equiv &3\text{ (mod }6) \\ x\equiv &1\text{ (mod }7)\end{cases}$$
0) Il sistema ammette soluzioni perché $5,6,7$ sono a due a due coprimi.
1) Calcoliamo $N=5\cdot 6\cdot 7 =210,$  $N_{1}=6\cdot 7=42,$ $N_{2}=5\cdot 7=35$ $N_{3}=5\cdot 6=30$
2) Risolvo le congruenze:$$\begin{align}N_{1}y_{1}\equiv 1\text{ (mod }n_{1)}\\ N_{2}y_{2}\equiv 1\text{ (mod }n_{3)}\\ N_{1}y_{3}\equiv 1\text{ (mod }n_3) \end{align}$$ovvero:$$\begin{align}42y_{1}\equiv 1\text{ (mod }5)\longrightarrow 2y_{1} \equiv 1\text{ (mod }5) \rightarrow y_{1}\equiv 3\text{ (mod }5) \\ 35y_{2}\equiv 1\text{ (mod }6)\longrightarrow -y_{2} \equiv 1\text{ (mod }6) \rightarrow y_{2}\equiv -1\text{ (mod }6) \\ 30y_{3}\equiv 1\text{ (mod }7)\longrightarrow 2y_{3} \equiv 1\text{ (mod }7) \rightarrow y_{3}\equiv 4\text{ (mod }7)\end{align}$$
3) La soluzione è$$x\equiv 2\cdot 42\cdot 3+3\cdot 35\cdot (-1)+1\cdot 30\cdot 4\text{ (mod }210)\longrightarrow x\equiv 57\text{ (mod }210)$$
Ricordiamo che questo teorema soddisfa una condizione **sufficiente** e non necessaria, per cui possono esserci dei casi per cui anche se i moduli non sono a due a due coprimi possono esserci soluzioni.
### Teorema fondamentale dell'aritmetica
Sia un numero intero $n>1.$ Allora $n$ si può fattorizzare nel prodotto di un numero finito di elementi irriducibili (detti **numeri primi**) $pj>1$:$$n=p_1^{h_{1}}p_2^{h_{2}}p_3^{h_{3}}...p_s^{h_{s}}$$dove i $p_j,j=1,...,s$ sono tutti distinti, gli esponenti $h_j$ sono positivi e $s\ge1.$ Inoltre tale fattorizzazione è unica.
