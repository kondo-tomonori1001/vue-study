<template>
  <div id="app">
    <HelloWorld :msg="msg"/>
    <List :pageNum="pageNum"/>
    <ParentShow />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import List from './components/List';
import ParentShow from './components/child2parent/ParentShow';

export default {
  name: 'App',
  components: {
    HelloWorld,
    List,
    ParentShow
  },
  data(){
    return {
      msg:"Welcome to Your Vue.js App",
      pageNum:7,
    }
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
