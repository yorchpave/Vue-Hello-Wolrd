<template>
  <div id="app">
    
    <Quotes msg="Jorge Padilla alv"/>
    <p v-for="(q, index) in quotes" :key="index">{{q}}</p>
  </div>
</template>

<script>
import Quotes from './components/Quotes.vue'

export default {
  name: 'app',
  mounted() {
    this.$on('newQuote', (quote) => {
      console.log('quote: ', quote)
      this.quotes.push(quote)
      })
  },
  components: {
    Quotes
  }, data(){
    return{
      quotes: ["algo"]
    }
  }
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
