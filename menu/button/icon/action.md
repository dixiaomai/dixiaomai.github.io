---
description: 根据不同点击方式，图标对应执行的各种动作
---

# 动作部分

```yaml
# 示例
actions:
  类型1: 动作
  类型2:
    - '动作1'
    - '动作2'
```

## **支持类型**

{% hint style="info" %}
节点可忽略大小写
{% endhint %}

* **LEFT** 左键点击
* **RIGHT** 右键点击
* **SHIFT\_LEFT** Shift+左键点击
* **SHIFT\_RIGHT** Shift+右键点击
* **MIDDLE** 中键点击
* **DOUBLE\_CLICK** 双击
* **DROP** 丢弃
* **CONTROL\_DROP** Ctrl+丢弃
* **ALL** 所有操作都将触发

## **动作写法**

{% page-ref page="../../../actions/normal-actions/" %}

