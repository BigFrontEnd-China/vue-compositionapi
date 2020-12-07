<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <!-- <HelloWorld msg="Hello Vue 3.0 + Vite" /> -->
  <!-- <Reactive /> -->
  <!-- <Ref /> -->
  <!-- <Readonly /> -->
  <!-- <WatchEffect /> -->
  <!--  <LifeCycle /> -->
  <!-- <Inject /> -->
  <!-- <Refs /> -->
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Reactive from './components/ReactiveApi/Reactive.vue'
import Ref from './components/ReactiveApi/Ref.vue'
import Readonly from './components/ReactiveApi/Readonly.vue'
import WatchEffect from './components/ReactiveApi/WatchEffect.vue'
import LifeCycle from './components/LifeCycle/index.vue'
import Inject from './components/Inject/index.vue'
import Refs from './components/Refs/index.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
    Reactive,
    Ref,
    Readonly,
    WatchEffect,
    LifeCycle,
    Inject,
    Refs
  }
}
</script>
