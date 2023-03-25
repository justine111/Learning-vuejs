<template>
    <h1>Archived Items</h1>
    <TodoList location="archive" />
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
        font-size: 1.2rem;
        margin: 3rem 0 2rem 0;
        text-align: center;
    }
</style>
