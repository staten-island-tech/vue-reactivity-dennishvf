<template>
  <h1>The Cars Shoe Store</h1>
  <div>
<ShoeCard
v-for="item in shoes"
:key="item.name"
:Item="item"
@addToCart="AddItem(item)"

/>
  
    <ShoppingCart 
    :cart="cart"/>  
    </div>
</template>

<script setup>
import ShoppingCart from "@/components/ShoppingCart.vue";
import ShoeCard from '@/components/ShoesCard.vue';
import { ref } from 'vue'
const shoes= [{    
          name: "Crocs",
          price: "$40",
          img: "https://footwearnews.com/wp-content/uploads/2023/10/Disney-Pixar-Crocs-Classic-Clog-Mater-Release-Date.webp",
        },
        {
          name: "Dunks",
          price: "$130",
          img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSHPzziENried8aYFI40pkxQX1OktR1KBJitw&usqp=CAU",
        },
        {
          name: "Vans",
          price: "$100",
          img: "https://i.etsystatic.com/11664848/r/il/6a3831/893832495/il_fullxfull.893832495_laas.jpg",
        },
        {
          name: "Air Forces",
          price: "$110",
          img: "https://bluebeecustoms.net/cdn/shop/products/229540238_4231440183618352_8556875875043492714_n_1024x1024@2x.jpg?v=1634674218",
        },
        {
          name: "Skechers",
          price: "$400",
          img: "https://m.media-amazon.com/images/I/51FlBg5uQ9L._AC_UY300_.jpg",
        },
        {
          name: "Jordans",
          price: "$800",
          img: "https://i.ytimg.com/vi/JMb6A7x6iao/maxresdefault.jpg",
        },]

        let cart= ref([])
        function AddItem(Pair){
          cart.value.push(Pair)
          console.log(cart.value)
        }
</script>

<style scoped>

</style>
