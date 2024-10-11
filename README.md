# MyDU Elements Mod

You need git LFS to download this repo.

![image](https://github.com/user-attachments/assets/eae9b10e-6a42-4dd0-be7c-f7d18ee366c4)

![image](https://github.com/user-attachments/assets/6b1df5d1-fa98-4fcf-8d83-18a2b968bda7)

# How does it work?

```mermaid
graph TD
    nodeFile --> materialFile
    materialFile --> albedoTexture[albedo tex<br/><br/>the colors of the texture]
    materialFile --> normalTexture[normal tex<br/><br/>normal map=RGB=XYZ texture]
    materialFile --> mraoTexture[mrao tex<br/><br/>metalness=R, roughness=G, ambient occlusion=B texture]
    materialFile --> emissionTexture[emission value<br/><br/>texture black=0 white=1 on the red channel]
    materialFile --> emissionValue[emission value<br/><br/>bright spots scale]
    nodeFile --> pkfx
    nqDef --> nodeFile
    nqDef --> icon
    pkfx[pkfx<br/><br/><i>binary file</i>] --> diffurerampTexture[diffuseramp<br/><br/>engine plume texture]
```

# Disclaimer

This mod needs to copy a texture file to `vfxs/textures/` folder. However it does not override ANY existing files.

The mod adds a skin called "Epstein" to engines. You still need to go in the BO and add that skin to players.

## Install Client Side

Use the [mod manager](https://github.com/VoidRunner87/mydu_mod_manager)

* Grab a [release](../../releases) version and extract on `<MYDU_CLIENT>/mods-cache`
* Open the mod manager, refresh and install it

## Install Server Side

* Add the mod to the manifest of the server. See the mod_manager for how to.

## Roadmap

* More elements
