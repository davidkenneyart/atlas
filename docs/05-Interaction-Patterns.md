# 06 · Interaction Patterns

## Overview

Interaction Patterns describe behaviour, not interface.

Interaction Patterns describe how builders interact with Atlas.

They are not implementation details.

They are repeatable behaviours that define how Atlas feels to use.

Every interaction should be:

- predictable
- direct
- easy to reverse
- consistent with the Core Model

Whenever a new interaction is proposed, it should build upon existing patterns rather than introducing new concepts.

---

# Drag Thing onto Thing

## Intent

Create a Connection between two Things.

## Interaction

- Select and drag a Thing.
- Hover over another Thing.
- The target Thing highlights.
- A temporary Connection is displayed.
- Release to create the Connection.
- The dragged Thing returns to its original position.

## Result

A Connection is created between the two Things.

The Connection initially has no label.

The builder may choose to describe the relationship immediately or later.

## Notes

Dragging expresses a relationship, not hierarchy.

No assumptions are made about the meaning of the Connection.

---

# Drag Thing onto Connection

## Intent

Insert a Thing into an existing Connection.

## Before

```
A ──── B
```

## After

```
A ──── C ──── B
```

## Result

The original Connection is replaced by two new Connections.

No additional Connections are created.

---

# Describe a Connection

## Intent

Give meaning to an existing Connection.

## Interaction

- Select the Connection.
- Enter a forward label.
- Optionally enter a reverse label.

Example:

```
Merge 001

Exhibited at

SOMA
```

Reverse:

```
SOMA

Exhibited by

Merge 001
```

## Result

The graph remains unchanged.

Only the description of the Connection changes.

---

# Add a Thing

## Intent

Introduce something new into Atlas.

## Interaction

A Thing may be created by:

- dragging content onto the canvas
- double-clicking the canvas
- selecting **Add Thing**

## Result

A new Thing is created.

No description is required.

The Thing exists immediately.

---

# Rename a Thing

## Intent

Give a Thing a human-readable label.

## Interaction

- Select the Thing.
- Rename.
- Enter a label.

## Result

Only the label changes.

The Thing itself remains the same.

---

# Add an Attribute

## Intent

Describe a Thing.

## Interaction

- Select a Thing.
- Choose **Add Attribute**.
- Enter an Attribute name.
- Atlas suggests previously used Attribute names.
- Enter a Value.
- Atlas suggests previously used Values for that Attribute.

## Result

The Thing becomes more richly described.

Vocabulary emerges naturally through use.

---

# Multi-selection

## Intent

Perform the same action on multiple Things.

## Example

Three Works are selected.

They are dragged onto one Exhibition.

## Result

Each selected Thing becomes connected to the target Thing.

No additional Connections are inferred.

Only the minimum number of Connections required by the gesture are created.

---

# Move a Thing

## Intent

Reorganise the workspace.

## Interaction

Drag a Thing to a new position on the canvas.

## Result

Only the visual layout changes.

The graph remains unchanged.

---

# Select a Thing

## Intent

Focus on a single Thing.

## Interaction

Click a Thing.

## Result

The inspector opens.

The builder may:

- rename the Thing
- add Attributes
- view Connections
- edit Connection labels

Selecting never changes the graph.

---

# Undo

## Intent

Reverse the previous action.

## Result

Every editing action should be reversible.

Builders should feel free to experiment without fear of damaging their graph.

---

# Principles

Every Interaction Pattern should support the following principles.

- Every gesture has one meaning.
- Builders remain in flow.
- The interface never interrupts momentum.
- The graph is the source of truth.
- Visual actions and textual actions should produce the same underlying model.
- Atlas should feel more like arranging ideas on a desk than managing records in a database.
