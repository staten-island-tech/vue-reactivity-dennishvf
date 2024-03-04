<template>
    <div>
<h1 class="title">Shopping Cart</h1>
<div v-for="item in props.cart" :key="item.name">
    <h3>{{ item.name }}</h3>
    <h3>{{ item.price }}</h3>
    <h3>${{ Total() }}</h3>
    </div>
    </div>
</template>

<script setup>


const props = defineProps({cart:Array})
const Total =() => {
return props.cart.reduce((sum, item)=> sum+item.price)
}
</script >

<style scoped>
title{
    font-size: x-large;
}
</style>