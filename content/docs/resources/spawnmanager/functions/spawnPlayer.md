---
title: spawnPlayer
---

## About
This export allows you to choose specifically when or where to spawn a player. You'll most likely want to use this if you've turned off the auto-spawn flag with [setAutoSpawn](./functions/setAutoSpawn).

 Once the player has spawned, the [playerSpawned](../../events/playerSpawned) event will be triggered. 


## Name
```
spawnPlayer
```

## Parameters

```
int spawn, function callback(object spawn)
```

### Optional Arguments

 - `spawn` this can be an index spawn point from a map resource registered by [mapmanager](../../../mapmanager), or can be added with [addSpawnPoint](./functions/addSpawnPoint). Alternatively you can just use a `spawn` object. If this isn't specified, a random spawn point will be picked out of the already registered spawn points (if any).

- `callback` is executed once the player has successfully spawned and passes a `spawn` object as specified in [playerSpawned](../../events/playerSpawned).

## Examples

##### Lua Example:
```lua
-- Spawns the player at a random spawnpoint
exports.spawnmanager:spawnPlayer()
```

```lua
-- Spawns the player at a specific spawnpoint with a callback
exports.spawnmanager:spawnPlayer(1, function(spawn)
    TriggerEvent('chat:addMessage', { args = { 'You have spawned! Congrats!' } })
end)
```

Or if you don't want to use a static spawnpoint, just pass a `spawn` object.

```lua
exports.spawnmanager:spawnPlayer({
    x = 466.8401,
    y = 197.7201,
    z = 111.5291,
    heading = 291.71,
    model = GetHashKey('a_m_y_skater_01'),
    skipFade = false
}, function(spawn)
    TriggerEvent('chat:addMessage', { args = { 'You have spawned! Congrats!' } })
end)
```