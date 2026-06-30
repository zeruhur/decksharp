---
title: "Guida al Design DECK#"
subtitle: "Complemento alla specifica DECK# v0.7.0"
author: Roberto Bisceglie
date: last-modified
version: 1.0
lang: it
cover-logo: ../assets/logo.svg
format:
  typst:
    toc: true
    toc-depth: 2
    number-sections: true
    fontsize: 11pt
    tbl-colwidths: auto
    template: ../../_extensions/typst-template.typ
    template-partials:
      - ../../_extensions/typst-show.typ
  odt:
    toc: true
  epub:
    toc: true
  docx:
    toc: true
  gfm:
    toc: false
---


version: 0.1.0 · status: draft

## 1. Natura di questo documento

Questa guida non prescrive come costruire un gioco su DECK#. Mostra cosa offre il sistema — le sue proprietà matematiche, le sue tensioni produttive, i suoi spazi di possibilità — perché il designer li possa riconoscere e sfruttare deliberatamente.

DECK# è un substrato. Il designer è l'autore. Questo documento è uno strumento di orientamento, non un vincolo.

## 2. La matematica del mazzo

Prima di assegnare qualsiasi significato, vale la pena capire la struttura che si eredita. Il mazzo DECK# annotato porta con sé proprietà che non sono ovvie ma che hanno implicazioni profonde sul design.

### 2.1 Il bilanciamento dei glifi

I sette glifi primari (—, •, +, ×, △, ○, □) compaiono ciascuno 7 o 8 volte sulle 52 carte regolari. Lo stesso vale per i modificatori.

Implicazione pratica: **qualunque semantica tu assegni a un glifo, quella semantica sarà distribuita uniformemente nel mazzo**. Se il cerchio ○ significa "carta evento", ci saranno 7–8 eventi nel mazzo, né troppo rari né dominanti. Il bilanciamento è una garanzia di sistema, non una responsabilità del designer.

Questo vale anche per le coppie primario+modificatore: esistono 32 coppie distinte su 52 carte. La varietà è alta; nessuna combinazione domina.

### 2.2 La struttura della connettività

I bordi aperti per carta si distribuiscono in tre fasce precise:

| Bordi aperti | Numero di carte |
|||
| 1 | 16 |
| 2 | 16 |
| 3 | 16 |
| 4 (tutti) | 4 |

Una simmetria quasi musicale: tre fasce da 16, più quattro carte con connettività massima. Se stai costruendo un gioco con elementi spaziali, questa distribuzione è la tua palette topologica: un terzo del mazzo crea vicoli, un terzo corridoi, un terzo incroci, quattro carte nodi.

### 2.3 La texture del valore ordinale

La connettività non è distribuita in modo perfettamente uniforme rispetto al valore della carta — e questo non è un difetto, è una texture che i giochi possono sfruttare.

| Fascia di valore | Bordi aperti medi |
|||
| A, J (basso) | 1.25 – 1.50 |
| 2, 5, 6 (medio-basso) | 1.50 |
| 3, 7, 10 (medio-alto) | 2.25 – 2.50 |
| 8, K (alto) | 3.00 |
| Q | 2.75 |

Se mappi il valore ordinale a "rango" o "potere", le carte alte tendono a essere anche più connesse spazialmente. Questo può essere una risonanza interessante — o una tensione da spezzare deliberatamente. Entrambe sono scelte di design valide, ma devono essere scelte consapevoli.

### 2.4 Cosa non è garantito

La connettività è ortogonale a seme e colore per costruzione deliberata — nessun seme domina un'altra dimensione dell'annotazione. Il valore ordinale, invece, presenta la texture descritta sopra. Tenerla a mente evita sorprese durante il playtesting.

## 3. I tre assi ereditati

Il mazzo standard porta tre assi informativi che DECK# non ridefinisce. Come questi assi vengono mappati a concetti di gioco è la prima grande decisione del designer — e probabilmente la più strutturante.

### 3.1 Il valore ordinale

Tredici gradi da A a K. Questo asse è il più ricco in termini di granularità.

Possibili mappature:

- **Potenza o intensità**: più alto = più forte. La mappatura più intuitiva, con la texture di connettività come corollario spaziale.
- **Fase o stadio**: A = inizio, K = fine. Utile per giochi narrativi o con archi temporali.
- **Tipo discreto**: A–6 = un tipo, 7–K = un altro. Riduce la granularità a vantaggio della semplicità.
- **Risorse quantificate**: il valore come numero puro. Efficace per giochi economici.

Le figure (J, Q, K) formano una sottoclasse naturale. Trattarle come categoria speciale aggiunge un livello di gerarchia senza costi di componenti.

### 3.2 Il colore

Rosso / Nero. Asse binario, massimamente visibile.

Possibili mappature:

- **Fazione o polarità**: la mappatura più immediata. Due forze, due fazioni, due stati.
- **Modalità**: azione/reazione, attacco/difesa, giorno/notte.
- **Costo e beneficio**: rosso = rischio, nero = sicurezza — o viceversa.

Il colore è l'asse con la maggiore saliency visiva. Assegnargli un significato di bassa importanza meccanica è uno spreco. Assegnargli troppa importanza lo rende un discriminatore di gioco prima ancora che il giocatore possa leggere le annotazioni.

### 3.3 Il seme

Quattro semi, due rossi e due neri. Il seme porta una struttura interna: non è solo un asse a quattro valori, ma un asse a quattro valori con due coppie cromatiche.

Possibili mappature:

- **Quattro categorie indipendenti**: classi, biomi, fazioni, tipi di risorsa.
- **Due coppie con distinzione interna**: cuori vs quadri come varianti di "rosso", fiori vs picche come varianti di "nero". Utile per sistemi con gerarchia a due livelli.
- **Ignora il seme, usa solo il colore**: legittimo se le quattro categorie creano troppa complessità per il gioco target.

### 3.4 La coerenza degli assi

Una domanda chiave da porsi prima del playtesting: **gli assi ereditati parlano tra loro in modo coerente con il tono del gioco?**

Se il valore mappa a "livello di minaccia" e il colore mappa a "alleato/nemico", il Re rosso sarà una minaccia massima da parte di un nemico. Il Due nero sarà una minaccia minima da parte di un alleato. Questa combinazione ha senso nel tuo gioco? Produce situazioni interessanti o confuse?

Non esiste una risposta unica. Esiste solo la necessità di averla posta.

## 4. Il vocabolario grafico

I sette glifi di DECK# sono aniconici: non raffigurano nulla. Questo è una caratteristica, non una limitazione. L'aniconicità garantisce che la semantica assegnata dal gioco non entri in conflitto con associazioni culturali pregresse — o che possa farlo deliberatamente.

### 4.1 Assegnare semantica ai glifi

Alcune considerazioni pratiche:

**Sfrutta le semantiche naturali senza esserne prigioniero.** La specifica suggerisce associazioni intuitive (△ = direzione, × = negazione, ○ = ciclo). Queste associazioni riducono il carico cognitivo per il giocatore nuovo. Usarle è spesso la scelta più efficiente; ignorarle è possibile ma richiede un sistema di riferimento compensativo (glossario, leggenda).

**Primario e modificatore sono due layer semantici distinti.** Non trattarli come due "proprietà" equivalenti. Una mappatura efficace tende ad avere il primario come categoria o tipo (cosa è questa carta) e il modificatore come qualità o stato (come si comporta). L'inversione è possibile ma rara.

**Considera il carico cognitivo totale.** Sette glifi per strato, due strati, più i tre assi ereditati: il giocatore può trovarsi a decodificare fino a cinque dimensioni per carta. La semplicità di lettura va testata sul campo, non assunta.

### 4.2 Conflitti visivi da evitare

La specifica elenca le forme riservate ai semi (cuore, rombo, trifoglio, picca). Il punto non è solo estetico: un glifo che assomiglia a un seme crea ambiguità di lettura in condizioni di gioco reali — carte usate, luce non ideale, giocatori non familiari col sistema.

Il quadrato □ e il cerchio ○ sono i glifi più sicuri. Il triangolo △ è sicuro in posizione angolare e piccolo. Linea — e croce + sono letti automaticamente come separatori o connettori — un'associazione da sfruttare o da contrastare con istruzione esplicita.

## 5. Il sistema spaziale

Il sistema spaziale di DECK# è opzionale a livello di profilo (Base vs Esteso), ma la sua struttura merita attenzione anche nei giochi di carte puri — perché definisce come le carte interagiscono fisicamente sul tavolo.

### 5.1 La connettività come grafo

Accostando carte sul tavolo, i bordi marcati come "muro" chiudono il passaggio; i bordi aperti creano connessione. Il risultato è un grafo topologico emergente: non è la griglia di un gioco di ruolo standard, non è una mappa fissa, è uno spazio che si costruisce carta per carta durante la partita.

Implicazioni di design:

- Il gioco può lasciare che il giocatore scelga l'orientamento delle carte (polo nord = variabile), creando un sistema generativo. Ogni sessione produce una mappa diversa.
- Il gioco può fissare l'orientamento, usando la connettività come proprietà intrinseca della carta — un corridoio è un corridoio, indipendentemente da come è posato.
- Il gioco può mescolare i due approcci: orientamento libero in fase di setup, fisso in fase di gioco.

### 5.2 La transizione hand→tile

Quando una carta passa dalla mano al tavolo, cambia ontologia: da informazione nascosta a componente fisico. Questa transizione deve essere specificata dal designer in tre punti:

**1. Rivelazione:** la carta viene posata coperta o scoperta? Una carta coperta è uno spazio di incertezza; una scoperta è informazione condivisa. Entrambe hanno senso in contesti diversi.

**2. Orientamento:** il polo nord è scelto dal giocatore o è fisso? La scelta dell'orientamento è un atto strategico se le annotazioni spaziali (connettività, direzione del triangolo) hanno peso meccanico.

**3. Attivazione:** le annotazioni spaziali diventano attive immediatamente o in un momento successivo? Una carta posata coperta con connettività che si attiva solo alla rivelazione crea una meccanica di sorpresa. Una carta con effetto ritardato crea pianificazione.

Queste tre decisioni non sono indipendenti. Definirle insieme produce il comportamento tattico del posizionamento.

## 6. I Jolly

I Jolly sono le due carte strutturalmente fuori sistema: nessun asse ereditato, nessuna annotazione DECK# tranne il polo nord sul recto. Sul dorso ricevono i marcatori di quadrante — identici a tutte le altre carte — per non essere riconoscibili a carte coperte. Sono variabili non istanziate.

La scelta di usarli — e come — dice qualcosa di fondamentale sull'architettura del gioco.

### 6.1 Wildcard meccanica

Il Jolly come carta universale: può essere giocata come qualsiasi carta del mazzo, o come qualsiasi valore/seme/glifo. Semplice da implementare, alto impatto strategico. Rischio: banalizzare le decisioni se troppo potente, o essere ignorata se troppo debole.

### 6.2 Carta evento

Il Jolly come interruzione del flusso normale: quando pescato o posato, innesca un effetto globale. Non è parte del mazzo "giocabile" in senso ordinario — è un marcatore di discontinuità. Utile per giochi con archi narrativi o fasi di gioco distinte.

### 6.3 Tracciatore di stato globale

Il Jolly come componente fisso sul tavolo, non in mano. Viene usato per tenere traccia di uno stato condiviso — un contatore, una fase, una condizione attiva. In questo caso non viene mai "giocato": è sempre visibile, sempre presente. Funziona in giochi con variabili di stato persistenti tra turni.

### 6.4 Jolly di categoria

I due Jolly come due entità distinte (non intercambiabili). Ognuno rappresenta qualcosa di irriducibile al sistema ordinale — un personaggio unico, una risorsa non generabile, un evento singolare. Richiede che il gioco dia loro un'identità esplicita.

**La domanda da porsi:** il tuo gioco ha bisogno di elementi che non si possano ottenere variando valore, seme, colore e glifi? Se sì, i Jolly sono lo strumento. Se no, usarli è opzionale — e ometterli è una scelta di design, non una mancanza.

## 7. Pattern di design

Questi non sono template. Sono configurazioni ricorrenti che emergono da come i profili Base ed Esteso vengono utilizzati in pratica. Riconoscerli aiuta a orientarsi nella fase di ideazione.

### 7.1 Gioco di carte puro

**Profilo Base.** Le carte restano in mano o vengono posate come azione (non come griglia). Il sistema spaziale è inattivo o marginale. Il nucleo del gioco è la gestione della mano e la risoluzione delle carte giocate.

DECK# aggiunge: due livelli semantici per carta (primario + modificatore), più i tre assi ereditati. È possibile costruire giochi con meccaniche di drafting, combo, o narrativa emergente senza mai posare una carta sul tavolo in modalità tile.

**Tensione produttiva:** il bilanciamento dei glifi garantisce equità di distribuzione. Un gioco di carte che sfrutta questo avrà meno problemi di "mazzo rotto" rispetto a un sistema custom.

### 7.2 Griglia tattica e dungeon crawler

**Profilo Esteso.** Le carte vengono posate sul tavolo in modalità tile, costruendo lo spazio di gioco. La connettività dei bordi definisce la topologia. Segnalini e dadi gestiscono entità e risoluzione.

DECK# aggiunge: uno spazio generativo che cambia ogni sessione, con proprietà topologiche predeterminate (connettività) ma disposizione variabile (orientamento). L'asimmetria della distribuzione della connettività (vedi sezione 2.3) può generare zone naturalmente più aperte o più chiuse.

**Tensione produttiva:** la transizione hand→tile è il momento meccanico più ricco. Come si rivela lo spazio — chi decide l'orientamento, quando si attivano i bordi — definisce il ritmo tattico del gioco.

### 7.3 Gioco solitario e cooperativo

**Profilo Base o Esteso.** Un solo giocatore (o gruppo cooperativo) contro il sistema. DECK# non include meccaniche oracolari per default — questa è una scelta deliberata. Il designer deve costruire un motore oracolare che usi il mazzo come fonte di risposta.

Approcci possibili:

- Pesca una carta e leggi il primario come risposta (sì/no/forse, basato su opposizioni binarie dei glifi).
- Combina valore + glifo primario per generare un evento da una tabella.
- Usa la connettività della carta pescata per determinare la direzione narrativa.

DECK# offre sufficiente spazio semantico multidimensionale per costruire sistemi oracolari ricchi senza richiedere componenti aggiuntivi.

### 7.4 Multiplayer asimmetrico

**Profilo Base o Esteso.** Giocatori con ruoli, risorse o capacità diverse. DECK# supporta l'asimmetria attraverso la mappatura degli assi: il colore (rosso/nero) è l'asse più naturale per differenziare fazioni. Il seme può aggiungere un secondo livello di differenziazione intra-fazione.

**Attenzione:** in un gioco asimmetrico, la distribuzione bilanciata dei glifi è una risorsa equa per tutti i giocatori. Se un giocatore ha accesso solo a un sottoinsieme del mazzo (per seme o colore), la distribuzione dei glifi in quel sottoinsieme non è più garantita uguale. Vale la pena verificare le distribuzioni parziali durante la progettazione.

## 8. Checklist del designer

Ogni gioco costruito su DECK# richiede che il designer specifichi esplicitamente i seguenti elementi. Questa checklist estende la sezione 11 della specifica con domande orientate al design.

### Assi ereditati

- [ ] Come viene mappato il valore ordinale (A–K)? È una scala continua o discretizzata per fasce?
- [ ] Come viene usato il colore (rosso/nero)? La mappatura è meccanicamente significativa?
- [ ] Come vengono usati i semi? Come quattro categorie, due coppie, o viene ignorata la distinzione di seme?
- [ ] Le tre mappature sono coerenti tra loro? Producono combinazioni interessanti o problematiche?

### Vocabolario grafico

- [ ] Quale semantica viene assegnata ai glifi primari? È documentata in modo chiaro per il giocatore?
- [ ] Quale semantica viene assegnata ai glifi modificatori? È distinta e complementare al primario?
- [ ] I glifi usati sfruttano o contrastano le semantiche naturali (sezione 4 della specifica)?

### Sistema spaziale (se applicabile)

- [ ] Il profilo è Base o Esteso?
- [ ] Se Esteso: come viene gestita la transizione hand→tile (rivelazione, orientamento, attivazione)?
- [ ] La distribuzione della connettività (1/2/3/4 bordi aperti) è congruente con il design dello spazio di gioco?

### Jolly

- [ ] I Jolly vengono usati? Se sì, quanti (zero, uno, entrambi)?
- [ ] Quale ruolo hanno: wildcard, evento, tracciatore di stato, entità distinta?
- [ ] Il loro ruolo è irriducibile a quello di qualsiasi altra carta del sistema?

### Giocabilità

- [ ] Quante dimensioni informative deve decodificare il giocatore per leggere una carta? Questo carico è sostenibile?
- [ ] La distribuzione bilanciata dei glifi è un asset per il gioco o crea un problema da gestire?
- [ ] Se il gioco usa un sottoinsieme del mazzo (per seme, colore o valore), la distribuzione dei glifi in quel sottoinsieme è stata verificata?

---

DECK#

© 2026 Roberto Bisceglie

This work is licensed under Creative Commons Attribution-ShareAlike 4.0 International. To view a copy of this license, visit https://creativecommons.org/licenses/by-sa/4.0/
