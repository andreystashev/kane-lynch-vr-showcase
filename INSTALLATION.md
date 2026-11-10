# Installation

## Requirements

- Windows 10/11, 64-bit, and a PC capable of running PC VR.
- Your own installed copy of the original **Kane & Lynch: Dead Men** on PC.
- A connected PC VR headset, tracked controllers and the matching PC VR software.
- A compatible graphics driver. DXVK also requires Vulkan support.

**The Steam version (App 8080) is the primary tested edition.** Some other verified game builds are accepted, but compatibility with every edition is not guaranteed. Co-op and multiplayer have not been tested.

## Windows installer

1. Download and run **KaneLynchVR-0.3.61-Setup.exe** from the project's Releases page.
2. Confirm the detected **kaneandlynch.exe**, or browse to your game's executable.
3. Choose a separate writable folder for the mod. The default installation does not require administrator rights. Do not select the game folder or another mod's folder.
4. Connect the headset and start its PC VR software.
5. Open **Kane & Lynch Dead Men VR Settings**, select the matching headset connection, then choose **Save & play**.

The **Play** shortcut uses saved settings. The **Settings** shortcut opens the configuration window. Steam libraries on other drives are detected automatically. The launcher starts Steam when required; finish any Steam sign-in or update prompt before playing.

## Headset connection

| Setup | Connection to select |
|---|---|
| Quest Link or Air Link through Meta's PC application | Meta |
| Virtual Desktop through its Streamer and VDXR | Virtual Desktop / VDXR |
| A headset connected through SteamVR | SteamVR |
| Another installed OpenXR runtime | OpenXR |

Automatic detection is available, but choose an explicit connection if several runtimes are installed. Leave **OpenXR runtime JSON (optional)** blank unless you intentionally use a custom runtime. The mod's connection selection does not replace Windows' global OpenXR registration.

Testing has focused on Quest hardware and Touch-style controllers. Meta, VDXR and SteamVR connection paths are included; other headsets and controller layouts may need further work.

## Renderer and graphics

**DXVK** is the fresh-install default. **Original** uses the game's Direct3D 9 renderer; **DXVK** translates it to Vulkan. **D3D9On12** translates it to Direct3D 12 and supports GPU frame transfer to the VR host. These choices normally preserve the game's visual style; they can differ in performance and compatibility.

All three renderers use the GPU to render the game. D3D9On12 can also avoid the CPU image-transfer path used by the other two modes. This does not guarantee a higher frame rate on every PC.

**D3D9On12 remains experimental:** a loading-related GPU timeout/system crash has been reported and is still under investigation. Use DXVK or Original if you encounter this problem.

Change the game's resolution and graphics settings **inside the game**. Start with a moderate resolution and increase it gradually; high settings can cause frame-rate drops or stutters. There is no universal performance preset for every headset and PC.

The launcher manages its selected renderer files using ownership checks. An unrelated renderer DLL is preserved and reported. The installer does not replace the original game executable, xlive.dll or saved games.

## Modifiers and movement

Use **Modifiers** for VR cutscenes, laser and aiming graphics, mounted mouse aiming, game-action hints and VR button hints. Use **Movement** for turning and stick settings. See [controls and settings](CONTROLS.md#modifiers) for the complete list.

VR cutscenes, logging and automatic recording are off initially. The ordinary laser and original mounted-gun crosshair are on; the extra handheld reticle is off.

## Portable ZIP

Extract the complete **KaneLynchVR-0.3.61-Portable.zip** into a separate writable folder. Open **KaneLynchVRSettings.cmd**, select the local game and connection, then choose **Save & play**. Keep the package files together; do not copy them over the game's original files.

If you move the mod to another PC, use **Find game** or browse to that PC's executable again. Distributed settings contain no personal game or runtime path. A game installed on a different drive may need a full path selected on that PC.

## Update and uninstall

Close the game and mod settings before updating, then run the newer Setup. The installer preserves ordinary preferences, recordings and unknown personal files. When relocating an installation, verified old mod files are cleaned only after the new installation is complete.

Use Windows **Installed Apps** or the included uninstaller to remove an installed copy. Personal settings and recordings can remain. Close all components before deleting a portable copy, and keep any recordings you want.

Python is not required for installation, VR, sound or controller input. Only the [optional recorder](TROUBLESHOOTING.md#optional-recording) needs Python and recording dependencies.
