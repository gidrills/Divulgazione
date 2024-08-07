# Cosa è una Rete Neurale #

## Definiamo una Rete neurale ##
Spesso e volentieri si tenede a fare confusione su cosa sia una rete neurale, cosa sia il Machine Learning e cosa il Deep Learning. Bè la verità è che per molti anni anche gli esperti hanno usato alcuni di questi termini in modo interscambiabile, ad oggi però
la teoria è abbastanza precisa, vediamo quindi cosa intendiamo con ognuno dei termini elencati.
- **AI** L'insieme delle discipline Natural Language Processing, Knowledge Representation, Automated Reasoning e Machine Learning
- **Machine Learning** Disciplina della AI che in particolare si occupa di far imparare ai computer, attraverso i dati, come risolvere i problemi senza essere esplicitamente istruita per farlo.
- **Neural Network** Tipo di modello (rappresentazione in termini matematici, ma anche non) di Machine Learning. In particolare questo modello si ispira alle rete neurale naturale.

Ok quindi una rete neural è un tipo di modello di Machine Learning che si ispire alla rete neurale umana, ma in che modo lo fa?
Bè semplificando molto una rete neurale umana possiamo dire che i neuroni naturali sono cellule in grado di ricevere e trasmettere informazioni attraverso segnali elettrici verso tutti gli altri neuroni collegati. La potenza dei segnali elettrici
dipende dalle sinapsi (i collegamenti tra questi neuroni). Nella immagine qui sotto schematizzo il comportamento.

<p align="center">
  <img src="https://github.com/user-attachments/assets/79441ba7-54d5-4807-b2b3-586e829446a2" alt="reteNeurale">
</p>
<p align="center">
  I cerchietti sono i neuroni, le linee sono le sinapsi tra neuroni.
</p>


Perfetto un neurone artificiale possiamo dire faccia la stessa cosa, il neurone artificiale è però più semplicemente una funzione e gli impulsi elettrici dei numeri (inputs) che questa funzione è in grado di elaborare per poi produrre  a sua volta un numero (output).

Ottimo e le sinpasi? La rappresentazione artificiale delle sinapsi sono la parte interessante delle reti neurali. Abbiamo detto che ogni neurone riceverà degli inputs dai neuroni vicini, ma questi input avranno tutti lo stesso impatto? 



## Ok, ma come funziona una rete neurale?

In realtà è abbastanza semplice, ci basta defi
- **Neurone** oggetto in grado di prendere diversi input (valori in ingresso) e restituire un singolo output (in matematica, è una funzione di più variabili f(x,y,....z)). 

Una rete neurale altro non è che un insieme di Neuroni artificiali organizzati in strutture dette layer. Tipicamente si utilizzano almeno 3 layers, input layer, hidden layer, output layer.


Una re
