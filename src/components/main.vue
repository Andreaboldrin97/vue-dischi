<template>
  <main>
    <div class="container">
      <div class="row row-cols-5">
      <cardAlbum/>
      </div>
    </div>
  </main>
</template>

<script>
import cardAlbum from '../components/cardAlbum.vue'
export default {
  components: {
    cardAlbum,
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