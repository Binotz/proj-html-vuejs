<template>
  <div class="latest-band">
    <SectionTitleVue msg="Latest Band News" />
    <div class="container">
      <div class="row">       
          <!-- left column -->
          <div class="left-column col-8">
            <div class="row gy-4">
            <!-- large post -->
                <div class="col-12">
                  <SingleCardComponentVue 
                    :rotation="'horizontal'"
                    imgSource="blog_music_techo.jpg" 
                    title="Technology and Music"
                    :description = description  
                  />
                </div>
            <!-- second row -->
              <!-- 2 vertical posts -->
              <div class="col-6">
                <SingleCardComponentVue
                  :rotation="'vertical'"
                  imgSource="blog-post3.jpg"
                  title="While my guitar gently weeps"
                  :description=description
                />
              </div>
              <div class="col-6">
                <SingleCardComponentVue
                  :rotation="'vertical'"
                  imgSource="blog-post4.jpg"
                  title="While my guitar gently weeps"
                  :description=description
                  />
              </div>
            <!-- Third row -->
            <!-- Large post -->
              <div class="col-12">
                <SingleCardComponentVue
                  :rotation="'horizontal'"
                  imgSource="blog_flavor_rock.jpg"
                  title="The flavor of rock"
                  :description=description
                />
              </div>
            </div>
          </div>
          <!-- right column -->
          <div class="right-column col-4">
          <div class="row h-100 gy-4">
            <div class="col-12">
              <SingleCardVerticalComponentVue
                class="vertical-post"
                imgSource="blog-post1.jpg" 
                title="Taking it back to the old school"
                :description = description
                :rotation="'vertical'"
              /> 
            </div>
            <div class="col-12"></div> 
              <SingleCardVerticalComponentVue
                class="vertical-post"
                imgSource="blog-post2.jpg" 
                title="Sharing the stage with a legend"
                :description = description
                :rotation="'vertical'"
              />
            </div>
              
            </div>
          </div>
          </div>

          
      </div>  
</template>

<script>
import SectionTitleVue from './SectionTitle.vue';
import SingleCardComponentVue from './SingleCardComponent.vue';
import SingleCardVerticalComponentVue from './SingleCardVerticalComponent.vue';

export default {
    name:"LatestBandSectionComponent",
    components:{
        SectionTitleVue,
        SingleCardComponentVue,
        SingleCardVerticalComponentVue
    },
    data(){
      return{
        description: 'Sed sit amet sem turpis. Carubitur cursus lacinia est at interdum risus id condimentum'
      }
    }
}
</script>

<style lang="scss" scoped>
@import '@/assets/variables.scss';

.container{
  padding-top: 1rem;
}
</style>
