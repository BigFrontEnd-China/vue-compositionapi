<template>
  <div>
    <Child></Child>
  </div>
</template>
<script>
import { provide, ref } from 'vue'
import Child from './Child.vue'
export default {
  components: {
    Child
  },
  setup(props) {
    const prv = ref(0)
    provide(prv)
  }
}
</script>