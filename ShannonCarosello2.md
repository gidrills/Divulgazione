# Slide 1

Titolo : Limite di Shannon, abbiamo già raggiunto il limite teorico alla compressione dei dati?
Sottotitolo: Capiamo cosa significa comprimere un messaggio senza perdere informazione e se il limite teorico è stato raggiunto.

# Slide 2 La informazione 54 caratteri

Per comprendere cosa sia l'informazione, possiamo partire da una definizione piuttosto intuitiva che fu proposta da Claude Shannon nel 1948: l'informazione è ciò che riduce la nostra incertezza.

L'informazione può essere trasmessa attraverso messaggi, che consistono in sequenze di caratteri provenienti da un alfabeto specifico.

Ad esempio:

- L'alfabeto inglese è composto da 26 caratteri, le lettere.
- L'alfabeto "informatico" invece, è formato da soli due caratteri, i bit: {0, 1}.


# Slide 3 La compressione

Scrivere messaggi brevi (comprimere) dato un alfabeto, dipendende dal tipo di codifica scelto.

Ad esempio per la stringa ABCDD potremmo usare queste 2 codifiche.

<table>
<tr>
  <th style="text-align:left;">Codifica 1</th>
  <th style="text-align:center;">Stringa inglese</th>
 <th style="text-align:center;">Stringa binario</th>
  <th style="text-align:center;">Totale bit</th>
</tr>
  <td>
    <strong>A</strong>: <code>00</code><br>
    <strong>B</strong>: <code>01</code><br>
    <strong>C</strong>: <code>11</code><br>
    <strong>D</strong>: <code>101</code>
  </td>
  <td style="text-align:center;">
    ABCDD<br>
  </td>
 <td style="text-align:center;">
    00 01 11 101 101<br>
  </td>
 
  <td style="text-align:center;">
    12 bit
  </td>
</tr>
</table>

---


<table>
<tr>
  <th style="text-align:left;">Codifica 2</th>
  <th style="text-align:center;">Stringa inglese</th>
 <th style="text-align:center;">Stringa binario</th>
  <th style="text-align:center;">Totale bit</th>
</tr>
  <td>
    <strong>D</strong>: <code>00</code><br>
    <strong>B</strong>: <code>01</code><br>
    <strong>C</strong>: <code>11</code><br>
    <strong>A</strong>: <code>101</code>
  </td>
  <td style="text-align:center;">
    ABCDD <br>
  </td> 
 <td style="text-align:center;">
    101 01 11 00<br>
  </td>
  <td style="text-align:center;">
    9 bit
  </td>
</tr>
</table>


---

E' facile osservare che la seconda codifica ci fa risparmiare 3 bit

### Domanda

Ottimo, ma esiste una codifica per la quale si raggiunge una compressione massima ? ->

# Slide 4

Shannon sviluppò una teoria per rispondere a questa domanda. Iniziò col formalizzare il concetto di informazione. 

Si domandò: come si può misurare quanta informazione è contenuta in un messaggio?

Bè intuitivamente possiamo dire che un messaggio fornisce più informazione quanto più ci sorprende, poichè elimina molta più incertezza ( informazione = ciò che elimina incertezza ).

Ad esempio, supponiamo Bob lanci un dado ma abbia un alfabeto limitato :

- gli eventi possibili sono {1, 2, 3 ,4 ,5 ,6}
- il suo alfabeto però consiste solo di {1, E, 6}


# Slide 5
Se bob nel suo messaggio scrive "E" fornirà meno informazione rispetto a scrivere "6". Questo perché "E" ha una probabilità di 2/3 di verificarsi e lascia incertezza ( potrebbero essere usciti 2,3,4 o 5 ), mentre "6" ha una probabilità di 1/6 e toglie tutta la incertezza.

La quantità di informazione di un messaggio dipende quindi dalla probabilità che l'evento (o gli eventi) a cui si riferisce si verifichino.

- In particolare dipende al logaritmo della probabilità I(x) = -log_2(x).

# Slide 6 Entropia della informazione

Ottimo, ancora uno sforzo. 

Ad un dado sono assocciati 6 eventi mutuamente esclusivi, e ogni evento come abbiamo visto ha una informazione associata. Possiamo fare una media di questa quantità: una media della quantità di informazione.

$$
H_{\text{dado}} = \frac{1}{6} \left[ I(\text{Estrazione} = 1) + I(\text{Estrazione} = 2) + I(\text{Estrazione} = 3) + ...\right] = 2.58496 Bit
$$

Questa quantità è detta entropia dell'informazione e rappresenta mediamente quanta informazione posso attendermi dalla lettura di un dado.

Ok, e come ci aiuta a comprendere il limte della compressione ? ->

### Qui si potrebbe poi aggiungere una nota di questo tipo "Per i più esperti, la formula generale includerebbe le probabilità che l'evento accada", in quanto nella formula più generale la I va moltiplicata per la probabilità che l'evento accada, ma nel caso specifico del dado non è necessario perchè sono tutte 1/6 queste probablità. 



# Slide 7 (Limite di Shannon)

Shannon usò l'entropia per dimostrare che esisteva un un limite alla compressione dei dati. 

In termini intuitivi il primo teorema di Shannon afferma che il limite massimo di compressione dei dati senza perdita di informazione è determinato dall'entropia della sorgente di informazione (il dado). 

In altri termini, la miglior codifica è quella che ci permette di costruire un messaggio il cui numero di bit per lettera è 2.5849 bits mediamente. Sotto quel valore è impossibile andare.


# Slide 8 Esempio reale

Il dado è un esempio, ma nella realtà anche le lettere dell'alfabeto hanno una diversa probabilità di apparire in un messaggio (la E compare circa il 13% delle volte in un testo in inglese).
Se nel caso del dado la probabilità di leggere "E" era 1/6 nel caso di un testo inglese è 13/100.

Analogamente quindi per un testo inglese è possibile calcolare l'entropia e quindi la compressione massima, che risulta essere 3.9 bits per lettera circa. 

- suggerimento: Inserire qui screen di wikipedia o tabella che riporta la frequency letter inglese https://en.wikipedia.org/wiki/Letter_frequency 

# Slide9 Esempio reale

Il sistema di codifica più usato ad oggi è quello di Huffman (evoluzione di Shannon-Fano), che comprime un testo inglese a circa 4,1083 bit per lettera, avvicinandosi al limite teorico di Shannon.

Altre codifiche, come quella aritmetica, possono raggiungere questo limite ma sono meno efficienti. 

Per un'immagine, l'"alfabeto" sono i pixel, e la compressione dipende dalla probabilità dei colori.

Ma tenendo conto delle ridondanze, potremmo superare il limite di Shannon? ->

# qui scrivo la Codifica Huffman per ogni carattere, si potrebbero tabellare, e mostrare in una figura (anche solo i primi 5-6 caratteri):
| Character | Shannon-Fano Code | Huffman Code |
|-----------|-------------------|--------------|
| A         | 001               | 1111         |
| B         | 111100            | 1100111      |
| C         | 11010             | 00011        |
| D         | 1011              | 0100         |
| E         | 0000              | 101          |
| F         | 111000            | 110001       |
| G         | 111011            | 010110       |
| H         | 1010              | 0110         |
| I         | 0101              | 1101         |
| J         | 11111110          | 11001010101  |
| K         | 1111100           | 1100100      |
| L         | 11000             | 0000         |
| M         | 11011             | 00010        |
| N         | 011               | 1001         |
| O         | 0100              | 1110         |
| P         | 111101            | 1100110      |
| Q         | 11111100          | 110010100    |
| R         | 1000              | 1000         |
| S         | 1001              | 0111         |
| T         | 0001              | 001          |
| U         | 11001             | 01010        |
| V         | 1111101           | 11001011     |
| W         | 111010            | 010111       |
| X         | 11111101          | 1100101011   |
| Y         | 111001            | 110000       |
| Z         | 11111111          | 11001010100  |



# Slide 10

La verità è che la entropia di Shannon appena calcolata si basa su un modello statistico incompleto. Per comodità noi abbiamo assunto implicitamente che non ci sia una dipendenza tra le lettere. Di fatto, la codifica Huffman considera la possibilità di leggere una "u" al 2.8 %, ma non considera la dipendenza tra "q" ed "u" ad esempio che in inglese è molto alta. Algoritmi usati in winrar, zip, 7zip ecc. tengono conto di queste dipendenze e codificano combinazioni di caratteri insieme.

 
