# Il Crivello di Eratostene
Il **crivello di Eratostene** è un antico procedimento per il *calcolo delle tabelle di numeri primi fino ad un certo numero $n$ prefissato*. Questo principio deve il proprio nome ad **Eratostene di Cirene**, il matematico che ne fu l'ideatore.

Il crivello di Eratostene funziona come un "**setaccio**" in cui vengono eliminati i numeri naturali positivi che non sono primi, in modo tale che rimangono solamente i numeri primi minori o uguali a $n$.

Supponiamo di voler trovare i numeri primi che si trovano da $1$ a $50$. Per cui partiamo dalla seguente tabella:![[crivelloeratostene01.svg]]
Innanzitutto bisogna rimuovere il numero $1$, che per definizione **non** è un numero primo. Dopodiché si passa al numero $2$. Il $2$ **è** un numero primo, per cui viene cerchiato (io lo coloro di verde), e *tutti i suoi multipli maggiori vengono eliminati dalla tabella*:
![[crivelloeratostene02.svg]]

Il numero successivo che non è stato "setacciato" è il $3$, per cui è un numero primo. Lo cerchio ed elimino tutti i suoi multipli maggiori:![[crivelloeratostene03.svg]]
Proseguo con il $5$:![[crivelloeratostene04.svg]]
E così via...

Alla fine, otterrò una situazione del genere:![[crivelloeratostene05.svg]]
Dove i numeri in verde sono tutti i numeri primi. 

Come faccio ad esserne sicuro? Consideriamo ad esempio il numero 11 e supponiamo, per assurdo, che tra i numeri rimasti ci sia un multiplo di 11 strettamente maggiore di $11$ che chiamiamo $m$. Allora $m=11k$, dove $k<11$, perché stiamo supponendo che $m$ sia compreso tra $1$ e $50$. Allora $k$ è un numero primo $p$ oppure $k$ è multiplo di un numero primo $p$ (minore di $11$). 

Quindi $m$ risulta essere multiplo di un numero primo $p$ (eventualmente uguale a $k$) minore di $11$, ma questo è un **assurdo**, poiché non dovrebbe comparire nell'elenco in quanto dovrebbe essere stato già cancellato in quanto multiplo di $p$ e strettamente maggiore di $p$.

Posso quindi dire con esattezza che i numeri primi da $0$ a $50$ sono: $2,3,5,7,11,13,17,19,23,29,31,37,41,43,47.$

Con procedimento analogo è possibile trovare tutti i numeri primi fino ad un $n$ fissato.