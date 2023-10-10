---
sidebar_label: 'Test'
sidebar_position: 12
---

# Test

Innermost symbols on line connecting entities represents the minimum
(either zero or one).

Outermost symbols on line connecting entities represents the minimum
(either one or many).

### Cardinality: Zero or One

```mermaid
%%{init: {'er': {'layoutDirection': 'LR'}}}%%
erDiagram
    A |o--o| B : ""
```

An occurrence of A is related to zero or one occurences of B (and vice versa).

### Cardinality: Exactly One

```mermaid
%%{init: {'er': {'layoutDirection': 'LR'}}}%%
erDiagram
    A ||--|| B : ""
```

An occurrence of A is related to one and only one occurence of B (and vice versa).

### Cardinality: Zero or More

```mermaid
%%{init: {'er': {'layoutDirection': 'LR'}}}%%
erDiagram
    A }o--o{ B : ""
```

An occurrence of A is related to zero or more occurences of B (and vice versa).

### Cardinality: One or More

```mermaid
%%{init: {'er': {'layoutDirection': 'LR'}}}%%
erDiagram
    A }|--|{ B : ""
```

An occurrence of A is related to zero or more occurences of B (and vice versa).

### Cardinality: Other

```mermaid
%%{init: {'er': {'layoutDirection': 'LR'}}}%%
erDiagram
    A }o--|| B : ""
```

An occurrence of A is related to exactly one occurence of B.

An occurrence of B is related to zero or more occurences of A.

```mermaid
%%{init: {'er': {'layoutDirection': 'LR'}}}%%
erDiagram
    A |o--|| B : ""
```

```mermaid
%%{init: {'er': {'layoutDirection': 'LR'}}}%%
erDiagram
    A }o--|{ B : ""
```
