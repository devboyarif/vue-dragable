<template>
    <div class="todo-item">
        {{ item.todo }}
    </div>
</template>

<script>
export default {
    props: ['item'],
}
</script>

<style>
    .todo-item {
        padding:10px 20px;
        border:1px solid #EEE;
    }

    .todo-item:hover {
        cursor:move;
    }
</style>
