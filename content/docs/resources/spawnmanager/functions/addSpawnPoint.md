---
title: addSpawnPoint
---

## About
This export allows you to add a spawn point to the spawnmanager and returns an index for that spawnpoint.

## Name
```
addSpawnPoint
```

## Parameters

```
object spawn
```

### Required Arguments

- **spawn**: An object containing the following information:
    - **(float) x**: The x coordinate of where the player will be spawned.
    - **(float) y**: The y coordinate of where the player will be spawned.
    - **(float) z**: The z coordinate of where the player will be spawned.
    - **(float) heading**: The heading that the player is facing when spawned.
    - **(Hash) model**: The ped model hash the player will spawn as.
    - **(bool) skipFade**: Whether to skip the fade in and out when spawning.

Examples
--------

##### Lua Example:
```lua
-- This export returns the index of the spawnpoint just created, so we can assign it to a variable.
local spawnpoint = exports.spawnmanager:addSpawnPoint({
    x = 466.8401,
    y = 197.7201,
    z = 111.5291,
    heading = 291.71,
    model = GetHashKey('a_m_y_skater_01'),
    skipFade = false
})

exports.spawnmanager:spawnPlayer(spawnpoint)
```
