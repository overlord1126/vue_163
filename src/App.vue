<template>
  <div id="app">
    <Homepage></Homepage>
  </div>
</template>

<script>
import Homepage from './components/homepage'

export default {
  name: 'app',
  components: {
    Homepage
  }
}
</script>
<style lang="less">
	@import '~vux/src/styles/reset.less';
</style>
<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
