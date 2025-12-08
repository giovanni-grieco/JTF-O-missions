# JTF Orange missions repository
Put missions PBOs in this repository.

# Naming Convention

## Rationale
The reason we do this is for mission maintance and for tracking in which period a certain mission was made in.
If from one version of the modpack to the next, we only add mods, no biggie. If we remove something then it's a problem because potentially a mission file depended from a mod we removed.
By appending modpack versions to the mission file we know what mission can potentially be broken when we change modpack (and version number).

## Where is the Modpack Version?
Check the modpack version in the [Modpack Change Log](https://discord.com/channels/722878134785015879/1329823560281227356) discord channel


## How to name mission files
If the modpack version number is X then the filemission follows the following format
```
your_mission_file_name_vX.map_name.pbo
```

For example, if X is 1.2.3, your mission file name should be
```
cool_op_name_v1.2.3.cool_map_name.pbo
```

if you want to version your own file mission... don't just reupload the file as is with the same name, GIT already provides versioning and you can always recover an old version. Feel free to overwrite using the same names.

## How to change a mission file after fixing/checking said mission file
If we have progressed with a major version number of the modpack (for example from V1 to V2) then we need to check all of those missions that have the major version number lower than the one of the modpack (so all those mission file with "_v1.y.z" because 1<2)

After you've made sure that a certain mission file works with the new modpack, simply rename the file to follow the same format
```
old_mission_v1.2.3.cool_map_name.pbo -> old_mission_but_has_been_checked_v2.cool_map_name.pbo
```
