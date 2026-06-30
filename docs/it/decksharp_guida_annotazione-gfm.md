# Guida all’Annotazione DECK#
Roberto Bisceglie
2026-06-30

version: 0.1.0 · status: draft

------------------------------------------------------------------------

## Cosa serve

- Un mazzo di carte francesi standard (52 carte + 2 Jolly)
- Un pennarello permanente nero a punta fine
- Un pennarello permanente rosso a punta fine
- La matrice di annotazione (sezione 13 della specifica, o il file
  `decksharp_matrix.csv`)

Tempo stimato: 15–20 minuti.

------------------------------------------------------------------------

## Prima di iniziare

Il mazzo DECK# si annota **una volta sola**, prima di qualsiasi partita.
Le annotazioni sono permanenti. Non ci sono annotazioni da fare durante
il gioco: gli stati variabili si gestiscono con token fisici (dadi,
segnalini, monete).

Ogni carta riceve quattro tipi di annotazione, in zone distinte:

| Annotazione | Zona | Strumento |
|----|----|----|
| Marcatori di quadrante | Dorso | Pennarello nero |
| Marcatori di connettività | Bordi fisici (recto) | Pennarello nero |
| Punto di orientamento (polo nord) | Angolo SE (recto) | Pennarello nero |
| Glifo primario + modificatore | Zone S/N e NE/SW (recto) | Nero o rosso (vedi sotto) |

**Regola cromatica:** il colore del glifo è sempre contrastante rispetto
al seme della carta. - Carte rosse (♥ ♦) → glifi in **nero** - Carte
nere (♣ ♠) → glifi in **rosso**

Il colore del glifo non è una scelta: si ricava automaticamente dal
seme.

------------------------------------------------------------------------

## Preparazione: divisione del mazzo

Separa il mazzo in tre gruppi:

1.  **Carte rosse** (♥ ♦) — 26 carte
2.  **Carte nere** (♣ ♠) — 26 carte
3.  **Jolly** — 2 carte, messe da parte

Lavora prima sulle **carte rosse**: richiedono solo il pennarello nero
per l’intera annotazione. Procedi poi con le **carte nere**: richiedono
il cambio di strumento solo nell’ultima fase (glifi in rosso). Affronta
i **Jolly** alla fine — hanno un’annotazione minima e separata.

------------------------------------------------------------------------

## Fase 1 — Marcatori di quadrante (dorso)

**Strumento:** pennarello nero.

Con le carte orientate sul dorso, traccia i marcatori di quadrante su
tutte le 54 carte (rosse + nere + Jolly).

I marcatori di quadrante sono identici su tutte le carte e indicano al
giocatore il centro e i lati della carta quando è posata coperta sul
tavolo. Scegli una delle due varianti e mantienila per tutto il mazzo:

**Variante minima** — quattro segmenti corti che partono dal punto medio
di ciascun bordo verso il centro, senza attraversarlo:

          |
      —     —
          |

**Variante estesa** — croce completa da bordo a bordo:

          |
      ————+————
          |

Lascia asciugare l’inchiostro prima di girare le carte.

------------------------------------------------------------------------

## Fase 2 — Marcatori di connettività (bordi)

**Strumento:** pennarello nero.

Consulta la matrice di annotazione. Per ogni carta, la colonna
**Connettività** indica quali bordi sono **aperti** (connessi). I bordi
non elencati ricevono un **marcatore di muro**: una linea spessa
tracciata lungo il margine bianco esterno della carta (~3–4 mm), sul
recto.

**Esempio:** se la matrice indica `N+W`, i bordi Nord e Ovest sono
aperti — non si toccano. I bordi Sud ed Est ricevono il marcatore di
muro.

Lascia qualche secondo di asciugatura tra una carta e l’altra prima di
sovrapporle.

------------------------------------------------------------------------

## Fase 3 — Punto di orientamento (polo nord)

**Strumento:** pennarello nero.

Traccia un piccolo punto `•` nell’angolo estremo in basso a destra di
ogni carta — la zona **SE** del recto. Questo punto rompe la simmetria
verticale delle carte standard e indica il polo nord: il lato con
l’indice pre-stampato in alto a sinistra (NW).

Il punto va su tutte le 52 carte regolari e sui 2 Jolly.

------------------------------------------------------------------------

## Fase 4 — Glifi primari e modificatori

**Strumento:** pennarello nero per le carte rosse (♥ ♦) · pennarello
rosso per le carte nere (♣ ♠).

Consulta la matrice di annotazione. Per ogni carta, annota:

- **Glifo primario** nella zona **S** (bordo medio inferiore, interno
  alla carta) e il suo speculare capovolto in zona **N** (bordo medio
  superiore).
- **Glifo modificatore** nell’angolo **NE** (angolo superiore destro) e
  il suo speculare capovolto in zona **SW** (angolo inferiore sinistro).

Le posizioni speculari (N e SW) servono a rendere la carta leggibile a
ventaglio, indipendentemente dall’orientamento in mano.

Il vocabolario DECK# comprende sette glifi:

| Glifo         | Come si traccia          |
|---------------|--------------------------|
| `•` punto     | un punto                 |
| `—` linea     | una linea orizzontale    |
| `+` croce     | due linee perpendicolari |
| `×` diagonale | due linee diagonali      |
| `△` triangolo | tre tratti               |
| `○` cerchio   | un anello chiuso         |
| `□` quadrato  | quattro tratti           |

------------------------------------------------------------------------

## Eccezione: i Jolly

I due Jolly ricevono il **marcatore di quadrante** sul dorso (Fase 1,
identico alle 52 carte regolari) e il **punto di orientamento** in zona
SE (Fase 3). Nessun marcatore di connettività, nessun glifo primario,
nessun modificatore.

Sono variabili non istanziate: ogni gioco decide se e come usarli.

------------------------------------------------------------------------

## Schema riepilogativo per carta

| Elemento                  | Posizione          | 52 carte regolari | 2 Jolly |
|---------------------------|--------------------|-------------------|---------|
| Marcatori di quadrante    | Dorso              | ✓                 | ✓       |
| Marcatori di connettività | Bordi recto        | ✓ (da matrice)    | —       |
| Punto polo nord           | Angolo SE recto    | ✓                 | ✓       |
| Glifo primario            | Zone S + N recto   | ✓ (da matrice)    | —       |
| Glifo modificatore        | Zone NE + SW recto | ✓ (da matrice)    | —       |

------------------------------------------------------------------------

## Come leggere la matrice di annotazione

La matrice elenca tutte le 54 carte con tre informazioni:

- **Connettività:** i bordi aperti, in notazione N/S/E/W separati da
  `+`. I bordi non elencati ricevono il marcatore di muro.
- **Primario:** il glifo da tracciare in zona S (e N speculare).
- **Modificatore:** il glifo da tracciare in zona NE (e SW speculare).

Il colore dei glifi non è nella matrice perché si ricava sempre dal
seme: nero per ♥/♦, rosso per ♣/♠.

------------------------------------------------------------------------

DECK#

© 2026 Roberto Bisceglie

This work is licensed under Creative Commons Attribution-ShareAlike 4.0
International. To view a copy of this license, visit
https://creativecommons.org/licenses/by-sa/4.0/
