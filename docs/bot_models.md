[index](../README.md#index)
### bot_models
```
"bot_models": [
    {
        "model_id": "unique_identifier",
        "model_name": "Name of the model",
        "model_description": "description of the model goes here",
        "name_variants": "european_names",
        "gender": "female",
        "rate": "D",
        "price_mult": 1.0,
        "psychocore_stability_decay_mult": 0.5,
        "part_damage_mult": 0.5,
        "default_traits": [
        ],
        "default_parts": {
            "cpu": "quadx",
            "powercore": "nova",
        },
        "list_target_chances": {
        },
        "list_target_tag_chances": {
            "all": 50,
        },
        "generate_bot_mind_table": "default",
    }
]
```
- model_id\
Unique identifier for this model. Don't make to plain/short in order to avoid collisions with other mods.

- default_parts\
The slots that this model comes with and the default parts within those slots. 
Each entry consists of a slot_id, part_id pair.\
In order for the game to be able to load the model, there must be an entry consisting of a slot_id that refers to a slot tagged with `cpu` and one that is tagged with `powercore` (see example above). A single entry can also be used, as long as the slot it refers to is tagged with both.

- model_name - _optional_\
The name of the model, as it will appear in the game. Not to be confused with the name of a bot.

- model_description - _optional_\
The description of the model, as it will appear in the game.

- name_variants - _optional_\
A name_table_id ([see mod doc](mod.md)) or a list of names. When a bot of this model is generated, its name will be randomly selected from this table.

- gender - _optional\
`male` or `female`

- rate - _optional_\
The rating/quality/rarity of this model. Must be one of S, A, B, C, D, E, F where S is the best and F the worst. Affects the final price of the model.\
__Make sure you enter the letter in uppercase.__

- price_mult - _optional_\
Affects the final price of the model.

- psychocore_stability_decay_mult - _optional_\
Affects how quickly the stability of a bot of this model decays when it gains experience.

- part_damage_mult - _optional_\
Affects how much integrity the different parts equipped on a bot of this model loses when they take damage.

- default_traits - _optional_\
Traits that bots of this model will always have upon generation.\
Traits currently in the game `tech_smart_inherent`, `tech_smart`, `sex_smart`, `sex_smart_inherent`.

 - list_target_chances - _optional_\
 Chances that this model will appear for specific events. Dict of event_id(?), weight pairs.\
 Weight != probability, so weight = 100 does not guarantee that the part will appear. It depends on how many other models (and parts?) are flagged for this event and their weight.

- list_target_tag_chances - _optional_\
Same as for `list_target_chances` but applies to events with a specific tag instead of specific events.\
Tags currently used in the game `all`, `cheap`, `nice`, `good`, `luxury`

- generate_bot_mind_table - _optional_\
Determines how much experience a bot of this model will have in each skill upon generation. Can be set to `default`, which will allow for the event triggering the generation to determine the starting experience in each skill.\
If not `default`, it can be set to a list of entries of the following format: `[skill_id, (min_xp, max_xp)]` where `skill_id` must be one of the possible skills prefixed with **bot_** e.g. `bot_combat`. The `min_xp` and `max_xp` makes up a range from which the starting experience for the specified skill will be randomized. `min_xp` can be set to a negative value, which allows for the possibility that the generated bot doesn't have any experience in that skill.

[index](../README.md#index) [top](#bot_models)
