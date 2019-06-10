<template>
  <div>
    <h1 class="name"><strong>Split</strong> order</h1>
    <Menu :items="items" />
  </div>
</template>

<script>
import Menu from '~/components/Menu'
export default {
  layout: 'orderfood',
  components: { Menu },
  data: () => ({
    items: [
      {
        id: 1,
        image: '',
        amount: 1,
        name: 'Le Pigeon Burger',
        price: '$9.50'
      },

      {
        id: 2,
        image: '',
        amount: 1,
        name: 'Le Pigeon Burger',
        price: '$9.50'
      },

      {
        id: 3,
        image: '',
        amount: 1,
        name: 'Le Pigeon Burger',
        price: '$9.50'
      },

      {
        id: 4,
        image: '',
        amount: 1,
        name: 'Le Pigeon Burger',
        price: '$9.50'
      }
    ]
  })
}
</script>

<style scoped>
.name {
  font-weight: normal;
}
</style>
