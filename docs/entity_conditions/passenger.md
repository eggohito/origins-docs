---
title: Passenger (Entity Condition)
date: 2021-10-07
---
# Passenger

[Entity Condition](../entity_conditions.md)

Checks for the entity that's currently riding the entity.

Type ID: `origins:passenger`

### Fields

Field | Type | Default | Description
------|------|---------|-------------
`bientity_condition` | [Bi-entity Condition](../bientity_conditions.md) | _optional_ | If specified, it will check for the entity/entities that fulfills the bi-entity condition.
`comparison` | [Comparison](../data_types/comparison.md) | `">="` | How the amount of entities that is currently riding the entity should be compared to the specified value.
`compare_to` | [Integer](../data_types/integer.md) | `1` | Which value the amount of entities currently riding the entity should be compared to.