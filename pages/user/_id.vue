<template>
    <div>
        这里是用户的动态路由的形式 用户信息：“李钦”
        <br>
        用户的id:{{$route.params.id}}
        <hr>

        <ul>
            <li v-for="todo in todos" :key="todo.text">
                <input type="checkbox" :checked="todo.done" @change="toggle(todo)">

                <span :class="{ done: todo.done }">{{ todo.text }}</span>
            </li>
            <li>
                <input type="text" 
                placeholder="what needs to be done"
                @keyup.enter="addTodo"
                >
            </li>
        </ul>
    </div>
</template>
<script>
import {mapMutations} from 'vuex'
export default {
    computed:{
        // todos(){
        //     return this.$store.state.todos.list
        // },
        todos () { return this.$store.state.todos.list }
    },
    methods:{
       addTodo(e){
           this.$store.commit("todos/add",e.target.value);
           e.target.value = ''
       },
       ...mapMutations({
           toggle:'todos/toggle'
       })

    },
    data(){
        return{
            info:{
                l:'李',
                w:'王'
            }
        }
    }
}
</script>
<style>
.done {
  text-decoration: line-through;
}
</style>

