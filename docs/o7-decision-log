# 07 · Decision Log

This document records significant design decisions made during the development of Atlas.

It exists to preserve intent.

The log records decisions, not discussions.

Each entry should explain:

- what changed
- why it changed
- what principle it supports

The Decision Log is historical.

Decisions should never be edited to reflect later thinking.

If a decision changes, add a new entry explaining why.

---

## D001 · Atlas begins with Things

**Decision**

Atlas begins with a Thing.

Everything else is built from Things and their relationships.

**Reason**

This provides the smallest possible starting point.

Builders should never need to decide what kind of Thing something is before adding it.

---

## D002 · Types removed from the Core Model

**Decision**

Types are no longer fundamental to Atlas.

They emerge through Attributes and Connections.

**Reason**

Types introduced unnecessary structure.

Builders already know what something represents.

Atlas should not require concepts that naturally emerge from the graph.

---

## D003 · Connections may exist without labels

**Decision**

Connections are created independently of their description.

Labels remain optional.

**Reason**

Builders often recognise relationships before they know how to describe them.

Meaning can emerge later.

---

## D004 · Attribute Values may reference Things

**Decision**

Attribute Values may be:

- literal
- references to existing Things

Reference Values create or reuse Connections.

**Reason**

This allows builders to work naturally while preserving a single underlying graph.

---

## D005 · The Canvas and Inspector are complementary

**Decision**

The Canvas and Inspector present different perspectives of the same graph.

Neither is considered the primary interface.

**Reason**

The Canvas supports spatial thinking.

The Inspector supports focused inspection and editing.

Both represent the same knowledge.

---

## D006 · Views never change the graph

**Decision**

Changing a View never modifies the Core Model.

**Reason**

Knowledge should be stored once.

Everything else is an interpretation.

---

## D007 · Discovery is read-only

**Decision**

Discovery may analyse and suggest.

It never modifies the graph.

**Reason**

Meaning belongs to the builder.

Atlas should reveal, not decide.

---

## D008 · The visual language is deliberately minimal

**Decision**

Atlas is built from three visual primitives:

- ○ Thing
- ◇ Description
- ──── Relationship

No additional symbols should be introduced unless they represent a genuinely new concept.

**Reason**

A small visual language is easier to learn, easier to remember and creates consistency across documentation, interface and branding.

---

## D009 · The interface should become invisible

**Decision**

Atlas should gradually disappear behind the builder's work.

**Reason**

People should think about their work.

Not about Atlas.

---

## D010 · Remove before adding

**Decision**

Whenever a new concept is proposed, the first question should be:

> Can this emerge from the existing model?

If the answer is yes, no new concept should be introduced.

**Reason**

Atlas grows through simplification rather than accumulation.
