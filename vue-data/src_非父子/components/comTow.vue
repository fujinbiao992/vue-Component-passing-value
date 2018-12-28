<template>
 <div>
  <p>我是comTow组件的内容区域</p>
  {{msg}}
  <p>{{test}}</p>
 </div>
</template>

<script>
//导入bus
import bus from '@/bus.js'
export default {
  name: 'comTow',
  data () {
    return {
      msg: '我是comTow组件中的内容',
      test:''
    }
  },
  //想办法去发射一个sender
  methods:{

  },
  created(){
    //箭头函数才指向的是外部APP
     bus.$on('sender',(val)=>{
       console.log(val+'我是comTwo')
       this.test=val
     })
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
