## About this repository

This is a compilation of all my config files for different games,
originally started as a small `autoexec.cfg` for CS2.

The problem I often had is that if I want to replay or finish something,
especially something old that doesn't have Steam Cloud support,
I'd have to spend a lot of time dialing in the exact settings I want.
By the time I'm done with configuration, I'm already over it.

I didn't want to spend time configuring and re-configuring my games anymore.
This repository aims to be a one-stop place for configs and guides
for every game I'd like to (re)play.

## Installation

**You'll need `git` to do this** (you can get it [here](https://git-scm.com/)).
If you don't want to install it, download this repository,
unpack it to your home directory (`%userprofile%`) and proceed.

You'll need to set the directory where you want to store
this repository, for example, `%userprofile%\cs_config`.

Open `cmd` (`Win+R`, type `cmd`),
**preferably as an administrator to make a symlink**
and set the environment variable to access this repo:

```bat
set CFGDIR=%userprofile%\cs_config
```

Next, either clone this repo with SSH key,

```bat
git clone --recurse-submodules git@github.com:wetfloo/cs_config.git "%CFGDIR%"
```

or with HTTPS,

```bat
git clone --recurse-submodules https://github.com/wetfloo/cs_config.git "%CFGDIR%"
```

or just download it and unpack it as outlined above.

Finally, link it to your games' directory
(Windows doesn't allow regular users to make symlinks for some reason).
To do this, **check out each game's specific instructions:**
- [Counter-Strike 2](cs2cfg/README.md)
- [Counter-Strike: Source](csscfg/README.md)
- [Counter-Strike 1.6](cs1cfg/README.md)
- [Left 4 Dead 2](l4d2cfg/README.md)
- [Serious Sam Classics](ssclassics_tfe/README.md)

## Tips & tricks

### List of mouse sens for games

Below I've compiled a list of mouse sens within games I like to play.
I really like having consistency across games in this regard

| Game                           | Sensitivity | DPI    | Notes                                                                                                                |
| ------------------------------ | ----------- | ------ | -------------------------------------------------------------------------------------------------------------------- |
| Any Source/Source 2 game       | `0.25`      | `3200` | Assuming `m_pitch` and `m_yaw` are both set to 0.022 (the default value)                                             |
| Any idTech game                | `0.25`      | `3200` | Assuming `m_pitch` and `m_yaw` are both set to 0.022 (the default value)                                             |
| Serious Sam Classics (TFE/TSE) | `0.2`       | `3200` | Player sensitivity set to 50%, mouse acceleration **OFF**, smoothing **OFF**. Set using `inp_fMouseSensitivity` cvar |
| Devil Daggers                  | `0.16`      | `3200` |                                                                                                                      |
