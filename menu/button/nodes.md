# Nodes

## Example Button

```yaml
  'A':
    update: 20
    display:
      mats: '<head:%player_name%>'
      name:
        - '&6&lWelcome, &e&l%player_name%'
      lore:
        - - ''
          - '&7Some of your information'
          - ''
          - '&8▪ &7ID: &a%player_name%'
          - '&8▪ &7LEVEL: &3Lv.&b%player_level%'
          - '&8▪ &7FOOD: &6%player_food_level%'
          - ''
          - '&8▪ &7LOCATION: &2%player_world%, &b%player_x%/%player_y%/%player_z%'
          - ''
          - '&6&lHow about Left Click :>'
        - - ''
          - '&7Some of your information'
          - ''
          - '&8▪ &7ID: &a%player_name%'
          - '&8▪ &7LEVEL: &3Lv.&b%player_level%'
          - '&8▪ &7FOOD: &6%player_food_level%'
          - ''
          - '&8▪ &7LOCATION: &2%player_world%, &b%player_x%/%player_y%/%player_z%'
          - ''
          - '&f&lHow about Left Click :>'
      amount: '%server_online%'
    actions:
      all: ['sound: BLOCK_NOTE_BLOCK_PLING-1-2']
      left:
        - 'close'
        - 'title: <title=&a&lHello, &b&l%player_name%><subtitle=&7&lReady to fly...>'
        - 'wait: 25'
        - 'title: <subtitle=&6&l5s>'
        - 'wait: 20'
        - 'title: <subtitle=&3&l4s>'
        - 'wait: 20'
        - 'title: <subtitle=&b&l3s>'
        - 'wait: 20'
        - 'title: <subtitle=&2&l2s>'
        - 'wait: 20'
        - 'title: <subtitle=&a&l1s>'
        - 'wait: 20'
        - 'title: <subtitle=&6&lWoooooooo!>'
        - 'js: player.setVelocity(player.getVelocity().setY(15))'
        - 'js: player.setNoDamageTicks(20*10)'
    icons:
      - condition: '"%player_name%" == "Arasple"'
        display:
          name: '&2&lWelcome, &a&lAuthor!'
          lore:
            - ''
            - '&7Hello Arasple'
            - ''
```

## Ⅰ. Update/Refresh Time

```yaml
# Update for name, lore, materials and placeholders
update: 10
# Re-calculated the priority icon
refresh: 60
```

## Ⅱ. Default Icon

```yaml
display:
  mats: ...
  name: ...
  lore: ...
actions:
  all:
    - '...'
```

## Ⅲ. Priority Icons

```yaml
icons:
  # Requirement
  - condition: '"%player_name%" == "Arasple"'
    display:
      mats: ...
    actions: ...
```

{% hint style="info" %}
The properties of the display part of the priority icon are not required, inherits the default icon by default
{% endhint %}



