<template>
  <div id="app">
    <HelloWorld v-bind:value="facts"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data(){
    return{
      facts: {
        fact: ""
      }
    }
  },
  methods:{
    getFact(){
      this.axios.get('http://37.77.104.246/api/random-fact.php')
      .then((response)=>{
        this.facts.fact = response.data;
      })
    }
  },
  mounted(){
    this.getFact();
    
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
