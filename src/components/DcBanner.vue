<template>
  <div>
    <img :src="imgBanner" alt="">
  </div>
</template>

<script>
  export default {
    name: "DcBannerComp",
    props: {
      imgBanner: String,
    }
  }
</script>

<style lang="scss" scoped>
  div{
    height: 400px;
    img {
      height: 100%;
      object-fit: cover;
      object-position: top;
    }
  }
</style>