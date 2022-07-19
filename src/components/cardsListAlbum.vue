<template>
    <div class="container">
        <div class="row row-cols-6" v-if="Album.length === 10">
            <cardAlbum v-for="(album , index) in Album" :key="index"
                  :author ="album.author"
                  :genre ="album.genre"
                  :poster ="album.poster"
                  :title ="album.title"
                  :year ="album.year"/>
        </div>
        <div v-else class="d-flex justify-content-center">
          <div class="loading-bar">
            <div class="loading">

            </div>
          </div>
        </div>
    </div>
</template>

<script>
import axios from "axios";
import cardAlbum from './cardAlbum.vue'
export default {
      components: {
        cardAlbum,
      },
      data : function(){
        return{
            Album : []
        }
      },
      methods:{
        getAlbum : function(){
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then((elemnt) =>{
              this.Album = elemnt.data.response ;
              console.log(this.Album)
            })
        }
      },
      created(){
        this.getAlbum()
      }
}
</script>

<style lang="scss" scoped>
@import "../styles/variables.scss";
.loading-bar{
  height: 10px;
  width: 900px;
  border: 2px solid white;
  .loading{
    background-color: $colorBreand ;
    height: 6px;
    width: 150px;
    animation-name: slidein;
    animation-duration: 4s;
    animation-iteration-count: infinite;
  }
}
@keyframes slidein {
  from {
    transform: translateX(0%);
  }

  to {
    transform: translateX(498%);
  }
}
</style>