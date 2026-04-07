## Serious Sam Classics installation

Follow the [previous installation instructions.](../README.md)

Get [TFE](https://store.steampowered.com/app/41050/Serious_Sam_Classic_The_First_Encounter/)
and [TSE](https://store.steampowered.com/app/41060/Serious_Sam_Classic_The_Second_Encounter/).
Download both, so that *TFE* can be mounted to *TSE*.
Do not run the games yet!

Find your Serious Sam *TSE* installation directory.
For example, mine is
`C:\Program Files (x86)\Steam\steamapps\common\Serious Sam Classic The Second Encounter`.

Now, set the environment variable to match that directory:

```bat
set SSTSEDIR=C:\Program Files (x86)\Steam\steamapps\common\Serious Sam Classic The Second Encounter
```

The lines below will move everything from the original game's directory into our repo,
then will link the new directory as if it were game's.
No files in this repo shall be overwritten.

```bat
robocopy "%SSTSEDIR%" "%CFGDIR%\ssclassics_tfe\dump" * /E /XC /XN /XO /MOVE
rmdir /s /q "%SSTSEDIR%"
mklink /D "%SSTSEDIR%" "%CFGDIR%\ssclassics_tfe\dump"
```

Get the [Classics Patch](https://github.com/SamClassicPatch/SuperProject/releases/latest),
install it for *TSE*.

Select *Player 0* in order to use my controls and configs.
Graphics and other settings should be applied automatically.

Optionally, you might want to set `Scripts/PersistentSymbols.ini` to *Read-Only*.
