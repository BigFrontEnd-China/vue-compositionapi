<template>
  <div>
    <button @click="increment">Count is: {{ readState.count }}, double is: {{ readState.double }}</button>
  </div>
</template>
<script>
import { reactive, ref, computed, readonly } from 'vue'

export default {
  setup() {
    const state = reactive({
      count: 0,
      double: computed(() => state.count * 2)
    })
    const readState = readonly(state)
    function increment() {
      readState.count++
    }
    return {
      readState,
      increment
    }
  }
}
</script>