<template>
  <main>
    <section class="music">
        <div class="strike"></div>
        <SectionTitleVue msg ="Music Is Life" />
    </section>
    
    <section class="latest-band-news">
        <LatestBandSectionComponentVue/>
    </section>

    <section class="latest-news">
        <LatestNewsVue />
    </section>
  </main>
</template>

<script>
import SectionTitleVue from './SectionTitle.vue';
import LatestBandSectionComponentVue from './LatestBandSectionComponent.vue';
import LatestNewsVue
 from './LatestNews.vue';
export default {
    name: "MainComponent",  
    components:{
        SectionTitleVue,
        LatestBandSectionComponentVue,
        LatestNewsVue
},
}
</script>

<style lang="scss" scoped>
@import '@/assets/variables.scss';
    section{
        padding: 3rem 0;
    }
    .music{
        padding: 4rem 0;
        background-color: $gray;
        color: white;
        .strike{
            width: 600px;
            margin: 0 auto;
            margin-top: -4rem;
            margin-bottom: 4rem;
            border:10px solid $mandy;
        }
    }
    .latest-band-news{
        background-color: $primary_color;
    }
    .latest-news{
        background-color: $secondary-color;
    }
</style>
