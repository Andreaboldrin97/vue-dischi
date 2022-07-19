<template>
  <div id="app">
    <header/>
    <main/>
    <footer/>
  </div>
</template>

<script>
import header from './components/header.vue'
import main from './components/main.vue'
import footer from './components/footer.vue'

export default {
  name: 'App',
  components: {
    header,
    main,
    footer,
  }
}
</script>

<style lang="scss">

</style>
