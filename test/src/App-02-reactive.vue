<template>
    <div class="app">
       <p>{{msg}}说</p>
       <button @click="add" >我被点击了{{counts.value}}次</button>
    </div>
</template>

<script>
import {reactive} from 'vue'
export default {
  name: 'App',
  data(){
    return{
       msg:'Tom'
    }
  },
  setup(props,context){//组合API的入口,在beforeCreateh和created之前执行
  // reactive把一个复杂数据类型包装成一个响应式数据(proxy实例)
    let counts=reactive({value:0})//返回一个proxy实例
    const add=()=>{
      counts.value +=1  
    }
    return {add,counts}
  }
}
</script>
