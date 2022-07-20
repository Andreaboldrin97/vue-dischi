<template>
    <div class="music-card m-3">
          <img :src="poster" :alt="title">
          <h6 class="text-center text-white pt-3">{{ title }}</h6>
          <div class="info-album text-center text-white-50 mb-2"> {{ author }} <br> {{ year }} </div> 
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
        img{
        width: 100%;
        }
        h6{
            text-transform: uppercase;
        }
        .info-album{
            font-size: 13px;
        }
    }
</style>