---
title: Action On Callback (Power Type)
date: 2021-04-04
---
# Action On Callback

[Power Type](../power_types.md).

Can execute an entity action on the player at certain times: when the power is chosen (gained through becoming the origin), when the player respawns, when the player loses the power (i.e. becomes another origin).

Type ID: `origins:action_on_callback`

### Fields

Field  | Type | Default | Description
-------|------|---------|-------------
`entity_action_chosen` | [Entity Action](../entity_actions.md) | _optional_ | If set, this action will be executed on the player when the power is gained.
`execute_chosen_when_orb` | [Boolean](../data_types/boolean.md) | true | When this is false, the `entity_action_chosen` will not be executed when the player changes their origin with an orb, but only when the player chooses an origin for the first time or their origin was reset to `origins:empty` via a command.
`entity_action_lost` | [Entity Action](../entity_actions.md) | _optional_ | If set, this action will be executed on the player when the power is lost.
`entity_action_added` | [Entity Action](../entity_actions.md) | _optional_ | If set, this action will be executed on the player when the power is added.
`entity_action_removed` | [Entity Action](../entity_actions.md) | _optional_ | If set, this action will be executed on the player when the power is removed.
`entity_action_respawned` | [Entity Action](../entity_actions.md) | _optional_ | If set, this action will be executed on the player right after the player respawns.

### Example

```json
{
  	"type": "origins:action_on_callback",
  	"entity_action_chosen": {
    	"type": "origins:execute_command",
    	"command": "team join TheNetherBoys @s",
    	"permission_level": 4
  	},
  	"entity_action_removed": {
    	"type": "origins:execute_command",
    	"command": "team leave @s",
    	"permission_level": 4
  	},
  	"execute_chosen_when_orb": true
}
```
Players will automatically join the team called "TheNetherBoys" when they choose an origin with this power, and will leave the team if they change their origin to another one (which doesn't have this power). Note that in order for this to work, the team must exist beforehand.