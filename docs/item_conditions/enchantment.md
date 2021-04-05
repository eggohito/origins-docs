---
title: Enchantment (Condition)
date: 2021-04-05
---
# Enchantment

[Item Condition](../item_conditions.md).

Checks the level of a certain enchantment on the item.

Type ID: `origins:enchantment`

### Fields:

Field  | Type | Default | Description
-------|------|---------|-------------
`enchantment` | [String](../data_types/string.md) | |  _ID of the enchantment of interest, e.g. `minecraft:protection`._
`comparison` | [Comparison](../data_types/comparison.md) | |  _How to compare the enchantment level the specified value._
`compare_to` | [Integer](../data_types/integer.md) | | _Which value to compare the enchantment level against._