<template>
  <div>{{prv}}</div>
  <button @click="increment">change inject value</button>
</template>
<script>
import { inject } from 'vue'
export default {
  setup() {
    const prv = inject('provide')
    function increment() {
      prv.value++
    }
    return {
      prv,
      increment
    }
  }
}
</script>