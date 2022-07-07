<template>
  <div id="app">
   <PageHeader />
    <DcBanner :imgBanner="imgUrl" />
    <main>
      <DcComponents />
      <ProductList />
    </main>
    <PageFooter />
  </div>
 
</template>

<script>
import PageHeader from "./components/PageHeader.vue";
import ProductList from "./components/ProductList.vue";
import PageFooter from "./components/PageFooter.vue";
import DcComponents from "./components/DcComponents.vue";
import DcBanner from "./components/DcBanner.vue";


export default {
  name: 'App',
  components: {
    PageHeader,
    ProductList,
    PageFooter,
    DcComponents,
    DcBanner
  },
  data(){
    return{
      imgUrl: require("./assets/img/jumbotron.jpg")
    }
  }
}
</script>

<style lang="scss">
@import './style/common.scss';
</style>
