## 气泡菜单 popover

### 描述

点击元素，弹出气泡式菜单。

### 使用效果

<preview url="https://editor.quickapp.cn/preview/2011/sL/2011sL1yEg08/build/pages/popover/"/>

### 使用方法

在`.ux`文件中引入组件

```html
<import name="q-popover" src="qaui/src/components/popover/index"></import>
```

### 示例

```html
<template>
  <div class="wrap">
    <div class="header">
      <q-popover
        contents="{{ contents }}"
        placement="{{ placementArr[0] }}"
        popover-width="{{ popoverWidth }}"
        trigger-size="{{ triggerSize }}"
        offset="{{ offset }}"
        arrow-space="{{ arrowSpace }}"
        onmenu-item-tap="handleClick"
      >
        <text slot="trigger" class="rootText">topLeft</text>
      </q-popover>
      <q-popover
        contents="{{ contents }}"
        placement="{{ placementArr[1] }}"
        popover-width="{{ popoverWidth }}"
        trigger-size="{{ triggerSize }}"
        offset="{{ offset }}"
        arrow-space="{{ arrowSpace }}"
        onmenu-item-tap="handleClick"
      >
        <text slot="trigger" class="rootText">top</text>
      </q-popover>
      <q-popover
        contents="{{ contents }}"
        placement="{{ placementArr[2] }}"
        popover-width="{{ popoverWidth }}"
        trigger-size="{{ triggerSize }}"
        offset="{{ offset }}"
        arrow-space="{{ arrowSpace }}"
        onmenu-item-tap="handleClick"
      >
        <text slot="trigger" class="rootText">topRight</text>
      </q-popover>
    </div>
    <div class="body">
      <q-popover
        contents="{{ contents }}"
        placement="{{ placementArr[3] }}"
        popover-width="{{ popoverWidth }}"
        trigger-size="{{ triggerSize }}"
        offset="{{ offset }}"
        arrow-space="{{ arrowSpace }}"
        onmenu-item-tap="handleClick"
      >
        <text slot="trigger" class="rootText">leftTop</text>
      </q-popover>
      <q-popover
        contents="{{ contents }}"
        placement="{{ placementArr[4] }}"
        popover-width="{{ popoverWidth }}"
        trigger-size="{{ triggerSize }}"
        offset="{{ offset }}"
        arrow-space="{{ arrowSpace }}"
        onmenu-item-tap="handleClick"
      >
        <text slot="trigger" class="rootText">left</text>
      </q-popover>
      <q-popover
        contents="{{ contents }}"
        placement="{{ placementArr[5] }}"
        popover-width="{{ popoverWidth }}"
        trigger-size="{{ triggerSize }}"
        offset="{{ offset }}"
        arrow-space="{{ arrowSpace }}"
        onmenu-item-tap="handleClick"
      >
        <text slot="trigger" class="rootText">leftBottom</text>
      </q-popover>
      <q-popover
        contents="{{ contents }}"
        placement="{{ placementArr[6] }}"
        popover-width="{{ popoverWidth }}"
        trigger-size="{{ triggerSize }}"
        offset="{{ offset }}"
        arrow-space="{{ arrowSpace }}"
        onmenu-item-tap="handleClick"
      >
        <text slot="trigger" class="rootText">rightTop</text>
      </q-popover>
      <q-popover
        contents="{{ contents }}"
        placement="{{ placementArr[7] }}"
        popover-width="{{ popoverWidth }}"
        trigger-size="{{ triggerSize }}"
        offset="{{ offset }}"
        arrow-space="{{ arrowSpace }}"
        onmenu-item-tap="handleClick"
      >
        <text slot="trigger" class="rootText">right</text>
      </q-popover>
      <q-popover
        contents="{{ contents }}"
        placement="{{ placementArr[8] }}"
        popover-width="{{ popoverWidth }}"
        trigger-size="{{ triggerSize }}"
        offset="{{ offset }}"
        arrow-space="{{ arrowSpace }}"
        onmenu-item-tap="handleClick"
      >
        <text slot="trigger" class="rootText">rightBottom</text>
      </q-popover>
    </div>
    <div class="footer">
      <q-popover
        contents="{{ contents }}"
        placement="{{ placementArr[9] }}"
        popover-width="{{ popoverWidth }}"
        trigger-size="{{ triggerSize }}"
        offset="{{ offset }}"
        arrow-space="{{ arrowSpace }}"
        onmenu-item-tap="handleClick"
      >
        <text slot="trigger" class="rootText">bottomLeft</text>
      </q-popover>
      <q-popover
        contents="{{ contents }}"
        placement="{{ placementArr[10] }}"
        popover-width="{{ popoverWidth }}"
        trigger-size="{{ triggerSize }}"
        offset="{{ offset }}"
        arrow-space="{{ arrowSpace }}"
        onmenu-item-tap="handleClick"
      >
        <text slot="trigger" class="rootText">bottom</text>
      </q-popover>
      <q-popover
        contents="{{ contents }}"
        placement="{{ placementArr[11] }}"
        popover-width="{{ popoverWidth }}"
        trigger-size="{{ triggerSize }}"
        offset="{{ offset }}"
        arrow-space="{{ arrowSpace }}"
        onmenu-item-tap="handleClick"
      >
        <text slot="trigger" class="rootText">bottomRight</text>
      </q-popover>
    </div>
  </div>
</template>
```

```js
export default {
  data() {
    return {
      contents: [
        {
          content: '描述内容',
          iconPath: '/common/images/default_black.png',
        },
        {
          content: '描述内容',
          icon: {
            type: 'category-fill',
            color: '#456FFF',
          },
        },
        {
          content: '描述内容',
        },
      ],
      placementArr: [
        'topLeft',
        'top',
        'topRight',
        'leftTop',
        'left',
        'leftBottom',
        'rightTop',
        'right',
        'rightBottom',
        'bottomLeft',
        'bottom',
        'bottomRight',
      ],
      popoverWidth: 95,
      triggerSize: [84, 33],
      offset: [0, 0],
      arrowSpace: 10,
    }
  },
  handleClick(data) {
    const { event, index } = data.detail
    console.log(event)
    console.log(index)
  },
}
```

```less
.wrap {
  background-color: #e1e1e1;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  padding: 130px 0;

  .header {
    width: 100%;
    padding: 0 20px;
    flex-direction: row;
    justify-content: space-around;
  }

  .body {
    width: 100%;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
    flex: 1;
  }

  .footer {
    width: 100%;
    padding: 0 20px;
    flex-direction: row;
    justify-content: space-around;
  }

  &-select {
    width: 95px;
    height: 33px;
    margin: 50px 0 200px;
    font-size: 14px;
    background-color: #ffffff;

    &-item {
      margin: 5px 0;
      font-size: 14px;
    }
  }

  .rootText {
    width: 84px;
    height: 33px;
    border-radius: 6px;
    font-size: 13px;
    color: rgba(0, 0, 0, 0.8);
    text-align: center;
    line-height: 33px;
    background-color: #ffffff;
  }
}
```

### API

#### 组件属性

| 属性         | 类型   | 默认值   | 说明                                                                                                                                                                                  |
| ------------ | ------ | -------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| popoverWidth | Number | 0        | 自定义气泡菜单宽度(必填)                                                                                                                                                              |
| contents     | Array  | []       | 气泡菜单内容数组，数组每一项为一个对象，对象的具体说明见下方文档                                                                                                                      |
| placement    | String | 'bottom' | 箭头出现位置，可选值有: 'top' \| 'topLeft' \| 'topRight' \| 'bottom' \| 'bottomLeft' \| 'bottomRight' \| 'left' \| 'leftTop' \| 'leftBottom' \| 'right' \| 'rightTop' \|'rightBottom' |
| offset       | Array  | [0, 0]   | 气泡菜单在水平和垂直方向的偏移量                                                                                                                                                      |
| arrowSpace   | Number | 10       | 当箭头位置不为 'top' \| 'left' \| 'right' \| 'bottom' 时箭头离所在边界的距离（自定义值需大于 10）                                                                                     |
| triggerSize  | Array  | []       | 用户通过 slot 自定义的组件的宽高（必填，而且须根据自己定义的宽高准确填入）                                                                                                            |

contents 属性数组每一项具体说明

| 属性     | 类型   | 说明                                                                           |
| -------- | ------ | ------------------------------------------------------------------------------ |
| content  | String | 菜单栏每一行的内容                                                             |
| iconPath | String | 菜单栏每一行的图标路径，iconPath 和 icon 只需填写一个，如都填写，优先使用 icon |
| icon     | Object | 组件库中 icon 组件配置项，目前只支持 type 和 color 两个属性                    |

#### 组件事件

| 事件名称    | 事件描述       | 返回值         |
| ----------- | -------------- | -------------- |
| menuItemTap | 点击菜单栏触发 | (event, index) |

#### slot

| 名称    | 描述                           |
| ------- | ------------------------------ |
| trigger | 自定义触发气泡菜单的组件，必填 |
