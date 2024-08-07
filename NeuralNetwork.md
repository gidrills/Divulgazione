# Cosa è una Rete Neurale #

## Definiamo una Rete neurale ##
Spesso e volentieri si tenede a fare confusione su cosa sia una rete neurale, cosa sia il Machine Learning e cosa il Deep Learning. Bè la verità è che per molti anni anche gli esperti hanno usato alcuni di questi termini in modo interscambiabile, ad oggi però
la teoria è abbastanza precisa, vediamo quindi cosa intendiamo con ognuno dei termini elencati.
- **AI** L'insieme delle discipline Natural Language Processing, Knowledge Representation, Automated Reasoning e Machine Learning
- **Machine Learning** Disciplina della AI che in particolare si occupa di far imparare ai computer, attraverso i dati, come risolvere i problemi senza essere esplicitamente istruita per farlo.
- **Neural Network** Tipo di modello (rappresentazione in termini matematici, ma anche non) di Machine Learning. In particolare questo modello si ispira alle rete neurale naturale.

## Ok quindi una rete neural è un tipo di modello di Machine Learning che si ispire alla rete neurale umana, ma in che modo lo fa? ##

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

Ok abbiamo capito a cosa servono queste sinapsi, ma effettivamente cosa sono le sinapsi in una rete artificiale? La risposta è piuttosto semplice in realtà, supponiamo di essere un neurone, quello colorato in nero in figura, come posso distinguere la potenza dei collegamenti, la risposta più semplice è associo un numero a questi collegamenti ovvero un "peso" ? Bè semplicemente dando più peso alla informazioni che viene da un determinato neuroni rispetto alla informazione che viene da un altro.

## ?

concentriamoci sul primo neurone dell'hidden layer (colorato in nero), come già detto riceverà informazioni da tutti i neuroni del layer precedente, ma ha senso dare lo stesso peso alle informazioni provenienti dai 4 neuroni diversi? Se due neuroni dicessero "no" e altri due neuroni dicessero "si" io neurone nero che informazione dovrei produrre? Produrrei probabilmente a mia volta un output che sarebbe o "si" o "no". Risulta ovvio che l'introduzione di un sistema per pesare le informazioni ottenute aiuti ad aumentare la complessità della rete neurale.

## Ok, ma come funziona una rete neurale?

In realtà è abbastanza semplice, ci basta defi
- **Neurone** oggetto in grado di prendere diversi input (valori in ingresso) e restituire un singolo output (in matematica, è una funzione di più variabili f(x,y,....z)). 

Una rete neurale altro non è che un insieme di Neuroni artificiali organizzati in strutture dette layer. Tipicamente si utilizzano almeno 3 layers, input layer, hidden layer, output layer.


Una re
