<template>
  <div>
    <input class="input is-primary" v-model="description" name="description" type="text" placeholder="Tarea...">
    <p class="help has-text-left has-text-danger">This is a help text</p>
    
    <button @click="addItem" class="button is-primary">Agregar Tarea</button>

  </div>
</template>

<script>
// import uuid from 'uuid';
import { uuid } from 'vue-uuid';
export default {
  name: 'AddItem',
  data() {
    return {
      description: ''
    }
  },
  methods: {
    addItem() {
      const newItem = {
        id: uuid.v1(),
        description: this.description
      }
      this.$emit('add-item', newItem);
      this.description = '';
    }
  }
}
</script>

<style scoped>
</style>