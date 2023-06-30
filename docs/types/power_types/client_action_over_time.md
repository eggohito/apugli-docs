---
title: Client Action Over Time (Power Type)
date: 2023-06-30
---

#   Client Action Over Time

[Power Type](../power_types.md).

Executes an action on the client-side of the entity that has the power within a certain interval.

Type ID: `apugli:client_action_over_time`


### Fields

Field | Type | Default | Description
------|------|---------|------------
`entity_action` | [Entity Action](../entity_action_types.md) | _optional_ | The action to execute on the entity that has the power each interval.
`rising_action` | [Entity Action](../entity_action_types.md) | _optional_ | The action to execute on the first interval tick in which the condition became true.
`falling_action` | [Entity Action](../entity_action_types.md) | _optional_ | The action to execute on the first interval tick in which the condition became false.
`interval` | [Integer](https://origins.readthedocs.io/en/latest/types/data_types/integer) | `20` | Interval of ticks between subsequent executions of the specified actions. Must be a value of at least 1.


### Examples

```json
{
    "type": "apugli:client_action_over_time",
    "entity_action": {
        "type": "apoli:add_velocity",
        "space": "local_horizontal_normalized",
        "z": 3
    },
    "interval": 100
}
```

This example will add horizontal velocity to the entity on the Z axis on the client-side.
