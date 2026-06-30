---
title: "DECK# Annotation Guide"
subtitle: "How to physically prepare your DECK# deck"
author: Roberto Bisceglie
date: last-modified
version: 1.0
lang: en
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

---

## What you need

- A standard French-suited playing card deck (52 cards + 2 Jokers)
- A fine-tip black permanent marker
- A fine-tip red permanent marker
- The annotation matrix (section 13 of the specification, or the `decksharp_matrix.csv` file)

Estimated time: 15–20 minutes.

---

## Before you begin

The DECK# deck is annotated **once**, before any play session. Annotations are permanent. There is no in-game annotation: variable states are managed with physical tokens (dice, tokens, coins).

Each card receives four types of annotation, in distinct zones:

| Annotation | Zone | Tool |
|---|---|---|
| Quadrant markers | Back | Black marker |
| Connectivity markers | Physical edges (front face) | Black marker |
| Orientation dot (north pole) | SE corner (front face) | Black marker |
| Primary glyph + modifier | S/N and NE/SW zones (front face) | Black or red (see below) |

**Color rule:** glyph color is always contrasting relative to the card's suit.
- Red cards (♥ ♦) → glyphs in **black**
- Black cards (♣ ♠) → glyphs in **red**

Glyph color is not a choice: it is automatically derived from suit.

---

## Preparation: sorting the deck

Separate the deck into three groups:

1. **Red cards** (♥ ♦) — 26 cards
2. **Black cards** (♣ ♠) — 26 cards
3. **Jokers** — 2 cards, set aside

Work first on **red cards**: they require only the black marker for all annotation. Then proceed to **black cards**: they require a tool switch only in the final phase (glyphs in red). Handle **Jokers** last — they have minimal, separate annotation.

---

## Phase 1 — Quadrant markers (back)

**Tool:** black marker.

With cards oriented face-down, draw quadrant markers on all 54 cards (red + black + Jokers).

Quadrant markers are identical on all cards and indicate the center and sides of the card to the player when it is placed face-down on the table. Choose one of the two variants and keep it consistent throughout the deck:

**Minimal variant** — four short segments starting from the midpoint of each edge toward the center, without crossing it:

```
      |
  —     —
      |
```

**Extended variant** — full cross from edge to edge:

```
      |
  ————+————
      |
```

Allow the ink to dry before flipping the cards.

---

## Phase 2 — Connectivity markers (edges)

**Tool:** black marker.

Consult the annotation matrix. For each card, the **Connectivity** column indicates which edges are **open** (connected). Edges not listed receive a **wall marker**: a thick line drawn along the external white margin of the card (~3–4 mm), on the front face.

**Example:** if the matrix shows `N+W`, the North and West edges are open — leave them unmarked. The South and East edges receive the wall marker.

Allow a few seconds of drying time between cards before stacking them.

---

## Phase 3 — Orientation dot (north pole)

**Tool:** black marker.

Draw a small dot `•` in the far lower right corner of each card — the **SE** zone of the front face. This dot breaks the vertical symmetry of standard cards and indicates the north pole: the side with the pre-printed index at top left (NW).

The dot goes on all 52 standard cards and both Jokers.

---

## Phase 4 — Primary glyphs and modifiers

**Tool:** black marker for red cards (♥ ♦) · red marker for black cards (♣ ♠).

Consult the annotation matrix. For each card, annotate:

- **Primary glyph** in the **S** zone (lower middle edge, inside the card) and its rotated mirror in the **N** zone (upper middle edge).
- **Modifier glyph** in the **NE** corner (upper right corner) and its rotated mirror in the **SW** zone (lower left corner).

The mirror positions (N and SW) make the card readable in a fan, regardless of orientation in hand.

The DECK# vocabulary comprises seven glyphs:

| Glyph | How to draw it |
|---|---|
| `•` dot | a single dot |
| `—` line | a horizontal line |
| `+` cross | two perpendicular lines |
| `×` diagonal | two diagonal lines |
| `△` triangle | three strokes |
| `○` circle | a closed ring |
| `□` square | four strokes |

---

## Exception: Jokers

The two Jokers receive the **quadrant marker** on the back (Phase 1, identical to the 52 standard cards) and the **orientation dot** in the SE zone (Phase 3). No connectivity markers, no primary glyph, no modifier.

They are uninstantiated variables: each game decides whether and how to use them.

---

## Summary chart per card

| Element | Position | 52 standard cards | 2 Jokers |
|---|---|---|---|
| Quadrant markers | Back | ✓ | ✓ |
| Connectivity markers | Front face edges | ✓ (from matrix) | — |
| North pole dot | SE corner front face | ✓ | ✓ |
| Primary glyph | S + N zones front face | ✓ (from matrix) | — |
| Modifier glyph | NE + SW zones front face | ✓ (from matrix) | — |

---

## How to read the annotation matrix

The matrix lists all 54 cards with three pieces of information:

- **Connectivity:** open edges, in N/S/E/W notation separated by `+`. Edges not listed receive the wall marker.
- **Primary:** the glyph to draw in the S zone (and its mirror in N).
- **Modifier:** the glyph to draw in the NE zone (and its mirror in SW).

Glyph color is not in the matrix because it is always derived from suit: black for ♥/♦, red for ♣/♠.

---

DECK#

© 2026 Roberto Bisceglie

This work is licensed under Creative Commons Attribution-ShareAlike 4.0 International. To view a copy of this license, visit https://creativecommons.org/licenses/by-sa/4.0/
