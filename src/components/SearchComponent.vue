<template>
  <div class="container position-absolute top-0 my-4">
    <select class="form-select text-secondary"  name="genre" id="genre" v-model="inputText">
     <option value="" v-for="genre in selectGenre" :key="genre">{{genres}}</option>
    </select>
  </div>
</template>

<script>
export default {
  name: "SearchComponent",
  data(){
     return {
         inputText: '',
     }
  },
  props:['selectGenre']
};
</script>

<style lang="scss" scoped>
</style>