<template>
 <div>
  <p>我是comTow组件的内容区域</p>
  {{msg}}
  <button @click="comTow">我想向app组件中发射数据</button>
 </div>
</template>
<script>
export default {
  name: 'comTow',
  data () {
    return {
      msg: '我是comTow组件中的内容'
    }
  },
  //想办法去发射一个sender
  methods:{
      comTow(){
        //每一个vue实例提供了一个$emit的方法,携带两个参数,一个是事件,第二个参数可以是自己的msg
        this.$emit('sender',this.msg)
      }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
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
