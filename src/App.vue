<template>
  <div id="app">
    <Son :tell_son="sendMsgToSon"></Son>
    <p>来自子组件的信息{{receiveMsgFromSon}}</p>
    <Child v-on:tell_dad="receiveMsg"></Child>
  </div>
</template>

<script>
import Son from './components/Son.vue';
import Child from './components/Child.vue'

export default {
  name: 'App',
  data(){
    return{
      sendMsgToSon:'Msg From Dad',
      receiveMsgFromSon:''
    }
  },
  components: {
    Son,
    Child
  },
  methods:{
    receiveMsg(data){
      this.receiveMsgFromSon = data;
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
