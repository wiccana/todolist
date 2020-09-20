<template>
  <div>
    <input class="input is-primary" v-model="description" name="description" type="text" placeholder="Tarea...">
    <p v-show="hasInputError" class="help has-text-left has-text-danger">La tarea no puede estar vacía!</p>
    
    <button id="addItem" @click="addItem" class="button is-primary">Agregar Tarea</button>

  </div>
</template>

<script>
import { uuid } from 'vue-uuid';
export default {
  name: 'AddItem',
  data() {
    return {
      description: '',
      hasInputError: false
    }
  },
  methods: {
    addItem() {
      if (this.description === ''){
          this.hasInputError = true;
      }else{
        const newItem = {
          id: uuid.v1(),
          description: this.description
        }
        this.$emit('add-item', newItem);
        this.description = '';
      }
    }
  },
  watch: {
    description: function(){
      this.hasInputError = false;
    }
  }
}
</script>

<style scoped>
  #addItem{
    margin-top: 20px;
  }
</style>