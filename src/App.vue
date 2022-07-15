<template>
  <div id="app">
    <HeaderComponentVue />
    <MainComponentVue />
  </div>
</template>

<script>
import HeaderComponentVue from './components/HeaderComponent.vue';
import MainComponentVue from './components/MainComponent.vue';

export default {
  name: 'App',
  components: {
    HeaderComponentVue,
    MainComponentVue
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap');

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body{
  font-family: 'Roboto', sans-serif;
}
</style>
