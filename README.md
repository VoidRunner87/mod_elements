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

# Creating and Adding Skins to a Player

This project already have the nqdef files. All you need is adding the skin to the player.

Below is how you would extend this to create more skins.

* Create an nqdef that is a skin. Ie:

```json
{
    "elements": {
        "SpaceEngineXtraSmall_Epstein": {
            "inherit": "SpaceEngineXtraSmall",
            "node": "resources_generated/mods/com.github.VoidRunner87.mod_elements/spaceengine_xs_blue/env_engine-space-blue_001_xs.node",
            "icon": "resources_generated/elements/engines/engine-space-military_001_xs/icons/env_engine-space-military_001_xs_icon.png"
        }
    }
}
```
The file above reads as:
* `Epstein` skin name for `SpaceEngineXtraSmall` inherits all properties except `node` and `icon` from `SpaceEngineXtraSmall`

Then add the skin to the player:

* Find the number id of the element
* ![image](https://github.com/user-attachments/assets/f4388c68-02ee-4181-879a-1c3b43471729)
* Use that to set the skin
* ![image](https://github.com/user-attachments/assets/428a9c8a-a6ae-4ed5-888b-fa7491d3de23)


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
