<template>
  <div>
    <button @click="increment">Count is: {{ refState }}</button>
  </div>
</template>
<script>
import { ref, computed } from 'vue'

export default {
  setup() {
    const refState = ref(0)
    function increment() {
      refState.value++
    }
    return {
      refState,
      increment
    }
  }
}
</script>