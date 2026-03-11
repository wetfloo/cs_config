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
mklink /D "%L4D2FOLDER%\left4dead2\cfg" "%CSCONFIGFOLDER%\l4d2cfg"
```

Make sure to add the following to the game's launch options:

```
+exec l4d2cfg/autoexec.cfg
```
