<template>
  <div id="app">
    <BaseHeader/>
    <BaseMain/>
  </div>
</template>

<script>
import BaseHeader from './components/BaseHeader.vue'
import BaseMain from './components/BaseMain.vue'

export default {
  name: 'App',
  components: {
    BaseHeader,
    BaseMain,
  }
}
</script>

<style lang="scss">
  @import'./styles/colors.scss';
  @import'./styles/general.scss';
  @import'../node_modules/bootstrap-icons/font/bootstrap-icons.css';
</style>
