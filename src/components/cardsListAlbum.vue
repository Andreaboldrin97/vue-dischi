<template>
    <div class="container">
        <div class="row row-cols-5">
            <cardAlbum/>
        </div>
    </div>
</template>

<script>
import cardAlbum from './cardAlbum.vue'
export default {
  components: {
    cardAlbum,
  }
}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";

</style>