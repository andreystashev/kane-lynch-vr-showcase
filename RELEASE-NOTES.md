# Kane & Lynch: Dead Men VR — 0.3.61 Public Alpha

An unofficial VR conversion for the original **Kane & Lynch: Dead Men (2007)** on PC. Requires your own copy of the game; the **Steam version (App 8080)** is the primary tested edition.

## Download pending

**Installer assets are not attached yet. This draft is not a playable download.**

- **KaneLynchVR-0.3.61-Setup.exe** — recommended Windows installer, with game detection and Play/Settings shortcuts.
- **KaneLynchVR-0.3.61-Portable.zip** — extract completely into a separate writable folder, then open **KaneLynchVRSettings.cmd**.

Connect your headset, select the matching connection in Settings and choose **Save & play**. Python is not required for the mod. The original game and saved games are not included.

## Included

- Stereo rendering, positional head tracking, tracked native arms and controller-based aiming.
- Second-hand support for long guns and the original near-face sniper optic.
- VR controls for actions, reloads, grenades, weapon inventory and squad orders.
- Hand-adapted team/ammunition information, contextual action labels and optional button hints.
- Configurable laser, native reticles, cutscene presentation, turning and mounted mouse aiming.
- Meta, Virtual Desktop / VDXR and SteamVR / OpenXR connection profiles.
- A correction for the first-scene GPU-transfer loop that could cause a black screen with D3D9On12, plus independent Settings windows for separate mod folders.

Fresh installations use **DXVK**, a laser on ordinary weapons and the original mounted machine-gun crosshair. The additional handheld reticle, VR cutscenes, diagnostic logging and automatic recording are off initially. Testing cheats are hidden.

## Read before playing

**This is an early alpha.** Performance, scripted interactions, hand/body poses and some rendering effects still need work. Stutters, frame-rate drops and mission-loading crashes are possible. D3D9On12 remains experimental; an earlier loading-related GPU timeout/system crash is still under investigation.

**VR cutscenes are optional.** Scenes were authored for fixed shots and may have no animation outside the original camera view. Looking around can reveal strange or incomplete character movement. Leave **VR cutscenes** off for the original cinematic framing on a virtual screen.

**The late-game vehicle-mounted machine-gun sequence is difficult to control in VR.** Enable **Modifiers → Aim mounted guns with the mouse** to use a physical mouse while retaining the VR view.

**Co-op and multiplayer are untested and are not guaranteed to work.** Not every headset, controller or game edition has been validated. If security software blocks the launcher, stop and report the detection; it has not been established as a false positive.

See the repository's **CONTROLS.md**, **INSTALLATION.md**, **KNOWN-ISSUES.md** and **TROUBLESHOOTING.md** for the complete controls, modifiers, limitations and optional recorder setup. Feedback with a mission and reproducible steps is welcome.

This is an independent fan project, unaffiliated with the original game's owners.
