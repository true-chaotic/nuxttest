<template>
  <button
    v-if="text"
    class="button"
    :style="{
      borderColor: borderColor
    }"
  >
    {{ text }}
    <marquee v-if="showMarquee">Another text</marquee>
  </button>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      required: true
    },
    borderColor: {
      type: String,
      default: 'red'
    },
    showMarquee: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style scoped>
.button {
  border: 1px solid red;
}
</style>
