<template>
    <div class="app">
        <input type="text" >
        <!-- <p>lastName:{{lastName}}</p> -->
        <p>fullName:{{fullName.value}}</p>
    </div>
</template>

<script>
import {ref,computed} from 'vue'
export default {
  name: 'App',
  setup(props,context){
    let fullName=ref(1)
    const Person=computed({
      get:()=>fullName+=1,
      set:(val)=>{

      }
    }),
  // return {Person,fullName}
  return {}
  }
}
</script>
