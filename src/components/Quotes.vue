<template>
  <div id='app'>
    {{msg}}
    <p>perrro</p>
    <textarea v-model="quote" name="textarea" id="ta" cols="30" rows="10"></textarea>
    <input @click='addQuote' type="button" value="Add Quote" />
    {{quote}}



  
    
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data(){
    return{
      name: ' Jorge', 
      quote: ''

    }

  },
  methods:{
    addQuote(){
      
      this.$emit('newQuote', this.quote)
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
