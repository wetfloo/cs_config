## CS 1.6 installation

Find your CS 1.6 installation directory.
For example, mine is `C:\Program Files (x86)\Steam\steamapps\common\Half-Life\cstrike`.

Now, set the environment variable to match that directory:

```bat
set CS1FOLDER=C:\Program Files (x86)\Steam\steamapps\common\Half-Life\cstrike```

Link the repo's config directory to game's directory:

```bat
mklink /D "%CS1FOLDER%\cs1cfg" "%CSCONFIGFOLDER%\cs1cfg"
```

Make sure to add the following to the game's launch options:

```
+exec cs1cfg/autoexec.cfg
```
