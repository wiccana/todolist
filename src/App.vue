<template>
  <div id="app"  class="container is-fluid">
      <h1 class="title is-1">Lista de Tareas</h1>
      
      <AddItem v-on:add-item="addItem"/>   <!-- add-item event calls addItem method -->
   
      <TodoList v-bind:items="items"/>
  </div>
</template>

<script>
import TodoList from './components/TodoList.vue'
import AddItem from './components/AddItem.vue';
import 'bulma/css/bulma.css'

export default {
  name: 'App',
  components: {
    TodoList,
    AddItem
  },
  data() {
    return {
      items: [
        {
          id: 1,
          description: 'Go workout'
        },
        {
          id: 2,
          description: 'Do laundry'
        },
        {
          id: 3,
          description: 'Cook food'
        },
        {
          id: 4,
          description: 'Clean up room'
        },
        {
          id: 5,
          description: 'Finish work'
        }
      ],
    }
  },
  methods: {
    addItem(newItem){
      this.items.push(newItem);
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
