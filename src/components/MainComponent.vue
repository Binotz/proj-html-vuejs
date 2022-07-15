<template>
  <main>
    <section class="music">
        <div class="strike"></div>
        <SectionTitleVue msg ="Music Is Life" />
    </section>
  </main>
</template>

<script>
import SectionTitleVue from './SectionTitle.vue';

export default {
    name: "MainComponent",  
    components:{
        SectionTitleVue
    },
}
</script>

<style lang="scss" scoped>
@import '@/assets/variables.scss';
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
</style>
