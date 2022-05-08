<template>
  <div class="container my-5">
    <div class="row">
      <div
        v-for="(card, index) in cards"
        :key="index"
        class="col-6 col-md-4 col-lg-3 mb-3">
        <CardComponent :item="card"/>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
import CardComponent from "./CardComponent.vue"

export default {
  name: "MainComponent",
  components:{
      CardComponent,
  },
  data() {
    return {
      cards: [],
    };
  },
  mounted() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((res) => {
        this.cards = res.data.response;
        console.log(res.data.response);
      })
      .catch((err) => {
        console.log(err);
      });
  },
};
</script>

<style lang="scss" scoped>
@import "src/assets/styles/general.scss";

.col-lg-3{
    width:20% !important;
}
</style>