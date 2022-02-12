### asset_packs
```
"asset_packs": [
  ("bots example_bot", "bots mybot"),
  ("bots best_bot", "subdir bots myunqiuebot")
]
```

THE FOLLOWING INFORMATION IS ONLY VALID WHEN IT COMES TO LOADING BOT IMAGES

The _asset_pack_ property tells the game where it should look for assets.
Each entry consists of two string, the first of which is very simple. It follows the following format `"bots bot_model_id"`.
So if you have created a model definition and given it the id "awesome_bot" the first string should be `"bots awesome_bot"`

The second string is indepented of model id but instead depend on where you've placed your image files (note that all images sould be placed under an asset folder).
In general, the string should consist of the relative path of your image folder w.r.t its assets folder ancestor, with all path seperators replaced by whitespace.

So, if your images are located in `mods/mymod/assets/mybot/` the string should simply be `"mybot"`. Note that the folder _mymod_ is not part of the string since it is not part of the relative path of _mybot_ w.r.t _assets_.

If you instead had your images in `mods/assets/mymod/mybot` the _mymod_ folder becomes part of the final string `"mymod mybot"`.\
For a longer path `mods/mod_name/assets/bots/combatants/group_a/bot/` the string sould be `"bots combatants group_a bot"`

There is one exception to the relative path rule, and that is when folders named images are present.\
For `mods/mod_name/assets/images/bots/bot/` the string should be `"bots bot"` in order to load properly, even though _images_ is part of the relative path.\
`mods/mod_name/assets/images/images/bots/bot` should also be `"bots bot"` while `mods/mod_name/assets/images/bots/images/bot` should be `"bost images bot"`

As is hopefully apparent from these examples, _images_ can (and should) only be ignored if it is placed in a continuous chain of _images_ folders directly beneath _assets_. 
