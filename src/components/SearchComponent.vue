<template>
  <div class="container position-absolute top-0 my-4">
    <select class="form-select text-secondary"  name="genre" id="genre" v-model="inputText" @change="changeSearch">
        <option value="">All</option>
     <option :value="genre" v-for="genre in selectGenre" :key="genre">{{genre}}</option>
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
  props:['selectGenre'],
  methods:{
      changeSearch(){
          this.$emit('search', this.inputText);
          
      }
  }
};
</script>

<style lang="scss" scoped>
</style>