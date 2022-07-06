<template>
<section>
    <div>
        <div class="products">
            <div class="container">
                 <span> -->Content goes here  </span>
            </div>
           
        </div>
        <ul class="dc-menu">
            <div class="container menu">
                 <li v-for="link, index in productsLink" :key="index">
                <img :src="link.image" :alt="link.alt">
                <a :href="link.url">
                    {{link.text.toLocaleUpperCase()}}
                </a>
            </li>
            </div>
           
        </ul>
    </div>
</section>
</template>

<script>
export default{
    name: "ProductList",
    data(){
        return{
            productsLink:[
                {
                    image: require('../assets/img/buy-comics-digital-comics.png'),
                    text:"DIGITAL COMICS",
                     url: '#',
                     alt:'Digital Comics'
                },
                 {
                    image: require('../assets/img/buy-comics-merchandise.png'),
                    text:"DC MERCHANDISE",
                     url: '#',
                     alt:'DC MERCHANDISE'
                },
                {
                    image: require('../assets/img/buy-comics-subscriptions.png'),
                    text:"SUBSCRIPTION",
                     url: '#',
                     alt:'SUBSCRIPTION'
                },
                {
                    image: require('../assets/img/buy-comics-shop-locator.png'),
                    text:"COMIC SHOP LOCATOR",
                     url: '#',
                     alt:'COMIC SHOP LOCATOR'
                },
                {
                    image: require('../assets/img/buy-dc-power-visa.svg'),
                    text:"DC POWER VISA",
                     url: '#',
                     alt:'DC POWER VISA'
                },
               
            ]
        };
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';
section{

    .products{
        background-color: $product_main_color;
         padding: 30px 0;
        span{
        color: white;
        }
    }
    .dc-menu{
        background-color: $dcmenu_main_color ;
        padding: 30px 10px;
        display: flex;
        .menu{
            display: flex;
        }
        li{
            padding: 0 10px ;
            justify-content: center;
           img{
            width: 50px;
            display: inline-block;
            margin-right: 10px;
            }

            a{
            text-decoration: none;
            color: white;
            font-size: 13px;
            margin-top: 20px;
            } 
        }
        
    }
   
}
</style>