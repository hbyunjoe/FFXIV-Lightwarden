# Installing Lightwarden

[← Back to the README](README.md)

This guide assumes a clean install of FFXIV. If you're installing on top of an existing setup (other ReShade presets, other mods, whatever you have), please use your best judgement, and check the [conflicts](README.md#conflicts) first.

## Before you start

- Check the [requirements](README.md#requirements).
- Remove anything listed under [conflicts](README.md#conflicts), such as REST, KeepUI or BetterShadows.

## 1. Install the game and XIVLauncher

1. Install the game as usual.
2. Install [XIVLauncher](https://goatcorp.github.io/), which comes with Dalamud, and log in through it once so Dalamud sets itself up.

<!-- Screenshot: XIVLauncher -->

## 2. Install ReShade with add-on support

1. Download ReShade **with full add-on support** from [reshade.me](https://reshade.me).
2. Run the installer and pick `ffxiv_dx11.exe` in the game folder.
3. Choose **DirectX 10/11/12**.
4. You don't need any of the effect packs it offers, so you can skip that page.

<!-- Screenshot: the ReShade installer -->

## 3. Copy Lightwarden's ReShade files

1. Copy `Lightwarden.addon64` into the game folder, next to `ffxiv_dx11.exe`.
2. Copy all the `.fx` files into ReShade's `reshade-shaders\Shaders` folder.

<!-- Screenshot: where each file goes -->

## 4. Change the game's graphics settings

Start the game, open System Configuration, and in the graphics settings change these:

- **Shadow Softening: Weak or Strong.** Avoid Strongest. Strongest does use a form of PCSS, but the game draws lower-resolution shadow maps at that setting for some reason.
- **Ambient Occlusion: GTAO.** By default Lightwarden uses its own visibility-bitmask AO, which is better, but there's a slider to mix in the game's GTAO for certain scenes. (Mixing AO is always a bad idea, though.)
- **Depth of Field: on.** Don't worry, the depth of field won't be doubled. Lightwarden needs the game's own depth of field switched on so it can read its focus values.

<!-- Screenshot: the graphics settings -->

## 5. Install the Dalamud plugin

1. Open Dalamud's settings with `/xlsettings`, go to **Experimental**, add this repository's URL under custom plugin repositories, and save.
2. Open the plugin installer with `/xlplugins`, search for **Lightwarden** and install it.

<!-- The repository URL goes here once there's a release -->
<!-- Screenshot: the custom repository setting -->

## 6. Restart the game

ReShade only loads add-ons when the game starts, so restart once after installing. The first start after installing takes longer while the shaders compile.

## 7. Pick a preset

Open Lightwarden's window and choose a preset from the dropdown at the top: **Default**, or **Lighter** if your frame rate needs it.

## Optional: OptiScaler, for HDR, DLAA, DLSS upscaling and frame generation

<!-- Coming later: installing the OptiScaler fork, and where NVIDIA's files come from -->
