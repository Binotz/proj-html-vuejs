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
        <LatestNewsComponentVue />
    </section>

    <section class="testimonial">
        <TestimonialComponentVue />
    </section>

    <section class="live-dates">
        <SectionTitle msg="Live Dates" />
        <LivesDateComponent />
    </section>

    <section class="all-live-dates">
        <AllLiveDatesComponent />
    </section>
  </main>
</template>

<script>
import SectionTitleVue from './SectionTitle.vue';
import LatestBandSectionComponentVue from './LatestBandSectionComponent.vue';
import LatestNewsComponentVue from './LatestNewsComponent.vue';
import TestimonialComponentVue from './TestimonialComponent.vue';
import SectionTitle from './SectionTitle.vue';
import LivesDateComponent from './LivesDateComponent.vue';
import AllLiveDatesComponent from './AllLiveDatesComponent.vue';

export default {
    name: "MainComponent",  
    components:{
    SectionTitleVue,
    LatestBandSectionComponentVue,
    LatestNewsComponentVue,
    TestimonialComponentVue,
    SectionTitle,
    LivesDateComponent,
    AllLiveDatesComponent
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
    .latest-news,
    .all-live-dates{
        background-color: $secondary-color;
        &:hover{
            background-color: white;
            *{
                background-color: white;
                a{
                    color: black;
                }
            }
        }
        >a{
            color: white;
        }
    }
    .testimonial{
        background-image: url('@/assets/img/home-testimonial-parallax.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        height: 1000px;
        padding: 0;
    }
    .live-dates{
        background-color: $primary_color;
    }
</style>
