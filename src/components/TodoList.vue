<template>
  <div id="list">
      <div v-bind:key="item.id" v-for="item in items" class="notification">
        <button class="delete"></button>
        <Item v-bind:item="item" />
      </div>
  </div>
</template>

<script>
import Item from './Item';

export default {
  name: 'TodoList',
  components: {
    Item
  },
  props: {
    "items": Array
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
