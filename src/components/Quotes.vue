<template>
  <div id='app'>
    {{msg}}
    <br>
    <br>
    <input v-model="message" placeholder="Add quote">
    <!--<p>Message is: {{ message }}</p>-->
    <input @click='addQuote()' type="button" value="Add Quote" />
    <br>
    <li v-for="(input, index) in quotes" :key="index">

      <h3 v-on:click="removeElement(input)">{{input}}</h3>  

    </li>
  </div>
</template>

<script>
export default {

  data(){

    return{
      message:'',
      quotes: [],
      

    }

  },

  props:{ //padre e hijo
    msg: String
    
  },
  methods:{
    addQuote(){
  
      this.quotes.push(this.message)
      this.message = " "
      },

    removeElement(input){
      var quoteIndex = this.quotes.indexOf(input)
  
      this.quotes.splice(quoteIndex, 1)  
      }

    }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
