<template>
  <div id="app">
    
    <Quotes msg="Jorge Padilla"/>
  </div>
  

</template>

<script>
import Quotes from './components/Quotes.vue'

export default {
  name: 'app',
  //mounted() {
    //this.$on('newQuote', (quote) => {
      //console.log('quote: ')
      //this.quotes.push(quotes)

     // })
 // },
  components: {
    Quotes
  }//, data(){
    //return{
    //  quotes: []
    //}
  //}
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
