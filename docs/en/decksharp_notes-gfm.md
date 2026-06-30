# DECK# Design Notes
Roberto Bisceglie
2026-06-30

version: 0.7.0 · internal document

------------------------------------------------------------------------

## DC-01 — System name: DECK

**Decision:** the system is named DECK#. **Alternative considered:**
Deckpack. **Rationale:** DECK# (from Greek: language, vocabulary)
reflects the nature of the system — a shared vocabulary for
communicating mechanical information. It is language-agnostic while
being a non-neutral name, which is appropriate: the name is a
meta-label, not a system component. Deckpack remains valid for potential
physical editions or commercial derivatives.

------------------------------------------------------------------------

## DC-02 — Base deck size: 52 + 2 Jokers

**Decision:** 54 cards total. **Rationale:** Jokers are structurally
distinct in the standard deck — the only cards without a suit or rank.
Excluding them would waste a design resource. Advertising cards present
in some decks are not standardized and are not part of the
specification.

------------------------------------------------------------------------

## DC-03 — Permanent marking

**Decision:** annotations with permanent marker. **Alternatives
considered:** erasable for all layers; mixed system. **Rationale:**
permanent marking transforms each deck into a unique artifact. Variable
states are tracked with physical tokens, which are already removable by
nature. The mixed system is available as an optional practice for
individual games but is not prescribed.

------------------------------------------------------------------------

## DC-04 — Open system: no rank → function mapping

**Decision:** DECK# does not assign mechanical functions by rank.
**Discarded alternative:** cardpack-spec v0.2.0 had defined Space (A–6)
/ Resource (7–10) / Actor (J–Q–K) as a fixed partition. **Rationale:**
that partition is the structure of a specific tactical game, not an open
vocabulary. It blocks any game that wants to use an Ace as a character
or a King as a territory. An open system does not prescribe what each
card represents — each game built on top does that.

------------------------------------------------------------------------

## DC-05 — Seven primary glyphs (closed vocabulary)

**Decision:** exactly 7 glyphs: dot, line, cross, diagonal, triangle,
circle, square. **Rationale:** they cover the primitive geometric shapes
producible with 1–4 strokes. Sufficiently visually distinct from each
other and from suits. The vocabulary is closed to guarantee
interoperability — a glyph not in the list does not exist in DECK#. The
asterisk from cardpack-spec v0.2.0 was excluded because visually
ambiguous and motivated by a semantic role (Joker) that the
specification must not pre-assign.

------------------------------------------------------------------------

## DC-06 — Glyph color: contrasting rule

**Original decision (v0.1–v0.6):** marker color is an independent
semantic layer, orthogonal to the glyph; convention not prescribed.
**Updated decision (v0.7):** glyph color follows a fixed contrasting
rule — black glyphs on red cards (♥/♦), red glyphs on black cards (♣/♠).
See DC-22. **Rationale for change:** a semantic axis that is “available
but not prescribed” never enters the canonical annotation. The
contrasting rule is simple, memorable, and guarantees high legibility on
all cards without requiring a color column in the matrix.

------------------------------------------------------------------------

## DC-07 — Back: exception for quadrant markers

**Original decision (v0.1–v0.5):** back excluded from annotation.
**Updated decision (v0.6):** the back of the 52 standard cards receives
only quadrant markers. Two variants allowed: minimal (four short
segments at midpoints) or extended (full `+` cross). The choice is left
to the annotator. Jokers do not receive quadrant markers on the back.
**Rationale for exception:** quadrant markers are identical on all 52
standard cards — they reveal no differential information. The original
rationale (preserving anonymity for fog of war) does not apply to
uniform markers. The benefit is eliminating the coexistence of quadrant
markers and the primary glyph in S zone (DA-01 / DC-21, now superseded).

------------------------------------------------------------------------

## DC-08 — North pole convention

**Decision:** north pole = side with index in canonical position (NW at
top left). Dot in SE as orientation marker. **Problem:** cards have
vertical symmetry for ergonomic reasons. With spatial elements, this
must be explicitly broken. **Rationale:** the SE dot is the least
invasive solution — it covers nothing, is asymmetric, requires one
stroke. A fixed arrow would have introduced spatial semantics even for
games without orientation.

------------------------------------------------------------------------

## DC-09 — Symmetrical placement in hand mode

**Decision:** annotations in two mirror positions — primary glyph in S
zone with mirror in N; modifier in NE corner with mirror in SW. See
DC-18 for specific zones. **Source:** cardpack-spec v0.2.0 (zones
updated in DC-18). **Rationale:** standard ergonomic convention for card
decks — indices are already duplicated and rotated for the same reason.
Guarantees fan readability without additional rules.

------------------------------------------------------------------------

## DC-10 — Quadrant markers

**Decision:** present on the **back** of the 52 standard cards (migrated
from front face in v0.6, see DC-07 rev.). Two variants: minimal (four
short segments) or extended (`+` cross). Absent on Jokers. **Source:**
cardpack-spec v0.2.0 (universality established in DC-17; migration to
back in DC-07 rev. v0.6). **Rationale:** on the front face, short
segments were necessary to avoid covering pips. On the back, the
extended variant (full cross) becomes viable without interference.

**Revision v0.7.1 (2026-05-13):** extended to Jokers on the back as
well. See DC-11 rev. for rationale.

------------------------------------------------------------------------

## DC-11 — Jokers as uninstantiated variables

**Decision:** Jokers receive only the SE dot (north pole). No primary
glyph, no modifier, no connectivity markers, no quadrant markers.
**Discarded alternative:** fixed asterisk in cardpack-spec v0.2.0.
**Rationale:** the asterisk assigns Jokers a specific functional role
before any game uses them. An open system leaves Jokers as neutral
surfaces. Their absence from the inherited axes is already sufficient to
distinguish them.

**Revision v0.7.1 (2026-05-13):** Jokers receive quadrant markers on the
back. The original rationale (Joker neutrality as a blank surface)
applies to the front face, not the back: quadrant markers are uniform on
all cards and convey no differential information. Their absence on Joker
backs made them recognizable when face-down, compromising fog of war.
The neutrality principle remains intact: the Joker is still free of
pre-assigned semantics on the front face.

------------------------------------------------------------------------

## DC-12 — Base and Extended profiles

**Decision:** two profiles with increasing requirements. **Source:**
cardpack-spec v0.2.0 (absent in DECK# v0.1). **Rationale:** the system
must be accessible with minimal materials but should not pretend all
games have the same requirements. The distinction is a scope
declaration, not a hierarchy.

------------------------------------------------------------------------

## DC-13 — “Designer responsibilities” section

**Decision:** explicit list of what every game built on DECK# must
specify. **Rationale:** without this section, a designer does not know
where their work begins. The list delimits the interface between
specification and game.

------------------------------------------------------------------------

## DC-14 — CC BY 4.0 License

**Decision:** Creative Commons Attribution 4.0 International.
**Alternatives considered:** CC0, CC BY-SA, proprietary license with
usage permission. **Rationale:** CC BY 4.0 balances openness and
attribution. It permits commercial use, does not impose copyleft on
derivatives, and requires only source citation. CC0 would have
sacrificed any ecosystem traceability. CC BY-SA would have created
friction for commercial games.

------------------------------------------------------------------------

## DC-15 — Single structural layer

**Decision:** glyphs are structural by definition. There is no separate
semantic layer added by the game — the designer interprets the
structural glyphs; they do not add their own layer. **Discarded
alternative:** two-layer model (DECK# structural + game semantic).
**Rationale:** the structural/semantic layer distinction is conceptual,
not physical. Only one annotation layer exists on the deck. Semantics is
a reading operation, not a writing one.

------------------------------------------------------------------------

## DC-16 — Three structural dimensions per card

**Decision:** each card is defined by three dimensions: Connectivity
(open edge patterns across 15 configurations), Primary (glyph in S
zone), Modifier (glyph in NE corner). Positional hierarchy, not
semantic: identical Primary + Modifier (e.g., ×/×) are legitimate
combinations. **Rationale:** three independent dimensions create a
combinatorial space (15 × 7 × 7 = 735 theoretical configurations) far
richer than the 52 slots needed, guaranteeing design freedom in
distribution.

------------------------------------------------------------------------

## DC-17 — Universal quadrant markers

**Decision:** quadrant markers are present on all 52 standard cards.
Absent on Jokers. **Discarded alternative:** variable presence as a
matrix dimension. **Rationale:** uniform spatial capability simplifies
annotation and shifts capacity management to the game, which can ignore
it, use it partially, or exploit it fully.

------------------------------------------------------------------------

## DC-18 — Zones: Primary in S, Modifier in NE

**Decision:** primary glyph in S zone (internal, lower middle edge) with
mirror in N; modifier in NE corner with mirror in SW. Center not
occupied by DECK# annotations. **Discarded alternative:** primary at
center (blocked by pips on number cards). **Rationale:** S zone is
visible when cards are held in a fan; it is clean and separated from
pips for all cards. NE is the second most visible corner. The center
remains readable for pips and available as a neutral visual space.

------------------------------------------------------------------------

## DC-19 — Annotation matrix as design artifact

**Decision:** the distribution of connectivity and glyphs across 52
cards is an authored artifact, orthogonal to rank/suit/color by
deliberate construction. No algorithmic formula connects substrate
properties to structural annotation. **Rationale:** formula-based
orthogonality would require using rank/suit as an index, implicitly
re-encoding them. Design-based orthogonality is more robust: no
systematic correlation, controlled topological variety.

------------------------------------------------------------------------

## DC-20 — Pre-session annotation as absolute standard

**Decision:** the DECK# deck is fully annotated before any session. No
in-game annotation for the structural layer. **Rationale:** consistent
with the deck-as-fixed-artifact model. Removes a source of ambiguity
from the “Designer responsibilities” section — it is not a game choice,
it is a system constraint.

------------------------------------------------------------------------

## DC-22 — Glyph color: contrasting rule

**Decision:** black glyphs on red cards (♥/♦); red glyphs on black cards
(♣/♠). Fixed rule, no color column in the matrix. **Discarded
alternatives:** (1) color as independent semantic axis in the matrix —
requires designed distribution and adds complexity; (2) all glyphs in
black — loses legibility on black cards. **Rationale:** contrasting
color is entirely derivable from suit (zero new differential
information) but maximizes visual separation between annotation and
substrate. The rule’s simplicity is its primary value: anyone annotating
the deck can derive it without consulting the matrix.

------------------------------------------------------------------------

## DC-21 — Coexistence of quadrant marker and primary glyph in S zone

**SUPERSEDED in v0.6 by DC-07 rev.** Quadrant markers migrate to the
back: coexistence with the primary glyph in S zone is no longer an
issue. Section 5.1 of the spec (placement diagram) has been removed.

------------------------------------------------------------------------

## Open decisions

**DA-01 — CLOSED** (DC-16, DC-18): coexistence of multiple glyphs in the
same zone is not an issue — each zone holds at most one DECK# glyph.

**DA-02 — Deck subset notation:** standard system for documenting which
subset is used (e.g., `DECK#/♠A–6`).

**DA-03 — CLOSED:** compatibility with non-standard decks is out of
scope by definition. DECK#’s prerequisite is a standard French/poker
deck (52 + 2 Jokers). Spanish, German, and tarot decks do not satisfy
the inherited substrate of section 3.

**DA-04 — CLOSED (rejected):** quadrant markers on the back would be
useful in tile mode with a face-down card, but the back pattern varies
from deck to deck in unpredictable ways — on decks with dense patterns
the markers would be illegible or hidden. DC-07 (back not annotatable)
remains valid without exceptions.

------------------------------------------------------------------------

DECK#

© 2026 Roberto Bisceglie

This work is licensed under Creative Commons Attribution-ShareAlike 4.0
International. To view a copy of this license, visit
https://creativecommons.org/licenses/by-sa/4.0/
