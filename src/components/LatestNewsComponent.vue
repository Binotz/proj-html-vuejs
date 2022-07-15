<template>
  <div class="latest-news">
    <a href="#">View all latest news</a>
  </div>
</template>

<script>
export default {
    name: "LatestNewsComponent"
}
</script>

<style lang="scss" scoped>
@import '@/assets/variables.scss';
.latest-news{
    display: flex;
    justify-content: center;
    align-items: center;
    text-transform: uppercase;
    a{
        text-decoration: none;
        color: white;
    }
}

</style>
