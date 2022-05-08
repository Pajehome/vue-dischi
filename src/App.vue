<template>
  <div id="app">
    <header>
      <header-component/>
    </header>

    <main>
      <main-component/>
    </main>
  </div>
</template>

<script>

import HeaderComponent from "./components/HeaderComponent.vue";
import MainComponent from "./components/MainComponent.vue";

export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent,
  }
}
</script>

<style lang="scss" >
@import 'src/assets/styles/general.scss';

</style>
