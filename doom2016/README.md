## Doom 2016 installation

Follow the [previous installation instructions.](../README.md)

Find your Doom 2016 save data directory.
For example, mine is
`C:\Users\alice\Saved Games\id Software\DOOM\base`.

Now, set the environment variable to match that directory:

```bat
set D2016DIR=C:\Users\alice\Saved Games\id Software\DOOM\base
```

Link the repo's config directory to game's directory:

```bat
mklink /D "%D2016DIR%\d2016cfg" "%CFGDIR%\doom2016"
```

Make sure to add the following to the game's launch options:

```
+exec d2016cfg/autoexec.cfg +r_renderAPI 1 +com_skipIntroVideo 1 +com_skipKeyPressOnLoadScreens 1
```

`+r_renderAPI 1` sets the game's render API to Vulkan.
`+com_skipIntroVideo 1` skips long intro sequence,
making the game boot much faster.
`+com_skipKeyPressOnLoadScreens 1` skips space bar taps
when the game's level is done loading.
