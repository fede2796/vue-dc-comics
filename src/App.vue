<template>
  <div id="app">
   <PageHeader />

    <main>
      <ProductList />
    </main>
    <PageFooter />
  </div>
 
</template>

<script>
import PageHeader from "./components/PageHeader.vue";
import ProductList from "./components/ProductList.vue";
import PageFooter from "./components/PageFooter.vue";


export default {
  name: 'App',
  components: {
    PageHeader,
    ProductList,
    PageFooter
}
}
</script>

<style lang="scss">
@import './style/common.scss';
</style>
