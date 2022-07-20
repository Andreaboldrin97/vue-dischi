<template>
   <select class="col-4 offset-4 rounded-3" v-model="selectedArtist" @change="$emit('select' , selectedArtist)">
          <option selected value="">ARTISTA</option>
          <option value="Bon Jovi">Bon Jovi</option>
          <option value="Queen">Queen</option>
          <option value="Sting">Sting</option>
          <option value="Steve Gadd Band">Steve Gadd Band</option>
          <option value="Iron Maiden">Iron Maiden</option>
          <option value="Eric Clapton">Eric Clapton</option>
          <option value="Deep Purple">Deep Purple</option>
          <option value="Metallica">Metallica</option>
          <option value="Dave Weckl<">Dave Weckl</option>
          <option value="Micheal Jacjson">Micheal Jackson</option>
    </select>
</template>

<script>
export default {
     data: function(){
        return{
            selectedArtist : ''
        }
    }

}
</script>

<style>

</style>