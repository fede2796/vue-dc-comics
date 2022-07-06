<template>
  <div id="app">
   <PageHeader />

    <main>
      <ProductList />
    </main>
  </div>
 
</template>

<script>
import PageHeader from "./components/PageHeader.vue";
import ProductList from "./components/ProductList.vue";


export default {
  name: 'App',
  components: {
    PageHeader,
    ProductList,
}
}
</script>

<style lang="scss">
@import './style/common.scss';
</style>
