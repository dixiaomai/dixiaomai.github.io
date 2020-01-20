# Expression \(Requirement\)

The priority icons are filtered and viewed by their condition

Expressions can use variables from PlaceholderAPI and arguments from the menu open command, the compile result must be boolean

## Examples

> "%player\_name%" == "Arasple"       Return true when "%player\_name%" equals "Arasple"
>
> player.hasPermission\("test"\)          Return true when the player has permission "test"

```yaml
- condition: '"%player_name%" == "Arasple"'
```

{% page-ref page="../../../actions/functional-actions/javascript.md" %}



