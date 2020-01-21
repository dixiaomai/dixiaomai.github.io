# Create Buttons

## Structure

* Button
  * Update Time \(lore, name, materials, placeholders etc.\)
  * Refresh Time \(priority icons\)
  * **Default Icon Display**
  * **Default Icon Actions**
  * Priority Icons
    * pIcon1
      * pIcon1's **Display Part**
      * pIcon1's **Actions Part**

## Example Button

```yaml
# Buttons of this menu
# You can re-define ones' slots
Buttons:
  # Character from 'shape'
  '#':
    # (Optional) The period for lore, materials and names to update (in ticks)
    update: 25
    # (Required) Default display part
    display:
      # Materials, or specify item
      mats: GRAY_STAINED_GLASS_PANE
      name:
        - '&3Tr&bMenu'
        - '&3TrMenu'
      lore:
        - - '&7Tr&fMenu &7by &bArasple'
          - '&7Advanced & Dynamic menus for Minecraft'
        - - '&7Tr&fMenu &7by &2Arasple'
          - '&7Thanks for using :>'
    # Click Actions
    actions:
      # ClickType - [Actions]
      all: ['sound: BLOCK_NOTE_BLOCK_PLING-1-2']
```

{% page-ref page="../button/" %}

