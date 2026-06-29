# DECK#

## Layered annotation system for standard playing card deck

version: 0.7.0 · status: draft

## 1. Nature and scope of the system

DECK# is a layered annotation protocol for a standard playing card deck (52 + 2 Jokers).

Its purpose is to allow anyone to build and play complex board games using materials available anywhere, at minimal cost: a standard French-suited deck and two permanent markers. No proprietary components, no dedicated materials, no dependency on specific publishers or manufacturers.

DECK# is inspired by **Piecepack** — an open component system for board games designed by James Kyle in 2000 — sharing its philosophy: a standardized, open substrate on which the community freely builds games. Like Piecepack, DECK# is open source.

DECK# **is not** a universal deck. It does not prescribe games, mechanics, gameplay semantics, or genres. It is an open system: it defines a shared graphic vocabulary and a physical annotation structure. Games built on DECK# use this vocabulary and assign their own meanings to it.

The standard deck carries three pre-existing information axes that DECK# recognizes as **active and untouchable**. Annotation adds information the card does not already have; it does not replace what is already there.

DECK# is language-agnostic. The entire graphic vocabulary consists of geometric glyphs and Arabic numerals. No text is necessary or permitted in annotations.

### Out of scope

The following elements are explicitly out of scope and delegated to individual games:

- The meaning of suits
- The meaning of the inherited red/black color axis
- The meaning of numeric ranks
- The meaning of each glyph (the vocabulary is shared; the semantics are not)
- The rank → mechanical function mapping (e.g., A–6 = space, 7–10 = resource)
- Movement rules and grid topology
- Resolution, combat, and interaction mechanics
- Economy and resource mechanics
- Wildcard activation conditions
- Victory conditions and scenario objectives
- Oracle mechanics for solo or cooperative play
- How many cards are used
- How cards are dealt
- The number of players

## 2. Design principles

- **Material accessibility:** the only physical requirement is a standard French-suited deck and two permanent markers (black and red). Materials available anywhere, with no proprietary or dedicated components.
- **Additive, non-destructive:** annotations add structural information without overwriting the inherited substrate.
- **Language-agnostic:** no text or letters. Only geometric glyphs and Arabic numerals.
- **Color constraint:** only black and red markers.
- **Dual use:** cards are valid both as hidden information held in hand and as physical components laid on the table.
- **Back reserved for quadrant markers:** the back of the 52 standard cards receives only quadrant markers — identical on all cards, therefore carrying no differential information. No other annotations on the back. Uniformity preserves the anonymity of face-down cards.
- **Complete artifact:** the DECK# deck is fully annotated before any play session. Structural annotation is permanent and fixed. Variable states are tracked with physical tokens, not annotations.

## 3. The inherited substrate

### 3.1 The three axes

| Axis | Values | Nature |
|---|---|---|
| Color | Red / Black | Binary |
| Suit polarity | Hearts vs Diamonds (red) — Clubs vs Spades (black) | Binary within color |
| Rank | A(1) — 2 — … — 10 — J — Q — K | Ordinal scale, 13 degrees |

These axes are immutable. Each game decides how to map them to game concepts; they cannot be physically redefined on the card.

### 3.2 Notes on the substrate

- Face cards (J, Q, K) form a subclass of the ordinal rank. Some games may treat them as a separate category.
- The Joker belongs to none of the three axes. It is structurally outside the system by definition. See section 7.
- The card back is a surface excluded from annotation. See Principle 5 (section 2).

## 4. The graphic vocabulary

### 4.1 Principles

- All glyphs can be drawn with a few strokes by anyone, without artistic skill.
- The only additional chromatic resource is the red marker. Black is the default color.
- No text. No glyph that references any specific alphabet.
- Glyphs must not be visually confused with the existing suits.

### 4.2 Primary glyphs

| Glyph | Strokes | Natural semantics (not prescribed) |
|---|---|---|
| •  dot | 1 | presence, activation, marker |
| — line | 1 | edge, separation, threshold |
| + cross | 2 | connection, crossing, union |
| × diagonal | 2 | negation, block, exclusion |
| △ triangle | 3 | direction, hierarchy, gradient |
| ○ circle | 1 curved | cycle, containment, neutral state |
| □ square | 4 | zone, region, closed space |

Seven glyphs. The "natural semantics" column suggests intuitive associations; it does not prescribe them.

### 4.3 Glyph color — contrasting rule

Primary and modifier glyphs are drawn in the **contrasting** color relative to the card's suit:

- Red cards (♥ ♦): glyphs in **black**
- Black cards (♣ ♠): glyphs in **red**

This rule ensures clear visual separation between annotation and substrate on all cards. The glyph color is entirely derivable from suit — it adds no differential information but maximizes legibility.

### 4.4 Numeric glyphs

Digits 0–9 (Arabic) may be used in annotatable zones as quantities, levels, or counters. They combine with color following the same logic as primary glyphs.

### 4.5 Visual conflicts to avoid

| Suit | Reserved shape |
|---|---|
| Hearts | Heart shape |
| Diamonds | Full or empty diamond |
| Clubs | Trefoil / three-lobed shape |
| Spades | Spade / inverted heart with stem |

The square □ and circle ○ do not conflict with any suit. The triangle △ is safe if drawn small and in a corner position.

## 5. Annotatable zones

```
[NW] ----[N]---- [NE]
  |               |
 [W]  [center]  [E]
  |               |
[SW] ----[S]---- [SE]
```

| Zone | Position | DECK# Annotation |
|---|---|---|
| S | Lower middle edge (internal) | Primary glyph |
| N | Upper middle edge (internal) | Mirror of primary — hand mode |
| NE | Upper right corner | Modifier glyph |
| SW | Lower left corner | Mirror of modifier — hand mode |
| SE | Lower right corner | Orientation dot (north pole) |
| NW | Upper left corner | Reserved — pre-printed index |
| Center / E / W | — | Not used by DECK# annotation |

**Physical edges:** connectivity markers occupy the external white margin of the card (~3–4 mm) — physically separate from the internal zones.

**Symmetrical placement rule:** each glyph appears in two mirror positions — primary zone and mirror zone. This ensures fan readability regardless of card orientation in hand.

**Note on NW:** corner partially occupied by the pre-printed index. No DECK# annotation in this zone.

## 6. The spatial system

### 6.1 The symmetry problem

Standard cards have vertical symmetry: they read the same upside down. As soon as a game introduces spatial elements, this symmetry must be explicitly broken.

### 6.2 The north pole convention

The north pole of a card is the side with the index in canonical position (NW at top left). Recommended practice for sessions with spatial elements: draw a small dot in the SE corner before the session begins — a corner free from printing, asymmetric with respect to the NW index.

### 6.3 Edge markers

| Marking | Structural meaning |
|---|---|
| Thick full-edge line | Wall: passage closed |
| Unmarked edge | Open: connected, passable |
| Dot • at edge midpoint | Threshold: intermediate state, defined by the game |

When cards are placed adjacent on the table, the edges in contact are read as the interface between two spaces.

### 6.4 Quadrant markers

Quadrant markers are found on the **back** of the 52 standard cards. They are identical on all cards — they reveal no differential information when the card is face-down.

Two variants are available; the choice is left to whoever annotates the deck:

**Minimal variant** — four short segments from the midpoint of each edge toward the interior, without crossing the center:

```
      |
  —     —
      |
```

**Extended variant** — full cross from edge to edge (the `+` from the DECK# vocabulary, applied to the back with a fixed structural function):

```
      |
  ————+————
      |
```

Both variants are drawn in black. Jokers receive quadrant markers on the back — identical to those on the 52 standard cards — but receive no annotation on the front face beyond the SE dot.

### 6.5 Internal direction

The triangle △ in a corner zone indicates direction. The orientation of the apex relative to the north pole defines the vector.

## 7. Jokers

Jokers receive the **SE dot** (north pole) on the front face and the **quadrant markers** on the back. No other structural elements: no connectivity markers, no primary glyph, no modifier.

They are **uninstantiated variables**: no pre-assigned semantics from the specification. The game decides everything. A game may use zero, one, or both Jokers.

Possible uses (not prescribed): mechanical wildcard, event card, global state tracker, category Joker.

## 8. Usage profiles

### Base Profile

Pure card game, hand management, narrative, solo scenarios.

**Components:** 1 annotated deck (52 + 2) · 1 fine-tip black permanent marker · 1 fine-tip red permanent marker.  
Estimated annotation time: 15–20 minutes.

### Extended Profile

Tactical grid game, dungeon crawler, skirmish, wargame.

**Additional components:** 6 d6 dice · 12 tokens in 4 distinct groups (3 per group; replaceable with coins, cubes, or any distinguishable objects).

Dice use: 2d6 for resolution, up to 4d6 as counters on a card. Token use: placed on cards to represent entities without covering annotations.

## 9. Card usage modes

### 9.1 Tile mode

Card face-up on the table, visible to all, fixed position. Spatial elements active.

### 9.2 Hand mode

Card in hand, hidden. Spatial elements generally inactive. Annotations must follow the symmetrical placement rule (section 5).

### 9.3 Hand → tile transition

The game must specify:

- Whether the card is placed face-down or face-up
- Whether orientation (north pole) is chosen by the player or fixed
- Whether spatial annotations become active immediately or at a later point

### 9.4 Annotation

The DECK# deck is fully annotated once, following the annotation matrix (section 13), and used across multiple sessions without modification. Structural annotation is permanent.

No in-game annotation is intended for the structural layer. Variable game states are tracked exclusively with removable physical tokens (dice, tokens, coins).

## 10. Physical hierarchy

The 52 standard cards have annotations on both faces. Jokers have annotations on the back and only the SE dot on the front face.

**Front face (52 standard cards):**

1. Inherited substrate (original printing): always visible, never intentionally covered
2. DECK# structural annotation: connectivity on physical edges, primary glyph in S/N zone, modifier in NE/SW zone, north pole dot in SE
3. Physical tokens: objects placed on the card, removable

**Back (all 54 cards):**

- Quadrant markers (minimal or extended variant) — identical on all cards

Structural annotation is fixed and complete. No zone on the front face holds more than one DECK# glyph at a time.

## 11. Designer responsibilities

Every game built on DECK# must specify:

1. How it maps the three inherited axes (rank, color, suit) to game concepts
2. What semantics it assigns to the DECK# vocabulary glyphs (primary and modifier)
3. How it interprets the spatial system: orientation, north pole, connectivity
4. How it interprets the quadrant markers (present on all cards)
5. Whether it uses Jokers and with what role
6. Which profile is required (Base or Extended)
7. What usage mode is intended and the hand → tile transition rules

## 12. License

DECK# is released under **Creative Commons Attribution 4.0 International (CC BY 4.0)**.

Anyone may use, modify, and distribute the specification and games built on it, including for commercial purposes, provided the original source is credited. Games built on DECK# are not required to release their own rulesets under the same license.

© Roberto Bisceglie — [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

## 13. Annotation matrix

The matrix defines the fixed structural annotations for all 54 cards. Each card receives:

- **Connectivity:** open edges (others receive a wall marker). Notation: N/S/E/W separated by `+`.
- **Primary:** glyph in S zone (and mirror in N zone for hand mode).
- **Modifier:** glyph in NE corner (and mirror in SW corner for hand mode).

All 52 standard cards also receive: SE dot (north pole) and quadrant markers.  
Jokers receive the SE dot on the front face and quadrant markers on the back.

The distribution is an authored design artifact, orthogonal to rank/suit/color by deliberate construction. Glyph color is not included as a column — it is entirely derived from suit according to the contrasting rule (section 4.3): black glyphs on ♥/♦, red glyphs on ♣/♠.

| Rank | Suit | Connectivity | Primary | Modifier |
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
| Joker | — | — | — | — |
| Joker | — | — | — | — |

---

DECK#

© 2026 Roberto Bisceglie

This work is licensed under Creative Commons Attribution-ShareAlike 4.0 International. To view a copy of this license, visit https://creativecommons.org/licenses/by-sa/4.0/
