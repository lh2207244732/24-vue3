<template>
    <div class="app">
       <p>{{msg}}说</p>
       <button @click="add" >我被点击了{{counts}}次</button>
    </div>
</template>

<script>
import {reactive,ref} from 'vue'
export default {
  name: 'App',
  data(){
    return{
       msg:'Tom'
    }
  },
  setup(props,context){//组合API的入口,在beforeCreateh和created之前执行
  // ref把一个普通数据类型包装成一个响应式数据(proxy实例)
  // ref(0)=reactive({value:0})
    let counts=ref(0)//返回一个ref类型的响应式数据
    const add=()=>{
      console.log(counts)
      counts.value +=1  
    }
    return {add,counts}
  }
}
</script>
