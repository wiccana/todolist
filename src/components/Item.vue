<template>
    <div>
        <p>{{ item.description }}   
        <button @click="$emit('delete-item',item.id)" class="delete"></button>
        </p>
    </div>
</template>

<script>
export default {
  name: 'Item',
  props: [
    "item"
  ]
}
</script>

<style scoped>
</style>