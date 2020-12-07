<template>
  <div>{{prv}}</div>
</template>
<script>
import { inject, ref } from 'vue'
export default {
  setup() {
    const prv = inject(ref('light'))
    return {
      prv
    }
  }
}
</script>