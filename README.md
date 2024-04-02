# The Return of Custom Backpack Framework - 1.0.0

This is an update to the Custom Backpack Framework mod originally created by
Aedenthorn. I have updated it to support Stardew Valley 1.6. It is
undergoing testing and likely still has some issues with the update.

The mod allows using Content Patcher to enable multiple additional backpack
slots. A companion mod exists to add up to 72 slots of inventory.

## Requirements

* Stardew Valley 1.6
* SMAPI 4.0.0
* Generic Mod Menu (Optional)

## Features

* Allows using Content Patcher to add additional backpack upgrades
* Enables scrolling in the inventory to allow more than 3 lines
* Configurable with Generic Mod Menu
* Supports Stardew Valley 1.6

## Technical Details

You will need a Content Patcher mod to actually obtain additional backpack
slots. See **The Return of More Backpack Upgrades** for a compatible mod
which will add up to 72 slots.

You can also use the dev console to set your inventory to an arbitrary size:

```
custombackpack 60
```

Note only multiples of 12 are supported.

## Conent Patcher

If you want to make your own Content Patcher mod which adds backpack
upgrades, you will need to target the
**platinummyr.CustomBackpackFramework/dictionary**. An example is provided
here:

```
{
    "Format": "2.0.0",
    "Changes": [
        {
            "Action": "EditData",
            "Target": "platinummyr.CustomBackpackFramework/dictionary",
            "Entries": {
                "24": {
                    "name": "Large Backpack",
                    "cost": 2000,
                    "texturePath": "platinummyr.CPCustomBackpacks/backpacks",
                    "textureRect":
                    {
                        "X":0,
                        "Y":0,
                        "Width": 12,
                        "Height":14
                    }
                }
        },
        {
            "Action": "Load",
            "Target": "platinummyr.CPCustomBackpacks/backpacks",
            "FromFile": "assets/backpacks.png"
        }
    ]
}
```

## Credits

* Aedenthorn for the original mod, and for making it open source
* platinummyr for updating to Stardew Valley 1.6
