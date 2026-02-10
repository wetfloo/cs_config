## Installation for CS2

### Windows

**You'll need `git` to do this** (you can get it [here](https://git-scm.com/)). If you don't want to install it, download this repository, unpack it to your home directory (`%userprofile%`) and proceed.

Get your CS installation directory.
For example, mine is `C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive`.

Open `cmd` (`Win+R`, type `cmd`), and type

```bat
set CSGOFOLDER="C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive"
```

Next, either clone this repo with SSH key

```bat
git clone git@github.com:wetfloo/cs_config.git %userprofile%\cs_config
```

Or with HTTPS

```bat
git clone https://github.com/wetfloo/cs_config.git %userprofile%\cs_config
```

Finally, link it to your game's directory

```bat
mklink /H "%CSGOFOLDER%\game\csgo\cfg\autoexec.cfg" "%userprofile%\cs_config\autoexec.cfg"
```

Make sure to add the following to the game's launch options

```
+exec autoexec.cfg
```

You're set!
