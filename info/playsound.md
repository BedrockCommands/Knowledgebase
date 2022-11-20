# Playsound

## Introduction

Introduced in version `1.0.5`. Using the `/playsound` command you can play sound effects to players anywhere in the world at any time.

## Syntax
```mcfunction
playsound <sound> [player] [position] [volume] [pitch] [minimumVolume]
```

## Defenitions

ㅤ- `sound`  is the sound effect to start playing. You can find the list of sound effects currently available at:
https://www.digminecraft.com/lists/sound_list_pe.php

ㅤ- `player` is optional. It refers to the player selectors `@a`, `@r` & `@p` , you may also use their gamertag.

ㅤ- `position` is optional. It refers to the `x y z` position from where the sound will be played.

ㅤ- `volume` is optional. It determines the size of the sphere in which the sound effect can be heard. `0.0` is the minimum size.  Sound & audible sphere size increases as value entered for `volume`  increases.

ㅤ- `pitch` is optional. It determines the pitch for the sound effect. It can be a value between `0.0` and `256`. The higher the value, the higher the pitch. Values less than or equal to `0.0` makes the sound inaudible.

ㅤ- `minimumVolume` is optional. It determines the minimum volume at which the sound will be heard outside of the audible sphere. It can be a value between `0.0` and `1.0` 

ㅤ
## Examples

```mcfunction
# Play a random explosion sound to closest player.
playsound random.explode @p
```
```mcfunction
# Execute upon all players at relative coordinates Play a random orb sound to self at relative coordinates with a volume of 10000
execute @a ~~~ playsound random.orb @s ~~~ 10000
```

- The second command example shown here can be used in a situation where you might want to play sound to players immediately after teleporting them as otherwise it won't play the sound without including the `execute` before the command.

- Increase the `volume` if you're teleporting them to a really far distance.
