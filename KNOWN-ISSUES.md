# Known issues — 0.3.61 alpha

This is an early public alpha. Testing has focused on the original Steam PC version, Quest hardware and Touch-style controllers. It is not a guarantee that every mission, edition, headset or controller works correctly.

## Cutscenes and scripted interactions

**VR cutscenes** are optional and off by default. The original scenes were authored for a fixed camera; some animations do not exist outside that shot. Looking around in VR can reveal incomplete character movement, unusual poses or other visual problems. Turn the option off to watch the original framing on a virtual cinema screen.

Some scripted actions, camera transitions and body/weapon poses can still be awkward in first person. Menu and cutscene behavior may vary between sequences.

## Mounted machine guns

The vehicle-mounted machine-gun sequence near the end of the campaign is especially difficult to control in VR. Controller aiming and right-stick adjustment remain rough, particularly while the vehicle turns.

Enable **Modifiers → Aim mounted guns with the mouse** to use the game's mouse aiming while retaining the VR view. Restart after changing the option. This is an alternative way to play the sequence, not a complete fix for its VR controls.

## Performance and loading

- Performance is still uneven. Frame-rate drops and stutters vary by scene, renderer, resolution, graphics settings and headset connection.
- The game renders the two eye views on alternating game frames. An external overlay's frame rate is not necessarily the rate of fresh stereo pairs reaching the headset.
- D3D9On12 is experimental. A loading-related GPU timeout/system crash has been reported and remains under investigation. DXVK is the recommended starting choice; Original is another alternative.
- Mission-loading crashes remain possible, including the original 32-bit game's address-space limits. This release does not fix every loading failure.
- A first-scene GPU-transfer loop that could leave the installed mod on a black screen has been corrected and retested with VDXR. This does not establish that every black screen or loading crash has the same cause.

## Rendering and compatibility

- Some reflections, effects and body/weapon poses still show artifacts. An intermittent grey weapon silhouette near the Japanese-garden entrance and a reflective floor section on the Tokyo streets need more scene-specific testing.
- Meta, Virtual Desktop / VDXR and SteamVR connection paths have been exercised, but testing across different devices is limited. A first-start stale-image issue was observed with SteamVR; later runs delivered fresh frames.
- Security software may block the launcher. If it does, stop and report the detection name, affected file and mod version. Detections have not been established as false positives. See [troubleshooting](TROUBLESHOOTING.md#security-software-blocks-a-file).
- Co-op and multiplayer have not been tested and are not guaranteed to work.

See [troubleshooting](TROUBLESHOOTING.md) for startup checks and optional diagnostic logging. Reproducible reports with a mission and exact steps are especially helpful.
