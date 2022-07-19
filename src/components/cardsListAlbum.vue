<template>
    <div class="container">
        <div class="row row-cols-5">
            <cardAlbum v-for="(album , index) in Album" :key="index"
                  :author ="album.author"
                  :genre ="album.genre"
                  :poster ="album.poster"
                  :title ="album.title"
                  :year ="album.year"/>
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

</style>