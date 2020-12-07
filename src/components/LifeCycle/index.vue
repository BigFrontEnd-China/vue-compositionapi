<template>
  <div v-if="componentReload.isReload">LifeCycle</div>
  <button @click="reload">reload</button>
</template>
<script>
import {
  reactive,
  onMounted,
  onUpdated,
  onUnmounted,
  onRenderTracked,
  onRenderTriggered
} from 'vue'
export default {
  setup() {
    const componentReload = reactive({
      isReload: true
    })
    function reload() {
      componentReload.isReload = !componentReload.isReload
    }
    onMounted(() => {
      console.log('mounted!')
    })
    onUpdated(() => {
      console.log('updated!')
    })
    onUnmounted(() => {
      console.log('unmounted!')
    })
    onRenderTracked((e) => {
      debugger
    })
    onRenderTriggered((e) => {
      debugger
    })
    return {
      componentReload,
      reload
    }
  }
}
</script>