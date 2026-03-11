## CS2 installation

Follow the [previous installation instructions.](../README.md)

Find your CS2 installation directory.
For example, mine is
`C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive`.

Now, set the environment variable to match that directory:

```bat
set CS2FOLDER=C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive
```

Link the repo's config directory to game's directory:

```bat
mklink /D "%CS2FOLDER%\game\csgo\cfg\cs2cfg" "%CSCONFIGFOLDER%\cs2cfg"
```

Make sure to add the following to the game's launch options:

```
+exec cs2cfg/autoexec.cfg -allow_third_party_software
```

`-allow_third_party_software` here supposedly allows
for OBS, RTSS, and other software to access the game.

`-autoconfig` can be used to reset the game's configuration to defaults.
Beware, this will also reset your graphics settings,
which are not controllable via cvars.

## Tips and tricks

### Quick buy

All the binds below are mapped to the numpad, unless specified otherwise.

| Key                         | Buy                                              |
| --------------------------- | ------------------------------------------------ |
| `1`                         | Default rifle (M4A4/AK47)                        |
| `2`                         | AWP                                              |
| `3`                         | Force buy rifle (FAMAS/Galil AR)                 |
| `4`                         | Force buy SMG (MP9/MAC-10)                       |
| `6`                         | Desert Eagle                                     |
| `7`                         | Five-SeveN/Tec-9                                 |
| `8`                         | Smoke + Flashbang                                |
| `9`                         | Smoke, HE, Molotov, Flashbang x2 (in that order) |
| `0`                         | Defuse kits                                      |
| `-`                         | Kevlar vest, **no helmet**                       |
| `+`                         | Kevlar vest, **with helmet**                     |
| `F3` (**not a numpad key**) | Autobuy (controlled by `cl_autobuy`, *modified*) |
| `DEL`(**not a numpad key**) | Sell back all (that's possible to sell)          |

### Desubtick toggle

`ex_desub_off` will **disable desubtick** for movement,
while `ex_desub_on` will enable it,
supposedly improving the movement consistency.
Desubticking is disabled by default,
aligning with the default configuration of CS2.

### Lineup crosshair

By default, `q` toggles radar zoom; however, when holding down
**left** and/or **right** mouse button(s) with a grenade equipped,
you can press `q` to toggle lineup crosshair.
This crosshair will only be active
until you release the buttons mentioned above.

### Quick-drop the bomb

Press `j` to drop the bomb and notify your teammates with a text message.
Dropping the bomb in this manner will switch you back to your knife.

### Local practice

`END` will restart the server with a special practice config.
`p` allows you to toggle nocli*p*, and `\` will clear any thrown utility.
