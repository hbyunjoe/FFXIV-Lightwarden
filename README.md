# Lightwarden

A graphics overhaul for Final Fantasy XIV. Lightwarden replaces and extends parts of the game's rendering to give it a more modern look, in the spirit of what ENB did for Skyrim, without replacing the game's textures or models.

**Status: in development. There is no public download yet.**

## What it does

- **Lighting:** soft sun and lamp shadows that sharpen near contact (PCSS, contact shadows), ambient occlusion (visibility bitmask), bounce light (screen-space global illumination with probe-based lamp bounce), and lamps that actually light the rooms they're in (baked shadows for every lamp, light from glowing scenery)
- **Atmosphere:** volumetric fog and light shafts (froxel-based), ground mist that moves round you, volumetric clouds, dust motes in the light, darker nights
- **Water:** planar and screen-space reflections, waves that follow the weather and wind, wakes, ripples and caustics
- **Characters:** skin with subsurface scattering (Burley diffusion) and light through thin parts like ears, eye shading, softer hair shadows, foot inverse kinematics, and lip sync that follows the voice lines (baked with NVIDIA Audio2Face)
- **Weather:** its own falling snow, wet surfaces and puddles, snow on surfaces, wind through grass and trees
- **Camera:** a choice of tonemappers (AgX, GT7, an ACES fit, film LUTs) with auto exposure and HDR10 output, a physically based lens flare that follows the aperture, depth of field that follows the game's cutscenes, bloom, halation, diffusion, chromatic aberration, lens dirt, film grain and motion blur
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

## Techniques and references

Lightwarden's code is its own, but it stands on published work. The main ones:

- **Tonemapping:** AgX (Troy Sobotka; Blender 4's version), the Gran Turismo 7 tonemapper (Polyphony Digital, 2025)
- **Soft shadows:** Percentage-Closer Soft Shadows (Fernando, 2005)
- **Ambient occlusion and bounce light:** Screen Space Indirect Lighting with Visibility Bitmask (Therrien et al., 2023); Dynamic Diffuse Global Illumination (Majercik et al., 2019); ReSTIR (Bitterli et al., 2020); SVGF (Schied et al., 2017)
- **Skin:** Burley's normalized diffusion for subsurface scattering (Burley, 2015)
- **Lens flare:** Physically-Based Real-Time Lens Flare Rendering (Hullin et al., 2011); Practical Real-Time Lens-Flare Rendering (Lee and Eisemann, 2013)
- **Motion blur:** A Fast and Stable Feature-Aware Motion Blur Filter (Guertin et al., 2014); Next Generation Post Processing in Call of Duty: Advanced Warfare (Jimenez, 2014)
- **Lip sync:** NVIDIA Audio2Face

A full list of papers and talks, and the licence notices for third-party code, will come with the first release.

## Disclaimer

Lightwarden is an unofficial, fan-made project. It is not affiliated with or endorsed by Square Enix. Third-party tools are against the game's terms of service; use it at your own risk. It changes only how the game looks on your own screen.
