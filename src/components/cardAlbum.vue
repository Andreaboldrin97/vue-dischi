<template>
    <div class="music-card">
          <img :src="poster" :alt="title">
          <h3 class="text-center text-white-50">{{ title }}</h3>
          <h6 class="text-center text-white-50"> {{ author }} <br> {{ year }} </h6> 
    </div>
</template>

<script>
export default {
    props : {
        author : String,
        genre : String,
        poster : String,
        title : String,
        year : [Number , String]
    }

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