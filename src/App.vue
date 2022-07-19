<template>
  <div id="app">
    <HeaderComponentVue :menuList="menuList" @setCurrentPage="setCurrentPage"/>
    <MainComponentVue />
    <FooterComponentVue :menuList="menuList" @setCurrentPage="setCurrentPage"/>
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
        link:'#music',
        currentPage: true
      },
      {
        text:'Meet The Band',
        link:'#all-live-dates',
        currentPage: false
      },
      {
        text:'Live Dates',
        link:'#live-dates',
        currentPage: false
      },
      {
        text:'Latest News',
        link:'#latest-band-news',
        currentPage: false
      },
      {
        text:'Albums',
        link:'#testimonial',
        currentPage: false
      },
      ],
    }
  },
  methods:{
    setCurrentPage: function(index){
      //reset dell'elemento corrente
      this.menuList.forEach(element => element.currentPage = false);
      //set dell'elemento attualmente selezionato tramite index
      this.menuList[index].currentPage = true;
    }
  },
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
