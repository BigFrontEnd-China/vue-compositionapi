<template>
  <button @click="increment">Count is: {{ count }}</button>
</template>

<script>
import { ref, computed, watchEffect } from 'vue'
export default {
  setup() {
    const count = ref(0)
    function increment() {
      count.value++
    }
    watchEffect(
      () => {
        console.log(count.value)
      },
      {
        onTrack(e) {
          debugger
        },
        onTrigger(e) {
          debugger
        }
      }
    )

    return {
      count,
      increment
    }
  }
}
</script>