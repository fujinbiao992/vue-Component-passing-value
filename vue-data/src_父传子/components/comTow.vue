<template>
 <div>
  <p>我是comTow组件的内容区域</p>
  {{msg}}
 </div>
</template>
<script>
export default {
  name: 'comTow',
  data () {
    return {
      msg: '我是comTow组件中的内容'
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
