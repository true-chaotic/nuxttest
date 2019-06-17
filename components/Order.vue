<template>
  <div
    class="order"
    :class="{
      order_white: white
    }"
  >
    <img :src="avatar" />
    <div>{{ name }}</div>
    <div>{{ price }}</div>
    <ul>
      <li v-for="(photo, index) in photos" :key="index">
        <img :src="photo" />
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ['avatar', 'name', 'price', 'photos', 'white']
}
</script>

<style scoped lang="postcss">
.order {
  padding: 10px;
  background-color: black;
  color: white;
  border-radius: 10px;
  text-align: center;
  box-shadow: 0 0 20px grey;
}

.order_white {
  background-color: white;
  color: black;
}
</style>
