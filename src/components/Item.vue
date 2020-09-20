<template>
        <p>{{ item.description }}</p>   
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