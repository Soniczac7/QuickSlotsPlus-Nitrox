
# QuickSlots+

> [!Note]
> This is a fork of the original mod made by [celvro](https://github.com/celvro), this is not an actively maintained repo but does contain changes to allow this mod to work on Nitrox without proper controller support.
>
> The mod may not work as expected while attempting to use a controller on this fork nor have I tested using a controller, but if you want to use keyboard and mouse from my testing it has worked perfectly.
>
> A release of the built files for this mod is avaliable in [releases](https://github.com/Soniczac7/QuickSlotsPlus-Nitrox/releases/latest).
>
> If an update is released to the original mod fixing this issue, I highly recommend using that version instead as this repo will not be maintained.

A C# mod for Subnautica to add more slots.

## Features

* Up to 20 slots with hotkeys
* Disable adding new items to the quick slots
* Custom hotkey labels
* Works with Nitrox

> [!Warning]
> Switched from SMLHelper to Nautilus, make sure to update.

## Requirements

* [BepInEx](https://www.nexusmods.com/subnautica/mods/1108)
* [Nautilus](https://www.nexusmods.com/subnautica/mods/1262) (formerly SMLHelper)

## Installation

1. Install BepInEx and the Nautilus plugin.
1. Extract `BepInEx\` folder from downloaded QuickSlotsPlus.zip into your Subnautica folder.

## Build from source

1. Install Visual Studio or use msbuild.
1. Create the publicized assemblies using https://github.com/elliotttate/Bepinex-Tools/releases
1. Change the $(GameDir) property in the .csproj file if needed, it defaults to Steam directory on C: drive.
1. In VS select Build -> Build Solution, it will copy the files into your BepInEx folder.
1. Launch Subnautica.

## Controller Support

Now supports Controller icons on hotbar!

## Nitrox

Manually edit Nautilus's `BepInEx\plugins\Modding Helper\mod.json` file and add `"NitroxCompat": true`.

Warning: Did not test this after the switch from SMLHelper to Nautilus.

### Add custom labels

1. Set hotkey in game, look at name.
2. Create a file named `BepInEx\plugins\QuickSlotsPlus\customLabels.json`. Limited support for unicode.
```json
{
    "LeftArrow": "⬅️",
    "RightArrow": "Right"
}
```
3. I've already added some [default custom labels](https://github.com/celvro/QuickSlotsPlus/blob/fe41a7685674630b3e1b4fba457562b3d6f3bd66/Utility/LabelUtil.cs#L112). 
You can override them with the KeyCode name.

## Known issues

* Can't use CTRL or ALT modifiers for hotkeys
* Sometimes while testing Nitrox my equipped tool icon disappeared

## Changes

### 2.0 (Nautilus update)

* Updated from SMLHelper to Nautilus
* Fixed display of controller icons for slot labels

[Noticed a bug?](https://github.com/celvro/QuickSlotsPlus/issues)
