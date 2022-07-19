<template>
  <main>
    <cardListAlbum/>
  </main>
</template>

<script>
import cardListAlbum from './cardsListAlbum.vue'
export default {
  components: {
    cardListAlbum,
  }
}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";
main{
  height: calc(100vh - 50px);
  background-color: $colorBody ;
  padding-top: 50px;
}
</style>