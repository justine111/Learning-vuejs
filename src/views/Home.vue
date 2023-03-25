<template>
    <h1>To-Do List</h1>
    <TodoList location="home"/>
</template>

<script>
    import TodoList from '../components/TodoList.vue';

    export default { 
        name: "HomePage",
        components: {
            TodoList
        }
    }
</script>

<style>
    h1 {
        font-weight: 600;
        font-size: 1.5rem;
        margin: 3rem 0 2rem 0;
        text-align: center;
    }
</style>
