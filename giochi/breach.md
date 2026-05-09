# BREACH

## Uno skirmish tattico per DECK#

**Sistema:** DECK# (Profilo Esteso)  
**Giocatori:** 2  
**Durata:** 30–60 minuti  
**Componenti aggiuntivi:** 6d6 · 6 pedine per giocatore (3 colore A + 3 colore B) · gettoni (monete vanno benissimo)

---

## Il concetto

Due squadre si contendono il controllo di un territorio che si rivela carta per carta. Lo spazio non è noto in anticipo: emerge durante il gioco. Ogni carta posata è una zona conquistata, un varco aperto, un muro scoperto.

Vinci eliminando tutte le unità avversarie o controllando 3 zone obiettivo simultaneamente.

---

## Mappatura degli assi DECK#

| Asse | Valore in BREACH |
|---|---|
| **Valore (A–K)** | Potenza della zona: A–6 = zona bassa (1–2 pt danno), 7–10 = zona media (3 pt), J–K = zona alta (4 pt) |
| **Colore** | Tipo di zona: **Rosso** = zona aperta (terreno scoperto, bonus attacco) · **Nero** = zona coperta (copertura, bonus difesa) |
| **Seme** | Effetto speciale della zona (vedi sotto) |
| **Primario** | Tipo di azione disponibile sulla carta |
| **Modificatore** | Condizione o stato della zona |

### Effetti del seme

| Seme | Effetto |
|---|---|
| ♥ | Zona di recupero: unità su questa carta recupera 1 danno a fine turno |
| ♦ | Zona instabile: dopo ogni combattimento su questa carta, il giocatore attivo pesca 1 carta e la aggiunge al territorio adiacente |
| ♣ | Zona di rifornimento: unità su questa carta può usare un'azione aggiuntiva una volta per round |
| ♠ | Zona di controllo: vale doppio per la condizione di vittoria (conta come 2 zone obiettivo) |

### Azioni del glifo primario

| Primario | Azione disponibile sulla carta |
|---|---|
| • (punto) | **Agguato:** attacca un'unità su carta adiacente con +1 dado |
| — (linea) | **Presidio:** l'unità non può essere spostata da questa carta fino al prossimo turno avversario |
| + (croce) | **Coordinazione:** attiva un'unità alleata adiacente come azione bonus |
| × (diagonale) | **Blocco:** chiude temporaneamente un bordo aperto a scelta fino al tuo prossimo turno |
| △ (triangolo) | **Avanzata:** l'unità può muoversi di 2 carte invece di 1 questo turno |
| ○ (cerchio) | **Rotazione:** sposta questa carta di 90° (cambia la connettività attiva) |
| □ (quadrato) | **Fortifica:** posiziona un gettone su questa carta; vale come muro aggiuntivo su un bordo a scelta |

### Condizioni del glifo modificatore

| Modificatore | Condizione della zona |
|---|---|
| • (punto) | Zona attiva: l'azione del primario costa 0 azioni aggiuntive |
| — (linea) | Zona neutra: nessun modificatore |
| + (croce) | Zona amplificata: l'azione del primario si applica a tutte le unità sulla carta |
| × (diagonale) | Zona compromessa: chi entra in questa carta perde 1 punto ferita |
| △ (triangolo) | Zona escalation: ogni round che un'unità rimane qui, il suo valore di attacco aumenta di 1 |
| ○ (cerchio) | Zona ciclica: a fine round, questa carta viene girata (polo nord ruota di 180°) |
| □ (quadrato) | Zona bunker: le unità qui ricevono +2 alla difesa |

---

## Le unità

Ogni giocatore ha **3 unità**, rappresentate da pedine di colore diverso. Ogni unità ha:

- **Punti Ferita (PF):** tracciati con un d6 posizionato accanto alla pedina, valore iniziale **6**
- **Valore di Attacco (ATK):** determinato dalla zona in cui si trova (valore della carta, vedi mappatura)
- **Valore di Difesa (DEF):** base 2, modificato dalla zona (colore e modificatore)

Le unità non hanno statistiche proprie fisse: sono ciò che la zona le rende. Spostarsi è una scelta tattica, non solo geografica.

---

## Setup

**1. Il territorio di partenza**

Pescare 6 carte dal mazzo mescolato. Posarle scoperte, orientate col polo nord verso l'alto (indice in NW), in una griglia 3×2 al centro del tavolo. Questo è il territorio neutro iniziale.

**2. Connettività**

Le 6 carte si accostano rispettando i bordi fisici. I bordi marcati come muro sono chiusi; i bordi aperti creano passaggi. Alcune carte potrebbero non connettersi a nessun'altra: rimangono zone isolate, raggiungibili solo con l'azione △ (Avanzata).

**3. Dispiegamento**

Ogni giocatore sceglie uno dei due lati corti della griglia. Posiziona le 3 unità su qualsiasi carta del proprio lato. Non si può partire sulla stessa carta di un'unità avversaria.

**4. I Jolly — le zone obiettivo**

I 2 Jolly vengono posati scoperti, uno su ciascun lato lungo della griglia (fuori dal territorio, come indicatori). Quando una carta viene rivelata e posata adiacente a un Jolly, quella carta diventa una **zona obiettivo** per tutta la partita. Se durante la partita non si rivelano carte adiacenti ai Jolly, i Jolly stessi sono zone obiettivo.

---

## Struttura del turno

I giocatori si alternano. Ogni turno ha 3 fasi in ordine:

### Fase 1 — Espansione

Il giocatore attivo pesca 1 carta dal mazzo e la posa adiacente a qualsiasi carta già sul territorio, scoperta, orientamento a scelta (polo nord in qualsiasi direzione). La carta deve essere adiacente a una carta esistente tramite almeno un bordo aperto compatibile — bordo aperto della carta nuova a contatto con bordo aperto di una carta esistente.

Se non esiste una posizione valida (tutti i bordi aperti della nuova carta sarebbero a contatto con muri), il giocatore sceglie liberamente l'orientamento.

**L'espansione è obbligatoria.** Se il mazzo è esaurito, si ricrea mescolando gli scarti tranne le carte già sul tavolo.

### Fase 2 — Movimento

Ogni unità può muoversi di **1 carta** attraverso un bordo aperto. Il movimento è opzionale per ogni unità. Non si può attraversare un muro o un bordo chiuso da ×.

- Se il glifo primario della carta di partenza è △, l'unità può muoversi di 2 carte (azione Avanzata).
- Non si può entrare in una carta occupata da 2 unità avversarie.

### Fase 3 — Azione

Ogni unità può compiere **1 azione** tra:

**a) Attacco** — se un'unità avversaria è sulla stessa carta o su una carta adiacente tramite bordo aperto.

Risoluzione:
1. Attaccante lancia tanti d6 quanti indicati dal valore della carta su cui si trova (A–6 = 1d6, 7–10 = 2d6, J–K = 3d6). Se il glifo primario è • (Agguato), aggiunge 1d6.
2. Difensore lancia tanti d6 quanti indicati dal suo valore di DEF (base 2, +2 se □ modificatore, +1 se zona nera).
3. Confronta il risultato più alto di ciascun gruppo. Chi ha il valore più alto infligge danni pari alla differenza all'avversario. In caso di pareggio, nessun danno.
4. Abbassa il d6 del difensore del valore di danni subiti. A 0 PF l'unità è eliminata e rimossa dal tavolo.

**b) Azione di zona** — usa l'azione del glifo primario della carta su cui si trova l'unità. Ogni azione di zona può essere usata una sola volta per carta per round (segnala con un gettone).

**c) Passa** — nessuna azione.

---

## Fine del turno e fine del round

Dopo che entrambi i giocatori hanno eseguito il loro turno, il round termina.

- Rimuovi i gettoni dalle azioni di zona usate.
- Applica gli effetti di fine round (♥ recupero, ○ rotazione carta).
- Verifica la condizione di vittoria.

---

## Vittoria

Vinci se, **a fine di qualsiasi round**, si verifica una delle seguenti condizioni:

1. **Eliminazione:** tutte le unità avversarie sono a 0 PF.
2. **Controllo:** hai almeno 1 unità su ciascuna delle 3 zone obiettivo simultaneamente.

Se entrambe le condizioni si verificano nello stesso round per entrambi i giocatori, vince chi ha eliminato più unità. In caso di ulteriore parità: patta.

---

## I Jolly in BREACH

I Jolly non entrano mai nel mazzo attivo e non vengono mai pescati. Funzionano esclusivamente come **marcatori fissi di zona obiettivo** — sono sempre visibili sul tavolo per tutta la partita. La loro assenza dal sistema ordinale li rende irriducibili a qualsiasi altra carta: nessuna altra carta può essere "più obiettivo" di un Jolly.

---

## Variante: Asimmetria

Un giocatore controlla 2 unità con PF 8 ciascuna. L'altro controlla 3 unità con PF 5 ciascuna. La condizione di vittoria per controllo rimane 3 zone obiettivo per entrambi; per eliminazione basta portare a 0 tutte le unità avversarie. Modifica il ritmo del gioco significativamente: testare.

---

## Note di design

**Perché il valore mappa alla potenza della zona e non dell'unità?**  
In BREACH le unità non hanno statistiche proprie: la loro forza dipende da dove si trovano. Questo valorizza il movimento come decisione tattica primaria e sfrutta la texture naturale della distribuzione della connettività — le carte con valore alto tendono ad avere più bordi aperti, quindi le zone più potenti tendono anche ad essere più esposte.

**Perché il colore mappa al tipo di zona (aperta/coperta)?**  
Il colore è l'asse più visibile a colpo d'occhio. In un gioco tattico la distinzione attacco/difesa è la più frequentemente consultata: assegnarla all'asse più leggibile riduce il carico cognitivo durante il gioco.

**Perché i Jolly sono zone obiettivo?**  
Perché non appartengono al sistema ordinale: non hanno valore, colore, seme, né glifi. Non possono essere "più forti" o "più deboli" di nessuna carta del mazzo. Questa neutralità assoluta li rende perfetti come riferimenti fissi — la posta in gioco che non cambia mentre il territorio intorno cambia.