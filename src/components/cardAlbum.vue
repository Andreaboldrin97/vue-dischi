<template>
    <div class="music-card">
          <img src="https://media-cdn.tripadvisor.com/media/photo-s/0c/bb/a3/97/predator-ride-in-the.jpg" alt="">
          <h3 class="text-center text-white-50">title</h3>
          <h6 class="text-center text-white-50">artista <br> anno </h6> 
    </div>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";
.music-card{
     background-color: $colorHeader;
    border: 1px solid red;
        img{
        width: 100%;
        }
    }
</style>