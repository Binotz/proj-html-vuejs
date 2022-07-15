<template>
  <header>
    <!-- Logo & menu -->
    <div class="header-bar">
        <img src="@/assets/img/avada-music-logo.png" alt="logo">
        <div class="menu">
            <i class="fa-solid fa-bars"></i>
        </div>
    </div>
    <!-- jumbotron content -->
    <div class="jumbotron">
        <h1>Untold Stories</h1>
        <h4>There is an untold story behind every favorite song.</h4>
        <div class="jumbotron-links">
            <a href="#" class="btn latest">Latest album</a>
            <a href="#" class="btn live">Live dates</a>
        </div>
    </div>
  </header>
</template>

<script>
export default {
    name: "HeaderComponent"
}
</script>

<style lang="scss" scoped>
@import '@/assets/variables.scss';

    header{
        background-image: url('@/assets/img/home_slider.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        height: 1000px;
    }
    .header-bar{
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 140px;
        padding: 2rem 4rem;
        i{
            color: white;
            font-size: 2rem;
        }
    }
    .jumbotron{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        height: calc(100% - 140px);
        color: white;
        h1{
            font-size: 8rem;
            margin-bottom: 1rem;
        }
        h4{
            margin-bottom: 3rem;
            font-style: italic;
            font-weight: 400;
        }
        .jumbotron-links{
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 1rem;
            a{
            color: white;
            text-decoration: none;
            &.btn{
                padding: 9px 25px;
                text-transform: uppercase;
                &.latest{
                    background-color: $secondary_color;
                }
                &.live{
                    border: 1px solid $white;
                }
            }
        }
        }
    }
</style>
