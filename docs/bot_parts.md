### bot_parts
```
# Example of a part entry
"bot_parts": [
    {
        "do_not_register": True,
        "id": "unique_identifier",
        "name": "Part name",
        "description": "description of the part goes here",
        "rate": "F",
        "price_mult": 1.0,
        "slot": "bot_arms",
        "damage_mult": 1.0,
        "possible_defects": [("scratch", 70, 100)],
        "repair_skills": [("mechanics", 100)],
        "difficulty": 1.0,
        "list_target_chances": {},
        "list_target_tag_chances": {
            "cheap": 20
        }
    }
]
```

- id\
Unique identifier of this part. Don't make to plain/short in order to avoid collisions with other mods.

- do_not_register - _optional_\
Whether or not the game should ignore/not load this part

- name - _optional_\
Name of the part, as it will be shown in the game

- description - _optional_\
Description of the part, as it will be displayed in the game

- rate - _optional_\
The rating/quality/rarity of this part. Must be one of S, A, B, C, D, E, F where S is the best and F the worst. Affects the final price of the part.\
__Make sure you enter the letter in uppercase.__ 

- price_mult - _optional_\
Affects the final price of the part.

- slot - _optional_\
The slot that this part belongs to/can be placed in. __This value should be the *id* of a part slot e.g. "bot_arms"__.\
Slots that currently exists in the game: `bot_skin`, `bot_cpu`, `bot_eyes`, `bot_vocoder`, `bot_powercore`, `bot_arms`, `bot_legs`,

- damage_mult - _optional_\
Affects how much integrity this part loses when it takes damage

- possible_defects - _optional_\
List of tuples with the following elements:
  1. defect_id - the id of a specific defect e.g. "scratch" in order to add "Scratch" as a possible defect
  2. integrity_cap - value between 0-100, the defect can only appear when the part's integrity is <= this value
  3. weight - determines how likely it is for the defect to appear once the integrity drops below the cap

- repair_skills - _optional_\
List of tuples where each entry consists of the following:
  1. skill - one of `combat`, `computers`, `electronics`, `mechanics`, `sex`, `social`
  2. weight - how much the skill contributes to the repair progress
 
 - difficulty - _optional_\
 Affects the time it takes to repair this part and the experience gained from it
 
 - list_target_chances - _optional_\
 Chances that this part will appear for specific events. Dict of event_id(?), weight pairs.\
 Weight != probability, so weight = 100 does not guarantee that the part will appear. It depends on how many other parts (and models?) are flagged for this event and their weight.

- list_target_tag_chances - _optional_\
Same as for `list_target_chances` but applies to events with a specific tag instead of specific events.\
Tags currently used in the game `all`, `cheap`, `nice`, `good`, `luxury`

[top](bot_parts.md#bot_parts)
