## UZDoom installation

Follow the [previous installation instructions.](../README.md)

Find your UZDoom config directory.
For example, mine is
`%userprofile%\Documents\My Games`.

Now, set the environment variable to match that directory:

```bat
set ZDOOMCFGDIR=%userprofile%\Documents\My Games
```

Link the repo's config directory to game's directory:

```bat
mklink /D "%ZDOOMCFGDIR%\UZDoom" "%CFGDIR%\zdoom\cfg"
```
