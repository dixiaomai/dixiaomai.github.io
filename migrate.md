# Migrate

## Supported Plugin

* DeluxeMenus

## How to migrate menus?

* To migrate menus at once, you need to copy the folder \(which contains multiple menus\) of your old menu plugin
* Drop the folder into the **plugins/TrMenu**, suppose it is called **mFolder**
* Type the command

```text
/TrMenu Migrate DeluxeMenus mFolder
```

* If everything goes well, you can find all your migrated menus in **plugins/TrMenu/migrated**
* Old menus will be renamed with the suffix **.MIGRATED**

To load the migrated menus, just copying them into the **plugins/TrMenu/menus** and use reload command

