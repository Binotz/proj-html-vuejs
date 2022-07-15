<template>
  <div class="card-layout">
    <div class="card-content">
        <img :src="require(`@/assets/img/${imgSource}`)" alt="Alt text">
        <div class="card-text">
          <h3>{{title}}</h3>
          <p>{{description}}</p>
        </div>
    </div>
  </div>
</template>

<script>
export default {
    name:"SingleCardComponent",
    props:{
        imgSource: String,
        title: String,
        description: String,
    },
}
</script>

<style lang="scss" scoped>
@import '@/assets/variables.scss';

img{
  width: 100%;
}
.card-content{
  position: relative;
  .card-text{
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    padding: 2rem;
    background-color: $gray;
    h3{
      color: $mandy;
    }
    p{
      color: $light_gray;
    }
  }
}
</style>
