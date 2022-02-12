### base mod structure

```
{
  "mod_id": "unique_identifier",
  "mod_description": "description of the mod goes here",
  "mod_priority": 0,
  
  "asset_packs": [],
  "dscs_tunings": {},
  "name_tables": {
    "example_name_table": [
      "Anna",
      "Beth"
    ]
  },
  
  "bot_part_defects": []
  "bot_part_slots": []
  "bot_parts": []
  "bot_models": [],
}
```
- mod_id\
Unique identifier for this mod. Will cause a collision if two mods have the same identifier so don't make it to plain.
- mod_description - _optional_\
Short description of what the mod does/adds. Is displayed in-game under "Game Mods".
- mod_priority - _optional_\
Is used to determine the load order of all installed mods. In case of a collision, the mod with the highest priority is the one that will be loaded. __Defaults to 0__
- asset_packs - _optional_\
Tells the game where to look for assets, basically a mapping.\
Entries should be on the following format `("bots example_bot", "mybot")`\
[more info here](asset_packs.md)

- dscs_tunings - _optional_\
Fine tune certain aspects of the game\
[more info here](dscs_tunings.md)

- name_tables - _optional_\
Here you can add your own name tables. The dict key will be the table id and the value should be a list of possible names.\
When adding name variants to a model, it's the key/table id that you should use.

- bot_part_defects - _optional_\
Part defect definitions goes here\
[more info here](bot_part_defects.md)

- bot_part_slots - _optional_\
Part slot definitions goes here\
[more info here](bot_part_slots.md)

- bot_parts - _optional_\
Part definitions goes here\
[more info here](bot_parts.md)

- bot_models - _optional_\
Model definitions goes here\
[more info here](bot_models.md)
