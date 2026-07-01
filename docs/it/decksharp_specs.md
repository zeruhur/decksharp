---
title: "Specifiche DECK#"
subtitle: "Sistema di annotazione stratificata per mazzo di carte standard"
author: Roberto Bisceglie
date: last-modified
version: 1.0
lang: it
cover-logo: ../assets/logo.svg
format:
  html: default
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

version: 0.7.0 · status: draft

## 1. Natura e scope del sistema

DECK# è un protocollo di annotazione stratificata su un mazzo di carte standard (52 + 2 Jolly).

Il suo scopo è permettere a chiunque di costruire e giocare giochi da tavolo complessi usando materiali reperibili ovunque e a costo minimo: un mazzo di carte francesi e due pennarelli permanenti. Nessun componente proprietario, nessun materiale dedicato, nessuna dipendenza da editori o produttori specifici.

DECK# è ispirato al **Piecepack** — sistema di componenti aperti per giochi da tavolo ideato da James Kyle nel 2000 — di cui condivide la filosofia: un substrato standardizzato e aperto su cui la comunità costruisce giochi liberamente. Come il Piecepack, DECK# è open source.

DECK# **non è** un mazzo universale. Non prescrive giochi, meccaniche, semantiche di gioco, né generi. È un sistema aperto: definisce un vocabolario grafico condiviso e una struttura fisica di annotazione. I giochi costruiti su DECK# usano questo vocabolario e ne assegnano i significati.

Il mazzo standard porta con sé tre assi informativi preesistenti che DECK# riconosce come **attivi e intoccabili**. L'annotazione aggiunge informazioni che la carta non possiede; non sostituisce quelle che già ha.

DECK# è agnostico alla lingua. L'intero vocabolario grafico è composto da glifi geometrici e cifre arabiche. Nessun testo è necessario o ammesso nelle annotazioni.

### Fuori scope

I seguenti elementi sono esplicitamente fuori scope e delegati ai singoli giochi:

- Il significato dei semi
- Il significato del colore rosso/nero degli assi ereditati
- Il significato dei valori numerici
- Il significato di ogni glifo (il vocabolario è condiviso, la semantica no)
- La mappatura valore → funzione meccanica (es. A-6 = spazio, 7-10 = risorsa)
- Regole di movimento e topologia della griglia
- Meccaniche di risoluzione, combattimento, interazione
- Meccaniche di economia e risorse
- Condizioni di attivazione delle wildcard
- Condizioni di vittoria e obiettivi di scenario
- Meccaniche oracolari per gioco solitario o cooperativo
- Quante carte vengono usate
- Come vengono distribuite le carte
- Il numero di giocatori

## 2. Principi di design

- **Accessibilità materiale:** l'unico requisito fisico è un mazzo di carte francesi standard e due pennarelli permanenti (nero e rosso). Materiali disponibili ovunque, senza componenti proprietari o dedicati.
- **Additivo, non distruttivo:** le annotazioni aggiungono informazioni strutturali senza sovrascrivere il substrato ereditato.
- **Agnostico alla lingua:** nessun testo o lettera. Solo glifi geometrici e cifre arabiche.
- **Vincolo cromatico:** solo pennarello nero e rosso.
- **Uso duale:** le carte sono valide sia come informazione nascosta in mano sia come componenti fisici sul tavolo.
- **Dorso riservato ai marcatori di quadrante:** il dorso delle 52 carte regolari riceve esclusivamente i marcatori di quadrante — identici su tutte le carte, quindi privi di informazione differenziale. Nessun'altra annotazione sul dorso. L'uniformità preserva l'anonimità delle carte coperte.
- **Artefatto completo:** il mazzo DECK# è annotato integralmente prima di qualsiasi sessione di gioco. L'annotazione strutturale è permanente e fissa. Gli stati variabili si tracciano con token fisici, non con annotazioni.

## 3. Il substrato ereditato

### 3.1 I tre assi

| Asse | Valori | Natura |
|---|---|---|
| Colore | Rosso / Nero | Binario |
| Polarità del seme | Cuori vs Quadri (rosso) — Fiori vs Picche (nero) | Binario interno al colore |
| Valore | A(1) — 2 — … — 10 — J — Q — K | Scala ordinale, 13 gradi |

Questi assi sono immutabili. Ogni gioco decide come mapparli a concetti di gioco; non può ridefinirli fisicamente sulla carta.

### 3.2 Note sul substrato

- Le figure (J, Q, K) formano una sottoclasse del valore ordinale. Alcuni giochi potranno trattarle come categoria separata.
- Il Jolly non appartiene a nessuno dei tre assi. È strutturalmente fuori sistema per definizione. Vedi sezione 7.
- Il dorso della carta è una superficie esclusa dall'annotazione. Vedi Principio 5 (sezione 2).

## 4. Il vocabolario grafico

### 4.1 Principi

- Tutti i glifi sono producibili con pochi tratti da chiunque, senza abilità grafica.
- L'unica risorsa cromatica aggiuntiva è il pennarello rosso. Il nero è il colore di default.
- Nessun testo. Nessun glifo che rimandi a un alfabeto specifico.
- I glifi non devono confondersi visivamente con i semi esistenti.

### 4.2 Glifi primari

| Glifo | Tratti | Semantiche naturali (non prescritte) |
|---|---|---|
| -  punto | 1 | presenza, attivazione, marcatore |
| — linea | 1 | bordo, separazione, soglia |
| + croce | 2 | connessione, incrocio, unione |
| × diagonale | 2 | negazione, blocco, esclusione |
| △ triangolo | 3 | direzione, gerarchia, gradiente |
| ○ cerchio | 1 curvo | ciclo, contenimento, stato neutro |
| □ quadrato | 4 | zona, regione, spazio chiuso |

Sette glifi. La colonna "semantiche naturali" suggerisce associazioni intuitive; non le prescrive.

### 4.3 Il colore dei glifi — regola contrastante

I glifi del primario e del modificatore sono tracciati nel colore **contrastante** rispetto al seme della carta:

- Carte rosse (♥ ♦): glifi in **nero**
- Carte nere (♣ ♠): glifi in **rosso**

Questa regola garantisce separazione visiva netta tra annotazione e substrato su tutte le carte. Il colore del glifo è interamente derivabile dal seme — non aggiunge informazione differenziale ma massimizza la leggibilità.

### 4.4 Glifi numerici

Le cifre 0–9 (arabiche) possono essere usate nelle zone annotabili come quantità, livelli, contatori. Si combinano con il colore seguendo la stessa logica dei glifi primari.

### 4.5 Conflitti visivi da evitare

| Seme | Forma riservata |
|---|---|
| Cuori | Forma a cuore |
| Quadri | Rombo pieno o vuoto |
| Fiori | Trifoglio / forma a tre lobi |
| Picche | Picca / cuore invertito con gambo |

Il quadrato □ e il cerchio ○ non confliggono con nessun seme. Il triangolo △ è sicuro se tracciato piccolo e in posizione angolare.

## 5. Le zone annotabili

```
[NW] ----[N]---- [NE]
  |               |
 [W]  [centro]  [E]
  |               |
[SW] ----[S]---- [SE]
```

| Zona | Posizione | Annotazione DECK# |
|---|---|---|
| S | Bordo medio inferiore (interno) | Glifo primario |
| N | Bordo medio superiore (interno) | Speculare del primario — hand mode |
| NE | Angolo superiore destro | Glifo modificatore |
| SW | Angolo inferiore sinistro | Speculare del modificatore — hand mode |
| SE | Angolo inferiore destro | Punto orientamento (polo nord) |
| NW | Angolo superiore sinistro | Riservato — indice pre-stampato |
| Centro / E / W | — | Non occupati dall'annotazione DECK# |

**Bordi fisici:** i marcatori di connettività occupano il margine bianco esterno della carta (~3–4 mm) — fisicamente separati dalle zone interne.

**Regola del posizionamento simmetrico:** ogni glifo compare in due posizioni speculari — zona primaria e zona speculare. Garantisce leggibilità a ventaglio indipendentemente dall'orientamento della carta in mano.

**Nota su NW:** angolo parzialmente occupato dall'indice pre-stampato. Nessuna annotazione DECK# in questa zona.

## 6. Il sistema spaziale

### 6.1 Il problema della simmetria

Le carte standard hanno simmetria verticale: si leggono uguale capovolte. Non appena un gioco introduce elementi spaziali, questa simmetria deve essere rotta esplicitamente.

### 6.2 La convenzione del polo nord

Il polo nord di una carta è il lato con l'indice in posizione canonica (NW in alto a sinistra). Pratica consigliata per sessioni con elementi spaziali: tracciare un punto piccolo nell'angolo SE prima dell'inizio — angolo libero dalla stampa, asimmetrico rispetto all'indice NW.

### 6.3 Marcatori di bordo

| Marcatura | Significato strutturale |
|---|---|
| Linea spessa a tutto bordo | Muro: passaggio chiuso |
| Bordo non marcato | Aperto: connesso, attraversabile |
| Punto -  a metà bordo | Soglia: stato intermedio, definito dal gioco |

Accostando le carte sul tavolo, i bordi a contatto si leggono come interfaccia tra due spazi.

### 6.4 Marcatori di quadrante

I marcatori di quadrante si trovano sul **dorso** delle 52 carte regolari. Sono identici su tutte le carte — non rivelano alcuna informazione differenziale quando la carta è coperta.

Sono disponibili due varianti; la scelta è lasciata a chi annota il mazzo:

**Variante minima** — quattro segmenti corti dal punto medio di ciascun bordo verso l'interno, senza attraversare il centro:

```
      |
  —     —
      |
```

**Variante estesa** — croce completa da bordo a bordo (`+` del vocabolario DECK#, applicato al dorso con funzione strutturale fissa):

```
      |
  ————+————
      |
```

Entrambe le varianti sono tracciate in nero. I Jolly ricevono i marcatori di quadrante sul dorso — identici a quelli delle 52 carte regolari — ma non ricevono alcuna annotazione sul recto oltre al punto SE.

### 6.5 Direzione interna

Il triangolo △ in una zona angolare indica direzione. L'orientamento dell'apice rispetto al polo nord definisce il vettore.

## 7. I Jolly

I Jolly ricevono il **punto SE** (polo nord) sul recto e i **marcatori di quadrante** sul dorso. Nessun altro elemento strutturale: nessun marcatore di connettività, nessun glifo primario, nessun modificatore.

Sono **variabili non istanziate**: nessuna semantica pre-assegnata dalla specifica. Il gioco decide tutto. Un gioco può usare zero, uno o entrambi i Jolly.

Usi possibili (non prescritti): wildcard meccanica, carta evento, tracciatore di stato globale, Jolly di categoria.

## 8. Profili di utilizzo

### Profilo Base

Gioco di carte puro, gestione della mano, narrativa, scenari solitario.

**Componenti:** 1 mazzo annotato (52 + 2) · 1 pennarello nero permanente fine · 1 pennarello rosso permanente fine.
Tempo di annotazione stimato: 15–20 minuti.

### Profilo Esteso

Gioco tattico su griglia, dungeon crawler, skirmish, wargame.

**Componenti aggiuntivi:** 6 dadi d6 · 12 segnalini in 4 gruppi distinti (3 per gruppo; sostituibili con monete, cubetti, qualsiasi oggetto distinguibile).

Uso dadi: 2d6 per risoluzione, fino a 4d6 come contatori su carta. Uso segnalini: posizionati sulle carte per rappresentare entità senza coprire le annotazioni.

## 9. Modalità d'uso delle carte

### 9.1 Tile mode

Carta sul tavolo, visibile a tutti, posizione fissa. Elementi spaziali attivi.

### 9.2 Hand mode

Carta in mano, nascosta. Elementi spaziali generalmente inattivi. Annotazioni devono seguire la regola del posizionamento simmetrico (sezione 5).

### 9.3 Transizione hand → tile

Il gioco deve specificare:

- Se la carta viene posata coperta o scoperta
- Se l'orientamento (polo nord) è scelto dal giocatore o fisso
- Se le annotazioni spaziali diventano attive immediatamente o in un momento successivo

### 9.4 Annotazione

Il mazzo DECK# viene annotato integralmente una volta, seguendo la matrice di annotazione (sezione 13), e usato in più sessioni senza modifiche. L'annotazione strutturale è permanente.

Non è prevista annotazione durante il gioco per il layer strutturale. Gli stati variabili della partita si tracciano esclusivamente con token fisici rimovibili (dadi, segnalini, monete).

## 10. Gerarchia fisica

Le 52 carte regolari hanno annotazioni su entrambe le facce. I Jolly hanno annotazioni sul dorso e solo il punto SE sul recto.

**Recto (52 carte regolari):**

1. Substrato ereditato (stampa originale): sempre visibile, mai coperto intenzionalmente
2. Annotazione strutturale DECK#: connettività sui bordi fisici, glifo primario in zona S/N, modificatore in zona NE/SW, punto polo nord in SE
3. Token fisici: oggetti posizionati sulla carta, rimuovibili

**Dorso (tutte le 54 carte):**

- Marcatori di quadrante (variante minima o estesa) — identici su tutte le carte

L'annotazione strutturale è fissa e completa. Nessuna zona del recto prevede più di un glifo DECK# per volta.

## 11. Responsabilità del designer

Ogni gioco costruito su DECK# deve specificare:

1. Come mappa i tre assi ereditati (valore, colore, seme) a concetti di gioco
2. Quale semantica assegna ai glifi del vocabolario DECK# (primario e modificatore)
3. Come interpreta il sistema spaziale: orientamento, polo nord, connettività
4. Come interpreta i marcatori di quadrante (presenti su tutte le carte)
5. Se usa i Jolly e con quale ruolo
6. Quale profilo è richiesto (Base o Esteso)
7. Quale modalità d'uso è prevista e le regole di transizione hand → tile

## 12. Licenza

DECK# è rilasciato sotto **Creative Commons Attribution 4.0 International (CC BY 4.0)**.

Chiunque può usare, modificare e distribuire la specifica e i giochi costruiti su di essa, anche a fini commerciali, a condizione di attribuire la fonte originale. I giochi costruiti su DECK# non sono tenuti a rilasciare i propri regolamenti con la stessa licenza.

© Roberto Bisceglie — [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

## 13. La matrice di annotazione

La matrice definisce le annotazioni strutturali fisse di tutte le 54 carte. Ogni carta riceve:

- **Connettività:** bordi aperti (gli altri ricevono marcatore di muro). Notazione: N/S/E/W separati da `+`.
- **Primario:** glifo in zona S (e speculare in zona N per hand mode).
- **Modificatore:** glifo in angolo NE (e speculare in angolo SW per hand mode).

Tutte le 52 carte regolari ricevono inoltre: punto SE (polo nord) e marcatori di quadrante.  
I Jolly ricevono il punto SE sul recto e i marcatori di quadrante sul dorso.

La distribuzione è un artefatto di design authored, ortogonale a valore/seme/colore per costruzione deliberata. Il colore dei glifi non è incluso come colonna — è interamente derivato dal seme secondo la regola contrastante (sezione 4.3): glifi neri su ♥/♦, glifi rossi su ♣/♠.

| Valore | Seme | Connettività | Primario | Modificatore |
|---|---|---|---|---|
| A | ♥ | N+W | — | • |
| 2 | ♥ | S | □ | + |
| 3 | ♥ | S+W | × | △ |
| 4 | ♥ | W | △ | + |
| 5 | ♥ | N+S+E | □ | △ |
| 6 | ♥ | N+S | — | • |
| 7 | ♥ | E+W | + | — |
| 8 | ♥ | E+W | • | — |
| 9 | ♥ | S+W | × | ○ |
| 10 | ♥ | N+S+W | • | + |
| J | ♥ | N | + | □ |
| Q | ♥ | W | • | △ |
| K | ♥ | N+E | △ | • |
| A | ♦ | E | + | ○ |
| 2 | ♦ | N+E | × | × |
| 3 | ♦ | N+S+E+W | ○ | + |
| 4 | ♦ | N+S+W | ○ | □ |
| 5 | ♦ | N | □ | • |
| 6 | ♦ | E+W | × | × |
| 7 | ♦ | S | + | — |
| 8 | ♦ | N+S+E+W | — | × |
| 9 | ♦ | S+E | □ | — |
| 10 | ♦ | N+S | — | × |
| J | ♦ | N+S | △ | • |
| Q | ♦ | N+S+E+W | ○ | — |
| K | ♦ | S+E+W | • | □ |
| A | ♣ | S | △ | • |
| 2 | ♣ | E+W | □ | • |
| 3 | ♣ | N+S+E | • | △ |
| 4 | ♣ | S+E | — | × |
| 5 | ♣ | N | □ | + |
| 6 | ♣ | E | + | ○ |
| 7 | ♣ | N+E+W | + | ○ |
| 8 | ♣ | N+E+W | □ | + |
| 9 | ♣ | S+E+W | ○ | □ |
| 10 | ♣ | S+E+W | — | ○ |
| J | ♣ | N+W | • | □ |
| Q | ♣ | N+E+W | △ | — |
| K | ♣ | N+S+E | × | + |
| A | ♠ | N | — | — |
| 2 | ♠ | W | × | + |
| 3 | ♠ | E | ○ | □ |
| 4 | ♠ | N+S+W | + | × |
| 5 | ♠ | S | × | □ |
| 6 | ♠ | E | • | △ |
| 7 | ♠ | N+S+E | ○ | × |
| 8 | ♠ | N+E+W | • | △ |
| 9 | ♠ | S+E+W | △ | ○ |
| 10 | ♠ | N+S | △ | — |
| J | ♠ | W | + | • |
| Q | ♠ | N+S+W | ○ | ○ |
| K | ♠ | N+S+E+W | — | △ |
| Jolly | — | — | — | — |
| Jolly | — | — | — | — |

---

DECK#

© 2026 Roberto Bisceglie

This work is licensed under Creative Commons Attribution-ShareAlike 4.0 International. To view a copy of this license, visit https://creativecommons.org/licenses/by-sa/4.0/
