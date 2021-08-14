<template>
    <div class="container">
        <div class="row">
            <div class="col-4">
                <!-- Todo List  -->
                <todo-list title="Todo List">
                    <todo-item v-for="todo in todos" :key="todo.id" :item="todo"></todo-item>
                </todo-list>
            </div>
            <div class="col-4">
                <!-- Inprogress List  -->
                <todo-list title="Inprogress List">
                    <todo-item v-for="todo in inProgress" :key="todo.id" :item="todo"></todo-item>
                </todo-list>
            </div>
            <div class="col-4">
                <!-- Completed List  -->
                <todo-list title="Completed List">
                    <todo-item v-for="todo in completed" :key="todo.id" :item="todo"></todo-item>
                </todo-list>
            </div>
        </div>
    </div>
</template>

<script>
import TodoList from './components/TodoList'
import TodoItem from './components/TodoItem'

export default {
    components:{
        TodoList,
        TodoItem
    },
    data:() => ({
        // todo List
        todos: [
            {id: 1, todo: 'Todo'},
            {id: 2, todo: 'Todo 2'},
        ],

        // Inprogress List
        inProgress: [
            {id: 1, todo: 'Todo'},
            {id: 2, todo: 'Todo 2'},
        ],

        // Completed List
        completed: [
            {id: 1, todo: 'Todo'},
            {id: 2, todo: 'Todo 2'},
        ],

    }),
}
</script>

<style>
.app{
    display:flex;
    justify-content:center;
    margin: 50px 0;
}
</style>
