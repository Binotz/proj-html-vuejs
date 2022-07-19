<template>
  <footer>
    <div class="footer-top">
        <img src="@/assets/img/avada-music-logo-retina.png" alt="footer logo">
        <ul>
            <li v-for="(elem, index) in menuList" :key="index">
                <a :href="elem.link" :class="{'active': elem.currentPage}" @mouseenter="setCurrent(index)"> {{ elem.text }} </a>
            </li>
        </ul>
    </div>
    <div class="footer-bottom">
        <p class="credits">
            Copyright 2012 - 2020 | AVADA THEME BY THEMEFUSION | ALL RIGHTS RESERVED | POWERED BY WORDPRESS
        </p>
        <div class="socials-icons">
            <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
            <a href="#"><i class="fa-brands fa-twitter"></i></a>
            <a href="#"><i class="fa-brands fa-instagram"></i></a>
        </div>
    </div>
  </footer>
</template>

<script>
export default {
    name: "FooterComponent",
    props:{
        menuList: Array
    },
    methods:{
        setCurrent: function(index){
            this.$emit('setCurrentPage', index);
            console.log(index);
        }
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
    .active{
        color: white;
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
