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
- Caso generale: se ho un numero $n$ lo scompongo in fattori primi: $n=p_{1}^{k_{1}}\cdot p_{2}^{k_{2}} \cdot...\cdot p_{r}^{k_{r}},$ dopodiché risaliamo ai casi particolari: $\varphi(n)=\varphi(p_{1}^{k_{1}})\cdot\varphi(p_{2}^{k_{2}})\cdot...\cdot\varphi(p_{r}^{k_{r}})=(p_{1}-1)p_{1}^{k_{1}-1}\cdot(p_{2}-1)p_{2}^{k_{2}-1}\cdot...\cdot(p_{1}-1)p_{r}^{k_{r}-1}$
###### Osservazione - $\varphi$ moltiplicativa
Si può dimostrare che $\varphi$ è moltiplicativa, infatti se $MCD(a,b)=1,$ $\varphi(ab)=\varphi(a)\cdot\varphi(b)$

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



