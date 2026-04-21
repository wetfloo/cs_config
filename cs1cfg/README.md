## CS 1.6 installation

Follow the [previous installation instructions.](../README.md)

Find your CS 1.6 installation directory.
For example, mine is
`C:\Program Files (x86)\Steam\steamapps\common\Half-Life\cstrike`.

Now, set the environment variable to match that directory:

```bat
set CS1DIR=C:\Program Files (x86)\Steam\steamapps\common\Half-Life\cstrike
```

Link the repo's config directory to game's directory:

```bat
mklink /D "%CS1DIR%\cs1cfg" "%CFGDIR%\cs1cfg"
```

Make sure to add the following to the game's launch options
(some options here added to play 4:3 stretched correctly):

```
+exec cs1cfg/autoexec.cfg -gl -full -stretchaspect
```
