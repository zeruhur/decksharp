# GUILD

## Un gioco di piazzamento lavoratori per DECK#

**Sistema:** DECK# (Profilo Base)
**Giocatori:** 2 · espandibile a 4 con un secondo mazzo
**Durata:** 45–60 minuti
**Componenti:** 1 mazzo DECK# · 6 gettoni per giocatore (monete o cubetti, 2 colori distinti)

---

## Il concetto

Due gilde si contendono il controllo di un mercato che cambia ogni round. Le carte sul tavolo sono le azioni disponibili: chi piazza un lavoratore su una carta la occupa e ne sfrutta l'effetto. Ma le carte vengono sostituite, le risorse si esauriscono, e una gilda che non pianifica perde terreno.

GUILD è un gioco di ottimizzazione e blocco. Non basta scegliere la mossa migliore per sé — bisogna anche impedire all'avversario di fare la sua.

---

## Mappatura degli assi DECK#

| Asse | Valore in GUILD |
|---|---|
| **Valore (A–6)** | Azione minore: effetto immediato, basso costo |
| **Valore (7–10)** | Azione maggiore: effetto più potente, costo medio |
| **Valore (J–K)** | Azione gilda: effetto speciale, disponibile una volta per round |
| **Colore rosso** | Azione di produzione: genera risorse |
| **Colore nero** | Azione di influenza: modifica il mercato o blocca l'avversario |
| **Seme** | Settore del mercato (vedi tabella) |
| **Primario** | Tipo di effetto dell'azione |
| **Modificatore** | Condizione di attivazione o bonus |

### Settori del mercato

| Seme | Settore | Tema |
|---|---|---|
| ♥ | Artigianato | Produzione diretta, conversione risorse |
| ♦ | Commercio | Scambio, guadagno, moltiplicatori |
| ♣ | Politica | Blocco, manipolazione, vantaggi asimmetrici |
| ♠ | Espansione | Crescita a lungo termine, punti vittoria diretti |

---

## Risorse

Ogni giocatore traccia le proprie risorse con i gettoni davanti a sé:

| Risorsa | Simbolo | Valore iniziale |
|---|---|---|
| Oro | gettoni chiari | 3 |
| Influenza | gettoni scuri | 3 |

Le risorse non hanno un massimo. Non si può scendere sotto 0 — un'azione che richiederebbe più risorse di quelle disponibili non può essere eseguita.

---

## Setup

**1. Il mercato iniziale**

Pesca 9 carte dal mazzo mescolato. Posale scoperte in una griglia 3×3 al centro del tavolo — questa è la **plancia mercato**. Orienta ogni carta col polo nord verso l'alto. Le carte non si accostano per connettività: in GUILD la griglia è fissa, la connettività non è attiva.

**2. La riserva**

Le carte rimanenti formano il **mazzo riserva**, coperto a lato del mercato.

**3. Lavoratori**

Ogni giocatore ha **3 lavoratori**, rappresentati dai propri gettoni (usa un colore per i lavoratori, l'altro per tracciare le risorse — oppure usa oggetti distinti).

**4. Primo giocatore**

Chi ha più Influenza inizia. In caso di parità: scelta libera.

---

## Struttura del round

Ogni round si svolge in tre fasi, in ordine:

### Fase 1 — Piazzamento

I giocatori si alternano piazzando **1 lavoratore alla volta** su una carta del mercato, finché entrambi hanno piazzato tutti i propri lavoratori (3 turni ciascuno, per un totale di 6 azioni di piazzamento per round).

**Regole di piazzamento:**
- Un lavoratore occupa una carta del mercato. Metti il gettone sulla carta.
- Una carta può ospitare **1 solo lavoratore** (primo arrivato, primo servito).
- Non puoi piazzare su una carta già occupata da un lavoratore avversario.
- Puoi piazzare su una carta già occupata da un **tuo** lavoratore solo se il modificatore è ○ (vedi Modificatore).
- Il costo di piazzamento dipende dal valore della carta:
  - A–6: gratuito
  - 7–10: paga 1 Oro
  - J–K: paga 1 Oro + 1 Influenza

Se non puoi permetterti il costo, non puoi piazzare su quella carta.

### Fase 2 — Raccolta

Simultaneamente, entrambi i giocatori raccolgono gli effetti di **tutte** le carte su cui hanno lavoratori, nell'ordine che preferiscono.

**Ordine di raccolta consigliato:** prima le azioni di produzione (rosso), poi quelle di influenza (nero) — per massimizzare le risorse disponibili prima di usarle.

### Fase 3 — Rinnovo del mercato

1. Rimuovi tutti i lavoratori dal mercato (tornano ai rispettivi giocatori).
2. Rimuovi dal mercato le carte con valore J, Q, K (azioni gilda usate): vanno negli scarti.
3. Pesca dal mazzo riserva tante carte quante ne mancano per riportare il mercato a 9 carte. Se il mazzo riserva si esaurisce, mescola gli scarti per formare un nuovo mazzo.
4. Il primo giocatore del round successivo è chi ha meno Punti Vittoria. In caso di parità, il primo giocatore rimane lo stesso.

---

## Effetti del glifo primario

Il glifo primario definisce il tipo di effetto dell'azione. Si combina con il colore (produzione vs. influenza) per determinare cosa fa la carta.

| Primario | Effetto se rosso (produzione) | Effetto se nero (influenza) |
|---|---|---|
| • (punto) | Guadagna 1 Oro | Guadagna 1 Influenza |
| — (linea) | Guadagna 2 Oro | Blocca una carta adiacente (vedi Blocco) |
| + (croce) | Guadagna 1 Oro e 1 Influenza | Copia l'effetto di una carta adiacente occupata da un tuo lavoratore |
| × (diagonale) | Converti: scambia fino a 3 Oro in Influenza o viceversa (1:1) | Rimuovi 1 lavoratore avversario da una carta adiacente (torna al proprietario) |
| △ (triangolo) | Guadagna risorse pari al valore della carta diviso 3 (arrotonda per difetto), in Oro | Guadagna 1 PV immediato |
| ○ (cerchio) | Raddoppia l'effetto della prossima carta che raccogli questo round | Guarda le prime 3 carte del mazzo riserva; rimettile nell'ordine che preferisci |
| □ (quadrato) | Guadagna 1 Oro + 1 PV | Proteggi questa carta: non può essere soggetta a effetti avversari fino al prossimo round |

**Blocco (effetto —/nero):** una carta adiacente (ortogonalmente nella griglia 3×3) non può essere piazzata né raccolta da nessuno per il resto del round corrente. Segnala con un gettone neutro. Non si può bloccare una carta già occupata.

---

## Effetti del glifo modificatore

Il modificatore si applica **dopo** l'effetto del primario, ogni volta che la carta viene raccolta:

| Modificatore | Effetto aggiuntivo |
|---|---|
| • (punto) | +1 Oro alla raccolta, indipendentemente dal primario |
| — (linea) | Nessun effetto aggiuntivo |
| + (croce) | Puoi piazzare un secondo lavoratore su questa carta il prossimo round (costo normale) |
| × (diagonale) | L'avversario perde 1 risorsa a tua scelta (Oro o Influenza) quando raccogli questa carta |
| △ (triangolo) | Se questa è la terza carta che raccogli in questo round, guadagna 1 PV bonus |
| ○ (cerchio) | Puoi piazzare su questa carta anche se hai già un lavoratore qui (eccezione alla regola base) |
| □ (quadrato) | Questa carta non viene rimossa durante il Rinnovo, anche se è J/Q/K |

---

## Le azioni gilda (J, Q, K)

Le figure sono le azioni più potenti del mercato. Costano di più (1 Oro + 1 Influenza) ma offrono effetti che cambiano la struttura del round.

Dopo la Fase 2, le carte J/Q/K su cui è stato piazzato un lavoratore vengono rimosse — sono azioni uniche per round. Quelle non occupate rimangono disponibili nel round successivo.

**Effetti speciali delle figure (si combinano con primario e modificatore normalmente, ma aggiungono:**

- **J:** dopo la raccolta, pesca 1 carta dalla riserva e aggiungila al mercato in qualsiasi posizione libera.
- **Q:** dopo la raccolta, puoi spostare 1 tuo lavoratore già piazzato su un'altra carta libera del mercato (raccoglie anche il nuovo effetto).
- **K:** dopo la raccolta, guadagna 1 PV + 1 risorsa a scelta.

---

## I Jolly — commissioni straordinarie

I 2 Jolly rimangono nel mazzo riserva. Quando vengono pescati durante il Rinnovo, vengono posati nel mercato come carte speciali.

Una carta Jolly non ha seme, valore, primario né modificatore. È una **commissione straordinaria**.

**Effetto:** quando piazzi un lavoratore su un Jolly, dichiari prima del piazzamento quale effetto vuoi ottenere tra questi tre:
- Guadagna 3 Oro
- Guadagna 3 Influenza
- Guadagna 2 PV

Il Jolly viene rimosso dal mercato dopo la raccolta (come le figure), indipendentemente da chi lo ha usato. Non torna mai nel mazzo.

---

## Punti Vittoria

I PV si tracciano separatamente (usa un foglio o un dado extra). Si guadagnano:

- Effetto △/nero: 1 PV immediato
- Effetto □/rosso: 1 PV a raccolta
- Effetto K: 1 PV a raccolta
- Modificatore △: 1 PV bonus (condizionato)
- Jolly: 2 PV (se scegli quell'opzione)
- **Maggioranza di settore** (conteggio finale): vedi Fine partita

---

## Fine della partita

La partita termina alla fine del round in cui il **mazzo riserva si esaurisce per la seconda volta** (ovvero: il mazzo riserva viene ricostituito dagli scarti una volta; alla seconda esaurimento, il round in corso si completa e si passa al conteggio).

### Conteggio finale

**1. Maggioranze di settore**

Per ogni seme (♥ ♦ ♣ ♠), conta quante carte di quel seme ciascun giocatore ha raccolto durante la partita (tieni le carte raccolte in pila davanti a te durante il gioco — non quelle del mercato, quelle usate).

- Maggioranza assoluta (più carte del seme): +3 PV
- Parità: +1 PV ciascuno
- Nessuna carta del seme: 0 PV

**2. Risorse residue**

- Ogni 3 Oro rimasti: +1 PV
- Ogni 3 Influenza rimasti: +1 PV (arrotonda per difetto)

**3. Il giocatore con più PV totali vince.**

In caso di parità: vince chi ha più risorse totali (Oro + Influenza). Ulteriore parità: vince chi ha più carte raccolte in totale.

---

## Variante a 4 giocatori (due mazzi)

Si usano due mazzi DECK# mescolati. I giocatori formano 2 squadre da 2 (Gilda Rossa vs. Gilda Nera — assegna i colori alle squadre, non ai giocatori singoli).

Variazioni al setup e alle regole:
- Il mercato si espande a **16 carte** (griglia 4×4).
- Ogni giocatore ha ancora 3 lavoratori: 12 lavoratori totali per round su 16 slot.
- I compagni di squadra non possono piazzare sulla stessa carta.
- Durante il Piazzamento, l'ordine è: G1-A → G2-A → G1-B → G2-B (alternato per squadra).
- I PV si sommano per squadra. Le maggioranze di settore sono per squadra (conta le carte di entrambi i giocatori della squadra).
- La durata si allunga a 60–90 minuti.

---

## Note di design

**Perché la connettività non è attiva in GUILD?**
In un piazzamento lavoratori il tavolo è una plancia, non uno spazio attraversabile. Attivare la connettività avrebbe aggiunto complessità senza valore tattico diretto — il movimento non è il verbo di questo gioco. La connettività rimane stampata sulle carte come informazione latente, disponibile per varianti future.

**Perché rosso = produzione e nero = influenza?**
La distinzione produzione/influenza è la più consultata durante il Piazzamento — "questa carta mi dà risorse o mi permette di disturbare l'avversario?" Il colore risponde a questa domanda prima ancora che si legga il glifo.

**Perché le figure vengono rimosse dopo l'uso?**
Per creare scarsità strategica: le azioni più potenti non sono permanenti. Un giocatore che non le usa in un round le perde comunque (se l'avversario le usa) o le trova ancora disponibili (se nessuno le ha toccate). Questo genera tensione attorno alle J/Q/K ogni round senza regole di esclusività complesse.

**Perché i Jolly hanno effetti fissi a scelta?**
Perché in un piazzamento lavoratori l'incertezza deve essere gestibile. Un Jolly con effetto completamente libero sarebbe un "jolly rotto" — troppo potente o troppo dipendente dalla situazione corrente. Tre opzioni fisse bilanciano flessibilità e prevedibilità, e rendono il Jolly una decisione, non una rendita.