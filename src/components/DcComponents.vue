<template>
<section>
    <div class="container">
        <span class="nowseries"> CURRENT SERIES</span>
        <div class="productlists">
            <ProductCard v-for="element, index in products" :key="index" :productDetails="element" />
        </div>
    </div>
    <div class="load">
        <span>Load More</span>
    </div>
</section>
</template>

<script>
import productsJson from '../assets/dc-comics.json';
import ProductCard from './ProductCard.vue';

export default {
    name:"DcComponents",
    components: {
    ProductCard
},
    data(){
        return{
            products : productsJson
        }
    }
}
</script>

<style lang="scss" scoped>

@import '../style/variables.scss';
    section{
        position: relative;
        background-color: black;
        color: white;
        padding: 10px 0; 
        .nowseries{
        background-color: $menunav_secondary_color;
        font-size: 25px;
        font-weight: 600;
        position: absolute;
        padding: 10px 35px;
        bottom: calc(100% - 25px);
        left: 15%;
        font-size: 25px;
        font-stretch: condensed;
    }
    .productlists{
        display: flex;
        flex-wrap: wrap;

    }
    .load{
        text-align: center;
        margin: 50px 0 20px;

        span{
            background-color: $menunav_secondary_color;
            padding: 10px 55px;
          font-size: 14px;
          font-weight: bold;
        }
        
    }
    }
    


    
</style>