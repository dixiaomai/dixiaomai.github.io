# Random Teleport



```yaml
    actions:
      all: ['sound: BLOCK_NOTE_BLOCK_PLING-1-2']
      left:
        - 'close'
        - |-
          js:
          function randomTeleport() {
            var x = TrUtils.randomInteger(0,2500);
            var z = TrUtils.randomInteger(0,2500);
            var randomLoc = TrUtils.createLocation(player.getWorld(), x, z);
            player.teleport(randomLoc);
            player.sendTitle("&3&lRandom teleporting...", "&6X: &3" + x + "&8; &6Z: &3" + z, 20, 60, 20);
          }
          randomTeleport();
```

