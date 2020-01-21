# JavaScript

## Aliases

* JS
* SCRIPT
* SCRIPTS
* JAVASCRIPT
* JAVASCRIPTS

## Example

```
JS: player.sendMessage("Hello, " + player.getName())
```

## Objects

* player
* bukkitServer \(  =  Bukkit.getServer\(\)
* clickEvent
* clickType
* clickItemStack

## Example

```yaml
'B':
    update: 40
    display:
      mats:
      - 'apple'
      - 'beef'
      - 'cookie'
    actions:
      all:
      - 'js: bukkitServer.dispatchCommand(bukkitServer.getConsoleSender(), "give %player_name% " + clickItemStack.getType().name());'
```



## Learn more

{% page-ref page="../../requirement-and-javascript/javascript.md" %}



