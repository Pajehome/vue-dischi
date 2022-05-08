<template>
  <div class="bg-card">
    <img class="w-75" :src="item.poster" :alt="item.title" />
    <h1>{{ item.title }}</h1>
    <span class="d-block">{{ item.author }}</span>
    <span>{{ item.year }}</span>
  </div>
</template>


<script>
export default {
  name: "CardComponent",
  props: {
    item: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "src/assets/styles/general.scss";
.bg-card {
  background-color: $background-secondary;
  width: 200px;
  height: 350px;
  text-align: center;
  padding-top: 17px;

  h1 {
    font-size: 1.5rem;
    text-transform: uppercase;
    width: 100%;
    display: flex;
    justify-content: center;
  }

  span{
      color: $text-secondary;
  }
}
</style>