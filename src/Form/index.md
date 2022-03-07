---
nav:
  path: /components
group:
  title: 实验性质的组件
toc: false
---

# Form

## 注意事项
- 使用条件：小程序项目需开启 `Component2` 选项
- 配合 a:for 指令使用时，推荐指定 key 值，否则可能出现异常情况
- Form 标签的 form 属性值与其内部 FormItem 标签 的form 属性值必须相同，且`全局唯一`；内部的 FormItem 标签的 name 属性必须`唯一`。详见下方代码示例。
- 配合组件库内的表单组件使用时候，需表单组件的 `mode` 属性值为 `form`。

## 代码示例

### 基本使用
<code src="../../demo/pages/FormBasic" ></code>

### 表单校验
<code src="../../demo/pages/FormValidate" ></code>

### 结合 a:for 指令
<code src="../../demo/pages/FormAFor" ></code>

### 结合 a:if 指令
<code src="../../demo/pages/FormAIf" ></code>

### 实例方法使用
<code src="../../demo/pages/FormInsMethod" ></code>

### 结合表单组件
<code src="../../demo/pages/Form" ></code>

## API

### 属性

#### Form
| 属性 | 类型 | 必填 | 默认值 | 说明 |
| -----|:-----:|:-----:|:-----:|----- |
| form | string | 是 | [] | 表单 uid |
| initialValues | Record<sring, any> | 否 | - | 表单初始值 |
| className | string | 否 | - | 类名 |

#### FromGroup
| 属性 | 类型 | 必填 | 默认值 | 说明 |
| -----|:-----:|:-----:|:-----:|----- |
| header | string | 否 | - | FormGroup 名称 |
| radius | boolean | 否 | false | FormGroup 形状是否为圆角 |
| className | string | 否 | - | 类名 |

#### FormItem
| 属性 | 类型 | 必填 | 默认值 | 说明 |
| -----|:-----:|:-----:|:-----:|----- |
| form | string | 是 | default | 表单 uid |
| name | string | 是 | default | 字段 uid |
| label | string | 否 | - | 字段名称 |
| initialValue | string | 否 | "" | 字段初始值 |
| position | `'horizontal'` &verbar; `'vertical'` | 否 | horizontal | 对齐方式 |
| rules | array | 否 | [] | 输入规则 |
| arrow | boolean | 否 | false | 表单项右侧箭头 |
| disabled | boolean | 否 | false | 是否禁用 |
| className | string | 否 | "" | 类名 |

### 事件

#### Form
| 事件名 | 说明 | 类型 |
| -----|-----|-----|
| onValuesChange | 字段更新，触发此回调 | ( changedFields: `Record<string, any>`, allFields: `Record<string, any>` ) => void |
| onFinish | 表单提交后，触发此回调 | ( changedFields: `Record<string, any>`, allFields: `Record<string, any>` ) => void |
| onFinishFailed | 表单提交失败后，触发此回调 | ( changedFields: `Record<string, any>`, allFields: `Record<string, any>` ) => void |

### 插槽

#### FormGroup
| 名称 | 说明 |
| ----|----|
| header | 标题内容 |


#### FormItem
| 名称 | 说明 |
| ----|----|
| extra | 表单项额外内容 |

### 实例方法

#### Form
| 事件名 | 说明 | 类型 |
| -----|-----|-----|
| getComponentIns | 获取组件示例，其值等同于[默认的 ref 返回值](https://opendocs.alipay.com/mini/framework/component-ref)  | () => Component |
| setFieldsValue | 设置表单字段值 | ( formName: `string`, fieldsVals: `Record<string, any>` ) => void |


### 样式类

#### Form
| 类名 | 说明 |
| -----|-----|
| onValuesChange | 字段更新，触发此回调 |
| onFinish | 表单提交后，触发此回调 |

#### FormGroup
| 类名 | 说明 |
| -----|-----|
| amd-form-group-header | 标题样式 |
| amd-form-group-radius | 圆角样式 |


#### FormItem

| 类名 | 说明 |
| -----|-----|
| amd-form-item-label | 标签样式 |
| amd-form-item-field | 字段样式 |
| amd-form-item-extra | 额外内容样式 |
| amd-form-item-arrow | 箭头样式 |



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
.__dumi-default-layout-content article table:nth-of-type(3) th:nth-of-type(2)  {
    width: 140px
} 
.__dumi-default-layout-content article table:nth-of-type(3) th:nth-of-type(3)  {
    width: 30px
} 
.__dumi-default-layout-content article table:nth-of-type(3) th:nth-of-type(4)  {
    width: 50px
}
.__dumi-default-layout-content article table:nth-of-type(4) th:nth-of-type(2)  {
    width: 180px
}
.__dumi-default-layout-content article table:nth-of-type(7) th:nth-of-type(2)  {
    width: 180px
}
</style> 