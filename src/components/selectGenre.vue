<template>
    <select class="col-4 rounded-3" v-model="selectedArtist" @change="$emit('select' , selectedArtist)">
          <option selected value="">GENERE</option>
          <option value="Rock">Rock</option>
          <option value="Pop">Pop</option>
          <option value="Jazz">Jazz</option>
          <option value="Metal">Metal</option>
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