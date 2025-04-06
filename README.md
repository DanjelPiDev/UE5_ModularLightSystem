# UE5 Modular Light System

Developed with Unreal Engine 5

> ⚠️ This repository serves only as documentation and for example purposes.  
The full Modular Light System package (including all assets and Blueprints) is available on Epic Games FAB -> [here](https://www.fab.com/listings/5e7bcd51-0d44-4f7c-8f29-4d08cb1e7662).

> The full documentation can be found here [Wiki](https://github.com/NullPointerExcy/UE5_ModularLightSystem/wiki).

To use the system in your project, please download it directly via FAB.  
This repository may include setup guides, usage notes, update logs, and additional resources.


---

<p align="center">
  <img src="./assets/Gradient_Flicker_Lights.gif" width="400"/>
  <img src="./assets/RNG_Lights.gif" width="400"/>
</p>

<p align="center">
  <img src="./assets/Gameplay.gif" width="600"/>
</p>

A modular, dynamic, and highly customizable lighting system for Unreal Engine 5, built entirely with Blueprints.  
This system is designed for both gameplay logic and level design, allowing interactive lights, circuit behavior, and visual feedback directly in the editor.

---

## Features

- Easy-to-use Blueprint components (BP_Light, BP_LightSwitchTrigger, etc.)
- Modular setup for lights, triggers, and future power supply logic (Only None cicuit behavior is currently working)
- Flicker presets and color gradients via curves
- Cable support using Unreal's built-in Cable Component
- Spline-based light movement, Movement along axis and random movement
- Enhanced Input System support (Change the InputAction to your action, see Setup)
- Destroyable lights (optional) with trigger zones
- Interaction support for player-controlled toggling (Player has to look at the switch / light, to interact with it)

---

## How to Use

### 1. Add the Interaction Manager to the Level

Drag and drop `BP_LightInteractionManager` from
`Content/ModularLightSystem/Blueprints/Manager/` into your level.

### 2. Enhanced Input System Required

Make sure your project uses the Enhanced Input System.
You must have an input action called `IA_Use` (Or you can change it inside the Blueprint `BP_LightInteractionManager`).
![img.png](assets/img.png)

### 3. Set the Input Mapping

Open `BP_LightInteractionManager` and add your input mapping context to the Input Mapping field.
This ensures the interaction key (like `E`, `F`, etc.) works correctly.

### 4. Use Light Components

You can now use:
 - BP_Light
 - BP_LightSwitchTrigger
 - BP_LightString (`WIP`)
 - BP_PowerSupply (`WIP`)

Located under
`Content/ModularLightSystem/Blueprints/Components/`

---

## Planned Features

- [ ] Circuit behavior (series/parallel) for light strings (Only "None" is currently working)
- [ ] Energy-based gameplay integration (power limiters, voltage drop, etc.)
- [ ] More Light presets (e.g. flickering neon, broken halogen, sci-fi light pulses)
- [ ] Light Models (e.g. light bulbs, LED strips, etc.)
- [ ] Editor UI / Widget for circuit overview (Currently uses debug lines and text labels, and lines are kinda broken in UE)
- [ ] Save/Load system for light states

---

## Requirements

- Unreal Engine 5.5+
- Blueprint-only project (no C++ required)
- Tested in UE 5.5.4 and should work out of the box

---

## Project Status

This project is actively developed. The core system is functional and stable.  
Contributions, feedback and suggestions are welcome!

---

## Support

If you like this project, feel free to share it.
