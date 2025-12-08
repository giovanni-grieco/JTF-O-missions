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
your_mission_file_name_v<X>.map_name.pbo
```

For example, if X is "1.2.3", your mission file name should be
```
cool_op_name_v1.2.3.cool_map_name.pbo
```

Sometimes X can have special instances. For example, if we're running an experimental modpack, X could look like "V0.1_experimental". This means that you need to follow the rule as before, just use the whole string.
```
cool_op_name_v0.1_experimental.cool_map_name.pbo
```

## I have multiple versions of a certain mission file... what do I do?
if you want to version your own file mission... don't just reupload the file as is with the same name, GIT already provides versioning and you can always recover an old version. Feel free to overwrite using the same names.

But if you really need to have multiple mission file in the repo, feel free to append your own version to the name.

The format should be
```
cool_op_name_v<X>_<your_own_version_number>.cool_map_name.pbo
```

If we assume that X is still "1.2.3" and your_own_version_number is "5" then
```
cool_op_name_v1.2.3_5.cool_map_name.pbo
```

## How to change a mission file after fixing/checking said mission file
If we have progressed with a major version number of the modpack (for example from V1 to V2) then we need to check all of those missions that have the major version number lower than the one of the modpack (so all those mission file with "_v1.y.z" because 1<2)

After you've made sure that a certain mission file works with the new modpack, simply rename the file to follow the same format
```
old_mission_v1.2.3.cool_map_name.pbo -> old_mission_but_has_been_checked_v2.cool_map_name.pbo
```
