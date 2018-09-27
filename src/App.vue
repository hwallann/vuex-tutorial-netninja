<template>
  <div id="app">
    <product-list-one v-bind:products="products"></product-list-one>
    <product-list-two v-bind:products="products"></product-list-two>
  </div>
</template>

<script type="text/javascript">
  import ProductListOne from '@/components/ProductListOne.vue'
  import ProductListTwo from '@/components/ProductListTwo.vue'
  export default {
    name:'app',
    components: {
      'product-list-one': ProductListOne,
      'product-list-two': ProductListTwo
    },
    data () {
      return {
        products: [
        {name: 'Banana Skin', price: 20},
        {name: 'Shiny Star', price: 40},
        {name: 'Green Shell', price: 60},
        {name: 'Red Shell', price: 80},
        ]
      }
    }
  }
</script>
<style lang="stylus">
#app
  font-family 'Avenir', Helvetica, Arial, sans-serif
  -webkit-font-smoothing antialiased
  -moz-osx-font-smoothing grayscale
  text-align center
  color #2c3e50

#nav
  padding 30px
  a
    font-weight bold
    color #2c3e50
    &.router-link-exact-active
      color #42b983
</style>
