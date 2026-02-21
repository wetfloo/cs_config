## CS2 installation

Find your CS2 installation directory.
For example, mine is `C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive`.

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
+exec cs2cfg/autoexec.cfg
```
