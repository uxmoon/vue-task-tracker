<template>
  <header>
    {{ title }}
    <Button
      @toggle-add-task="$emit('toggle-add-task')"
      :text="toggleText ? 'Close' : 'Add task'"
      :color="toggleText ? 'darkred' : 'green'"
    />
  </header>
</template>

<script>
import Button from './Button'

export default {
  name: 'Header',
  components: {
    Button,
  },
  props: {
    title: String,
    toggleText: Boolean,
  },
  emits: ['toggle-add-task'],
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>
