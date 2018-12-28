<template>
  <div id="app">
    <p>我是app组件的内容</p>
    {{msg}}
    <br>
    <p>{{test}}</p>
    <hr>
    <br>
    <com-one :dataOne="msg"></com-one>
    <br>
    <br>
    <hr>
    <br>
    <!--
      click事件名称
      on-事件监听(始终看着你,当看到消息变化,就去执行处理函数)
      sender可以是自定义的,
     -->
    <com-tow v-on:sender="sender"></com-tow>
    <br>

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
      test:''
    }
  },
  components:{
    comOne,
    comTow
  },
  methods:{
    senter(val){
      console.log(val)
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
