### bot_part_defects
```
"bot_part_defects": [
  {
      "do_not_register": True,
      "id": "unique_identifier",
      "name": "Defect name",
      "description": "Description of the defect goes here",
      "can_apply_multiple": False,
      "part_price_mult": 1.0,
      "repairable": True,
      "fix_requirements": [],
      "difficulty": 1.0,
      "disabling": False,
      "destroyed": False,
  }
]
```
- id\
Unique identifier for this part. Don't make to plain/short in order to avoid collisions with other mods.

- do_not_register - _optional_\
If set to True, the game will not load this part defect.

- name - _optional_\
The name of the defect, as it will appear in the game.

- description - _optional_\
Description of the defect, as it will appear in game.

- can_apply_multiple - _optional_\
Whether or not this defect can be applied multiple times to the same part.

- part_price_mult - _optional_\
Affects how much the _part_ price is changed when this defect is preset.

- repairable - _optional_\
Whether or not a part, on which this defect has appeard, can be repaired.

- fix_requirements - _optional_\
NOT USED

- difficulty - _optional_\
A measure of how hard this defect is to repair/remove. Affects how much experience is gained when repairing.

- disabling - _optional_\
Whether or not the presence of this defect will disable the part.

- destroyed - _optional_\
Whether or not the apperance of this defect will destroy the part.

[top](bot_part_defects.md#bot_part_defects)
