<template>
    <div class="container-fluid mt-5">
        <div class="row">
            <div class="col-4">
            <!-- Todo List  -->
                <todo-list title="Todo List">
                <draggable
                    :list="todos"
                    group="todosApp"
                    ghostClass="on-drag"
                    animation="400"
                >
                        <todo-item v-for="todo in todos" :key="todo.id" :item="todo"></todo-item>
                </draggable>
                    </todo-list>
            </div>
            <div class="col-4">
             <!-- Inprogress List  -->
            <todo-list title="Inprogress List">
                <draggable
                    :list="inProgress"
                    group="todosApp"
                    ghostClass="on-drag"
                    animation="400"
                >
                        <todo-item v-for="todo in inProgress" :key="todo.id" :item="todo"></todo-item>
                </draggable>
            </todo-list>

            </div>
            <div class="col-4">
                <!-- Completed List  -->
                <todo-list title="Completed List">
                    <draggable
                        :list="completed"
                        group="todosApp"
                        ghostClass="on-drag"
                        animation="400"
                    >
                            <todo-item v-for="todo in completed" :key="todo.id" :item="todo"></todo-item>
                    </draggable>
                </todo-list>
            </div>
        </div>
    </div>
</template>

<script>
import TodoList from './components/TodoList'
import TodoItem from './components/TodoItem'
import draggable from 'vuedraggable'

export default {
    components:{
        TodoList,
        TodoItem,
        draggable
    },
    data:() => ({
        // todo List
        todos: [
            {id: 1, todo: 'Todo'},
            {id: 2, todo: 'Todo 2'},
        ],

        // Inprogress List
        inProgress: [
            {id: 3, todo: 'Todo 3'},
            {id: 4, todo: 'Todo 4'},
        ],

        // Completed List
        completed: [
            {id: 5, todo: 'Todo 5'},
            {id: 6, todo: 'Todo 6'},
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

.on-drag{
    background-color: #4833c0;
    color: #fff;
    z-index: 10;
}
</style>
