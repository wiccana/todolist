<template>
    <div id="todo" class="container is-fluid">
      <h1 class="title is-1">Lista de Tareas</h1>
            
            <input class="input is-primary" type="text" placeholder="Tarea...">
            <p class="help has-text-left has-text-danger">This is a help text</p>
            
            <button @click="addItem" class="button is-primary">Agregar Tarea</button>
            
            <div id="list">

              <div class="notification">
                <button class="delete"></button>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit lorem ipsum dolor sit amet, consectetur adipiscing elit
              </div>
              <div class="notification">
                <button class="delete"></button>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit lorem ipsum dolor sit amet, consectetur adipiscing elit
              </div>
              <div class="notification">
                <button class="delete"></button>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit lorem ipsum dolor sit amet, consectetur adipiscing elit
              </div>

            </div>

    </div>
</template>

<script>
export default {
  name: 'TodoList',
  props: {
    msg: String
  },
  methods: {
    addItem(){
      console.log('adding item');
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  #list {
    padding: 20px;
  }
  .todo-item{
    margin:  10px;
    display: blocK;
  }
</style>
