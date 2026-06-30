# 05 · Architecture

## Overview

Atlas is built from a small number of independent systems.

Each system has a single responsibility.

Together they create the experience of building, connecting and understanding knowledge.

The architecture is deliberately modular.

Each part should be understandable in isolation.

The Core Model remains the centre of the system.

Everything else presents, analyses, stores or exports it.

---

## Architecture


                   Builder

                      │

              Interaction Layer

        ┌─────────────┼─────────────┐
        │             │             │
        │             │             │
     Canvas      Inspector      Search
        │             │             │
        └─────────────┼─────────────┘
                      │

                 Core Model

      Things · Attributes · Connections

        ┌─────────────┼─────────────┐
        │             │             │
     Discovery    Publishing    Storage

---

## Core Model

The Core Model is the heart of Atlas.

It stores only three concepts.

- Things
- Attributes
- Connections

It contains no knowledge of:

- interface
- publishing
- visual appearance
- artificial intelligence
- storage implementation

Everything else depends upon it.

The Core Model depends upon nothing.

---

## Canvas

The Canvas is the builder's workspace.

It is responsible for:

- displaying Things
- displaying Connections
- positioning Things
- selecting Things
- dragging
- zooming
- panning

The Canvas never modifies the graph directly.

The Canvas presents one perspective of the Core Model. Builder interactions are translated into changes to the Core Model.

---

## Inspector

The Inspector is responsible for editing.

Builders use it to:

- rename Things
- add Attributes
- edit Attribute values
- describe Connections
- review existing information

The Inspector presents a focused view of a single Thing and its relationships.

It does not own it.

---

## Views

Views change how the graph is seen.

Examples include:

- colour by Attribute
- shape by Attribute
- size by Connectivity
- filtering
- highlighting
- grouping

Views never modify the graph.

They are interpretations of the graph.

---

## Discovery

Discovery observes the graph.

Its purpose is to reveal information that already exists.

Examples include:

- paths
- clusters
- isolated Things
- repeated structures
- highly connected Things
- suggestions

Discovery may suggest. It never decides.

Discovery never modifies the graph.

It only observes it.

---

## Publishing

Publishing transforms Atlas into other formats.

Examples include:

- websites
- portfolios
- catalogues
- exhibition guides
- PDFs
- printed material

Publishing never modifies the graph.

It produces representations of it.

---

## Storage

Storage is responsible for persistence.

Its only responsibility is to store and retrieve the Core Model.

The storage mechanism should be replaceable without affecting the rest of Atlas.

---

## Profiles

Profiles store builder preferences.

Examples include:

- preferred Views
- workspace layout
- keyboard shortcuts
- interaction preferences

Profiles personalise Atlas.

They never alter the underlying graph.

---

## Design Principles

Every architectural decision should reinforce the following principles.

- The Core Model remains independent.
- Every system has one responsibility.
- Systems communicate through the Core Model.
- Discovery observes rather than edits.
- Views interpret rather than transform.
- Publishing exports rather than owns.
- Storage persists rather than understands.

---

## Summary

Atlas is intentionally simple.

At its centre is a graph composed of Things, Attributes and Connections.

Everything else exists to help builders build, understand and share it.

The architecture should remain small enough that each part can be understood independently, while together supporting complex creative practices.
