# DELVE

## Un dungeon crawler solitario per DECK#

**Sistema:** DECK# (Profilo Esteso)  
**Giocatori:** 1 (espandibile a 2 cooperativo)  
**Durata:** 30–50 minuti  
**Componenti:** 1 mazzo DECK# · 6d6 · 6 gettoni (monete) · 1 pedina

---

## Il concetto

Scendi in un dungeon che non conosci. Ogni carta posata rivela una stanza: cosa contiene, come è connessa alle altre, quanto è pericolosa. Non sai cosa c'è oltre il prossimo bordo aperto. Sopravvivi abbastanza a lungo da raggiungere la stanza finale.

DELVE è un gioco di risorse limitate e decisioni irreversibili. Non si torna indietro facilmente. Ogni stanza rivela informazioni ma consuma qualcosa.

---

## Mappatura degli assi DECK#

| Asse | Valore in DELVE |
|---|---|
| **Valore (A–6)** | Stanza sicura — esplorazione, recupero, oggetti |
| **Valore (7–10)** | Stanza pericolosa — incontro, trappola, scelta |
| **Valore (J–K)** | Stanza boss — combattimento obbligatorio |
| **Colore rosso** | Stanza attiva: l'effetto si applica immediatamente all'ingresso |
| **Colore nero** | Stanza latente: l'effetto si applica solo se ti fermi (non transiti) |
| **Seme** | Tipo di stanza (vedi tabella) |
| **Primario** | Contenuto della stanza |
| **Modificatore** | Condizione ambientale |

### Tipo di stanza per seme

| Seme | Tipo |
|---|---|
| ♥ | Rifugio — recupero, riposo, oggetti benefici |
| ♦ | Passaggio — corridoio, scelta di direzione, informazione |
| ♣ | Pericolo — trappola, incontro, consumo di risorse |
| ♠ | Profondità — boss, tesoro, punto di non ritorno |

---

## Il personaggio

Il personaggio ha tre risorse, tracciate con d6:

| Risorsa | Valore iniziale | Significato |
|---|---|---|
| **Vita (❤)** | 6 | A 0: il personaggio muore, partita persa |
| **Torcia (🔦)** | 6 | A 0: il dungeon è al buio — non puoi rivelare nuove stanze |
| **Forza (⚔)** | 6 | Usata per combattere — si recupera solo in ♥ |

Posiziona tre d6 davanti a te con i valori indicati. Abbassali quando le risorse calano.

---

## La struttura del dungeon

Il dungeon si costruisce carta per carta durante la partita. Si parte da **una carta di ingresso** (la prima carta pescata, posata al centro del tavolo, polo nord verso l'alto). La pedina del personaggio parte su questa carta.

Le carte non ancora rivelate sono il dungeon inesplorato. Il mazzo è il buio davanti a te.

### Regola del polo nord

In DELVE l'orientamento è fisso: ogni carta si posa sempre con il polo nord verso l'alto (indice in NW in alto a sinistra). Il designer del dungeon sei tu, ma la mappa risponde alle sue leggi, non alle tue.

---

## Struttura del turno

### Fase 1 — Torcia

Abbassa la Torcia di 1. Se scende a 0, non puoi rivelare nuove stanze questo turno (salta la Fase 2). Puoi ancora muoverti nelle stanze già rivelate.

### Fase 2 — Esplorazione (opzionale se Torcia > 0)

Pesca 1 carta dal mazzo. Posala adiacente a qualsiasi carta già sul tavolo tramite un bordo aperto compatibile — bordo aperto della nuova carta a contatto con bordo aperto di una carta esistente.

La carta rivela una nuova stanza. Leggi subito il suo tipo (seme) e annota mentalmente cosa ti aspetta se ci entri.

Se nessuna posizione valida esiste (tutti i bordi aperti della carta sono incompatibili con i bordi aperti disponibili), posa la carta comunque nella posizione più logica e trattala come stanza isolata — raggiungibile solo con l'azione △ del glifo primario (vedi Glifo primario).

### Fase 3 — Movimento

Muovi la pedina di **1 stanza** attraverso un bordo aperto. Non puoi attraversare muri. Non puoi restare ferma se esiste almeno un bordo aperto dalla stanza corrente.

**Eccezione:** puoi scegliere di **sostare** — restare nella stanza corrente. Sosta conta come movimento. Applicare l'effetto di sosta è una scelta, non un obbligo (ma vedi Colore nero).

### Fase 4 — Stanza

Applica l'effetto della stanza in cui ti trovi:

**Se la stanza è rossa:** applica l'effetto immediatamente, che tu soste o transiti.  
**Se la stanza è nera:** applica l'effetto solo se hai sostato.

#### Effetti per seme e valore

**♥ Rifugio (stanza sicura A–6):**
- Recupera Vita pari a (7 − valore della carta), minimo 1. Non puoi superare 6.
- Se sosti: recupera anche 1 Forza.

**♥ Rifugio (stanza pericolosa 7–10):**
- Il rifugio è compromesso. Recupera 1 Vita solo se sosti e superi una prova (lancia 1d6: risultato ≥ 4).

**♦ Passaggio:**
- Rivela immediatamente 1 carta aggiuntiva dal mazzo e posala adiacente (senza consumare Torcia).
- Se sosti: rivela 2 carte aggiuntive invece di 1.

**♣ Pericolo (stanza sicura A–6):**
- Trappola minore: perdi 1 risorsa a scelta (Vita, Torcia o Forza).
- Se sosti: puoi disarmarla — lancia 1d6, risultato ≥ 3: nessuna perdita.

**♣ Pericolo (stanza pericolosa 7–10):**
- Incontro: vedi Combattimento.

**♠ Profondità (qualsiasi valore):**
- Punto di non ritorno: una volta entrato, non puoi tornare nelle stanze precedenti attraverso questa carta (il bordo da cui sei venuto diventa muro per te, segnalo con un gettone).
- Se stanza boss (J–K): vedi Combattimento obbligatorio.
- Se non boss: tesoro — guadagna 1 Forza e pesca subito 1 carta aggiuntiva.

---

## Il glifo primario — azioni speciali

Il glifo primario della stanza in cui ti trovi offre un'azione speciale, usabile **una volta per visita** (non per partita):

| Primario | Azione |
|---|---|
| • (punto) | **Cerca:** guarda le prime 3 carte del mazzo senza rivelarle. Rimettile nell'ordine che preferisci. |
| — (linea) | **Barricata:** chiudi un bordo aperto a scelta di questa stanza con un gettone-muro permanente. |
| + (croce) | **Segnale:** recupera 1 Torcia. |
| × (diagonale) | **Fuga:** puoi muoverti di 2 stanze questo turno invece di 1, ignorando gli effetti della prima stanza attraversata. |
| △ (triangolo) | **Scatto:** puoi raggiungere una stanza isolata (senza bordi aperti compatibili) come se fosse adiacente. |
| ○ (cerchio) | **Respiro:** recupera 1 Vita e 1 Forza. Poi pesca 1 carta — se è ♣ o ♠, perdila senza effetto. |
| □ (quadrato) | **Fortifica:** questa stanza non applica più effetti negativi finché ci sei. Dura fino a quando esci. |

---

## Il glifo modificatore — condizione ambientale

Il modificatore si applica sempre, in qualsiasi stanza, indipendentemente dal primario:

| Modificatore | Condizione |
|---|---|
| • (punto) | **Illuminata:** non consuma Torcia quando entri in questa stanza (non in Fase 1, ma all'ingresso). |
| — (linea) | **Neutra:** nessuna condizione. |
| + (croce) | **Connessa:** i bordi aperti di questa stanza contano come aperti anche per le carte adiacenti che avrebbero muri su quel lato. |
| × (diagonale) | **Corrotta:** ogni volta che usi l'azione del primario in questa stanza, perdi 1 Vita. |
| △ (triangolo) | **Crescente:** ogni round che rimani in questa stanza, l'effetto del seme si applica di nuovo (in bene o in male). |
| ○ (cerchio) | **Ciclica:** a fine round, gira la carta di 90° (cambia la connettività attiva). |
| □ (quadrato) | **Schermata:** gli effetti di stanze adiacenti non si propagano qui. |

---

## Combattimento

Il combattimento si risolve con un sistema a confronto di dadi. Non c'è tracciamento dei punti ferita del nemico: ogni combattimento è un singolo scontro risolutivo.

**Forza del nemico:** determinata dal valore della carta.

| Valore | Dadi nemico | Dadi personaggio |
|---|---|---|
| 7–8 | 2d6 (tieni il più alto) | Forza d6 (lancia tanti d6 quanti punti Forza hai, tieni il più alto) |
| 9–10 | 2d6 (tieni i due più alti, somma) | Forza d6 (somma i due più alti) |
| J | 3d6 (tieni i due più alti, somma) | Forza d6 (somma i due più alti) |
| Q | 3d6 (somma tutti) | Forza d6 (somma i tre più alti) |
| K | 4d6 (somma tutti) | Forza d6 (somma i tre più alti) |

**Risoluzione:**
- Personaggio vince: nessuna perdita. Se stanza ♠: guadagna 2 Forza e pesca 1 carta.
- Pareggio: perdi 1 Vita. Il nemico è ancora lì — puoi fuggire (azione ×) o combattere di nuovo al prossimo turno.
- Nemico vince: perdi Vita pari alla differenza tra i totali. Se Vita scende a 0: partita persa.

**Modificatore al combattimento:**
- Stanza rossa: +1 al tiro del personaggio (terreno aperto, vantaggio tattico).
- Stanza nera: +1 al tiro del nemico (copertura per il nemico).

---

## I Jolly — le stanze Abisso

I 2 Jolly rimangono nel mazzo e vengono rivelati durante l'esplorazione come qualsiasi altra carta. Quando una carta Jolly viene rivelata:

1. Posala normalmente (orientamento fisso, polo nord in alto).
2. Non ha connettività: tutti e quattro i suoi bordi sono **aperti**. Il Jolly è sempre accessibile da qualsiasi direzione.
3. Non ha seme, valore, primario né modificatore. È una **stanza Abisso**.

**Effetto della stanza Abisso:**  
Quando entri in una stanza Abisso, scegli:
- **Scendi:** perdi 2 Vita e 1 Torcia, ma pesca 3 carte e aggiungile al dungeon (rivelazione immediata, posizionamento a scelta tramite bordi aperti).
- **Osserva:** non perdi nulla, ma non puoi usare alcuna azione speciale questo turno.

Il secondo Jolly funziona allo stesso modo. Le due stanze Abisso sono distinte — entrarci due volte nella stessa partita è possibile.

---

## Condizione di vittoria

Il dungeon ha una **stanza finale**: la carta con valore K di ♠ (K♠). Quando questa carta viene rivelata, è visibile a tutti (già lo è, essendo sul tavolo).

**Vinci** quando:
- Entri nella stanza K♠ con Vita > 0 dopo aver sconfitto il boss in combattimento.

**Perdi** se:
- Vita scende a 0 in qualsiasi momento.
- Il mazzo si esaurisce prima che K♠ venga rivelata (il dungeon ha avuto la meglio su di te).

---

## Variante cooperativa a 2

Un secondo giocatore entra nel dungeon con le stesse risorse iniziali. I due personaggi si muovono separatamente ma condividono il dungeon rivelato.

Variazioni:
- Nel combattimento, se entrambi i personaggi sono nella stessa stanza, sommano i dadi Forza.
- Se un personaggio scende a 0 Vita, l'altro può raggiungerlo entro 2 turni per "stabilizzarlo" (riporta a 1 Vita, perde 2 Forza propria). Una sola volta per partita.
- Vincono entrambi se K♠ viene conquistata con almeno 1 personaggio vivo.

---

## Note di design

**Perché A–6 / 7–10 / J–K come soglie?**  
La distribuzione della connettività in DECK# mostra che A e J tendono ad avere meno bordi aperti, K e 8 di più. In DELVE questo crea una risonanza: le stanze boss (J–K) tendono ad essere più connesse — più esposte, più raggiungibili, più centrali nella mappa emergente. Non è garantito, ma è una pressione statistica che il giocatore sentirà nel corso della partita.

**Perché rosso = attivo e nero = latente?**  
Il colore è il discriminatore più immediato in una carta. La distinzione attivo/latente è la più consultata durante il gioco — "questo effetto mi colpisce subito o solo se mi fermo?" Assegnarla al colore riduce il carico cognitivo al minimo.

**Perché il Jolly ha tutti i bordi aperti?**  
Perché la stanza Abisso deve essere raggiungibile da qualsiasi direzione — è un'anomalia del dungeon, non una stanza normale. L'assenza di connettività annotata diventa essa stessa un'informazione: quando vedi una carta senza marcatori di bordo, sai che è un Jolly prima ancora di guardarne il fronte.