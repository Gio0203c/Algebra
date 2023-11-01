# Gli Assiomi di Peano

In molti testi scolastici, viene detto che:
$\boxed{\text{Per ogni numero naturale esiste sempre il suo successivo, quindi l'insieme }\mathbb{N}\text{ è infinito.}}$
Questa affermazione in realtà è falsa. Consideriamo un insieme di persone sedute attorno ad un tavolo, e consideriamo che ognuno abbia come successivo la persona alla propria sinistra. Di seguito una rappresentazione:
![[peano-coaching-circle-1030x1014-min.png]]
Questo insieme soddisfa queste proprietà, ma non è infinito. In realtà questa proprietà è il secondo assioma di peano. Gli assiomi di peano sono 5:

1) Zero è un *numero naturale*.
2) Per ogni numero naturale, *esiste sempre il suo successivo*.
3) Numeri diversi *hanno* successivi *diversi*.
4) Zero *non è il successivo di nessun numero*.
5) Se un insieme $A$ di numeri *contiene lo zero* e di ogni numero *contiene anche il successivo*, allora $A$ contiene **tutti** i numeri naturali.

Il quinto assioma è detto **Principio di Induzione**, e grazie ad esso possiamo capire che (se valido), si può arrivare a qualunque numero naturale dallo zero.

Cerchiamo di spiegare tutto per gradi. Prendiamo i seguenti insiemi:

|                         |                        |
| ----------------------- | ---------------------- |
| 1)<br><br> ![[peano01.PNG]] | 2)<br><br>![[peano02.PNG]] |
| 3)<br><br>![[peano03.PNG]]  | 4)<br><br> ![[peano04.PNG]]    |
| 5)<br><br> ![[peano05.PNG]]     |6)<br><br> ![[peano06.PNG]]                       |

I primi due assiomi da soli non bastano come verità assoluta, perché questi sei casi rispettano questi due assiomi, ma sono errati. 

Introducendo il terzo assioma, notiamo che i casi $(3)$ e $(4)$ non sono più validi, perché in entrambi i casi 1 è il successivo di due numeri diversi tra di loro, quindi non rispetta l'assioma.

Introducendo il quarto assioma escludiamo i casi $(2)$ e $(5)$, dato che in un caso è il successivo di 2, mentre in un altro è successivo a sé stesso. In questo modo l'assioma non viene rispettato.

Ora, potrebbe sembrare che il quinto assioma non centri nulla con gli altri quattro, ma invece è proprio il più importante. Prendendo il caso $(6)$, e dando l'assioma per vero, da zero devo poter arrivare a qualsiasi elemento che è contenuto nell'insieme. Come posso vedere nell caso $(6)$ da zero non posso arrivare a mela/pera/banana, pertanto va escluso anche quello.

L'ultimo caso rimasto è l'$(1)$, che rispetta tutti gli assiomi di Peano.