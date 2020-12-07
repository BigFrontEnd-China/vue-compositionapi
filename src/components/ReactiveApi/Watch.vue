<template>
  <div>
    <!-- reactive -->
    <!-- <button @click="increment">Count is: {{ state.count }}, double is: {{ state.double }}</button> -->
    <!-- ref -->
    <button @click="increment">Count is: {{ refState }}</button>
    <!-- toRefs -->
    <!-- <button @click="increment">Count is: {{ count }}, double is: {{ double }}</button> -->
  </div>
</template>
<script>
import { reactive, ref, computed, readonly, watchEffect, watch } from 'vue'

export default {
  setup() {
    const state = reactive({
      count: 0,
      double: computed(() => state.count * 2)
    })
    const refState = ref(0)
    const refsState = toRefs(state)
    function increment() {
      /* state.count++ */
      refState.value++
    }
    watchEffect(
      () => {
        /* 副作用的内容 */
        console.log(refState.value)
      },
      {
        onTrack(e) {
          console.log(e)
          debugger
        },
        onTrigger(e) {
          console.log(e)
          debugger
        }
      }
    )
    return {
      /*       state, */
      refState,
      /*  ...refsState, */
      increment
    }
  }
}
</script>