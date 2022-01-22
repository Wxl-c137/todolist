<template>
    <ul class="todo-main">
        <Item v-for="todoObj in todos" :key="todoObj.id" :todo="todoObj" />
        <Item />
        <Item />
        <Item />
    </ul>
</template>

<script>
import Item from './Item'

export default {
    name: 'List',
    components: { Item },
    data() {
        return {
            todos: [
                { id: '001', title: '111', done: true },
                { id: '001', title: '111', done: true },
                { id: '001', title: '111', done: true }
            ]
        }
    },
}
</script>

<style scoped>
/*main*/
.todo-main {
    margin-left: 0px;
    border: 1px solid rgba(100, 53, 175, 0.397);
    border-radius: 2px;
    padding: 0px;
}

.todo-empty {
    height: 40px;
    line-height: 40px;
    border: 1px solid #ddd;
    border-radius: 2px;
    padding-left: 5px;
    margin-top: 10px;
}
</style>