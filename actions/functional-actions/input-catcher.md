---
description: It's a functional action that reacts to the player's input
---

# Input Catcher

## Aliases

* CATCH
* CATCHER

## Example

```yaml
- |-
  Catcher:
   <Type=CHAT>
   <Before=Tell: &3&lPlease type a value>
   <Valid=TELL:&6You typed a number &a$input>
   <Invalid=TELL:&cInvalid number input>
   <Require=TrUtils.isNumber("$input")>
   <Cancel=TELL:&7Canceld...>
```

{% tabs %}
{% tab title="TYPE" %}
The way of the plugin to gather player's input text

**CHAT**: Plugin close player's inventory, and reacts to the next chat message

**SIGN:** Open a new sign and reacts to the lines when the player finishes editing
{% endtab %}

{% tab title="BEFORE" %}
The action that runs when this catcher action is called
{% endtab %}

{% tab title="VALID" %}
The action that runs when there's a input value and requirement\(if there is a requirement\) returns true
{% endtab %}

{% tab title="INVALID" %}
The action that runs when there's a input value and requirement returns false
{% endtab %}

{% tab title="CANCEL" %}
When the catcher is canceld
{% endtab %}
{% endtabs %}



