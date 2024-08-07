# Cosa è una Rete Neurale #

## Definiamo una Rete neurale ##
Spesso e volentieri si tenede a fare confusione su cosa sia una rete neurale, cosa sia il Machine Learning e cosa il Deep Learning. Bè la verità è che per molti anni anche gli esperti hanno usato alcuni di questi termini in modo interscambiabile, ad oggi però
la teoria è abbastanza precisa, vediamo quindi cosa intendiamo con ognuno dei termini elencati.
- **AI** L'insieme delle discipline Natural Language Processing, Knowledge Representation, Automated Reasoning e Machine Learning
- **Machine Learning** Disciplina della AI che in particolare si occupa di far imparare ai computer, attraverso i dati, come risolvere i problemi senza essere esplicitamente istruita per farlo.
- **Neural Network** Tipo di modello (rappresentazione in termini matematici, ma anche non) di Machine Learning. In particolare questo modello si ispira alle rete neurale naturale.

## Ok quindi una rete neurale è un tipo di modello di Machine Learning che si ispira alla rete neurale umana, ma in che modo lo fa? ##

Bè semplificando molto una rete neurale umana possiamo dire che i neuroni sono cellule in grado di ricevere e trasmettere informazioni attraverso segnali elettrici, la potenza dei segnali elettrici è poi regolata dalle sinapsi, ovvero i collegamenti tra i neuroni.


Perfetto, una rete artificiale è molto simile, un neurone artificiale è però più semplicemente una funzione, in grado di prendere degli input e produrre un output.

Questi input sono tipicamente valori che semplificando possiamo dire vanno da -1 a 1. Mentre le funzioni sono dette funzioni di attivazioni e sono tipicamente abbastanza semplici.
Per comodità di sviluppo si tende a organizzare i neuroni artificiali in layer e tipicamente ogni neurone di un layer è collegato con tutti i neuroni del layer successivo come in figura.

<p align="center">
  <img src="https://github.com/user-attachments/assets/79441ba7-54d5-4807-b2b3-586e829446a2" alt="reteNeurale">
</p>
<p align="center">
  I cerchietti sono i neuroni, le linee i collegamenti tra neuroni (sinapsi).
</p>


Perfetto, e le sinapsi? Bè questa è la parte interessante delle reti neurali sia naturali che artificiali. Partiamo da una domanda, come facciamo a dire a una rete che si sta comportando bene o che si sta comportando male? Bè rafforziamo le sinapsi, rafforziamo i collegamenti tra alcuni neuroni che vogliamo si "attivino" di più e riduciamo i collegamenti tra altri che vogliamo si attivino "meno". In altri termini stabiliamo quali neuroni lavorano bene insieme e quali lavorano male. 
Nella figura sopra quindi i collegamenti dovrebbero avere dei colori diversi, per distinguere che non sono tutti uguali.

<p align="center">
  <img src= "https://github.com/user-attachments/assets/7286a608-50ab-4ad0-bbb3-42d491370690" alt = "reteNeurale">
</p>

Il rafforzamento dei collegamenti avviene durante quella che è detta "fase di training" di una rete neurale in cui a una rete neurale si fanno analizzare una grosso di quantità di dati, e si rafforzano i collegamenti tra i neuroni che sembrano comportarsi meglio.

## Un po' di matematica ##

Abbiamo compreso in termini intuitivi cosa sia una rete neurale, aggiungiamo poca, pochissima matematica.

Abbiamo detto che un neurone è una funzione i cui input sono gli outuput dei neuroni del layer precedente. Quindi un neurone come nell'immagine sopra può essere scritto come una funzione dei 4 output dei neuroni del layer precedente. La funzione è $$f(x_1, x_2, x_3, x_4)$$.
Tipicamente questa funzione è detta Funzione di Attivazione ed è molto semplice in quanto è necessario calcolarne la derivata più e più volte durante la fase di training. Le funzioni più usate sono la ReLu la cui derivata è molto semplice e la tangente iperbolica (che seppur abbia un nome spaventoso è una funzione piuttosto semplice).
Per quanto riguarda il peso da attribuire ai collegamenti, basta aggiungere dei pesi, che quantifichino quanto l'informazione x_1, x_2, x_3, x_4 siano importanti. Questi pesi andranno indicati con w_1, w_2, w_3 e w_4. E per comodità in questo esempio facciamoli assumere valori tra 0 e 1. Un peso con valore 1 indicherà che l'informazione è molto importante, un peso con valore 0.5 mediamente importante e un peso con valore 0.25 poco importante. In questo modo la funzione diventa $$f(x_1, x_2, x_3, x_4)$$






