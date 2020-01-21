# Create Menu

## Method Ⅰ. Create menu in the menu folder

* Go into the folder **plugins/TrMenu/menus**，create a yaml file
* The filename is the menu's id

{% hint style="info" %}
You can create multiple subdirectories under menu folder, which allows you to manage menus well when they're a lot of them
{% endhint %}

## Method Ⅱ. Custom path load

Add your custom menu file's path in **settings.yml**

```yaml
MENU-FILES:
  - 'plugins/XXX/zzz.yml'
```

## Method Ⅲ. Internal Menus

Create your custom menu inside **settings.yml**

```yaml
MENUS:
  - internalMenu:
      title: 'Internal Menu in settings.yml'
      shape:
        - '#########'
        - '    |    '
        - '#########'
      buttons:
        '#':
          display:
            mats: green stained glass pane
        '|':
          display:
            mats: apple
            name: '&6Nice to meet you~'
```

