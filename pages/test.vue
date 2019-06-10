<template>
  <div>
    <h1>Hello world</h1>
    <p>Hello</p>
    <ul v-if="list.length > 0">
      <li v-for="item in list" :key="item">Hi <Button :text="item" /></li>
    </ul>
    <Button text="Some other text" border-color="green" :show-marquee="true" />
    <Button show-marquee="true" />
  </div>
</template>

<script>
import Button from '~/components/Button.vue'

export default {
  components: {
    Button
  },

  data: () => ({
    list: ['a'] // ['a', 'b', 'c', '😃', '🐱']
  })
}
</script>

<style scoped></style>
