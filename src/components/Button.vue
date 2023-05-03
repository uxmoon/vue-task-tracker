<template>
  <button
    @click="onClick()"
    :style="{ backgroundColor: color }"
    class="btn"
    type="button"
  >
    {{ text }}
  </button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    text: String,
    color: String,
  },
  methods: {
    onClick() {
      this.$emit('btn-click')
    },
  },
}
</script>
