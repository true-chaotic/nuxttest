<template>
  <div>
    <h1 class="name"><strong>Split</strong> order</h1>
    <Menu :items="items" />
    <ul class="orders-list">
      <li
        v-for="(order, index) in orders"
        :key="order.name"
        class="orders-item"
      >
        <Order v-bind="order" :white="index > 0" />
      </li>
    </ul>
    <PlaceOrder :full="full" text="Set reminder" @click="full = !full" />
  </div>
</template>

<script>
import Menu from '~/components/Menu'
import Order from '~/components/Order'
import PlaceOrder from '~/components/PlaceOrder'

export default {
  layout: 'orderfood',
  components: { Menu, Order, PlaceOrder },
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
        name: 'Roasted Potato Salad',
        price: '$15.00'
      },

      {
        id: 3,
        image: '',
        amount: 1,
        name: 'Croissant',
        price: '$7.50'
      },

      {
        id: 4,
        image: '',
        amount: 1,
        name: 'Hot Cheese Burrito',
        price: '$8.00'
      }
    ],
    orders: [
      {
        avatar: '#',
        name: 'You',
        price: '$555',
        photos: ['/images/croissant.png', '/images/burrito.png']
      },
      {
        avatar: '#',
        name: 'Tom',
        price: '$555',
        photos: ['/images/potato.png']
      }
    ],
    full: false
  }),

  head: {
    title: 'Our page'
  }
}
</script>

<style scoped>
.name {
  font-weight: normal;
}

.orders-item {
  display: inline-block;
  vertical-align: top;
  margin: 0 20px;
}
</style>
