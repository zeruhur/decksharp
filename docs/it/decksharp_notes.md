---
title: "Note di Design DECK#"
subtitle: "Traccia delle decisioni di progettazione"
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

version: 0.7.0 · documento interno

***

## DC-01 — Nome del sistema: DECK #

**Decisione:** il sistema si chiama DECK#.
**Alternativa considerata:** Deckpack.
**Motivazione:** DECK# (dal greco: lingua, vocabolario) riflette la natura del sistema — un vocabolario condiviso per comunicare informazioni meccaniche. È agnostico alla lingua pur essendo un nome non neutro, il che è appropriato: il nome è un'etichetta meta, non un componente del sistema. Deckpack resta valido per eventuali edizioni fisiche o derivati commerciali.

***

## DC-02 — Ampiezza del mazzo base: 52 + 2 Jolly

**Decisione:** 54 carte totali.
**Motivazione:** i Jolly sono strutturalmente distinti già nel mazzo standard — l'unica carta priva di seme e valore. Escluderli sarebbe sprecare una risorsa di design. Le carte pubblicitarie presenti in alcuni mazzi non sono standardizzate e non entrano nella specifica.

***

## DC-03 — Marcatura permanente

**Decisione:** annotazioni con pennarello indelebile.
**Alternative considerate:** cancellabile per tutti i layer; sistema misto.
**Motivazione:** la marcatura permanente trasforma ogni mazzo in un artefatto unico. Gli stati variabili vengono tracciati con token fisici già rimovibili per natura. Il sistema misto è disponibile come pratica opzionale per i singoli giochi ma non viene prescritto.

***

## DC-04 — Sistema aperto: nessuna mappatura valore → funzione

**Decisione:** DECK# non assegna funzioni meccaniche per valore.
**Alternativa scartata:** cardpack-spec v0.2.0 aveva definito Space (A-6) / Resource (7-10) / Actor (J-Q-K) come partizione fissa.
**Motivazione:** quella partizione è la struttura di un gioco tattico specifico, non un vocabolario aperto. Blocca qualsiasi gioco che voglia usare un Asso come personaggio o un Re come territorio. Un sistema aperto non prescrive cosa rappresenta ogni carta — lo fa ogni gioco costruito sopra.

***

## DC-05 — Sette glifi primari (vocabolario chiuso)

**Decisione:** esattamente 7 glifi: punto, linea, croce, diagonale, triangolo, cerchio, quadrato.
**Motivazione:** coprono le forme geometriche primitive producibili con 1-4 tratti. Sufficientemente distinti visivamente tra loro e dai semi. Il vocabolario è chiuso per garantire interoperabilità — un glifo non presente non esiste in DECK#. L'asterisco di cardpack-spec v0.2.0 è stato escluso perché visivamente ambiguo e motivato da un ruolo semantico (Jolly) che la specifica non deve pre-assegnare.

***

## DC-06 — Colore dei glifi: regola contrastante

**Decisione originale (v0.1–v0.6):** il colore del pennarello è un layer semantico indipendente, ortogonale al glifo; convenzione non prescritta.
**Decisione aggiornata (v0.7):** il colore dei glifi segue la regola contrastante fissa — glifi neri su carte rosse (♥/♦), glifi rossi su carte nere (♣/♠). Vedi DC-22.
**Motivazione del cambiamento:** un asse semantico "disponibile ma non prescritto" non entra mai nell'annotazione canonica. La regola contrastante è semplice, memorabile e garantisce alta leggibilità su tutte le carte senza richiedere una colonna colore nella matrice.

***

## DC-07 — Dorso: eccezione per marcatori di quadrante

**Decisione originale (v0.1–v0.5):** dorso escluso dall'annotazione.
**Decisione aggiornata (v0.6):** il dorso delle 52 carte regolari riceve esclusivamente i marcatori di quadrante. Due varianti ammesse: minima (quattro segmenti corti ai punti medi) o estesa (croce completa `+`). La scelta è lasciata a chi annota. I Jolly non ricevono marcatori di quadrante nemmeno sul dorso.
**Motivazione dell'eccezione:** i marcatori di quadrante sono identici su tutte le 52 carte regolari — non rivelano nessuna informazione differenziale. La motivazione originale (preservare l'anonimità per fog-of-war) non si applica a marcatori uniformi. Il beneficio è eliminare la coesistenza con il glifo primario in zona S (DA-01 / DC-21, ora superate).

***

## DC-08 — Convenzione del polo nord

**Decisione:** polo nord = lato con indice NW canonico. Punto in SE come marcatore di orientamento.
**Problema:** le carte hanno simmetria verticale per motivi ergonomici. Con elementi spaziali, va rotta esplicitamente.
**Motivazione:** il punto in SE è la soluzione meno invasiva — non copre nulla, è asimmetrico, richiede un tratto. Una freccia fissa avrebbe introdotto semantica spaziale anche per giochi senza orientamento.

***

## DC-09 — Posizionamento simmetrico in hand mode

**Decisione:** annotazioni in due posizioni speculari — glifo primario in zona S con speculare in N; modificatore in angolo NE con speculare in SW. Vedi DC-18 per le zone specifiche.
**Fonte:** cardpack-spec v0.2.0 (zone aggiornate in DC-18).
**Motivazione:** convenzione ergonomica standard dei mazzi — gli indici sono già duplicati e ruotati per la stessa ragione. Garantisce leggibilità a ventaglio senza regole aggiuntive.

***

## DC-10 — Marcatori di quadrante

**Decisione:** presenti sul **dorso** delle 52 carte regolari (migrazione dal recto in v0.6, vedi DC-07 rev.). Due varianti: minima (quattro segmenti corti) o estesa (croce `+`). Assenti sui Jolly.
**Fonte:** cardpack-spec v0.2.0 (universalità stabilita in DC-17; migrazione al dorso in DC-07 rev. v0.6).
**Motivazione:** sul recto i segmenti corti erano necessari per evitare di coprire i pip. Sul dorso la variante estesa (croce completa) diventa praticabile senza interferenze.

**Revisione v0.7.1 (2026-05-13):** estesi anche ai Jolly sul dorso. Vedi DC-11 rev. per la motivazione.

***

## DC-11 — Jolly come variabili non istanziate

**Decisione:** i Jolly ricevono solo il punto SE (polo nord). Nessun glifo primario, nessun modificatore, nessun marcatore di connettività, nessun marcatore di quadrante.
**Alternativa scartata:** asterisco fisso in cardpack-spec v0.2.0.
**Motivazione:** l'asterisco trasforma i Jolly in un ruolo funzionale specifico prima che un gioco li usi. Un sistema aperto lascia i Jolly come superfici neutre. La loro assenza dagli assi ereditati è già sufficiente a distinguerli.

**Revisione v0.7.1 (2026-05-13):** i Jolly ricevono i marcatori di quadrante sul dorso. La motivazione originale (neutralità del Jolly come superficie bianca) si applica al recto, non al dorso: i marcatori di quadrante sono uniformi su tutte le carte e non trasmettono alcuna informazione differenziale. La loro assenza sul dorso dei Jolly li rendeva riconoscibili a carte coperte, compromettendo il fog-of-war. Il principio di neutralità rimane integro: il Jolly è ancora privo di semantica pre-assegnata sul recto.

***

## DC-12 — Profili Base ed Esteso

**Decisione:** due profili con requisiti crescenti.
**Fonte:** cardpack-spec v0.2.0 (assente in DECK# v0.1).
**Motivazione:** il sistema deve essere accessibile con il minimo materiale ma non fingere che tutti i giochi abbiano gli stessi requisiti. La distinzione è una dichiarazione di scope, non una gerarchia.

***

## DC-13 — Sezione "Responsabilità del designer"

**Decisione:** lista esplicita di ciò che ogni gioco costruito su DECK# deve specificare.
**Motivazione:** senza questa sezione un designer non sa dove inizia il suo lavoro. La lista delimita l'interfaccia tra specifica e gioco.

***

## DC-14 — Licenza CC BY 4.0

**Decisione:** Creative Commons Attribution 4.0 International.
**Alternative considerate:** CC0, CC BY-SA, licenza proprietaria con permesso d'uso.
**Motivazione:** CC BY 4.0 bilancia apertura e attribuzione. Permette uso commerciale, non impone copyleft sui derivati, richiede solo citazione della fonte. CC0 avrebbe rinunciato a qualsiasi tracciabilità dell'ecosistema. CC BY-SA avrebbe creato frizioni per giochi commerciali.

***

## DC-15 — Layer unico strutturale

**Decisione:** i glifi sono strutturali per definizione. Non esiste un layer semantico separato aggiunto dal gioco — il designer interpreta i glifi strutturali, non aggiunge un layer proprio.
**Alternativa scartata:** modello a due layer (strutturale DECK# + semantico per gioco).
**Motivazione:** la distinzione layer strutturale / layer semantico è concettuale, non fisica. Sul mazzo c'è un solo strato di annotazione. La semantica è un'operazione di lettura, non di scrittura.

***

## DC-16 — Tre dimensioni strutturali per carta

**Decisione:** ogni carta è definita da tre dimensioni: Connettività (pattern di bordi aperti tra 15 configurazioni), Primario (glifo in zona S), Modificatore (glifo in angolo NE). Gerarchia posizionale, non semantica: Primario + Modificatore identici (es. ×/×) sono combinazioni legittime.
**Motivazione:** tre dimensioni indipendenti creano uno spazio combinatorio (15 × 7 × 7 = 735 configurazioni teoriche) molto più ricco dei 52 slot necessari, garantendo libertà di design nella distribuzione.

***

## DC-17 — Marcatori di quadrante universali

**Decisione:** i marcatori di quadrante sono presenti su tutte le 52 carte regolari. Assenti sui Jolly.
**Alternativa scartata:** presenza variabile come dimensione della matrice.
**Motivazione:** la capacità spaziale uniforme semplifica l'annotazione e sposta la gestione della capacità al gioco, che può ignorarla, usarla parzialmente o sfruttarla integralmente.

***

## DC-18 — Zone: Primario in S, Modificatore in NE

**Decisione:** glifo primario in zona S (interno, bordo medio inferiore) con speculare in N; modificatore in angolo NE con speculare in SW. Centro non occupato da annotazioni DECK#.
**Alternativa scartata:** primario al centro (bloccato dai pip sulle carte numerali).
**Motivazione:** zona S è visibile quando le carte sono tenute a ventaglio; è pulita e separata dai pip per tutte le carte. NE è il secondo angolo più visibile. Il centro resta leggibile per i pip e disponibile come spazio visivo neutro.

***

## DC-19 — Matrice di annotazione come artefatto di design

**Decisione:** la distribuzione di connettività e glifi sulle 52 carte è un artefatto authored, ortogonale a valore/seme/colore per costruzione deliberata. Non esiste formula algoritmica che colleghi proprietà del substrato all'annotazione strutturale.
**Motivazione:** l'ortogonalità per formula richiederebbe di usare valore/seme come indice, re-encodandoli implicitamente. L'ortogonalità per design è più robusta: nessuna correlazione sistematica, varietà topologica controllata.

***

## DC-20 — Annotazione pre-gioco come standard assoluto

**Decisione:** il mazzo DECK# viene annotato integralmente prima di qualsiasi sessione. Nessuna annotazione in gioco per il layer strutturale.
**Motivazione:** coerente con il modello del mazzo come artefatto fisso. Rimuove una fonte di ambiguità dalla sezione "Responsabilità del designer" — non è una scelta del gioco, è un vincolo del sistema.

***

## DC-22 — Colore dei glifi: regola contrastante

**Decisione:** glifi neri su carte rosse (♥/♦); glifi rossi su carte nere (♣/♠). Regola fissa, nessuna colonna colore nella matrice.
**Alternative scartate:** (1) colore come asse semantico indipendente nella matrice — richiede distribuzione progettata e aggiunge complessità; (2) tutti i glifi in nero — perde leggibilità su carte nere.
**Motivazione:** il colore contrastante è interamente derivabile dal seme (zero informazione differenziale nuova) ma massimizza la separazione visiva tra annotazione e substrato. La semplicità della regola è il valore principale: chiunque annoti il mazzo può ricavarla senza consultare la matrice.

***

## DC-21 — Convivenza marcatore di quadrante e glifo primario in zona S

**SUPERATA in v0.6 da DC-07 rev.** I marcatori di quadrante migrano sul dorso: la coesistenza con il glifo primario in zona S non si pone più. La sezione 5.1 della spec (diagramma di posizionamento) è stata rimossa.

***

## Decisioni aperte

**DA-01 — CHIUSA** (DC-16, DC-18): la coesistenza di più glifi nella stessa zona non si pone — ogni zona ha al massimo un glifo DECK#.

**DA-02 — Notazione per subset di mazzo:** sistema standard per documentare quale sottoinsieme viene usato (es. `DECK#/♠A-6`).

**DA-03 — CHIUSA:** compatibilità con mazzi non standard fuori scope per definizione. Il prerequisito di DECK# è un mazzo francese/poker standard (52 + 2 Jolly). Mazzi spagnoli, tedeschi, tarocchi non soddisfano il substrato ereditato della sezione 3.

**DA-04 — CHIUSA (rigettata):** i marcatori di quadrante sul dorso sarebbero utili in tile mode con carta coperta, ma il pattern del dorso varia da mazzo a mazzo in modo imprevedibile — su dorsi con motivi fitti i marcatori sarebbero illeggibili o nascosti. DC-07 (dorso non annotabile) rimane valido senza eccezioni.

---

DECK#

© 2026 Roberto Bisceglie

This work is licensed under Creative Commons Attribution-ShareAlike 4.0 International. To view a copy of this license, visit https://creativecommons.org/licenses/by-sa/4.0/
