<template>
  <div id="app">
    <h1>Displaying Data Using Emit</h1>
  <!--  <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Result />
    <Loop />
    <Parent />
    <Child /> 
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
//import Result from './components/Result.vue'
//import Loop from './components/Loop/Loop.vue'
import Parent from './components/Parent.vue'
import Child from './components/Child.vue'

export default {
  name: 'App',
  components: {
  //  HelloWorld
  //Loop
  //Result
  Parent,
  Child,
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
