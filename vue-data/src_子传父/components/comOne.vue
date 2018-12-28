<template>
  <div>
  <p>我是comOne组件的内容区域</p>
  {{msg}}
  <br>
  <br>
  {{dataOne}}
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
  return {
      msg: '我是comOne组件中的内容'
    }
  },
  //props属性,读取的是自己组件身上的属性,可以自定义属性值
  //props是属于comOne自己的东西,props身上的属性可以在当前组件身上随意的使用
  props:['dataOne']
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
