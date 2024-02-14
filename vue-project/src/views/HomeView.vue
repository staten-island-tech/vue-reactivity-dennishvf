<template>
  <div>
<DestCard
v-for="destination in destinations"
:key="destination.name"
:Destination="destination"
/>
  </div>
</template>

<script setup>
import DestCard from '@/components/DestCard.vue';
const destinations= [{    
          name: "Crocs",
          International: true,
          price: "$40",
          img: "https://footwearnews.com/wp-content/uploads/2023/10/Disney-Pixar-Crocs-Classic-Clog-Mater-Release-Date.webp",
        },
        {
          name: "Dunks",
          International: true,
          price: "$130",
          img: "https://sneakerfortress.com/cdn-cgi/image/width=1200,height=675,fit=crop,quality=80,format=auto,onerror=redirect,metadata=none/wp-content/uploads/2024/01/Untitled-design.jpg",
        },
        {
          name: "Vans",
          International: true,
          price: "$100",
          img: "https://i.etsystatic.com/11664848/r/il/6a3831/893832495/il_fullxfull.893832495_laas.jpg",
        },
        {
          name: "Air Forces",
          International: false,
          price: "$110",
          img: "https://bluebeecustoms.net/cdn/shop/products/229540238_4231440183618352_8556875875043492714_n_1024x1024@2x.jpg?v=1634674218",
        },
        {
          name: "Skechers",
          International: false,
          price: 400,
          img: "https://m.media-amazon.com/images/I/51FlBg5uQ9L._AC_UY300_.jpg",
        },
        {
          name: "Jordans",
          International: true,
          price: 800,
          img: "https://i.ytimg.com/vi/JMb6A7x6iao/maxresdefault.jpg",
        },]
</script>

<style scoped>

</style>
