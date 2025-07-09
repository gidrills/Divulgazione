
**Slide 1**
Redis, il database nato in Italia e usato da Twitter e GitHub!

Scopri la storia di antirez e di come ha creato Redis! →

**Slide 2**

Conosci Salvatore Sanfilippo? 

Più noto come antirez, è un programmatore siciliano che ha rivoluzionato il mondo dei database.

Non aveva esperienza precedente in database, forse proprio questo gli ha permesso di introdurre innovazioni rivoluzionarie!

**Slide 3**

La svolta inaspettata di Salvatore.

Studente di Architettura con la passione della sicurezza informatica, scopre per caso una vulnerabilità importante e finisce a lavorare nella cybersecurity a Milano.

Inventò l'*Idle Scan*, famoso attacco ancora oggi utilizzato.

**Slide 4**

Dalla Sicilia a Redis.

Con un amico fonda Merzia, società specializzata in Web 2.0.

Nel 2007 creano LLOOGG, uno strumento di analytics per blogger che mostrava in tempo reale il comportamento degli utenti.

Problema? MySQL, il database scelto inizialmente, non riusciva a reggere il carico di dati.

Come mai ? →

**Slide 5**

MySQL era troppo lento a causa delle letture e scritture sul disco.

Antirez pensa: "E se mettessi tutto in memoria RAM?”

Nasce così LMDB (LLOOGG Memory Database), il primo prototipo di Redis!

Capiamo meglio →

**Slide 6**

La differenza tra Ram e Disco è semplice. 

- La RAM è veloce, ma volatile (se spegni il computer perdi tutti i dati).
- Il Disco è lento, ma non volatile.

Redis salva tutti i dati in RAM, in questo modo si ottengono tempi di accesso estremamente rapidi.

Ok e se si spegne il computer che succede? →

**Slide 7**

Redis implementa anche funzionalità di backup che salvano periodicamente i dati anche sul disco. In questo modo, se il computer si spegne, si perdono solo i dati salvati tra un backup e l’altro.

Così si ha il massimo della velocità, con perdite minime di dati in caso di interruzione.

**Slide 8**

Inoltre, diversamente dai database tradizionali, Redis lavora con strutture dati semplici e veloci (liste, set, hash tables) :

- **Liste**: ottime per le notifiche, permettono di aggiungere/rimuovere elementi velocemente da inizio o fine.
- **Set**: ideali per gestire dati unici come follower o like, eliminano duplicati automaticamente!

---

**Slide 9**

Questo lo ha reso incredibilmente popolare tra aziende come GitHub, Instagram e Twitter! E, secondo i sondaggi di Stack Overflow, Redis è stato il database più amato dagli sviluppatori dal 2017 al 2022!

---

**Slide 10**

Redis è diventato uno standard tecnologico globale partendo, come spesso succede, da una semplice esigenza personale e dalla passione di una singola persona.

Tu conoscevi Redis? In che occasioni lo hai utilizzato?
