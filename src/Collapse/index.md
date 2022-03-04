---
nav:
  path: /components
group:
  title: 数据展示
toc: false
---

# Collapse

可以折叠 / 展开的内容区域。

- 对复杂区域进行分组和隐藏，保持页面的整洁；
- 手风琴模式 是一种特殊的折叠面板，只允许单个内容区域展开。
- 内部由多个 CollapseItem 组成，详见代码示例。

## 注意事项

- Collapse 组件与 CollapseItem 组件必须有相同的 uid，且 uid 全局唯一。

## 代码示例

<code src='../../demo/pages/Collapse'></code>

## API

### 属性

#### Collapse
| 属性 | 类型 | 必填 | 默认值 | 说明 |
| -----|-----|-----|-----|----- |
| name | string[] | 否 | [] | 当前激活的索引 |
| accordion | boolean | 否 | - | 是否是手风琴模式，仅一个内容被展开 |
| className | string | 否 | - | 类名 |
| uid | string | 是 | - | `必须全局唯一`，需与内部的 CollapseItem 组件的 uid 一致 |

#### CollapseItem
| 属性 | 类型 | 必填 | 默认值 | 说明 |
| -----|-----|-----|-----|----- |
| icon | string | 否 | - | icon 内容 |
| title | string | 否 | - | 标题栏内容 |
| name | string | 是 | - | 标识，必须唯一 |
| disabled | boolean | 否 | false | 禁用状态 |
| brief | string | 否 | - | 副标题 |
| expandIcon | string | 否 | - | 面板展开图标 |
| closeIcon | string | 否 | - | 面板收缩图标 |
| className | string | 否 | - | 类名 |
| uid | string | 是 | - | `必须全局唯一`，需与外部 Collapse 组件的 uid 一致  |

### 事件
#### Collapse
| 事件名 | 说明 | 类型 |
| -----|-----|-----|
| onChange | 面板展开/收缩时，获取当前展开的面板 | ( value : `string[]`) => void |

### 插槽
#### CollapseItem
| 插槽名称 | 说明 |
| -----|-----|
| title | CollapseItem 组件标题插槽，当 title 属性存在时，插槽不生效 |
| brief | CollapseItem 组件副标题插槽，当 brief 属性存在时，插槽不生效 |

### 样式类
#### Collapse
| 类名 | 说明 |
| -----|-----|
| amd-collapse | 整体样式 |

#### CollapseItem
| 类名 | 说明 |
| -----|-----|
| amd-collapse-item | 单个样式 |
| amd-collapse-item-active | 激活状态下单个样式 |
| amd-collapse-item-disabled | 禁用状态下单个样式 |
| amd-collapse-item-title | 单个 title 样式 |
| amd-collapse-item-icon | 单个 icon 样式 |
| amd-collapse-item-line | 单个 line 样式 |
| amd-collapse-item-brief-node | 单个 副标题 样式 |
| amd-collapse-item-content-wrap | 单个 内容容器 样式 |
| amd-collapse-item-content | 单个 内容 样式 |

<style> 
table th:first-of-type { width: 180px; } 
.__dumi-default-layout-content article table:first-of-type th:nth-of-type(2)  {
    width: 140px
} 
.__dumi-default-layout-content article table:first-of-type th:nth-of-type(3)  {
    width: 30px
} 
.__dumi-default-layout-content article table:first-of-type th:nth-of-type(4)  {
    width: 50px
} 
.__dumi-default-layout-content article table:nth-of-type(2) th:nth-of-type(2)  {
    width: 140px
} 
.__dumi-default-layout-content article table:nth-of-type(2) th:nth-of-type(3)  {
    width: 30px
} 
.__dumi-default-layout-content article table:nth-of-type(2) th:nth-of-type(4)  {
    width: 50px
} 
</style> 