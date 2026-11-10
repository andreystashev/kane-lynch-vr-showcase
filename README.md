# Kane & Lynch: Dead Men VR — Public Alpha

**[Download 0.3.61 — Windows installer](https://github.com/andreystashev/kane-lynch-vr-showcase/releases/download/v0.3.61/KaneLynchVR-0.3.61-Setup.exe)** · [Portable ZIP](https://github.com/andreystashev/kane-lynch-vr-showcase/releases/download/v0.3.61/KaneLynchVR-0.3.61-Portable.zip) · [All releases](https://github.com/andreystashev/kane-lynch-vr-showcase/releases)

An unofficial VR mod for the original **Kane & Lynch: Dead Men (2007)** on PC, with stereo rendering, positional head tracking, motion-controller aiming and tracked native arms.

This is an **early public alpha** for playing the original campaign in VR. Shooting, cover, squad orders, inventory, missions and progression use the original game's systems, with adapted controls and presentation. Performance, scripted sequences and some interactions still need work.

You need your own copy of the original PC game. **The Steam version (App 8080) is the primary tested edition.** No game executable, game assets or saved games are included. This is an independent fan project, unaffiliated with the original game's owners.

## What the mod adds

- First-person stereo views and head tracking, including physical head movement for looking around cover.
- Controller-driven arms and weapon aiming, with second-hand support for long guns.
- The sniper rifle's original scope, activated by bringing the right controller near your face.
- Controller access to actions, reloads, grenades, weapon selection and squad commands.
- A hand-adapted team/ammunition display, contextual action labels and optional control hints.
- Optional laser and native aiming graphics, including the original mounted machine-gun crosshair.
- Optional VR cutscenes, with the original cinematic framing on a virtual screen as the default.
- Headset audio routing and a separate optional gameplay recorder.

## Install and play

1. Install the original game and connect your PC VR headset.
2. Run **KaneLynchVR-0.3.61-Setup.exe**, confirm the detected game executable and choose a separate folder for the mod.
3. Open **Kane & Lynch Dead Men VR Settings**, select your headset connection and choose **Save & play**.

The default installation does not require administrator rights or Python. The Play shortcut uses your saved settings. A Portable ZIP is available if you prefer to extract the complete mod into a writable folder.

[Installation](INSTALLATION.md) · [Controller controls](CONTROLS.md) · [Troubleshooting and recording](TROUBLESHOOTING.md) · [Known issues](KNOWN-ISSUES.md)

## Settings and modifiers

The **Modifiers** page lets you choose VR cutscenes, laser and aiming graphics, optional mouse aiming for mounted guns, and separate game-action and VR-control hints. The **Movement** page provides smooth/snap turning, turn speed, snap angle and stick deadzone.

Fresh installations use **DXVK**. **Original** and experimental **D3D9On12** are also available. Results vary by scene and PC; see the [renderer notes](INSTALLATION.md#renderer-and-graphics).

By default, ordinary weapons use **only the laser sight**; the additional native reticle is off. Mounted machine guns retain the original crosshair. VR cutscenes, diagnostic logs and automatic recording are off. Contextual game-action hints are on; extra VR button hints are optional.

## Alpha limitations

- **VR cutscenes can look strange.** Original shots were made for a fixed camera, and animation may be missing outside that shot. Looking around can reveal incomplete or unnatural character movement. Leave **VR cutscenes** off to watch the original framing on a cinema screen.
- **The vehicle-mounted machine-gun sequence near the end of the game is difficult to control in VR.** Controller aiming and right-stick adjustment remain rough. Enable **Aim mounted guns with the mouse** in Modifiers to aim with a physical mouse while keeping the VR view.
- **Performance and stability are still uneven.** Expect scene-dependent frame-rate drops, stutters and possible loading crashes. D3D9On12 has an unresolved report of a loading-related GPU timeout/system crash; DXVK or Original are alternatives.
- Some body/weapon poses, reflections and effects can still show visual artifacts. Not every mission, headset or controller has been validated.
- **Co-op and multiplayer have not been tested and are not guaranteed to work.**

Meta Quest Link / Air Link, Virtual Desktop / VDXR and SteamVR / OpenXR connection profiles are included. Testing has focused on Quest hardware and Touch-style controllers; support for other setups needs more feedback.

## Feedback

Please report reproducible problems in [Issues](https://github.com/andreystashev/kane-lynch-vr-showcase/issues), including the mod version, mission, renderer, connection, headset and steps to reproduce the problem. State whether it affects the game window, the headset or both.

Logs are optional: enable **Diagnostics → Enable diagnostic logs**, restart the game, reproduce the issue and run **Collect-KL1-Diagnostics.cmd**. Turn logging off again afterward. See [troubleshooting](TROUBLESHOOTING.md) before sharing diagnostic files.

[Third-party notices](THIRD-PARTY-NOTICES.md) and license texts accompany the download.
