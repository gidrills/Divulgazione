# Cosa è una Rete Neurale #

## Definiamo una Rete neurale ##
Spesso e volentieri si tenede a fare confusione su cosa sia una rete neurale, cosa sia il Machine Learning e cosa il Deep Learning. Bè la verità è che per molti anni anche gli esperti hanno usato alcuni di questi termini in modo interscambiabile, ad oggi però
la teoria è abbastanza precisa, vediamo quindi cosa intendiamo con ognuno dei termini elencati.
- **AI** L'insieme delle discipline Natural Language Processing, Knowledge Representation, Automated Reasoning e Machine Learning
- **Machine Learning** Disciplina della AI che in particolare si occupa di far imparare ai computer, attraverso i dati, come risolvere i problemi senza essere esplicitamente istruita per farlo.
- **Neural Network** Tipo di modello (rappresentazione in termini matematici, ma anche grafici) di Machine Learning. In particolare questo modello si ispira alle rete neurale naturale.

## Ok quindi una rete neurale è un tipo di modello di Machine Learning che si ispira alla rete neurale umana, ma in che modo lo fa? ##

Bè, semplificando molto una rete neurale umana possiamo dire che i neuroni sono cellule in grado di ricevere e trasmettere informazioni attraverso segnali elettrici, la potenza dei segnali elettrici è poi regolata dalle sinapsi, ovvero i collegamenti tra i neuroni.


Perfetto, una rete artificiale è molto simile, un neurone artificiale è però più semplicemente una funzione, in grado di prendere degli input e produrre un output.

Questi input sono tipicamente valori che semplificando possiamo dire vanno da -1 a 1. Mentre le funzioni sono dette funzioni di attivazione e sono tipicamente abbastanza semplici per evitare calcoli troppo pesanti in fase di addestramento.
Per comodità di sviluppo si tende a organizzare i neuroni artificiali in layer e tipicamente ogni neurone di un layer è collegato con tutti i neuroni del layer successivo come in figura.

<p align="center">
  <img src="https://github.com/user-attachments/assets/79441ba7-54d5-4807-b2b3-586e829446a2" alt="reteNeurale">
</p>
<p align="center">
  I cerchietti sono i neuroni, le linee i collegamenti tra neuroni (sinapsi).
</p>


Perfetto, e le sinapsi ? Questa è la parte interessante delle reti neurali sia naturali che artificiali. Partiamo da una domanda, come facciamo a dire a una rete che si sta comportando bene o che si sta comportando male? Bè Rafforziamo le sinapsi, rafforziamo i collegamenti tra alcuni neuroni che vogliamo si "attivino" di più e riduciamo i collegamenti tra altri che vogliamo si attivino "meno" . In altri termini stabiliamo quali neuroni lavorano bene insieme e quali lavorano male. 
Nella figura sopra quindi i collegamenti dovrebbero avere dei colori diversi, per distinguere che non sono tutti uguali.

<p align="center">
  <img src= "https://github.com/user-attachments/assets/1f2558b4-004d-4ca2-8997-45f3986bebac" alt = "reteNeurale">
</p>
<p align="center">
  Rispettivamente w1,w2,w3,w4 evidenziati in colore rosso, giallo, verde, blu. Inoltre sono anche indicati i valori output prodotti dai neuroni dell'input layer
</p>

Il rafforzamento dei collegamenti avviene durante quella che è detta "fase di training" di una rete neurale in cui a una rete neurale si fanno analizzare una grossa quantità di dati, e si rafforzano i collegamenti tra i neuroni o si riducono.

## In termini più matematici ##

Abbiamo compreso in termini intuitivi cosa sia una rete neurale, aggiungiamo poca, pochissima matematica.

Abbiamo detto che un neurone è una funzione i cui input sono gli outuput dei neuroni del layer precedente. Quindi il neurone cerchiato in nero nell'immagine sopra può essere scritto come una funzione dei 4 output dei neuroni del layer precedente. La funzione è $$f(x_1, x_2, x_3, x_4)$$.
Tipicamente questa funzione è detta Funzione di Attivazione ed è molto semplice in quanto è necessario calcolarne la derivata più e più volte durante la fase di training. Le funzioni più usate sono la ReLu la cui derivata è molto semplice e la tangente iperbolica (che seppur abbia un nome spaventoso è una funzione anche essa piuttosto semplice).
Per quanto riguarda il peso da attribuire ai collegamenti, basta aggiungere dei pesi, che quantifichino quanto l'informazione $$x_1, x_2, x_3, x_4$$ siano importanti. Questi pesi andranno indicati con $$w_1, w_2, w_3 e w_4$$. E per comodità in questo esempio facciamoli assumere valori tra 0 e 1. Ad esempio, un peso con valore 1 indicherà che l'informazione è molto importante, un peso con valore 0.5 mediamente importante e un peso con valore 0.25 poco importante e così via. Addirittura se per esempio il peso $$w_4$$ andasse a 0 questo vorrebbe dire che non importa quale outpur il neurone 4 del layer precedente stia producendo io lo ignorerò completamente.
In questo modo la funzione diventa $$f(x_1w_1,x_2w_2,x_2w_3,x_4w_4)$$

## Training ## 

Una rete neurale prima di poter essere utilizzata deve essere addestrata. L'addestramento altro non è che il momento in cui si scelgono i "pesi", o come abbiamo detto prima, stabiliamo quali neuroni vogliamo si attivino di più insieme. E' importante notare che una volta terminata la fase di training i pesi non verranno più toccati. 

Per comprendere come avviene il training a livello matematico sono necessarie conoscenze universitarie di matematica ma a livello intuitivo possiamo spiegarlo come segue. 
Supponiamo di star insegnando una rete neurale come distinguere i numeri scritti a mano. 

Supponiamo di avere 50 immagini e di voler processare 10 immagini per volta (si dice che avremo 5 batch da 10 immagini) e ovviamente di sapere i risultati che ci attendiamo.
All'inizio i pesi vengono calcolati casualmente,  vengono inserite le 10 immagini in input (input layer) , la rete neurale farà i suoi conti e restituirà un output. L'output viene confrontato con quello che ci attendevamo e se non coincide si dirà alla rete di calcolare
nuovamente i pesi (stavolta però tenendo conto del fatto che i vecchi pesi hanno funzionato male) si procederà così al secondo batch con i nuovi pesi, la rete farà nuovamente i conti e restituirà un output, tale output sarà confrontato con i risultati attesi e così via. Terminati i 5 batch di immagini, avremo completato una epoca (tutto il campione di immagini sarà stato esaminato) a quel punto l'addestramento potrà terminare o continuare con una seconda epoca in cui si rianalizeranno le stesse immagini della prima partendo dai pesi che abbiamo ottenuto finora.

### Come scegliere i pesi ###

Nella realtà ovviamente le reti neurali sono gigantesche e la quantità di pesi è spropositata quindi non si puo andare completamente a caso per la scelta dei pesi, si impiegherebbe una eternità. Serve quindi un criterio per comprendere come aggiornare i pesi. 
Volendo evitare di complicare troppo la spiegazione, possiamo dire che è possibile definire una funzione, detta funzione di loss stavolta in grado di misurare la distanza tra i valori che la rete neurale ha prodotto e i valori che ci si aspettava. Questa funzione sarà chiaramente una funzione che dipende dai pesi (w_1,w_2 ecc.) e che noi vorremo "minimizzare" ovvero vorremo trovare in quale punto questa funzione varrà 0, cioè per quali pesi (w_1,w_2 ecc) la distanza tra i valori ottenuti dalla rete neurale e quelli attesi è nulla, cosa che accade esattamente quando i valori ottenuti dalla rete neurale e quelli attesi coincidono.
Fortunatamente in matematica esiste uno strumento potentissimo per fare questo, la derivata. La derivata ci dice se in un certo punto la funzione cresce o decresce, e se variando il peso w_1 ad esempio la funzione crescerà o decrescerà. La soluzione sarà quindi semplicemente quella di calcolare la derivata della funzione di loss alla conclusione di ogni batch e aggiornare i pesi aumentandoli o diminuendoli a seconda che la derivata (in realtà si parlerebbe di gradiente, ma lasciamo stare i formalismi) cresca o decresca.

Tutto qui, questo è come funziona una rete neurale in termini intuitivi.




