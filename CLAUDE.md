# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**DECK#** (pronounced "Deck Sharp") is an open-source standardized annotation system for regular playing cards (52 + 2 Jokers). It is a layered protocol enabling complex tabletop games using only a standard deck and two permanent markers (black and red). Version: 0.7.0 (Draft). License: CC BY 4.0.

This is a **design and documentation project** — there are no build systems, compilers, or test suites. All content is in Markdown, CSV, and NanDeck format.

## Repository Structure

| Path | Purpose |
|------|---------|
| `decksharp_specs.md` | Primary system specification (canonical reference) |
| `decksharp_guida_design.md` | Designer's guide with mathematical analysis and checklist |
| `decksharp_notes.md` | Design decision log (some entries superseded) |
| `decksharp_matrix.csv` | Annotation lookup for all 54 cards (connectivity + primary glyph + modifier) |
| `decksharp_nandeck.txt` | NanDeck script for automated card generation |
| `decksharp_nandeck.pdf` | Generated card deck ready for print-on-demand |
| `giochi/` | 5 example games built on the DECK# Extended profile |
| `prim-mod.csv` | Glyph combination reference table |

## Core System Concepts

Understanding these is essential before editing any spec or game file.

**Three inherited axes** (from the standard deck, not annotated):
- Value: A, 2–10, J, Q, K
- Color: Red / Black (determines marker color for glyphs)
- Suit: ♥ ♦ ♣ ♠

**Vocabulary** (fixed — do not expand without strong justification):
- 7 primary glyphs: `—`, `•`, `+`, `×`, `△`, `○`, `□`
- Glyphs can carry a modifier (a second red-ink overlay)
- Glyph color is derived from card suit (Red suits → red marker; Black suits → black marker)

**Spatial system** — 8 annotation zones on the card face (NW/N/NE/E/SE/S/SW/W) plus edges for connectivity markers.

**Two usage profiles:**
- **Base** — card-based games (hand-held cards)
- **Extended** — grid-based tactical games (cards laid as tiles)

**Jokers** are intentionally uninstantiated (blank slate); each game assigns them freely.

**Connectivity distribution** is mathematically fixed: 16 cards with 1 open border, 16 with 2, 16 with 3, 4 with all 4 open. Do not alter this distribution.

## Design Invariants

These constraints are fundamental to the system — changes require explicit versioning:

- Only 2 markers are ever used (black + red); glyph color is never a free choice
- The glyph vocabulary is exactly 7 primary symbols (not 6, not 8)
- The card back (dorso) may only carry identical quadrant markers — no unique information
- DECK# defines vocabulary and structure only; individual games define semantics
- Annotations are additive — they never replace or override the substrate (suit/color/value)

## Example Games (`giochi/`)

All 5 games use the Extended profile and are self-contained Markdown documents:

| File | Genre | Players |
|------|-------|---------|
| `breach.md` | Tactical skirmish | 2 |
| `delve.md` | Dungeon crawler | 1 |
| `guild.md` | Economic / narrative | 3–4 |
| `lore.md` | Narrative / cooperative | 2–3 |
| `veil.md` | Deduction / social | 3–6 |

Each game independently maps: value → mechanic, color → faction/mode, suit → category, glyphs → actions.

## Editing Guidelines

- **`decksharp_specs.md`** is the authoritative source. When there is a conflict between spec and game files, the spec wins unless a deliberate game-level exception is documented.
- **`decksharp_notes.md`** records design rationale. When making design changes, add a new dated entry explaining the decision and marking any superseded ones.
- **`decksharp_matrix.csv`** must stay in sync with the spec's annotation assignments — update both together.
- **`decksharp_nandeck.txt`** uses NanDeck scripting syntax; changes here affect the printable PDF output.
- Game files in `giochi/` are independent works — they may use DECK# vocabulary freely but must not redefine the core glyph set or connectivity rules.

## NanDeck

The `decksharp_nandeck.txt` file is a script for [NanDeck](https://www.nandeck.com/), a Windows application for card generation. To regenerate the PDF, open the script in NanDeck and run the build. There is no CLI equivalent.
