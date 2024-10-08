# Machine Learning e Vantaggio Quantistico #

Nell' ottobre del 2019 la comunità scientifica è stata sorpresa da un articolo pubblicato da Google sulla rivista Nature in cui affermava di aver ottenuto la supremazia quantistica (Quantum Primacy) . Google era riuscita a dimostrare che il loro computer quantistico era in grado di eseguire una computazione  (ha impiegato 200 secondi) in un tempo esponenzialmente minore rispetto a uno classico (10 000 anni). Il risultato raggiunto da Google però risulta essere meno sorprendente se si considera che il problema computazionale a cui si sottoponevano le macchine era appositamente disegnato per far si che il computer quantistico vincesse. Era un problema computazione privo di qualunque utilità pratica.
Tralasciando eventuali contestazioni delle aziende rivali (IBM per prima ha affermato che in realtà il computer classico era in grado di compiere il calcolo in 2 giorni), risulta ovvio che il prossimo obiettivo per gran parte della comunità a lavoro su questo campo sia quello di ottenere la Supremazia Quantistica per un problema computazionale di effettiva utilità: il cosidetto Vantaggio Quantistico. 

Ed è in questo scenario che si inserisce il Quantum Machine Learning. Cosa è quindi il Quantum Machine Learnig, sarà un primo esempio di vantaggio quantistico?

## Cosa è il Quantum Machine Learning ##
Ad oggi, gran parte delle persone probabilmente conosce già come funziona una rete neurale artificiale, alternativamente consiglio la lettura di questo https://github.com/gidrills/Divulgazione/blob/main/NeuralNetwork.md


Per parlare di reti neurali quantistiche è necessaria solo ancora un pochino di teoria.

In informatica pura, si utilizzano i bit, in informatica quantistica si utilizzano i qubit. Nulla di troppo complicato, possiamo vedere i bit come una moneta in grado di assumere lo stato 0 o 1 mentre il qubit come una sfera "magica" in grado di essere lanciata e poter assumere tutti gli stati possibili tra 0 e 1 (0.1 ma anche 0.234 ma anche 0.452 ecc.), questa è una analogia che effettivamente si utilizza in ambito accademico, quindi nulla di troppo assurdo.

<p align="center">
  <img src=https://github.com/user-attachments/assets/e37ed8b7-47d6-4080-b558-8b823b8585f3>
</p>




Quindi sì, in un certo senso un qubit può contenere molta più informazione di un bit.
Ecco, una rete neurale quantstica funziona in modo un po' diverso da una rete neurale classica, non esistono i neuroni, non esiste proprio una rete, esiste piuttosto un circuito quantistico in grado di operare sui qubit. Come opera sui qubit? Attraverso l'utilizzo di gate quantistici, oggetti in grado di "ruotare" il qubit. La parte interessante è che a seconda di quanto si ruotino questi qubit è possibile ottenere risposte diverse dalla rete quantistica e qui abbiamo l'analogia con la rete neurale classsica. In una rete neurale classica si cercano i pesi migliori per ottenere una risposta corretta dalla rete neurale, in una rete neurale quantistica si cercano le rotazioni migliori (letteralmente, di quanti gradi ruotare il qubit e in che direzione). Naturalmente la teoria è molto più complessa, una rete neurale quantistica deve operare con almeno 4-6 qubit e questi possono essere "legati" tra di loro in modo tale che la rotazione di uno di questi qubit forzi la rotazione dell'altro. Ma l'obiettivo è sempre e comunque cercare le rotazioni migliori.

## Perfetto abbiamo visto come funzionano le reti neurali quantistiche, ma quindi queste portano un effettivo vantaggio?

La risposta semplice è "no", e la risposta complicata come spesso accade è "dipende". Per definire un effettivo vantaggio quantistico sono necessarie le seguenti condizioni:

- **Performance**: L'algoritmo quantistico risolve il problema bene, ovvero è in grado di generalizzare dai dati di training per fare previsioni efficaci.
- **Speedup**: L'algoritmo quantistico risolve il problema più velocemente di uno classico.
- **Relevance**: L'algoritmo deve essere utile (altrimenti parleremmo solo di Supremazia Quantistica).
- **Available**: La tecnologia per implementare l'algoritmo deve essere accessibile (dimostrare il vantaggio quantistico su un dispositivo costoso non avrebbe senso).

Riguardante al primo, e terzo punto come già evideziato da F. Petruccione nel suo libro "Machine Learning with Quantum Computers" (ultimo capitolo per chi fosse interessato alle dimostrazioni), la ricerca sembra suggerire che gli algoritmi quantistici di machine learning siano in grado di mantenere un certo grado di espressività (sono in grado di comprendere argomenti complessi) senza overfittare. Condizione che è spesso difficile ottenere con algoritmi classici in quanto prendendo ad esempio una rete neurale classica, aumentare l'espressività si puo tradurre in richiedere di aumentare il numero di neuroni (o di layer),
Riguardante al terzo punto i risultati più incoraggianti vengono anche questa volta dalla ricerca, come evidenzia Hirotoshi Hirai, nel suo articolo pubblicato su Nature il 13/04/2024 "Practical application of quantum neural network to materials informatics" ad oggi le reti neurali quantistiche hanno ricevuto una attenzione maggiore grazie alla loro capacità di resistere all'overfitting senza perdere in espressività pur mantenendo il campione di training "piccolo".  


