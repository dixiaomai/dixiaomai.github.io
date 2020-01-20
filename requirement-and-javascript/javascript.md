# JavaScript

## Get Ready

Expressions always require a lot of PlaceholderAPI variables in order to fulfill powerful features 

So you'd better download the Cloud Expansions you need.

The link below is where you can find the variables

{% embed url="https://github.com/PlaceholderAPI/PlaceholderAPI/wiki/Placeholders" %}

## Ⅰ. Action JavaScript

{% code title="Single line" %}
```yaml
- 'js: player.sendMessage("&8Hello, there");'
```
{% endcode %}

{% code title="Multiple lines" %}
```yaml
- |-
  js:
  player.setVelocity(10);
  player.sendTitle("Title", "Subtitle");
```
{% endcode %}

{% code title="Functions Example 1 \[ScreenClean\]" %}
```yaml
- |-
  js:
  function cleanScreen(){
    for (var i=0; i<100; i++){
      player.sendMessage("");
    }
    player.sendMessage("&aDone");
  }
  cleanScreen();
```
{% endcode %}

{% code title="Functions Example 2 \[RandomTeleport\]" %}
```yaml
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
{% endcode %}

## TrUtils

This is a class where you can call many methods in JavaScript

{% page-ref page="../api/trutils.md" %}

