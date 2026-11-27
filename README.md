# Lightwarden

A graphics overhaul for Final Fantasy XIV. Lightwarden replaces and extends parts of the game's rendering to give it a more modern look, in the spirit of what ENB did for Skyrim, without replacing the game's textures or models.

**Status: in development. There is no public download yet.**

## What it does

- **Lighting:** softer and more accurate sun and lamp shadows, bounce light, and lamps that actually light the rooms they're in
- **Atmosphere:** volumetric fog and light shafts, ground mist that moves round you, volumetric clouds, darker nights
- **Water:** real reflections, waves that follow the weather and wind, wakes and ripples
- **Characters:** better skin, eyes and hair shading, foot inverse kinematics, and lip sync that follows the voice lines
- **Weather:** its own falling snow, wet surfaces and puddles, wind through grass and trees
- **Camera:** a film-style tonemap with HDR output, depth of field that follows the game's cutscenes, bloom, lens effects and motion blur
- **Presets:** save, share and switch between complete looks

## How it's built

Lightwarden has three parts that work together:

1. **A ReShade add-on:** the engine. It changes how the game draws the world.
2. **ReShade effects:** the camera and film: tonemap, bloom, colour grade, lens and depth of field.
3. **A Dalamud plugin:** the control panel. It holds every setting and tells the other two what is happening in the game.

## Requirements (planned)

- Final Fantasy XIV on Windows, launched with XIVLauncher and Dalamud
- ReShade with full add-on support
- Optional, for HDR output and frame generation: OptiScaler

Install instructions will be added with the first release.

## Disclaimer

Lightwarden is an unofficial, fan-made project. It is not affiliated with or endorsed by Square Enix. Third-party tools are against the game's terms of service; use it at your own risk. It changes only how the game looks on your own screen.
