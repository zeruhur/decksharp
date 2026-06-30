---
title: "DECK# Game Design Guide"
subtitle: "Companion to DECK# specification v0.7.0"
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

## 1. Nature of this document

This guide does not prescribe how to build a game on DECK#. It shows what the system offers — its mathematical properties, its productive tensions, its spaces of possibility — so the designer can recognize and deliberately exploit them.

DECK# is a substrate. The designer is the author. This document is an orientation tool, not a constraint.

## 2. The mathematics of the deck

Before assigning any meaning, it is worth understanding the structure you inherit. The annotated DECK# deck carries properties that are not obvious but have deep implications for design.

### 2.1 Glyph balance

The seven primary glyphs (—, •, +, ×, △, ○, □) each appear 7 or 8 times across the 52 standard cards. The same holds for modifiers.

Practical implication: **whatever semantics you assign to a glyph, that semantics will be uniformly distributed throughout the deck**. If the circle ○ means "event card," there will be 7–8 events in the deck — neither too rare nor dominant. Balance is a system guarantee, not a designer responsibility.

This also holds for primary+modifier pairs: there are 32 distinct pairs across 52 cards. Variety is high; no combination dominates.

### 2.2 Connectivity structure

Open edges per card are distributed across three precise tiers:

| Open edges | Number of cards |
|||
| 1 | 16 |
| 2 | 16 |
| 3 | 16 |
| 4 (all) | 4 |

An almost musical symmetry: three tiers of 16, plus four cards with maximum connectivity. If you are building a game with spatial elements, this distribution is your topological palette: one third of the deck creates dead ends, one third corridors, one third intersections, and four cards are nodes.

### 2.3 The texture of ordinal rank

Connectivity is not distributed perfectly uniformly relative to card rank — and this is not a flaw; it is a texture that games can exploit.

| Rank range | Average open edges |
|||
| A, J (low) | 1.25 – 1.50 |
| 2, 5, 6 (low-mid) | 1.50 |
| 3, 7, 10 (high-mid) | 2.25 – 2.50 |
| 8, K (high) | 3.00 |
| Q | 2.75 |

If you map ordinal rank to "rank" or "power," high cards tend to be more spatially connected as well. This can be an interesting resonance — or a tension to deliberately break. Both are valid design choices, but they must be conscious choices.

### 2.4 What is not guaranteed

Connectivity is orthogonal to suit and color by deliberate construction — no suit dominates another dimension of annotation. Ordinal rank, however, exhibits the texture described above. Keeping this in mind avoids surprises during playtesting.

## 3. The three inherited axes

The standard deck carries three information axes that DECK# does not redefine. How these axes are mapped to game concepts is the designer's first major decision — and probably the most structuring one.

### 3.1 Ordinal rank

Thirteen degrees from A to K. This axis is the richest in terms of granularity.

Possible mappings:

- **Power or intensity**: higher = stronger. The most intuitive mapping, with connectivity texture as a spatial corollary.
- **Phase or stage**: A = beginning, K = end. Useful for narrative games or those with temporal arcs.
- **Discrete type**: A–6 = one type, 7–K = another. Reduces granularity in favor of simplicity.
- **Quantified resources**: rank as a pure number. Effective for economic games.

Face cards (J, Q, K) form a natural subclass. Treating them as a special category adds a level of hierarchy at no component cost.

### 3.2 Color

Red / Black. Binary axis, maximally visible.

Possible mappings:

- **Faction or polarity**: the most immediate mapping. Two forces, two factions, two states.
- **Mode**: action/reaction, attack/defense, day/night.
- **Cost and benefit**: red = risk, black = safety — or vice versa.

Color is the axis with the highest visual salience. Assigning it a mechanically low-importance meaning is a waste. Assigning it too much importance makes it a game discriminator before the player can even read the annotations.

### 3.3 Suit

Four suits, two red and two black. Suit carries an internal structure: it is not merely a four-value axis, but a four-value axis with two chromatic pairs.

Possible mappings:

- **Four independent categories**: classes, biomes, factions, resource types.
- **Two pairs with internal distinction**: hearts vs diamonds as variants of "red," clubs vs spades as variants of "black." Useful for systems with a two-level hierarchy.
- **Ignore suit, use only color**: legitimate if four categories create too much complexity for the target game.

### 3.4 Axis coherence

A key question to ask before playtesting: **do the inherited axes speak to each other in a way that is coherent with the game's tone?**

If rank maps to "threat level" and color maps to "ally/enemy," the Red King will be a maximum threat from an enemy. The Black Two will be a minimal threat from an ally. Does this combination make sense in your game? Does it produce interesting or confusing situations?

There is no single answer. There is only the necessity of having asked.

## 4. The graphic vocabulary

DECK#'s seven glyphs are aniconic: they depict nothing. This is a feature, not a limitation. Aniconicity ensures that the semantics assigned by the game do not conflict with pre-existing cultural associations — or that it can do so deliberately.

### 4.1 Assigning semantics to glyphs

Some practical considerations:

**Exploit natural semantics without being bound by them.** The specification suggests intuitive associations (△ = direction, × = negation, ○ = cycle). These associations reduce the cognitive load for new players. Using them is often the most efficient choice; ignoring them is possible but requires a compensatory reference system (glossary, legend).

**Primary and modifier are two distinct semantic layers.** Do not treat them as two equivalent "properties." An effective mapping tends to have the primary as category or type (what this card is) and the modifier as quality or state (how it behaves). The reversal is possible but rare.

**Consider total cognitive load.** Seven glyphs per layer, two layers, plus three inherited axes: the player may need to decode up to five dimensions per card. Reading simplicity must be field-tested, not assumed.

### 4.2 Visual conflicts to avoid

The specification lists the shapes reserved for suits (heart, diamond, trefoil, spade). The point is not merely aesthetic: a glyph that resembles a suit creates reading ambiguity in real play conditions — worn cards, non-ideal lighting, players unfamiliar with the system.

The square □ and circle ○ are the safest glyphs. The triangle △ is safe in a corner position and when small. The line — and cross + are automatically read as separators or connectors — an association to exploit or counter with explicit instruction.

## 5. The spatial system

DECK#'s spatial system is optional at the profile level (Base vs Extended), but its structure deserves attention even in pure card games — because it defines how cards interact physically on the table.

### 5.1 Connectivity as a graph

When cards are placed adjacent on the table, edges marked as "wall" close the passage; open edges create connection. The result is an emergent topological graph: not the grid of a standard role-playing game, not a fixed map, but a space that is built card by card during play.

Design implications:

- The game can allow the player to choose card orientation (north pole = variable), creating a generative system. Each session produces a different map.
- The game can fix orientation, using connectivity as an intrinsic card property — a corridor is a corridor, regardless of how it is placed.
- The game can mix both approaches: free orientation during setup, fixed during play.

### 5.2 The hand → tile transition

When a card moves from hand to table, it changes ontology: from hidden information to physical component. This transition must be specified by the designer across three points:

**1. Reveal:** is the card placed face-down or face-up? A face-down card is a space of uncertainty; a face-up one is shared information. Both make sense in different contexts.

**2. Orientation:** is the north pole chosen by the player or fixed? Choosing orientation is a strategic act if spatial annotations (connectivity, triangle direction) carry mechanical weight.

**3. Activation:** do spatial annotations become active immediately or at a later point? A card placed face-down with connectivity that activates only on reveal creates a surprise mechanic. A card with a delayed effect creates planning opportunities.

These three decisions are not independent. Defining them together produces the tactical behavior of placement.

## 6. Jokers

Jokers are the two cards structurally outside the system: no inherited axis, no DECK# annotation except the north pole dot on the front face. On the back they receive quadrant markers — identical to all other cards — so they are not recognizable when face-down. They are uninstantiated variables.

The choice to use them — and how — says something fundamental about the game's architecture.

### 6.1 Mechanical wildcard

The Joker as universal card: it can be played as any card in the deck, or as any rank/suit/glyph. Simple to implement, high strategic impact. Risk: trivializing decisions if too powerful, or being ignored if too weak.

### 6.2 Event card

The Joker as an interruption of normal flow: when drawn or played, it triggers a global effect. It is not part of the "playable" deck in the ordinary sense — it is a discontinuity marker. Useful for games with narrative arcs or distinct game phases.

### 6.3 Global state tracker

The Joker as a fixed component on the table, not in hand. Used to track a shared state — a counter, a phase, an active condition. In this case it is never "played": it is always visible, always present. Works in games with persistent state variables between turns.

### 6.4 Category Joker

The two Jokers as two distinct entities (not interchangeable). Each represents something irreducible to the ordinal system — a unique character, a non-generatable resource, a singular event. Requires the game to give them an explicit identity.

**The question to ask:** does your game need elements that cannot be obtained by varying rank, suit, color, and glyphs? If so, Jokers are the tool. If not, using them is optional — and omitting them is a design choice, not an omission.

## 7. Design patterns

These are not templates. They are recurring configurations that emerge from how the Base and Extended profiles are used in practice. Recognizing them helps orient the ideation phase.

### 7.1 Pure card game

**Base Profile.** Cards stay in hand or are played as an action (not placed as a grid). The spatial system is inactive or marginal. The core of the game is hand management and resolution of played cards.

DECK# adds: two semantic levels per card (primary + modifier), plus the three inherited axes. Games with drafting, combo, or emergent narrative mechanics are possible without ever placing a card in tile mode.

**Productive tension:** glyph balance guarantees distribution equity. A card game that exploits this will have fewer "broken deck" problems than a custom system.

### 7.2 Tactical grid and dungeon crawler

**Extended Profile.** Cards are placed on the table in tile mode, building the play space. Edge connectivity defines the topology. Tokens and dice manage entities and resolution.

DECK# adds: a generative space that changes each session, with predetermined topological properties (connectivity) but variable arrangement (orientation). The asymmetry of connectivity distribution (see section 2.3) can naturally produce more open or more closed zones.

**Productive tension:** the hand → tile transition is the richest mechanical moment. How space is revealed — who decides orientation, when edges activate — defines the tactical rhythm of the game.

### 7.3 Solo and cooperative game

**Base or Extended Profile.** A single player (or cooperative group) against the system. DECK# does not include oracle mechanics by default — this is a deliberate choice. The designer must build an oracle engine that uses the deck as a source of answers.

Possible approaches:

- Draw a card and read the primary glyph as an answer (yes/no/maybe, based on binary glyph oppositions).
- Combine rank + primary glyph to generate an event from a table.
- Use the connectivity of the drawn card to determine narrative direction.

DECK# provides sufficient multidimensional semantic space to build rich oracle systems without requiring additional components.

### 7.4 Asymmetric multiplayer

**Base or Extended Profile.** Players with different roles, resources, or capabilities. DECK# supports asymmetry through axis mapping: color (red/black) is the most natural axis for differentiating factions. Suit can add a second level of intra-faction differentiation.

**Caution:** in an asymmetric game, balanced glyph distribution is a fair resource for all players. If a player has access only to a subset of the deck (by suit or color), glyph distribution in that subset is no longer guaranteed equal. It is worth verifying partial distributions during design.

## 8. Designer checklist

Every game built on DECK# requires the designer to explicitly specify the following elements. This checklist extends section 11 of the specification with design-oriented questions.

### Inherited axes

- [ ] How is ordinal rank (A–K) mapped? Is it a continuous scale or discretized into tiers?
- [ ] How is color (red/black) used? Is the mapping mechanically significant?
- [ ] How are suits used? As four categories, two pairs, or is the suit distinction ignored?
- [ ] Are the three mappings mutually coherent? Do they produce interesting or problematic combinations?

### Graphic vocabulary

- [ ] What semantics are assigned to primary glyphs? Is it clearly documented for the player?
- [ ] What semantics are assigned to modifier glyphs? Is it distinct and complementary to the primary?
- [ ] Do the glyphs used exploit or contrast the natural semantics (section 4 of the specification)?

### Spatial system (if applicable)

- [ ] Is the profile Base or Extended?
- [ ] If Extended: how is the hand → tile transition managed (reveal, orientation, activation)?
- [ ] Is the connectivity distribution (1/2/3/4 open edges) congruent with the play space design?

### Jokers

- [ ] Are Jokers used? If so, how many (zero, one, both)?
- [ ] What role do they have: wildcard, event, state tracker, distinct entity?
- [ ] Is their role irreducible to that of any other card in the system?

### Playability

- [ ] How many information dimensions must the player decode to read a card? Is this load sustainable?
- [ ] Is balanced glyph distribution an asset for the game or does it create a problem to manage?
- [ ] If the game uses a deck subset (by suit, color, or rank), has glyph distribution in that subset been verified?

---

DECK#

© 2026 Roberto Bisceglie

This work is licensed under Creative Commons Attribution-ShareAlike 4.0 International. To view a copy of this license, visit https://creativecommons.org/licenses/by-sa/4.0/
