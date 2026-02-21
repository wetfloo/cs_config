## Installation

**You'll need `git` to do this** (you can get it [here](https://git-scm.com/)). If you don't want to install it, download this repository, unpack it to your home directory (`%userprofile%`) and proceed.

You'll need to set the directory where you want to store this repository, for example, `%userprofile%\cs_config`.

Open `cmd` (`Win+R`, type `cmd`), **preferably as an administrator to make a symlink** and set the environment variable to access this repo:

```bat
set CSCONFIGFOLDER=%userprofile%\cs_config
```

Next, either clone this repo with SSH key,

```bat
git clone git@github.com:wetfloo/cs_config.git "%CSCONFIGFOLDER%"
```

or with HTTPS,

```bat
git clone https://github.com/wetfloo/cs_config.git "%CSCONFIGFOLDER%"
```

or just download it and unpack it as outlined above.

Finally, link it to your games' directory (Windows doesn't allow regular users to make symlinks for some reason). To do this, **check out each game's specific instructions:**
- (Counter-Strike 2)[docs/CS2.md]
- (Counter-Strike 1.6)[docs/CS1.md]
