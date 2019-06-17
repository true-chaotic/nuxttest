<template>
  <button @click="$emit('click', $event)">
    <span v-if="full">{{ text }}</span> ->
  </button>
</template>

<script>
export default {
  props: ['full', 'text']
}
</script>

<style scoped></style>
