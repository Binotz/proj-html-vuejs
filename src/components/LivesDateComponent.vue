<template>
  <div class="container">
    <ul class="li-dates-list">
        <li v-for="(date,index) in datesList" :key="index">
            <i class="fa-solid fa-plus" @click="showCard(index)"></i>
            <span @click="showCard(index)">{{ date.title }}</span>
            <div class="expanded-info" :class="{'d-none': index !== currentCard}">
                <img src="@/assets/img/fss-demo-main.jpg" alt="Maps">
                <div class="info-text">
                    <h3>{{date.infoTitle}}</h3>
                    <p>{{date.infoDescription}}</p>
                    <a :href="date.bookLink">BOOK NOW</a>
                </div>
            </div>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
    name: "LivesDateComponent",
    data(){
        return{
            hideCard: true,
            currentCard: -1,
            datesList:[
                {
                    title: '17/08/2020 gem festival 2020 anakalia, georgia',
                    map: '@/assets/img/fss-demo-main.jpg',
                    infoTitle: 'Untold Stories',
                    infoDescription: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur esse deserunt, quaerat excepturi, nostrum nemo quam tempore atque sapiente nobis ea molestias modi ad repudiandae dolores? Laborum expedita saepe incidunt.',
                    bookLink: '#'
                },
                {
                    title: '24/9/2020 groovefest dominical republic',
                    map: '@/assets/img/fss-demo-main.jpg',
                    infoTitle: 'Untold Stories',
                    infoDescription: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur esse deserunt, quaerat excepturi, nostrum nemo quam tempore atque sapiente nobis ea molestias modi ad repudiandae dolores? Laborum expedita saepe incidunt.',
                    bookLink: '#'
                },
                {
                    title: '31/10/2020 oasis festival 2020 marrakech, morocco',
                    map: '@/assets/img/fss-demo-main.jpg',
                    infoTitle: 'Untold Stories',
                    infoDescription: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur esse deserunt, quaerat excepturi, nostrum nemo quam tempore atque sapiente nobis ea molestias modi ad repudiandae dolores? Laborum expedita saepe incidunt.',
                    bookLink: '#'
                },
                {
                    title: '07/11/2020 moga festival - essaouria, morocco',
                    map: '@/assets/img/fss-demo-main.jpg',
                    infoTitle: 'Untold Stories',
                    infoDescription: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur esse deserunt, quaerat excepturi, nostrum nemo quam tempore atque sapiente nobis ea molestias modi ad repudiandae dolores? Laborum expedita saepe incidunt.',
                    bookLink: '#'
                },
                {
                    title: '10/12/2020 envision festival - uvita, costa rica',
                    map: '@/assets/img/fss-demo-main.jpg',
                    infoTitle: 'Untold Stories',
                    infoDescription: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur esse deserunt, quaerat excepturi, nostrum nemo quam tempore atque sapiente nobis ea molestias modi ad repudiandae dolores? Laborum expedita saepe incidunt.',
                    bookLink: '#'
                },
            ],
        }
    },
    methods:{
        showCard: function(index){
            (index === this.currentCard) ? this.currentCard = -1 : this.currentCard = index;
        }
    }
}
</script>

<style lang="scss" scoped>
@import '@/assets/variables.scss';
.li-dates-list{
    margin-bottom: 4rem;
    li{
        width: 100%;
        padding: 1rem;
        background-color: $gray;
        margin-bottom: .5rem;
        i{
            color: white;
            padding: 0 1rem;
            font-size: .6rem;
        }
        span{
            color: $secondary_color;
            text-transform: uppercase;
        }
    }
    .expanded-info{
        display: flex;
        padding: 1rem;
        padding-top: 2rem;
        img{
            width: calc(100% / 3);
            margin-right: 3rem;
        }
        .info-text{
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            h3{
                color: white;
                padding-top: 1rem;
            }
            p{
                color: $lynch;
            }
            a{
                align-self: flex-start;
                padding: 1rem 3rem;
                background-color: $mandy;
                color: white;
                text-decoration: none;
                border-radius: 5px;
            }
        }
    }
}
</style>
