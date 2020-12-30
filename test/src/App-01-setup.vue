<template>
    <div class="app">
       hello
    </div>
</template>

<script>

export default {
  name: 'App',
  beforeCreate(){
    console.log('beforeCreate...')
  },
  created(){
    console.log('created...')
  },
  setup(props,context){//组合API的入口,在beforeCreateh和created之前执行
    console.log('setup...')
    console.log(props)
    console.log(context)
  }
}
</script>
