---
title: Dimension
date: 2021-04-04
---
# Dimension

[Entity Condition](../entity_conditions.md).

Checks whether the player is in a specified dimension.

Type ID: `origins:dimension`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`dimension` | [Identifier](../data_types/identifier.md) | |  _ID of the dimension the player needs to be in for this condition to evaluate to true. Vanilla dimensions are `minecraft:overworld`, `minecraft:the_nether` and `minecraft:the_end`, but IDs of custom/modded dimensions should also work._