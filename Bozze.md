###### Esempio - risoluzione di un'equazione diofantea
Avendo a disposizione soltanto strane monete da 13 euro e potendone ricevere di resto solo da 33 euro, qual è il minimo numero di monete per effettuare un pagamento di esattamente 21 euro?

Che si può formalizzare con $13x-33y=21.$ Con $x,y>0.$

Iniziamo risolvendo l'equazione associata $13x-33y=1$ tramite l'algoritmo di Euclide.$$\begin{align}33 & =2\cdot 13+7 \\ 13& =1\cdot 7+6 \\ 7& =1\cdot 6+1\\6&=6\cdot1+0\end{align}$$Per cui, essendo $1$ l'ultimo resto non nullo, $MCD(13,33)=1.$

Dopodiché dobbiamo riscrivere le nostre equazioni esplicitando i resti:$$\begin{align}1&=7-1\cdot 6 \\6&=13-1\cdot 7 \\ 7&=33-2\cdot 13\end{align}$$Andando nell'equazione dell'$1$ a sostituire $6$ e $7$ in funzione di $13$ e $33$ otterremo $1=7-1\cdot6=7-1\cdot(13-1\cdot7)=$ $2\cdot7-1\cdot 13=2\cdot(33-2\cdot 13)-1\cdot 13$

Quindi $1=2\cdot33-5\cdot13.$ Per tornare al caso iniziale, basterà moltiplicare tutto per $21:$$$\begin{align}21\cdot(2\cdot33-5\cdot13)&=21\cdot1\\ 42\cdot 33-105\cdot 13&=21 \end{align}$$L'equazione quindi diventerà $13\cdot(-105)-33(-42)=21.$ Il problema è che $x$ e $y$ devono essere maggiori di zero. Applichiamo quindi questa procedura.$$\begin{align}&13\cdot (-105)-33\cdot(-42)=21 & +\\ (13\cdot33-33\cdot 13=0) \cdot4=\ & 13\cdot132-33\cdot 52=0 &= \\ ------------- &-------------& \\ & 13\cdot 27-33\cdot 10=21\end{align}$$Adesso le $x$ e $y$ sono positivi, quindi la soluzione è accettabile. L'insieme di tutte le soluzioni si può scrivere come:$$\begin{cases} x=27+33K \\y=10+13K\end{cases}$$al variare di $k.$

