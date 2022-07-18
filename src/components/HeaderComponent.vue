<template>
  <header>
    <!-- Logo & menu -->
    <div class="header-bar">
        <img src="@/assets/img/avada-music-logo.png" alt="logo">
        <div class="menu">
            <i class="fa-solid fa-bars" @click="triggerMenu()"></i>
            <div class="menu-open" :class="{'d-none': !displayMenu}">
                <div class="header-menu">
                    <img src="@/assets/img/avada-music-logo.png" alt="logo">
                    <i class="fa-solid fa-xmark" @click="triggerMenu()"></i>
                </div>
                <ul>
                    <li v-for="(page,index) in menuList" :key="index">
                        <a :href="page.link" @click="triggerMenu()">{{page.text}}</a>
                    </li>
                </ul>
            </div>
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
    name: "HeaderComponent",
    props:{
        menuList: Array
    },
    data(){
        return{
            displayMenu: false,
        }
    },
    methods:{
        triggerMenu: function(){
            this.displayMenu = !this.displayMenu;
        }
    }
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
                    &:hover{
                        background-color: white;
                        color: black;
                    }
                }
            }
        }
        }
    }
    .menu-open{
        position: fixed;
        top: 0;
        left: 0;
        bottom: 0;
        right: 0;
        background-color: $mandy;
        .header-menu{
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 2rem;
            i{
                padding-right: 2rem;
            }
        }
        img{
            padding-left: 2rem;
        }

        ul{
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 80%;
            li{
                font-size: 3rem;
                margin-bottom: 2rem;
                a{
                    text-decoration: none;
                    color: #f8959e;
                    &:hover{
                        color: white;
                    }
                }
            }
        }

    }
</style>
