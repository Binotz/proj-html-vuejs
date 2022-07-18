<template>
  <div class="card-layout">
    <div class="card-content">
      <img :src="require(`@/assets/img/${imgSource}`)" alt="Alt text">
        <div class="card-text">
          <h3>{{title}}</h3>
          <p>{{description}}</p>
        </div>
        <!-- Overlay -->
        <div class="overlay">
          <div class="overlay-text">
            {{ title }}
          </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    name:"SingleCardVerticalComponent",
    props:{
        imgSource: String,
        title: String,
        description: String,
        rotation: String
    },
}
</script>

<style lang="scss" scoped>
@import '@/assets/variables.scss';

img{
  height: 740px;
  width: 100%;
  
}
.card-content{
  position: relative;
  .overlay{
    display: none;
    position: absolute;
    top: 0;
    right: 0;
    left: 0;
    bottom: 0;
    justify-content: center;
    align-items: center;
    background-color: rgba(255, 0,0, .3);
    .overlay-text{
      color: white;
    }
  }
  .card-text{
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    padding: 2rem;
    background-color: $gray;
    h3{
      color: $mandy;
      font-size: 1.3rem;
    }
    p{
      color: $light_gray;
    }
  }
  &:hover{
    .overlay{
      display: flex;
      font-size: 1.5rem;
    }
    .card-text{
      display:none;
    }
  }
}
</style>
