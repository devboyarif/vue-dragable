<template>
    <div class="todo-item">
        <div class="title">
            {{ title }}
        </div>
        <slot></slot>
    </div>
</template>

<script >
export default{
    props: ['title'],

}
</script>

<style>
.todo-item{
    padding: 10px 20px;
    margin: 0 10px;
    border: 1px solid #EEE;
    font-family: sans-serif;
}

.title{
    padding: 10px;
    font-size:20px;
    font-weight: 600;
    margin-bottom: 10px;
    text-align: center;
    border-bottom: 1px solid #EEE;
}
</style>
