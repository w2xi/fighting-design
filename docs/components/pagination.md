# Pagination 分页器

用它处理过多的数据吧

- [源代码](https://github.com/FightingDesign/fighting-design/tree/master/packages/fighting-design/pagination)
- [文档编辑](https://github.com/FightingDesign/fighting-design/blob/master/docs/docs/components/pagination.md)

:::danger
组件仍在测试阶段，高频更新中，部分参数暂不稳定！
:::

## 基本使用

`v-model:current` 属性来绑定当前页码

`total` 属性配置总页数

::: demo

```vue
<template>
  <f-pagination v-model:current="current" :total="total" />
</template>

<script lang="ts" setup>
  import { ref } from 'vue'

  const current = ref(1)
  const total = ref(100)
</script>
```

:::

## 页数选择器

`page-sizes` 属性用来表示你想要开启最大页数选择器、传入值是一个数字类型的数组

::: demo

```vue
<template>
  <f-pagination v-model:current="current" :total="total" :page-size="pagesize" :page-sizes="pageSizes" />
</template>

<script lang="ts" setup>
  import { ref } from 'vue'

  const current = ref(1)
  const total = ref(100)
  const pagesize = ref(10)
  const pageSizes = ref([10, 20, 30, 40, 50])
</script>
```

:::

## 带背景色或圆角

`background` 属性控制分页是否带背景色

`round` 属性控制分页是否带圆角

::: demo

```vue
<template>
  <f-pagination v-model:current="current" :total="total" background />
  <f-pagination v-model:current="current" :total="total" round />
</template>

<script lang="ts" setup>
  import { ref } from 'vue'

  const current = ref(1)
  const total = ref(100)
</script>
```

:::

## 自定 Icon

::: demo

```vue
<template>
  <f-pagination v-model:current="current" :total="100" :prev-icon="FIconCloud" :next-icon="FIconBlock" />
</template>

<script lang="ts" setup>
  import { ref } from 'vue'
  import { FIconCloud, FIconBlock } from '@fighting-design/fighting-icon'

  const current = ref(1)
</script>
```

:::

## 禁用状态

`disabled` 属性表示是否禁用分页功能

::: demo

```vue
<template>
  <f-pagination v-model:current="current" :total="100" disabled />
</template>

<script lang="ts" setup>
  import { ref } from 'vue'

  const current = ref(1)
</script>
```

:::

## 展示快速跳转搜索框

`jump-search` 属性表示是否禁用分页功能

::: demo

```vue
<template>
  <f-pagination v-model:current="current" :total="100" jump-search />
</template>

<script lang="ts" setup>
  import { ref } from 'vue'

  const current = ref(1)
</script>
```

:::

## Attributes

| 参数                | 说明                         | 类型                                                               | 可选值 | 默认值 |
| ------------------- | ---------------------------- | ------------------------------------------------------------------ | ------ | ------ |
| `v-model:current`   | 当前选中页码                 | number                                                             | ——     | 1      |
| `total`             | 总页数                       | number                                                             | ——     | 0      |
| `v-model:page-size` | 每页条数                     | number                                                             | ——     | 10     |
| `page-sizes`        | 每页多少条                   | []                                                                 | ——     | ——     |
| `background`        | 是否带有背景色               | boolean                                                            | ——     | false  |
| `round`             | 是否带有圆角                 | boolean                                                            | ——     | false  |
| `prev-icon`         | 自定义的上一页图标           | <a href="/components/interface.html#fightingicon">FightingIcon</a> | ——     | ——     |
| `next-icon`         | 自定义的下一页图标           | <a href="/components/interface.html#fightingicon">FightingIcon</a> | ——     | ——     |
| `disabled`          | 是否禁用                     | boolean                                                            | ——     | false  |
| `change`            | 改变页码回调函数             | Function                                                           | ——     | ——     |
| `jump-search`       | 是否展示快速跳转搜索框       | boolean                                                            | ——     | false  |
| `prev-click`        | 点击上一页触发的回调         | Function                                                           | ——     | ——     |
| `next-click`        | 点击下一页触发的回调         | Function                                                           | ——     | ——     |
| `page-size-change`  | 每页条数发生变化时触发的回调 | Function                                                           | ——     | ——     |

## Interface

组件导出以下类型定义：

```ts
import type { PaginationInstance, PaginationProps } from 'fighting-design'
```

## Contributors

<a href="https://github.com/Tyh2001" target="_blank">
  <f-avatar round src="https://avatars.githubusercontent.com/u/73180970?v=4" />
</a>

<a href="https://github.com/OnlyShadows" target="_blank">
  <f-avatar round src="https://avatars.githubusercontent.com/u/54928569?v=4" />
</a>