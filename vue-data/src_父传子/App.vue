<template>
  <div id="app">
    <p>我是app组件的内容</p>
    {{msg}}
    <br>
    <hr>
    <br>
    <!--
      com-one是一个属于app自己的tempale中的属性,
      在app这个组件内部的tempale属性中,可以使用APP组件里边的数据
      动态的去绑定App自己里的msg属性
     -->
    <com-one :dataOne="msg"></com-one>
    <br>
    <br>
    <hr>
    <br>
    <!-- 
      
     -->
    <com-tow></com-tow>
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
      msg:'我是app组件的内容区域'
    }
  },
  components:{
    //注册组件
    comOne,
    comtow
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
