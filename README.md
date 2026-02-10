## Installation for CS2

### Windows

**You'll need `git` to do this** (you can get it [here](https://git-scm.com/)). If you don't want to install it, download this repository, unpack it to your home directory (`%userprofile%`) and proceed.

Find your CS installation directory.
For example, mine is `C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive`.
Additionally, you'll need to set the directory where you want to store this repository, for example, `%userprofile%\cs_config`.

Open `cmd` (`Win+R`, type `cmd`), and set the environment variables:

```bat
set CSGOFOLDER=C:\Program Files (x86)\Steam\steamapps\common\Counter-Strike Global Offensive
set CSGOCONFIGFOLDER=%userprofile%\cs_config
```

Next, either clone this repo with SSH key,

```bat
git clone git@github.com:wetfloo/cs_config.git "%CSGOCONFIGFOLDER%"
```

or with HTTPS,

```bat
git clone https://github.com/wetfloo/cs_config.git "%CSGOCONFIGFOLDER%"
```

or just download it and unpack it as outlined above.

Finally, link it to your game's directory:

```bat
mklink /H "%CSGOFOLDER%\game\csgo\cfg\autoexec.cfg" "%CSGOCONFIGFOLDER%\cs2\autoexec.cfg"
```

Make sure to add the following to the game's launch options:

```
+exec autoexec.cfg
```

You're set!
