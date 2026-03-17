## Left 4 Dead 2 installation

Follow the [previous installation instructions.](../README.md)

Find your L4D2 installation directory.
For example, mine is
`C:\Program Files (x86)\Steam\steamapps\common\Left 4 Dead 2`.

Now, set the environment variable to match that directory:

```bat
set L4D2FOLDER=C:\Program Files (x86)\Steam\steamapps\common\Left 4 Dead 2
```

Link the repo's config directory to game's directory:

```bat
mklink /D "%L4D2FOLDER%\left4dead2\cfg\l4d2cfg" "%CSCONFIGFOLDER%\l4d2cfg"
```

Make sure to add the following to the game's launch options:

```
+exec l4d2cfg/autoexec.cfg
```

`-novid` can be used to skip the game's intro cinematics.

## Tips & tricks

### Useful commands

#### Toggle commands

There are three versions of each *toggle command*:
`on`, `off` and `toggle`. For example, for `voice_` command prefix
there are `voice_on`, `voice_off` and `voice_toggle`.

| Command              | Explanation                                             | Default value |
| -------------------- | ------------------------------------------------------- | ------------- |
| `voice_*`            | Controls voice state                                    | `off`         |
| `music_*`            | Controls music state                                    | `on`          |
| `volume_*`           | Controls master volume state                            | `on`          |

#### Other commands

| Command             | Explanation                                                              |
| ------------------- | ------------------------------------------------------------------------ |
| `valve`             | Sets network settings to be suitable for official Valve servers          |
| `comp`              | Sets network settings to be suitable for unofficial competitive servers  |
| `spec`              | Join spectators                                                          |
| `sur`               | Join survivors                                                           |
| `inf`               | Join infected                                                            |
| `reexec`            | Reload the current `autoexec.cfg`, pulling all the changes into the game |
| `practice`          | Will start a game with `sv_cheats` set to `1`, without zombies or bots   |
| `disc`              | Disconnect & reload current config                                       |
| `spraylogo`         | Spray logo                                                               |
| `flashlight_toggle` | Toggles flashlight                                                       |

### Controls

These are some important controls.
Movement is done with ESDF.

| Key      | Action                                   |
| -------- | ---------------------------------------- |
| `1`      | Primary weapon                           |
| `2`      | Secondary weapon                         |
| `4`      | Medkit, w/o quick use                    |
| `5`      | Pills/adrenaline, without quick use      |
| `MOUSE4` | Quickly use pill-adrenaline if held      |
| `x`      | Quickly use a medkit on yourself if held |
| `z`      | Quickly use a medkit on someone if held  |
| `MOUSE5` | Shove                                    |
| `MOUSE3` | `flashlight_toggle`                      |
| `c`      | Voice chat, hold to talk                 |
| `v`      | `voice_toggle`                           |
| `a`      | `spraylogo`                              |
