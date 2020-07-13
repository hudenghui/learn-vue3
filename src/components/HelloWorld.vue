<template>
  <div>{{ count }} {{ object.foo }}</div>
</template>

<script>
import { h, ref, reactive } from 'vue'

export default {
  setup() {
    const count = ref(0)
    const object = reactive({ foo: 'bar' })

    return () => h('div', [count.value, object.foo])
  },
}
</script>
