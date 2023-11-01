# Identità di Bezout
Siano $a$ e $b$ due numeri interi, e sia $d$ il loro **MCD**, allora esistono due numeri $x$ e $y$ per cui $$ax+by=d$$Prendiamo ad esempio i numeri $24$ e $10.$

Inizio calcolando il Massimo Comun Divisore con l'algoritmo di Euclide: 
1) Divido inizialmente il valore più grande per il più piccolo, poi divido il successivo con il resto ottenuto dalla divisione precedente, fino a trovare resto zero:
	- $24:10=2$ con resto $4$
	- $10:4=2$ con resto $2$
	- $4:2=2$ con resto $0$
Avendo ottenuto zero come resto posso affermare con esattezza che 2 è il massimo comun divisore tra 10 e 24.
2) Adesso riscrivo tutte le divisioni come identità:
	- $24 = 2\cdot 10+4$
	- $10 = 2 \cdot 4 + 2$
	- $4 = 2\cdot 2 + 0$

Dopodiché esplicito tutti i resti:
- $4=24-2\cdot 10$
- $2=10-2\cdot 4$

Nell'ultima identità sostituisco:$$\begin{align}2=10-2\cdot(24-2\cdot 10) & =10-2\cdot 24+4\cdot 10 \\ 2=\underset{x}{\underbrace{5}}\cdot 10 -& \underset{y}{\underbrace{2}} \cdot 24 \end{align}$$