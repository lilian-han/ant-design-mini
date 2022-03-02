---
nav:
  path: /components
group:
  title: 数据展示
  order: 1
toc: false
---

# Avatar

头像，可展示头像以及用户名等简要信息。

## 代码示例

<code src="../../demo/pages/Avatar"></code>

## API

### 属性

| 属性 | 类型 | 必填 | 默认值 | 说明 |
| --- | --- | --- | --- | --- |
| size | `'x-small'` &verbar; `'small'` &verbar; `'medium'` &verbar; `'large'` | 否 | "medium" | x-small(80 x 80)；small(88 x 88)；medium(104 x 104)；large(120 x 120) |
| src | string | 否 | - | 头像地址，默认为灰色的内置图片 |
| name | string | 否 | - | 第一行信息 |
| desc | string | 否 | - | 第二行补充信息，当 name 不存在时，不显示；当 size=x-small，不显示 |
| className | string | 否 | - | 类名 |

### 样式类
| 类名 | 说明 |
| -----|-----|
| amd-avatar | 整体样式 |
| amd-avatar-src | 图片样式 |
| amd-avatar-content | 头像描述样式 |
| amd-avatar-name | name 样式 |
| amd-avatar-desc | desc 样式 |

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

</style> 