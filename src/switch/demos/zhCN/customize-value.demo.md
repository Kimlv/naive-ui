# 自定义选中的值

使用 `checked-value` 和 `unchecked-value` 制定选中的值。

```html
<n-switch
  checked-value="周末加班"
  unchecked-value="周末支持一下"
  @update:value="handleUpdateValue"
/>
```

```js
import { defineComponent } from 'vue'
import { useMessage } from 'naive-ui'

export default defineComponent({
  setup () {
    const message = useMessage()
    return {
      handleUpdateValue (value) {
        message.info(value)
      }
    }
  }
})
```
