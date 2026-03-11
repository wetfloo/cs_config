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
| `MOUSE3` | Flashlight                               |
| `c`      | Voice chat, hold to talk                 |
| `v`      | Voice chat toggle, by default it's off   |
| `a`      | Spray                                    |

### Useful commands

| Command | Explanation                                                             |
| ------- | ----------------------------------------------------------------------- |
| `valve` | Sets network settings to be suitable for official Valve servers         |
| `comp`  | Sets network settings to be suitable for unofficial competitive servers |
| `spec`  | Join spectators                                                         |
| `sur`   | Join survivors                                                          |
| `inf`   | Join infected                                                           |

### Ex-commands

**Ex-commands** are a special type of commands
that basically alias to executable config files.
These commands are intended to make file execution easier,
without needing to type of the full path.

| Command       | Explanation                                                              |
| ------------- | ------------------------------------------------------------------------ |
| `reexec`      | Reload the current `autoexec.cfg`, pulling all the changes into the game |
| `ex_practice` | Will start a game with `sv_cheats` set to `1`, without zombies or bots   |
