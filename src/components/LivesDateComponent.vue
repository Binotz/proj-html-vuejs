<template>
  <div class="container">
    <ul class="li-dates-list">
        <li>
            <i class="fa-solid fa-plus"></i>
            <span>17/08/2020 gem festival 2020 anakalia, georgia</span>
        </li>
        <li>
            <i class="fa-solid fa-plus"></i>
            <span>24/9/2020 groovefest dominical republic</span>
        </li>
        <li>
            <i class="fa-solid fa-plus"></i>
            <span>31/10/2020 oasis festival 2020 marrakech, morocco</span>
        </li>
        <li>
            <i class="fa-solid fa-plus"></i>
            <span>07/11/2020 moga festival - essaouria, morocco</span>
        </li>
        <li>
            <i class="fa-solid fa-plus"></i>
            <span>10/12/2020 envision festival - uvita, costa rica</span>
        </li>
    </ul>
  </div>
</template>

<script>
export default {
    name: "LivesDateComponent"
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
}
</style>
