<template>
  <div id="app">
    <p> 我是 app 根组件区域 </p>
    {{ msg }}
    <br>
    <hr>
    <br>
    <com-one></com-one>
    <br>
    <hr>
    <br>
    <com-two></com-two>
  </div>
</template>
<script>
import comOne from '@/components/comOne.vue'
import comTwo from '@/components/comTwo.vue'
export default {
  name: 'App',
  data () {
    return {
      msg: 'w我是 app 根组件的内容'
    }
  },
  components: {
    comOne,
    comTwo
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
