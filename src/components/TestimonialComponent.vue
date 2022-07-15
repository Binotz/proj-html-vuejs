<template>
  <div class="interview">
    <!-- <img src="@/assets/img/home-interview-parallax.jpg" alt="interview"> -->
    <p>"I just listened to it and said to myself, "Man, I really love this album." Still, today, it just sounds so fresh. It sounds full of ideas. These guys knew what they were doing. They're good. And they're inventive. I haven't heard anything this year that's as inventive. I don't really expect to."</p>
    <img src="@/assets/img/band_interview_play_icon.png" alt="play button">
  </div>
</template>

<script>
export default {
    name: 'interviewComponent'
}
</script>

<style lang="scss" scoped>
img{
    width: 70px;
}
p{
    font-size: 1.8rem;
    font-style: oblique;
    margin-bottom: 2rem;
}
.interview{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: white;
    width: 45%;
    text-align: center;
    margin: 0 auto;
    height: 1000px;
}
</style>
