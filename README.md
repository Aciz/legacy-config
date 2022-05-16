# Aciz's ETL configs

![2022-05-16-233818-goldrush](https://user-images.githubusercontent.com/14221121/168679044-96e7b54c-ea42-47dd-bb0c-a85a7cd3cfdd.png)


This repository contains my [ET: Legacy](https://www.etlegacy.com/) config files. This includes my standard `autoexec.cfg`, map-specific autoexec configs with spawnpoints setup for each map along with `r_mapOverBrightBits` setting and my custom HUD. The map autoexecs include original 6 maps, most of the competitive map pool and whatever happens to be in rotation at [TeamMuppet ETLegacy](https://et.trackbase.net/server/45410) server (and I've bothered to make config for), where I mostly play.

The configs are updated for
* ET: Legacy engine **2.80.2**
* Legacy mod **2.80.2**

## Usage
This config is only contains settings which are adjusted from default. **Any cvar not included in `autoexec.cfg` is meant to be at it's default setting.** The only exception to this is binds, the config contains `unbindall` command at the start, and then sets all default bindings + whatever I have personally adjusted from defaults.

Along with spawnpoints, map-specific configs contain per-map `r_mapOverBrightBits` setting. Since the cvar is latched, I have bound `vid_restart` to `KP_DEL`, and simply hit that at the start of each map, to apply the correct setting.

## Installation
* Download the repository as ZIP or clone with `git clone git@github.com:Aciz/legacy-config.git`
* Backup your `etconfig.cfg` in `fs_homepath/legacy/profiles/yourprofile/etconfig.cfg`
  * If you already have `autoexec.cfg` and `hud.dat`, backup these as well
  * Backup is recommended as starting point for this config is default settings
* Move the config files found in this repository's `legacy` folder to your homepath's `legacy` folder
* Reset your cvars, exec the `autoexec.cfg` and do `vid_restart`
  * `com_hunkMegs` requires restarting the game to apply
```
cvar_restart; exec autoexec; vid_restart
```

---

## Binds and scripts
Here's a brief overview of the custom binds and scripts I have in the config.

### Class binds
Class binds are bound to numpad. Following table visualizes the binds in numpad.

```
-------------------------------------
|     7     |     8     |     9     |
|           |           |           |
| Medic     | Engineer  | Engineer  |
|           | SMG       | Rifle     |
------------------------------------
|     4     |     5     |     6     |
|           |           |           |
| Field Ops | Cvops     | Cvops     |
|           | Sten      | Sniper    |
-------------------------------------
|     1     |     2     |     3     |
|           |           |           |
| Soldier   | Soldier   | Cvops     |
| Panzer    | MG42      | FG42      |
-------------------------------------
```

### Spawntimer binds
Spawntimer binds are bound to arrow keys Following table visualizes the binds in arrow keys.

```
            -------------
            |     ^     |            
            |           |            
            | Unload    |            
            |           |            
-------------------------------------
|     <     |     v     |     >     |
|           |           |           |
| Check     | Set       | Share     |
|           |           |           |
-------------------------------------
```

Explanation of the actions:
* Unload = turns off spawntimer
* Check = prints current spawntimes to console
* Set = sets spawntimer
* Share = executes `sharetimer` command

### Other scripts and binds

* `F5` - executes `autoexec.cfg`
* `INS` - set Axis spawnpoint
* `HOME` - default spawnpoint for both teams
* `PGUP` - set Allied spawnpoint
* `DEL` - toggle borderless fullscreen / windowed mode
  * Note: I have a 2560x1440 monitor, and the windowed mode is set to `r_mode 16` (1920x1080). If you have 1920x1080 screen or lower, you might wanna adjust this to `r_mode 12` (1366x768) for example.
* `KP_SLASH` - toggle `cg_drawGun 1/2`
* `KP_INS` - toggle `r_mapOverBrightBis 1/2`
  * doesn't execute `vid_restart`
* `KP_DEL` - executes `vid_restart`
