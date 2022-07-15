<template>
  <div class="section-title">
    <h2>{{msg}}</h2>
    <div class="strike"></div>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos temporibus vel, quae distinctio, consectetur voluptatibus, cum maxime quam laborum repellat vero ipsam! Officia voluptate quia quis blanditiis maxime! Voluptatibus, aspernatur.</p>
  </div>
</template>

<script>
export default {
    name:"SectionTitle",
    props:{
        msg: String
    },
}
</script>

<style lang="scss" scoped>
@import '@/assets/variables.scss';

.section-title{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 25%;
    margin: 0 auto;
    text-align: center;
    padding: 2rem 0;
}
h2{
    margin-bottom: 2rem;
    font-size: 4.5rem;
    color: white;
}
p{
    color: $lynch;
}
.strike{
    width: 350px;
    height: 1px;
    border: 1px solid $lynch;
    margin-bottom: 3rem;
}
</style>
