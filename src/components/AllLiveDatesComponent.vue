<template>
  <div class="latest-news">
    <a href="#">View all live dates</a>
  </div>
</template>

<script>
export default {
    name: "AllLiveDatesComponent"
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
