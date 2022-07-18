<template>
  <div class="banner">
    <a href="#">{{msg}}</a>
  </div>
</template>

<script>
export default {
    name: "ViewAllComponent",
    props:{
        msg: String
    }
}
</script>

<style lang="scss" scoped>
@import '@/assets/variables.scss';
.banner{
    display: flex;
    justify-content: center;
    align-items: center;
    text-transform: uppercase;
    height: 120px;
    a{
        text-decoration: none;
        color: white;
    }
    &:hover{
      a{
        color: black;
      }
    }
}

</style>
