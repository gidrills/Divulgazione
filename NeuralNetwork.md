# Cosa è una Rete Neurale #

## Definiamo una Rete neurale ##
Spesso e volentieri si tenede a fare confusione su cosa sia una rete neurale, cosa sia il Machine Learning e cosa il Deep Learning. Bè la verità è che per molti anni anche gli esperti hanno usato alcuni di questi termini in modo interscambiabile, ad oggi però
la teoria è abbastanza precisa, vediamo quindi cosa intendiamo con ognuno dei termini elencati.
- **AI** L'insieme delle discipline Natural Language Processing, Knowledge Representation, Automated Reasoning e Machine Learning
- **Machine Learning** Disciplina della AI che in particolare si occupa di far imparare ai computer, attraverso i dati, come risolvere i problemi senza essere esplicitamente istruita per farlo.
- **Neural Network** Tipo di modello (rappresentazione in termini matematici, ma anche non) di Machine Learning. In particolare questo modello si ispira alle rete neurale naturale.

Ok quindi una rete neural è un tipo di modello di Machine Learning che si ispire alla rete neurale umana, ma in che modo lo fa?

Bè semplificando molto una rete neurale umana possiamo dire che i neuroni sono cellule in grado di ricevere e trasmettere informazioni attraverso segnali elettrici, la potenza dei segnali elettrici è poi regolata dalle sinapsi, i collegamenti tra i neuroni.
Perfetto una rete artificiale è molto simile, un neurone artificiale è però più semplicemente una funzione, in grado di prendere degli input e produrre un output. Per comodità di sviluppo si tende a organizzare i neuroni artificiali in layer e tipicamente ogni neurone di un layer è collegato con tutti i neuroni del layer successivo come in figura.

<p align="center">
  <img src="https://github.com/user-attachments/assets/79441ba7-54d5-4807-b2b3-586e829446a2" alt="reteNeurale">
</p>
<p align="center">
  I cerchietti sono i neuroni, le linee i collegamenti tra neuroni.
</p>

Il neurone artificiale è però più semplicemente una funzione e l' impulso elettrico un numero.
Ovviamente ogni neurone può ricevere più numeri, in modo più formale diremo può ricevere più "inputs", e produrre un solo numero l' "output".
I neuroni artificiali sono rappresentati tipicamente come dei cerchietti e le loro connessioni (i canali attraverso cui ricevono gli inputs) con delle righe.




## Ok, ma come funziona una rete neurale?

In realtà è abbastanza semplice, ci basta defi
- **Neurone** oggetto in grado di prendere diversi input (valori in ingresso) e restituire un singolo output (in matematica, è una funzione di più variabili f(x,y,....z)). 

Una rete neurale altro non è che un insieme di Neuroni artificiali organizzati in strutture dette layer. Tipicamente si utilizzano almeno 3 layers, input layer, hidden layer, output layer.


Una re
