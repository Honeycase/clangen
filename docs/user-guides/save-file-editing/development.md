## Development Changes

This is a tab that ONLY goes over the specific changes development made to the save files. Refer to the cards within the [introduction](#sfe) for editing instructions beyond what's covered within this tab.

Due to the changes to the development save files, you will need to do some editing if you wish to make it a stable save again.

!!! warning
     The development version is in ACTIVE development. This could mean features change, additions get removed, save files corrupt due to a change in the files and need manual editing, etc. Do not expect a stable experience.

## clan_cats

hidden skill is no more


## clan.json

!!! tip
     clan.json is now moved to be within the clans save folder instead of being separate.

"clanname" is now `"save_id"` to make it more straightforward of what the values purpose is.

"gameplay" can now be "cruel_season" without a crash. 

`"cruel_cards": [],` the list of cards that are applied to the clan for cruel season. Card names are available in game folder > resources > cruel_season

```json
    "cruel_cards": [
        "all_apprentices",
        "always_greenleaf",
        "public_enemy",
        "mouths_to_feed"
    ],
```

For "other_clans", "name" is now `"prefix"`. The function did not change.

`"poi"` is the clan's code for their "points of interests". They have "gathering", "moonplace", and "terrian". POI names are available in game folder > resources > dicts > points_of_interest.json

```json
    "poi": {
        "gathering": [
            "gather_fourtrees",
            "gather_island"
        ],
        "moonplace": [
            "moon_cave",
            "moon_mothermouth"
        ],
        "terrain": [
            "terrain_batcaves",
            "terrain_well",
            "terrain_eaglenest",
            "terrain_fordriver",
            "terrain_rookery"
        ]
    }
```

---

## clan_cats.json

Nothing in the code actually changes except for the new appearance options. The new sick sprites are applied automatically without changing the pose code, just like before. [\[Dev Ver.\] Visual Sprite Guide](https://docs.google.com/spreadsheets/d/18T-VPGo4GJP35ECYnkzqKZThd6t8j7TwN97QspXtXY0/edit?gid=1808652489#gid=1808652489)

New eyes (doubling the eyes pool):

- Blue category: "AURORA", "SEA", "BLUEBELL", "PERIWINKLE"
- Yellow category: "DUSK", "DAWN", "MUSTARD", "EARTHY", "MAPLE", "SAND", "WILDFIRE"
- Green Category: "FOREST", "OLIVE", "CATTAIL", "GRASSYGREEN", "FERN", "LICHEN", "MOSSY", "LEAF", "AQUAMARINE", "CACTUS", "LIME"

New pelt:

- "Freckled"/"freckled"

New poses are updating sick sprites for kitten, short haired adolescent, short haired adult, and elder.

---

## freshkill_pile

Previously, you could have 4 moons of freshkill. Now it's only 3 moons. This brings back some challenge to the game, especially for larger clans.

```json
{
    "expires_in_3": 15,
    "expires_in_2": 23.0,
    "expires_in_1": 36.0
}
```

---

## history files

leader ceremonies are now formatted by life, instead of being one large paragraph of text
