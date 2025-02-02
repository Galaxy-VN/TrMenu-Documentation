---
description: 初次安装本插件后，会在插件目录下产生一些文件
---

# 配置

## 文件

{% tabs %}
{% tab title="lang/zh\_CN.yml" %}
TLocale 语言文件, 你可以编辑本插件几乎所有的消息
{% endtab %}

{% tab title="data/globalData.yml" %}
全局缓存数据变量存储的地方

服务器开启状态下请勿编辑
{% endtab %}

{% tab title="data/itemRepository.yml" %}
物品仓库数据存储的地方

服务器开启状态下请勿编辑
{% endtab %}

{% tab title="menus" %}
默认的菜单加载目录

菜单文件（YAML）可放在该目录或其子目录下，将会被插件自动加载
{% endtab %}

{% tab title="settings.yml" %}
TrMenu 的主配置文件
{% endtab %}
{% endtabs %}

## 设置

{% code title="settings.yml \(v3.0 BETA-2\)" %}
```yaml
#
# 插件的选项
#
Options:
  #
  # 插件使用的语言
  # 修改为 zh_CN 即可切换为中文
  #
  Language: en_US

#
# 菜单加载器
#
Loader:
  # 自定义加载目录
  Menu-Files:
    - 'plugins/CustomMenusFolder'

#
# 菜单设置
#
Menu:
  # 选项
  Settings:
    # 绑定物品触发开启菜单的最低间隔 (防止频刷)
    Bound-Item-Interval: 3
  # 图标
  Icon:
    # 是否默认开启子图标继承主图标
    Inherit: false
    # 显示物品
    Item:
      # 默认名称颜色
      Default-Name-Color: "&7"
      # 默认Lore颜色
      Default-Lore-Color: "&7"
      # 优先着色
      # 若开启，则先替换颜色再处理函数变量
      Pre-Color: false

#
# 动作相关
#
Action:
  # 捕获器
  Inputer:
    # 取消词（正则）
    Cancel-Words:
      - 'cancel|quit|end'
      - 'q'

#
# 快捷绑定执行的动作
# 具体注解详见 [USAGE-快捷绑定] 章节
#
Shortcuts:
  Offhand: []
  Sneaking-Offhand:
    - condition: 'perm *trmenu.shortcut'
      execute: 'open: Example'
      deny: 'return'
  Right-Click-Player: 'open: Profile'
  Sneaking-Right-Click-Player: [ ]
  PlayerInventory-Border-Left: [ ]
  PlayerInventory-Border-Right: [ ]
  PlayerInventory-Border-Middle: [ ]

#
# 注册自定义命令
# 具体注解详见 [USAGE-命令注册] 章节
#
RegisterCommands:
  openMenus:
    aliases: [ ]
    permission: null
    execute:
      - 'tell: &7Argument `example` Required!'
    arguments:
      example: 'open: example'
```
{% endcode %}

## 语言

TODO

