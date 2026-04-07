## Devil Daggers installation

Follow the [previous installation instructions.](../README.md)

Find your Devil Daggers configuration file directory.
On Windows, it's
`%APPDATA%\Devil Daggers`.

Now, set the environment variable to match that directory:

```bat
set DDCFGDIR=%APPDATA%\DevilDaggers
```

Overwrite the existing config by removing the old one first,
and then linking the new one:

```bat
del "%DDCFGDIR%\config"
mklink "%DDCFGDIR%\config" "%CFGDIR%\DevilDaggers\config"
```
