<template>
  <div>
  <p>我是comOne组件的内容区域</p>
  {{msg}}
  <br>
  <br>
  <button @click="comOneBus">发射数据</button>
  </div>
</template>

<script>
//引入
import bus from '@/bus.js'
export default {
  name: "HelloWorld",
  data() {
  return {
      msg: '我是comOne组件中的内容'
    }
  },
  methods:{
    //this是发射给自己实例,这里是需要进行发射数据的位置!
    //想要发射给bus所以是bus.$emit
    comOneBus(){
       bus.$emit('sender',this.msg)
    }
 },
 //是因为生命周期渲染的问题,导致渲染顺序不一样!
created(){
  this.comOneBus()
}
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
