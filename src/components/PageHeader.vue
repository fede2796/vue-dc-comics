<template>
<header class="container">
    <!-- Header Logo -->
    <div class="logo-dc">
        <img src="../assets/img/dc-logo.png" alt="Logo DC">
    </div>
    <!-- Header Nav -->
    <nav>
        <ul class="menu">
            <li v-for="link , index in menuLinks" :key="index" :class="{'current': link.current}">
                <a href="link.url">{{link.text}}</a>
            </li>
        </ul>
    </nav>
</header>
</template>

<script>
export default{
    name: "PageHeader",
    data(){
        return{
            menuLinks:[
            {
                text:"CHARACTERS",
                url:'#',
                current:false
            },
            {
                text:"COMICS",
                url:'#',
                current:true
            },
            {
                text:"MOVIES",
                url:'#',
                current:false
            },
             {
                text:"TV",
                url:'#',
                current:false
            },
             {
                text:"GAMES",
                url:'#',
                current:false
            },
             {
                text:"COLLECTIBLES",
                url:'#',
                current:false
            },
             {
                text:"VIDEOS",
                url:'#',
                current:false
            },
             {
                text:"FANS",
                url:'#',
                current:false
            },
             {
                text:"NEWS",
                url:'#',
                current:false
            },
             {
                text:"SHOP",
                url:'#',
                current:false
            },

           
            ],
             
        };
    }
}
</script>

<style lang="scss" scoped>
@import '../style/variables.scss';

header{
    display: flex;
    justify-content: center;
    justify-content: space-between;
    margin-top: 30px;
    //  Logo

    .logo-dc{
        text-align: center;
        img{
            width: 70px;
            display: inline-block;
        }
    }

    // Menù
    .menu{
        display: flex;
        justify-content: center;
        margin-top: 20px;

        li{
            padding: 8px;

            a{
            color: $menunav_main_color;
            text-decoration: none;
            font-size: 13px;
            }
             &.current{
                color:$menunav_secondary_color;
                border-bottom: 5px solid  $menunav_secondary_color;
                padding-bottom: 40px;
            }
            &.current a{
                color:$menunav_secondary_color ;
            }
        
           
        }
        
    }
}
</style>