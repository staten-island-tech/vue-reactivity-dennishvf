<template>
    <div>
<h1>{{ Destination.name }}</h1>
<img :src="Destination.img">
<h2>{{ clicked }}</h2>
<button @click="increment">Click me</button>
    </div>
</template>

<script setup>
import {ref} from "vue";
const props= defineProps({
    Destination: Object,
});
//clicker stuff
const clicked=ref(0);
function increment(){
    clicked.value++
}
</script>

<style scoped>

</style>