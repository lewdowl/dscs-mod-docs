[index](../README.md#index)
### bot_part_slots
```
"bot_part_slots": [
    {
        "id": "bot_legs",
        "name": "Legs",
        "list_priority": 6,
        "category_price_mult": 1,
        "slot_tags": [],
        "beauty_weight": 10,
        "event_damage": {
            "training_combat": 50,
        }
    }
]
```
- id\
Unique identifier for this slot. Don't make to plain/short in order to avoid collisions with other mods.

- list_priority\
Used to determine the placement of this slot when in a inside of a collection of other slots e.g. when viewing the _Chassi_ of a bot.\
It's usually ok for multiple slots to have the same `list_priority`, but it has been noted to cause issues when using 1 and 3 (the values used by `bot_cpu` and `bot_powercore` respectively) when slot_tags is not defined.

- name - _optional_\
The name of the slot, as it will appear in the game.

- category_price_mult - _optional_\
Affects the price of parts that have their `slot` property set to the id of this slot.

- beauty_weight - _optional_

- event_damage - _optional_\
Affects how much damage parts using this slot id should take when the specified event triggers.\
Each entry consist of a event, weight pair.


[index](../README.md#index) [top](#bot_part_slots)
