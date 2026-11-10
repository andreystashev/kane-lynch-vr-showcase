# Troubleshooting and optional recording

## Game or VR output does not start

Confirm the selected **kaneandlynch.exe** and headset connection in Settings. Connect the headset through the matching PC application first. If several runtimes are installed, choose the explicit Meta, VDXR or SteamVR connection instead of Automatic. Leave the optional OpenXR runtime JSON blank unless you use a custom runtime.

Steam editions need the original game installation and a working Steam client. Finish any Steam sign-in or update prompt, then try again. If Setup rejects the game's executable, report the edition and the displayed compatibility information; do not replace the game's EXE or xlive.dll to force it through the check.

Keep the game window focused while playing. **F9** toggles the headset output; **F7** recenters the view.

## Black screen, loading crash or poor performance

Try a fresh launch with **DXVK**, the recommended default, or **Original**. D3D9On12 remains experimental and has an unresolved report of a loading-related GPU timeout/system crash. A different renderer can be a useful alternative, but it does not resolve every possible cause.

Lower the game's resolution and graphics settings for comparison. Test the same mission and scene so the results are useful. An overlay's frame counter may not represent fresh stereo pairs; menus are not representative of gameplay performance.

The original 32-bit game's address-space limit can still cause mission-loading failures. Include the mission, renderer and whether the desktop game continues responding in a report.

## Cutscenes look wrong

Turn off **Modifiers → VR cutscenes** and restart to watch the original cinematic framing on a virtual screen. The original game may have no animation outside its intended camera shot, so freely looking around an adapted sequence can reveal unusual or incomplete poses.

## Vehicle-mounted gun is too difficult to aim

Enable **Modifiers → Aim mounted guns with the mouse**, restart and aim with a physical mouse while wearing the headset. This replaces controller aiming for mounted guns and keeps the VR view active. The late-game vehicle sequence remains a known rough area.

## Sound plays on both the headset and speakers

Check the audio-mirroring setting in your PC VR software. For SteamVR, check its audio output/mirroring options. The mod routes game sound to the selected headset connection, but runtime mirroring can also send it to desktop speakers.

## Security software blocks a file

Stop and report the file name, detection name, mod version and SHA256 details. Detections affecting the launcher have not been established as false positives. Do not assume that any download carrying the mod's name is trustworthy; compare its checksum with the official release.

## Diagnostic logs

Logs are off during normal play. Enable **Settings → Diagnostics → Enable diagnostic logs**, restart the game and reproduce the issue. Run **Collect-KL1-Diagnostics.cmd** from the mod folder to prepare a support archive. Turn the checkbox off again afterward.

Include the mod version, mission, renderer, headset connection, headset/controller model, graphics settings and exact steps. State whether the problem appears in the game window, the headset or both. Review the archive before sharing it: diagnostics can contain local paths and crash information.

## Optional recording

Recording does not start automatically. VR itself does not require Python. To use the recorder, install **Python 3**, **FFmpeg** and these Python packages:

```powershell
python -m pip install SoundCard NumPy
```

Make FFmpeg available through PATH. A compatible FFmpeg already installed with Virtual Desktop Streamer can also be detected. NVIDIA NVENC is used when available; software encoding requires an FFmpeg build with libx264 and can reduce game performance.

Start the game, then run **Record-KaneLynch-VR.cmd** from the same mod folder once. While playing:

| Hotkey | Action |
|---|---|
| Ctrl+F10 | Start a new recording |
| Ctrl+F11 | Stop and save the clip; keep the hotkey handler available |
| Ctrl+F12 | Save any active clip and exit the hotkey handler |

Clips are saved in **recordings**. A clip continues in one file through menus and loading screens; if source frames temporarily stop, the recorder holds the last frame while time and audio continue. It records playback audio, not the microphone. Nothing is recorded before you start a clip.

If another mod's recorder already owns these hotkeys, exit that handler before starting this one. Wait for saving to finish before closing the recorder process.
