<template lang="html">
  <p :class='purchasedClass'>{{ item.name }}</p>
</template>

<script>
export default {
    name: 'shopping-list-item',
    props: ['item'],
    computed: {
        purchasedClass: function () {
            return this.item.isPurchased ? 'purchased' : 'not-purchased'
        }
    }

}
</script>

<style lang="css" scoped>
.not-purchased {
    background-color: gold;
}

.purchased {
    text-decoration: line-through;
    background-color: green;
}

</style>