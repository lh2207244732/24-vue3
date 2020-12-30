<template>
    <div class="app">
      <p>f:{{familyAge.fatherAge}}</p>
      <p>s:{{familyAge.son.sonAge}}</p>
       <button @click="updata" >updata</button>
    </div>
</template>

<script>
import {shallowReactive} from 'vue'
export default {
  name: 'App',
  data(){
    return{
       msg:'Tom'
    }
  },
  setup(props,context){
    let familyAge=shallowReactive({
        fatherAge:45,
        son:{
          sonAge:18
        }
    }),
    updata=()=>{
      console.log(familyAge)
      familyAge.fatherAge+=1
      familyAge.son.sonAge+=1
    }
    return {updata,familyAge}
  }
}
</script>
