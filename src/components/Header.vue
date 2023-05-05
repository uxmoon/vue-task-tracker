<template>
  <header>
    {{ title }}
    <Button
      v-show="homePage"
      @btn-click="$emit('toggle-add-task')"
      :text="toggleForm ? 'Close' : 'Add task'"
      :color="toggleForm ? 'darkred' : 'green'"
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
    toggleForm: Boolean,
  },
  emits: ['toggle-add-task'],
  computed: {
    homePage() {
      if (this.$route.path === '/') {
        return true
      } else {
        return false
      }
    },
  },
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
