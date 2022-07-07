<template>
<footer>
    <div class="footer-top">
        <div class="container">
            <div class="dccomics">
            <h1>DC COMICS</h1>
                        <ul>
                            <li v-for="link, index in menuLinks" :key="index">
                                <a href="#">
                                    {{link.name}}
                                </a>
                            </li>
                        </ul>
                        <h1>SHOP</h1>
                        <ul>
                            <li v-for="link, index in shop" :key="index">
                                <a href="#">
                                    {{link.name}}
                                </a>

                            </li>
                        </ul>
            </div>
           <div class="dc">
                <h1>DC</h1>
                        <ul>
                            <li v-for="link, index in dc" :key="index">
                                <a href="#">
                                    {{link.name}}
                                </a>
                            </li>
                        </ul>
           </div>
           <div class="sites">
                <h1>SITES</h1>
                        <ul>
                            <li v-for="link, index in sites" :key="index">
                                <a href="#">
                                    {{link.name}}
                                </a>
                            </li>
                        </ul>
           </div>
            <div class="image">
            <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>

       
         
    </div>
    <div class="footerbottom">
        <div class="container">
            <div class="sign">
                <h1>SIGN-UP NOW!</h1>
            </div>
            
            <div class="icon">
                <h3>FOLLOW US</h3>
                        <ul>
                            <li v-for="link, index in icon" :key="index">
                               <img :src="link.img" :alt="link.alt">
                            </li>
                        </ul>
            </div>
        </div>
        
    </div>
</footer>
</template>

<script>
export default{
    name: "PageFooter",
    data(){
        return{
            menuLinks: [
                {
                     name: "Characters"
                },
                {
                     name: "Comics"
                },
                {
                     name: "movies"
                },
                {
                     name: "Tv"
                },
                {
                     name: "Games"
                },
                {
                     name: "Videos"
                },
                {
                     name: "News"
                },
            ],
            shop: [
                {
                    name:"Shop DC"
                },
                {
                    name:"Shop DC Collectibles"
                }
            ],
            dc:[
                {
                    name:"Term of Use"
                },
                {
                    name:"Privacy policy(New)"
                },
                {
                    name:"Ad Choices"
                },
                {
                    name:"Advertising"
                },
                {
                    name:"Jobs"
                },
                {
                    name:"Subscription"
                },
                {
                    name:"Talent Workshops"
                },
                {
                    name:"CPSC Certificates"
                },
                {
                    name:"Ratings"
                },
                {
                    name:"Shop Help"
                },
                {
                    name:"Contact us"
                },
            ],
            sites:[
                {
                    name:"DC"
                },
                {
                    name:"MAD Magazine"
                },
                {
                    name:"DC Kids"
                },
                {
                    name:"DC Universe"
                },
                {
                    name:"DC Power Visa"
                },
            ],
            icon:[
                {
                    img:require('../assets/img/footer-facebook.png')
                },
                {
                    img:require('../assets/img/footer-twitter.png')
                },
                {
                    img:require('../assets/img/footer-youtube.png')
                },
                {
                    img:require('../assets/img/footer-pinterest.png')
                },
                {
                    img:require('../assets/img/footer-periscope.png')
                }
            ]
           
        }
    }
}
</script>

<style lang="scss" scoped>

@import '../style/variables.scss';
footer{
    .footer-top{
        height: 350px;
        background-image: url('../assets/img/footer-bg.jpg');
        display: flex;
        .container{
            display: flex;
        }
        h1{
            color: white;
            font-size: 15px;
            padding-top: 20px;
        }
        li{
            padding: 2px;
             a{
                color: $footer_color_menu;
                text-decoration: none;
                font-size: 13px;
             }
        }
        .dc{
            margin-left: 20px;
        }
        .sites{
            margin-left: 20px;
        }
        .image{
            margin-left: 200px;
            img{
                width: 350px;
                padding-bottom: 20px;
                background-size: cover;
            }
        }
    }
    .footerbottom{
        height: 150px;
        background-color: #303030;
        padding-top: 30px;

        .container{
            display: flex;
            justify-content: space-between;
        }

        h1{
            border: 3px solid #0778e1 ;
            color: white;
            font-size: 15px;
            width: 100%;
            padding: 10px;
        }

        h3{
            color: #0778e1;
            padding-top: 5px;
        }
        .icon{
            display: flex;
            ul{
                display: flex;
            }
            li{
                padding: 5px;
            img{
                width: 70%;
            }
        }
        }
    }
}
</style>