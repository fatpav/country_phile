<template lang="html">
<div>
  <h1>Buy some stuff, Stoopid.</h1>
  <shopping-list-item v-for='(item, index) in items' :key='index' :item='item'></shopping-list-item>
</div>
</template>

<script>

import ShoppingListItem from './components/ShoppingListItem.vue'

export default {
  name: 'app',
  data () {
    return {
      items : [
        {name: 'Rusks', isPurchased: false},
        {name: 'Whisky', isPurchased: false},
        {name: 'Cocaine', isPurchased: false}
      ]
    }
  },
  components: {
    'shopping-list-item': ShoppingListItem
  }
}
</script>

<style>

</style>