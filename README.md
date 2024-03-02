# Autoclear 插件

## 简介

Autoclear 是一个为 Terraria 服务器设计的 TShock 插件，它提供了一个智能自动扫地功能。这个插件能够根据配置自动清理地面上的物品，帮助服务器保持整洁。

## 功能

- 根据配置文件中设定的规则自动清理地面上的物品。
- 支持自定义清扫的临界值和清扫物品的类型。
- 可以发送自定义消息和具体清扫结果给所有玩家。

## 配置文件

Autoclear 插件的配置文件 `AutoClear.json` 位于 TShock 的保存路径下。这个 JSON 文件包含了清扫规则和消息设置。

配置文件的结构如下：

```json
{
  "NonSweepableItemIDs": ["不清扫的物品ID1", "不清扫的物品ID2", ...],
  "SmartSweepThreshold": 100, // 智能清扫数量临界值
  "SweepSwinging": true, // 是否清扫挥动武器
  "SweepThrowable": true, // 是否清扫投掷武器
  "SweepRegular": true, // 是否清扫普通物品
  "SweepEquipment": true, // 是否清扫装备
  "SweepVanity": true, // 是否清扫时装
  "CustomMessage": "", // 自定义消息
  "SpecificMessage": true // 是否发送具体清扫消息
}
```

- **NonSweepableItemIDs**：一个整数列表，包含不希望被清扫的物品的 ID。
- **SmartSweepThreshold**：一个整数，表示触发智能清扫的地面物品数量临界值。
- **SweepSwinging**、**SweepThrowable**、**SweepRegular**、**SweepEquipment**、**SweepVanity**：布尔值，表示是否清扫对应类型的物品。
- **CustomMessage**：一个字符串，用于自定义清扫时发送给玩家的消息。
- **SpecificMessage**：一个布尔值，表示是否发送包含清扫物品详细信息的消息。

## 使用

在配置文件中设置好清扫规则后，插件会在服务器的每个游戏更新周期自动执行清扫操作。

## 开发者信息

- **作者**：大豆子[Mute适配1447]，肝帝熙恩更新

## 支持与反馈

如果您在使用过程中遇到问题或有任何建议，欢迎在官方论坛或社区中提出 issues。

- GitHub 仓库：https://github.com/THEXN/Autosmartclear
