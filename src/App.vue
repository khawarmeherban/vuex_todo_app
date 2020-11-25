<template>
  <div id="app">
    <div class="container">
      <addTodo />
      <filter-todos/>
      <Todos />
      
    </div>
      
  </div>
</template>

<script>
import Todos from './components/Todos.vue';
import addTodo from './components/addTodo.vue';
import FilterTodos from './components/FilterTodos.vue'

export default {
  name: 'App',
  components: {
    addTodo,
    Todos,
    FilterTodos,
   
  }
}
</script>

<style>
 body{
   font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
   line-height: 1.6;
   background:#e8f7f0;

 }
 .container{
   max-width: 1100px;
   margin: auto;
   overflow: hidden;
   padding: 0 2rem;
 }
</style>
