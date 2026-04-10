## CS2 installation

Follow the [previous installation instructions.](../README.md)

Find your CS2 installation directory.
For example, mine is
`C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive`.

Now, set the environment variable to match that directory:

```bat
set CS2DIR=C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive
```

Link the repo's config directory to game's directory:

```bat
mklink /D "%CS2DIR%\game\csgo\cfg\cs2cfg" "%CFGDIR%\cs2cfg"
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

### Useful commands

#### Toggle commands

There are three versions of each *toggle command*:
`on`, `off` and `toggle`. For example, for `voice_` command prefix
there are `voice_on`, `voice_off` and `voice_toggle`.

| Command              | Explanation                                                        | Default value |
| -------------------- | ------------------------------------------------------------------ | ------------- |
| `voice_*`            | Controls voice state                                               | `off`         |
| `music_*`            | Controls music state                                               | `on`          |
| `volume_*`           | Controls master volume state                                       | `on`          |
| `sndbg_*`            | Controls if the game will continue playing sound when not in focus | `on`          |
| `crosshair_recoil_*` | Controls if the crosshair should follow recoil or not              | `off`         |
| `crosshair_util_*`   | Lineup crosshair. [Explanation](<#lineup-crosshair>)               | `off`         |
| `desub_*`            | Performs de-subticking                                             | `off`         |

#### Other commands

Just your normal everyday commands that you might want to consider.

| Command         | Explanation                                                                    |
| --------------- | ------------------------------------------------------------------------------ |
| `reexec`        | Reload the current `autoexec.cfg`, pulling all the changes into the game       |
| `disc`          | Disconnect & reload current config                                             |
| `practice`      | Restart the server with `sv_cheats` set to `true`, and other helpful settings  |
| `clear_util`    | Removes all the utility from the map                                           |
| `crosshair_big` | Makes your crosshair big, useful for screenshots                               |

#### Knife spawns

Below is the list of commands that spawn knives.
The names of commands are pretty much self-explanatory.

- `knife_spawn_bayonet`
- `knife_spawn_classic`
- `knife_spawn_flip`
- `knife_spawn_gut`
- `knife_spawn_karambit`
- `knife_spawn_m9`
- `knife_spawn_huntsman`
- `knife_spawn_falchion`
- `knife_spawn_bowie`
- `knife_spawn_butterfly`
- `knife_spawn_shadowdaggers`
- `knife_spawn_paracord`
- `knife_spawn_survival`
- `knife_spawn_ursus`
- `knife_spawn_navaja`
- `knife_spawn_nomad`
- `knife_spawn_stiletto`
- `knife_spawn_talon`
- `knife_spawn_default`
- `knife_spawn_skeleton`

#### Fun commands

Some commands to have fun with on a local server.

| Command            | Explanation                                              |
| ------------------ | -------------------------------------------------------- |
| `fun_blocks`       | Allows you to build using blocks, just like in Minecraft |
| `fun_car`          | Spawns a driveable car                                   |
| `fun_dancing_prop` | Spawns dancing furniture                                 |
| `fun_decoy`        | Turns decoys into explosive rockets                      |
| `fun_robot`        | Spawns a robot that can be either friendly or hostile    |

### Quick buy

All the binds below are mapped to the numpad, unless specified otherwise.

| Key                         | Buy                                              |
| --------------------------- | ------------------------------------------------ |
| `1`                         | Default rifle (M4A4/AK47)                        |
| `2`                         | Force buy rifle (FAMAS/Galil AR)                 |
| `3`                         | Force buy SMG (MP9/MAC-10)                       |
| `9`                         | Smoke, HE, Molotov, Flashbang x2 (in that order) |
| `0`                         | Defuse kits                                      |
| `-`                         | Kevlar vest, **no helmet**                       |
| `+`                         | Kevlar vest, **with helmet**                     |
| `F3` (**not a numpad key**) | Autobuy (controlled by `cl_autobuy`, *modified*) |
| `DEL`(**not a numpad key**) | Sell back all (that's possible to sell)          |

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

`p` allows you to toggle `noclip`, and `\` will perform `clear_util`.
