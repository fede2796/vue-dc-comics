<template>
<div class="wrapper">
    <img :src="productDetails.thumb">
    <h2>{{productDetails.series}}</h2>
</div>
</template>

<script>
export default{
    name: "ProductCard",
    props: {
        productDetails: Object
    }
}
</script>

<style lang="scss" scoped>

.wrapper{
    margin: 18px;
    width: calc((100%/6) - 36px);

    img{
        height: 185px;
        height: 185px;
        width: 100%;
        object-fit: cover;
        object-position: top;
        margin: 20px 0;
    }
}
</style>