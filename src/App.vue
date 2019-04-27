<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="@/assets/images/logo.png"> -->
    <TestPacket/>
  </div>
</template>

<script>
import TestPacket from './pages/TestPacket.vue'
export default {
  name: 'app',
  components: {
    TestPacket
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
