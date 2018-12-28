<template>
  <div id="app">
    <p>我是app组件的内容</p>
    {{msg}}
    <br>
    <hr>
    <br>
    <com-one></com-one>
    <br>
    <br>
    <hr>
    <br>
    <com-tow></com-tow>
    <br>
<!--
因为生命周期的原因,所以会导致渲染执行的顺序不一样,主要集中在on(监听)emit(发射)的前后执行顺序上



 -->
  </div>
</template>

<script>
//引入
import comOne from '@/components/comOne.vue'
import comTow from '@/components/comTow.vue'
export default {
  name:'App',
  data(){
    return {
      msg:'我是app组件的内容区域',
    }
  },
  components:{
    comOne,
    comTow
  },
  methods:{
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
