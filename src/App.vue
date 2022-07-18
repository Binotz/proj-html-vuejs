<template>
  <div id="app">
    <HeaderComponentVue />
    <MainComponentVue />
    <FooterComponentVue :menuList="menuList"/>
  </div>
</template>

<script>
import HeaderComponentVue from './components/HeaderComponent.vue';
import MainComponentVue from './components/MainComponent.vue';
import FooterComponentVue from './components/FooterComponent.vue';  

export default {
  name: 'App',
  components: {
    HeaderComponentVue,
    MainComponentVue,
    FooterComponentVue
  },
  data(){
    return{
      menuList:[
      {
        text:'Home',
        link:'#',
        currentSection: false
      },
      {
        text:'Meet The Band',
        link:'#',
        currentSection: false
      },
      {
        text:'Live Dates',
        link:'#',
        currentSection: false
      },
      {
        text:'Latest News',
        link:'#',
        currentSection: false
      },
      {
        text:'Albums',
        link:'#',
        currentSection: false
      },
      ],
    }
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400;700&display=swap');
@import '@/assets/variables.scss';
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body{
  font-family: 'Roboto', sans-serif;
}
ul{
  list-style-type: none;
  margin-bottom: 0;
}
.latest-news,
.all-live-dates{
  a{
    color: white;
  }
  &:hover{
    a{
      color: black;
    }
  }
}
</style>
