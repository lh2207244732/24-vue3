<template>
    <div class="app">
       <p>{{person}}说</p>
        <button
        @click="add"
        >
          我被点击了{{count}}次
        </button>
    </div>
</template>

<script>

export default {
  name: 'App',
  /*
  data(){
    return{   
      person:'Tom',
      count:1
    } 
  },
  methods:{
    add(){
      this.count+=1
    }
  }
  */
  setup(){//组合API的入口
  
  }
}
</script>
