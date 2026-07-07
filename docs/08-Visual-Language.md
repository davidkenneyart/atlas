# 08 · Visual Language

## Overview

Atlas is built from a deliberately small visual language.

The same language should be recognisable throughout the project.

- documentation
- interface
- branding
- publishing

Every visual element should communicate meaning.

Nothing should exist purely for decoration.

---

## The Atlas Alphabet

The Atlas visual language is composed of three symbols.

![Atlas Alphabet](../design/visual-language/atlas-alphabet.png)

Together they represent the three fundamental concepts of Atlas.

| Symbol | Meaning |
|---------|---------|
| ○ | Thing |
| ◇ | Description |
| ──── | Relationship |

No additional symbols should be introduced unless they represent a genuinely new concept.

---

## Geometry

The alphabet is constructed from a shared geometry.

| Element | Specification |
|----------|---------------|
| Thing diameter | 30 units |
| Stroke width | 2 units |
| Description | 30 × 30 units, rotated 45° |
| Relationship | 30 units long, 2 units high |

These proportions define the language.

Implementations may scale freely provided the proportions remain unchanged.

---

## Composition

The symbols combine to express more complex structures.

```
○────○
```

Two connected Things.

```
○────○────○
```

A path.

```
     ○
     │
○────○────○
```

A hub.

Complexity emerges through composition.

No additional symbols are required.

---

## Canvas

The Canvas presents only:

- Things
- Relationships

Descriptions belong in the Inspector and supporting interfaces.

The Canvas exists to reveal structure.

Not detail.

---

## Inspector

The Inspector presents descriptions and relationships.

The alphabet should provide a visual bridge between the interface and the documentation.

Builders should quickly recognise:

- ○ as a Thing
- ◇ as a Description
- ──── as a Relationship

---

## Branding

The Atlas identity should emerge from the same visual language.

Branding should never introduce concepts absent from the product.

Likewise, the product should naturally reflect the visual language established by the brand.

---

## Accessibility

The visual language should never be the only means of communication.

Every visual concept should have an equivalent textual representation.

The symbols reinforce understanding.

They do not replace it.

---

## Design Principles

Every visual decision should reinforce the following principles.

- Every visual element carries meaning.
- Simplicity is preferred over decoration.
- Consistency is preferred over novelty.
- One geometry.
- One stroke.
- The work remains the focus.
- The interface should become invisible.
- Reduce before adding.
