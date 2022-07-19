<template>
  <div class="container">
    <ul class="li-dates-list">
        <li v-for="(date,index) in datesList" :key="index">
            <i class="fa-solid fa-plus" @click="showCard(index)"></i>
            <span @click="showCard(index)">{{ date.title }}</span>
            <div class="expanded-info" :class="{'d-none': index !== currentCard}">
                <iframe :src="date.map" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
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
                    map: 'https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d5892.64075412956!2d41.5457671697754!3d42.39962239999998!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x405dd353aaaaaaab%3A0xc41938c02329eac9!2sGEM%20FEST!5e0!3m2!1sit!2sit!4v1658153373115!5m2!1sit!2sit',
                    infoTitle: 'Untold Stories',
                    infoDescription: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur esse deserunt, quaerat excepturi, nostrum nemo quam tempore atque sapiente nobis ea molestias modi ad repudiandae dolores? Laborum expedita saepe incidunt.',
                    bookLink: '#'
                },
                {
                    title: '24/9/2020 groovefest dominical republic',
                    map: 'https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d964355.9969704004!2d-70.10508426593894!3d19.23815131125682!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8ea89347d50f4aa7%3A0x1db3694f5f3d65b9!2sMeet*21%20Festival!5e0!3m2!1sit!2sit!4v1658153637318!5m2!1sit!2sit',
                    infoTitle: 'Untold Stories',
                    infoDescription: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur esse deserunt, quaerat excepturi, nostrum nemo quam tempore atque sapiente nobis ea molestias modi ad repudiandae dolores? Laborum expedita saepe incidunt.',
                    bookLink: '#'
                },
                {
                    title: '31/10/2020 oasis festival 2020 marrakech, morocco',
                    map: 'https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d108745.99417066008!2d-8.036573532708045!3d31.59790083495368!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0xdafef2e8604c055%3A0x2e898d4ce0c2d753!2sEPIC%20Yoga%20Festival%20Marrakech!5e0!3m2!1sit!2sit!4v1658153721905!5m2!1sit!2sit',
                    infoTitle: 'Untold Stories',
                    infoDescription: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur esse deserunt, quaerat excepturi, nostrum nemo quam tempore atque sapiente nobis ea molestias modi ad repudiandae dolores? Laborum expedita saepe incidunt.',
                    bookLink: '#'
                },
                {
                    title: '07/11/2020 moga festival - essaouria, morocco',
                    map: 'https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3401.3653420708793!2d-9.771762884562735!3d31.51412425460299!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0xdad9b090ed8e551%3A0xd912b3f1ec76e36a!2sMoga%20Hostel!5e0!3m2!1sit!2sit!4v1658153771922!5m2!1sit!2sit',
                    infoTitle: 'Untold Stories',
                    infoDescription: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur esse deserunt, quaerat excepturi, nostrum nemo quam tempore atque sapiente nobis ea molestias modi ad repudiandae dolores? Laborum expedita saepe incidunt.',
                    bookLink: '#'
                },
                {
                    title: '10/12/2020 envision festival - uvita, costa rica',
                    map: 'https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3938.683668564071!2d-83.77006798478872!3d9.182980289085677!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8fa159d1ab7ef603%3A0x97fedf8fe56d2356!2sEnvision%20Festival!5e0!3m2!1sit!2sit!4v1658153810104!5m2!1sit!2sit',
                    infoTitle: 'Untold Stories',
                    infoDescription: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Consequatur esse deserunt, quaerat excepturi, nostrum nemo quam tempore atque sapiente nobis ea molestias modi ad repudiandae dolores? Laborum expedita saepe incidunt.',
                    bookLink: '#'
                },
            ],
        }
    },
    methods:{
        showCard: function(index){
            // se clicco sull'elemento aperto, imposto la currentCard ad un numero negativo in modo da essere sicuro di non mostrare elementi, altrimenti la imposto come index
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
        iframe{
            width: calc(100% / 3);
            height: 200px;
            margin-right: 3rem;
        }
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
