# Setup Menu

## Ⅰ. Menu Title

```yaml
# The display title of inventory
Title: 'Hello, TrMenu'

# The update time of inventory's title (in ticks)
Title-Update: -1
```

```yaml
# The inventory's title
Title:
  - 'Hello TrMenu'
  - 'This are animated titles,'
  - 'You can also use variables!'
  - 'Thx for using, %player_name%!'

# The update time of inventory's title (in ticks), Default: -1
Title-Update: 40
```

## Ⅱ. Inventory Type

```yaml
Type: CHEST
```

（If this is set, the **shape** will probably not work and you have to define **slots** for each button）

**Available Inventory Type**

[https://bukkit.windit.net/javadoc/org/bukkit/event/inventory/InventoryType.html](https://bukkit.windit.net/javadoc/org/bukkit/event/inventory/InventoryType.html)

## Ⅲ. Shape \(Composing the menu\)

```yaml
# Defines the layout of this menu
# *(Each character represents a button)
Shape:
  - '########C'
  - ' QTRMENU '
  - '   SAP   '
  - '         '
  - '#########'
```

This defines the size of a chest at the same time

## Ⅳ. Open/Close Requirement & Deny Actions

```yaml
# (Optional)
Open-Requirement: 'player.hasPermission("trmenu.use")'

# (Optional)
Open-Deny-Actions:
  - 'tell: &7You need permission &ctrmenu.use &7to open this menu.'

# (Optional)
Close-Requirement: null

# (Optional)
Close-Deny-Actions: []
```

## Ⅴ. Open/Close Actions

```yaml
# (Optional) These run when a player successfully opened the menu
Open-Actions:
  - 'sound: BLOCK_CHEST_OPEN-1-2'
# (Optional)
Close-Actions:
  - 'sound: BLOCK_CHEST_CLOSE-1-2'
```

这些是打开、关闭菜单后都会执行的动作

## Ⅵ. Menu Options & Binding Open

```yaml
# Defines the commands used to open this menu
Open-Commands:
  - 'example'
  - 'menu'

# Menu Options (All are optional)
Options:
  # Automatically download PlaceholderAPI's expansions
  Depend-Expansions:
    - 'server'
    - 'player'
    - 'progress'
    - 'math'
  # (Default: true)
  Lock-Player-Inv: true
  # Use the arguments of an open command as variables (Var: {N*}) (Default: false)
  Transfer-Args: false
  # Each time when an icon updates, plugin refreshes the player's inventory
  # [!] Do not recommend. You should only enabled this when you require fast animations in lower Minecraft version
  Update-Inventory: false
  # Force the arguments it needs (Default: 0)
  Force-Transfer-Args: 0
  # Bind this menu with items have specific lore
  Bind-Item-Lore:
    - 'OPEN_MENU'
```



