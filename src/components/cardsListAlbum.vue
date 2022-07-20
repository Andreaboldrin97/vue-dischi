<template>
    <div class="container">
      <div class="row px-5 py-3">
        <selectGenre @select="valueAlbum"/>
        <selectArtist/>
      </div>
        <div class="row row-cols-6" v-if="Album.length === 10">
            <cardAlbum v-for="(album , index) in Album" :key="index"
                  :author ="album.author"
                  :genre ="album.genre"
                  :poster ="album.poster"
                  :title ="album.title"
                  :year ="album.year"/>
        </div>
        <div v-else class="d-flex justify-content-center">
          <div class="loading-bar rounded">
            <div class="loading">

            </div>
          </div>
        </div>
    </div>
</template>

<script>
import axios from "axios";
import cardAlbum from './cardAlbum.vue'
import selectGenre from './selectGenre.vue'
import selectArtist from './selectArtist.vue'

export default {
      components: {
        cardAlbum,
        selectGenre,
        selectArtist
      },
      data : function(){
        return{
            Album : [],
            genreAlbum : []
        }
      },
      methods:{
        getAlbum : function(){
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then((element) =>{
              this.Album = element.data.response ;
              console.log(this.Album)
            })
        },
        valueAlbum : function(needle){
          console.log(needle)
          this.genreAlbum = [...this.Album].filter((element) => element.genre.includes(needle));
          console.log(this.genreAlbum)
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
    background-color: $colorBreand;
    height: 6px;
    width: 150px;
    animation-name: slidein;
    animation-duration: 2s;
    animation-iteration-count: infinite;
    animation-direction: alternate; 
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