<template>
    <div>
<h1 class="title">Shopping Cart</h1>
<div v-for="item in props.cart" :key="item.name">
    <h3>{{ item.name }}</h3>
    <h3>${{ item.price }}</h3>
    </div>
    <div>
        <h3>Total price: $ {{ totalPrice() }}</h3>
    </div>
    </div>
</template>

<script setup>

//export default {};
const props = defineProps({cart:Array});

const totalPrice = () => {
    return props.cart.reduce((total,pair) => total+pair.price, 0)
}
  
</script >

<style scoped>
title{
    font-size: x-large;
}
</style>