<template>
  <div id="list">
      <div v-bind:key="item.id" v-for="item in items" class="notification">
        <Item v-bind:item="item" v-on:delete-item="$emit('delete-item',item.id)"/>
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

</style>
