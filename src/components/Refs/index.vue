<template>
  <div ref="root">{{root}}</div>
</template>

<script>
import { ref, onMounted } from 'vue'

export default {
  setup() {
    const root = ref(null)
    onMounted(() => {
      console.log(root.value) // <div/>
    })

    return {
      root
    }
  }
}
</script>