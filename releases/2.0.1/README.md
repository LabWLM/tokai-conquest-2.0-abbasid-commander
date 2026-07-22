# TOKAI Conquest 2.0.1 Abbasid Critical Bugfix

**Current Release: 2.0.1**

This release package is limited to the **Abbasid 1.3** level contract.

Build ID: `TOKAI CONQUEST 2.0.1 ABBASID CRITICAL BUGFIX RELEASE`

The previous 2.0 package remains available under [`releases/2.0/`](releases/2.0/README.md).

## Improvements since 2.0

- Restores ammo-resupply and team-switch interaction handling.
- Clears out-of-bounds blackout state on death, undeploy, and redeploy so Commander mode can recover correctly after death.
- Uses team-relative colors for the Commander result and A-E objective HUD, and keeps the objective HUD in the team-scoped UI.
- Adds safer ammo-station VFX lookup and re-enables the five Abbasid ammo VFX objects for joining human players.
- Adds validity guards to kill, assist, revive, and Commander airstrike-credit event handling.
- Restores the OOB and invisible-wall event routes. Abbasid 1.3 has no applicable OOB test area, so OOB runtime behavior remains unverified in this release.

Verified in-game: startup without runtime errors, ammo resupply, team movement, the top A-E objective display, UAV, Precision Airstrike, and recovery from the death blackout back into Commander mode.

## Known issues

- Ammo-box VFX may not blink even though ammo resupply itself works normally.
- The Commander Vote UI blinks at roughly one-second intervals; in rare cases its button cannot be pressed.
- Changing class on the respawn screen can feel slightly slow.
- SFT may temporarily rise to approximately 50.
- Abbasid 1.3 has no applicable OOB area, so OOB runtime behavior has not been verified.

Vote UI, VFX, and performance improvements are in development for 2.0.2. No unfinished 2.0.2 artifact is included here.

## Portal-Script-Import

Import both files in this directory together through the Portal Script Manager:

- `tokai-conquest-2.0.1-abbasid-critical-bugfix-release.ts`
- `tokai-conquest-2.0.1-abbasid-critical-bugfix-release.Strings.json`

The TypeScript and Strings JSON are a paired import. Do not import or replace only one of them.

## Portal-Level-Upload

`Lab_MP_Abbasid_CustomConquest1.3.spatial.json` is the Portal level upload file for Abbasid 1.3.

## Level-Source

`Lab_MP_Abbasid_CustomConquest1.3.tscn` is the Godot source scene used to edit the level. It is **not** a file for direct Portal upload.

## SHA-256

| File | SHA-256 |
| --- | --- |
| `Portal-Script-Import/tokai-conquest-2.0.1-abbasid-critical-bugfix-release.ts` | `A731957423372C882595359825FD880DBF7D3DF05213A7BF9DF66305CF0DAFFF` |
| `Portal-Script-Import/tokai-conquest-2.0.1-abbasid-critical-bugfix-release.Strings.json` | `395EFDB61300BF504D0D5C5EB3C0A5BDD4FC1610922122A6E97B2F653DECE2B3` |
| `Level-Source/Lab_MP_Abbasid_CustomConquest1.3.tscn` | `55D305ACC2810AE4B250F7CE2357B6E02332A63C14555F7B84DC4BF44702E0DC` |
| `Portal-Level-Upload/Lab_MP_Abbasid_CustomConquest1.3.spatial.json` | `1D839C35905249B6687AF0C657A452E8EC2624C90CB518CA171230679992757C` |

## License and attribution

This release is distributed under the MIT License. It is based on the Custom Conquest Template TypeScript workflow maintained by PlumRice and on the original Custom Conquest visual-script concept by Andy. TOKAI Conquest and its Commander implementation were modified and implemented by LabWLM.

See `LICENSE` and `NOTICE.md` for license and attribution details.

## Unofficial project disclaimer

This is an unofficial community project. It is not an official Electronic Arts or DICE project and is not affiliated with, endorsed by, supported by, or sponsored by Electronic Arts or DICE.

Battlefield and related names, trademarks, and game assets are the property of their respective owners.
