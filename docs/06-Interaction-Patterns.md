# 06 · Interaction Patterns

## Overview

Interaction Patterns describe behaviour, not interface.

They define how Atlas behaves.

They are not implementation details.

They are repeatable behaviours that should remain consistent regardless of platform or visual design.

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

The builder may choose to describe the relationship immediately, later or never.

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

Describe an existing relationship.

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

## Notes

Connection labels describe relationships.

They never create them.

---

# Add a Thing

## Intent

Introduce something new into Atlas.

## Interaction

A Thing may be created by:

- dragging content onto the Canvas
- double-clicking the Canvas
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

# Add a Description

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

## Notes

Values may be:

- literal values
- references to existing Things

Selecting a Thing as a Value creates or updates the corresponding Connection.

---

# Select a Thing

## Intent

Focus on a single Thing.

## Interaction

Click a Thing.

## Result

The selected Thing becomes the current focus.

The Inspector updates to reflect the current selection.

Selecting never changes the graph.

---

# Inspect a Thing

## Intent

Understand a Thing without leaving the current context.

## Interaction

Select a Thing.

## Result

The Inspector presents a concise summary of the selected Thing.

This may include:

- label
- descriptions
- key relationships
- available actions

The Canvas remains visible.

## Notes

The Inspector is intended for orientation rather than comprehensive editing.

---

# Explore a Thing

## Intent

View a Thing in greater detail.

## Interaction

Choose to explore the currently selected Thing.

## Result

The Canvas smoothly transitions to a view centred on the selected Thing.

The Thing's internal structure is revealed using the same spatial language as the wider graph.

The builder remains within the same graph.

## Notes

Exploration changes perspective rather than opening a separate screen.

The graph itself never changes.

---

# Semantic Zoom

## Intent

Reveal different levels of information without changing context.

## Interaction

Zoom the Canvas.

## Result

Different levels of detail become visible according to scale.

Higher-level views present summaries.

Closer views reveal richer structure.

The underlying graph remains unchanged.

## Notes

Zoom changes perspective, not data.

---

# Follow a Relationship

## Intent

Navigate through the graph.

## Interaction

Select a connected Thing from either the Canvas or the Inspector.

## Result

The selected Thing becomes the current focus.

The Inspector updates.

The Canvas recentres on the selected Thing if required.

Navigation never changes the graph.

---

# Inspect a Selection

## Intent

Understand the current selection.

## Interaction

Select one or more Things.

## Result

The Inspector reflects the current selection.

For a single Thing it presents information about that Thing.

For multiple Things it presents a summary of the selection.

## Notes

The Inspector always reflects the current selection rather than assuming a single Thing.

---

# Reuse Vocabulary

## Intent

Encourage consistency without imposing structure.

## Behaviour

Atlas remembers previously used:

- Attribute names
- Attribute values
- Connection labels

Suggestions appear naturally while builders work.

Builders remain free to create new vocabulary at any time.

---

# Multi-selection

## Intent

Perform the same action on multiple Things.

## Example

Three Things are selected.

They are dragged onto another Thing.

## Result

Each selected Thing becomes connected to the target Thing.

No additional Connections are inferred.

Only the minimum number of Connections required by the gesture are created.

---

# Move a Thing

## Intent

Reorganise the workspace.

## Interaction

Drag a Thing to a new position on the Canvas.

## Result

Only the visual layout changes.

The graph remains unchanged.

---

# Delete

## Intent

Remove a Thing, Connection or Description.

## Result

Deletion should always be predictable.

Builders should always understand what will be removed before confirming the action.

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
- Scale changes perspective, not data.
- Visual actions and textual actions produce the same underlying model.
- The same interaction language applies at every level of detail.
- The same knowledge may be presented in different ways without changing the graph.
- Atlas should feel more like exploring a landscape than managing records in a database.
