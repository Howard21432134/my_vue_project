
<template>
  <div id="app">
    <h1 v-text = "title"></h1>
    <input v-model = "newItem" v-on:keyup.enter="addNew">
    <ul>
      <li v-for="item in items" v-bind:class = "{finished: item.isFinished}" v-on:click = "toggleFinish(item)">
        {{item.label}}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data : function(){
    return{
      title:'this is a todo list',
      items:[

      ],
      newItem:''
    }
  },
  methods:{
    toggleFinish: function(item){
      item.isFinished = !item.isFinished
    },
    addNew:function(){
      this.items.push({
        label:this.newItem,
        isFinished:false
      })
      this.newItem=''
    }
  }
}
</script>

<style>
.finished{
  text-decoration:underline;
}

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
