<template>
    <select class="col-4 rounded-3" v-model="selectedArtist" @select="$emit('select' , selectedArtist)">
          <option selected disabled value="">GENERE</option>
          <option value="rock">Rock</option>
          <option value="pop">Pop</option>
          <option value="jazz">Jazz</option>
          <option value="metal">Metal</option>
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