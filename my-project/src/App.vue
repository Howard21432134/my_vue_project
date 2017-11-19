
<template>
  <div id="app">
    <h1>{{title}}</h1>
  </div>
</template>

<script>
import Hello from './components/Hello'
export default {
  data : function(){
    return{
      title:'this is a todo list'
    }
  }
}
</script>

<style>
html{
height :100%;
}
body{
  display:flex;
  align-items:center;
  justify-content:center;
  height:100%;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
