<template>
  <footer>
    <div class="footer-top">
        <img src="@/assets/img/avada-music-logo-retina.png" alt="footer logo">
        <ul>
            <li v-for="(elem, index) in menuList" :key="index">
                <a :href="elem.link"> {{ elem.text }} </a>
            </li>
        </ul>
    </div>
    <div class="footer-bottom">
        <p class="credits">
            Copyright 2012 - 2020 | AVADA THEME BY THEMEFUSION | ALL RIGHTS RESERVED | POWERED BY WORDPRESS
        </p>
        <div class="socials-icons">
            <i class="fa-brands fa-facebook-f"></i>
            <i class="fa-brands fa-twitter"></i>
            <i class="fa-brands fa-instagram"></i>
        </div>
    </div>
  </footer>
</template>

<script>
export default {
    name: "FooterComponent",
    props:{
        menuList: Array
    }
}
</script>

<style lang="scss" scoped>
@import '@/assets/variables.scss';
.footer-top{
    display: flex;
    justify-content: space-between;
    background-color: $gray;
    img{
        width: 300px;
        padding: 3rem;
    }
    ul{
        display: flex;
        gap: 1rem;
        align-items: center;
        padding-right: 1rem;
        a{
            text-decoration: none;
            color: $light_gray;
        }
    }
}
.footer-bottom{
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: $primary_color;
    color: $light_gray;
    .credits{
        padding: 3rem;
        font-size: .6rem;
        margin-bottom: 0;
    }
    .socials-icons{
        i{
            padding: .8rem;
            background-color: $gray;
            margin-left: .3rem;
            color: $light_gray;
        }
    }
}
</style>
