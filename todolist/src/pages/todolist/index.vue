<template>
    <div class="todolist">
        <div class="head">
            <input type="text" v-model='task' />
            <button @click="addItem">提交</button>
        </div>
        <transition-group  class="list" tag='ul' name="fade" appear>
            <li 
                class="item"
                v-for="item in list"
                :key="item.id"
                @click="delItem(item.id)"
            >
                {{item.task}}
            </li>
        </transition-group>
        <p class="footer">共计{{total}}个项目</p>
    </div>
</template>
<script>
export default {
    name:'Todolist'
}
</script>