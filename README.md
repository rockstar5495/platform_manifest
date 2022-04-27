<p align="center">
  <img src="https://i.imgur.com/lyJkVeK.png"/>
</p>

We aim to bring a more consistent, fluent and smooth experience with all your must-have customizations, for you, for the community, and for everyone.

# Build guide

Prior to building, you will need basic knowledge of [Git](https://www.atlassian.com/git/tutorials/atlassian-git-cheatsheet).

### Requirements
- Around 100G disk space.
- A computer with at least 16GB RAM running Linux (recommended) or MacOS.
- Build environment [setup](https://github.com/akhilnarang/scripts). 

### Instructions
1. Run the following commands to sync source

```
repo init -u https://github.com/rockstar5495/platform_manifest -b 12.1
```
2. To sync source, enter

```
 repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)
```

3. Once the source is downloaded/synced, prepare your device trees, dependencies and start the build by the following commands

```
   source build/envsetup.sh
   lunch awaken_<devicecodename>-userdebug
   make bacon -j$(nproc --all)
```

### Compilation Help
To get help with build errors, please visit [**Android Building Help**](https://t.me/AndroidBuildingHelp).
