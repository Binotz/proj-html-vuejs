<template>
  <div class="latest-band">
    <SectionTitleVue msg="Latest Band News" />
    <div class="container">
      <div class="row">       
          <!-- left column -->
          <div class="left-column col-8">
            <div class="row">
                <div class="col-12">
                  <SingleCardComponentVue 
                    imgSource="blog_music_techo.jpg" 
                    title="Technology and Music"
                    :description = description  
                  />
                </div>
            </div>
            <!-- second row -->
            <div class="row">
              <div class="col-6">
                <SingleCardComponentVue
                  imgSource="blog-post3.jpg"
                  title="While my guitar gently weeps"
                  :description=description
                />
              </div>
              <div class="col-6">
                <SingleCardComponentVue
                  imgSource="blog-post3.jpg"
                  title="While my guitar gently weeps"
                  :description=description
                  />
              </div>
            </div>
            <!-- Third row -->
            <div class="row">
              <div class="col-12">
                <SingleCardComponentVue
                imgSource="blog_flavor_rock.jpg"
                title="The flavor of rock"
                :description=description
                />
              </div>
            </div>
          </div>
          <!-- right column -->
          <div class="rigth-column col-4">
          <div class="row">
            <div class="col">
              <SingleCardComponentVue
                imgSource="blog-post1.jpg" 
                title="Taking it back to the old school"
                :description = description
              /> 
              <SingleCardComponentVue
                imgSource="blog-post2.jpg" 
                title="Sharing the stage with a legend"
                :description = description
              /> 
            </div>
          </div>
          </div>
      </div>  
    </div>

  </div>
</template>

<script>
import SectionTitleVue from './SectionTitle.vue';
import SingleCardComponentVue from './SingleCardComponent.vue';

export default {
    name:"LatestBandSectionComponent",
    components:{
        SectionTitleVue,
        SingleCardComponentVue        
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
.row{
  margin-bottom: 2rem;
}
</style>
