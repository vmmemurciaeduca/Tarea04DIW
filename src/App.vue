<template>
    <div>
        <Header />
        <hr />
        <Breadcrumbs :path="path" />
        <ProductPage/>
        <Footer />
    </div>
  
</template>

<script>
import Breadcrumbs from './components/Breadcrumbs.vue'
import Footer from './components/Footer.vue'
import Header from './components/Header.vue'
import ProductPage from './components/ProductPage.vue'

export default {
  name: 'App',
  components: {
    Footer,
    Header,
    ProductPage,
    Breadcrumbs
  },
  data() {
    return {
      path: ['Hardware VR', 'Oculus Rift'],
    }
  }
}
</script>

<style>

body{
  margin: 0px;
  padding: 0px;
  box-sizing: border-box;
}

hr {
  border:none;
  height: 20px;
  height: 50px;
  margin-top: 0;
  border-bottom: 1px solid #FFD55E;
  box-shadow: 0 20px 20px -20px #333;
  margin: -50px auto 10px; 
}

</style>
