# 脚本

## 准备

为了充分发挥表达式判断的强大优势，需要安装一些相关的 PlaceholderAPI 拓展

可以在这里查询

{% embed url="https://github.com/PlaceholderAPI/PlaceholderAPI/wiki/Placeholders" %}

## Ⅰ. Action JavaScript

{% code title="单行" %}
```yaml
- 'js: player.sendMessage("&8Hello, there");'
```
{% endcode %}

{% code title="多行" %}
```yaml
- |-
  js:
  player.setVelocity(10);
  player.sendTitle("Title", "Subtitle");
```
{% endcode %}

{% code title="Functions Example 1 \[清屏\]" %}
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

{% code title="Functions Example 2 \[随机传送\]" %}
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

该类提供一些你可以在 JavaScript 脚本中调用的方法

