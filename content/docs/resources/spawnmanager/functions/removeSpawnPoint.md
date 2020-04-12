---
title: removeSpawnPoint
---

## About
This export allows you to remove an existing spawnpoint from the spawnmanager.

## Name
```
removeSpawnPoint
```

## Parameters

```
int spawnIdx
```

### Required Arguments

- **spawnIdx** The index of the spawnpoint to remove.

Examples
--------

##### Lua Example:
```lua
-- Add a new spawnpoint!
-- This export returns the index of the spawnpoint just created, so we can assign it to a variable.
local spawnpoint = exports.spawnmanager:addSpawnPoint({
    x = 466.8401,
    y = 197.7201,
    z = 111.5291,
    heading = 291.71,
    model = GetHashKey('a_m_y_skater_01'),
    skipFade = false
})

-- Now let's remove it...
exports.spawnmanager:removeSpawnPoint(mySpawnPoint)
```
