<script setup>
import ProductCard from './ProductCard.vue'
const products = [
   {
    image: "/images/watch01.jpg",
    price: 10000,
    likes: 100,
    name: "Rolex",
    about: "The Oyster Perpetual"
},
{
    image: "/images/watch02.jpg",
    price: 1200,
    likes: 200,
    name: "Joseph Abboud",
    about: "Tevise Stainless"
},
{
    image: "/images/watch03.jpg",
    price: 25000,
    likes: 3000,
    name: "Poedagar",
    about: "Luminous mens's"
},
{
    image: "/images/watch04.jpg",
    price: 1000,
    likes: 800,
    name: "Rolex",
    about: "The Oyster Perpetual"
},
{
    image: "/images/watch05.jpg",
    price: 1500,
    likes: 100,
    name: "Joseph Abboud",
    about: "Tevise Stainless"
},
{
    image: "/images/watch06.jpg",
    price: 100,
    likes: 1000,
    name: "Poedagar",
    about: "Luminous mens's"
},
{
    image: "/images/watch07.jpg",
    price: 15000,
    likes: 2000,
    name: "Rolex",
    about: "The Oyster Perpetual"
},
{
    image: "/images/watch08.jpg",
    price: 18000,
    likes: 1200,
    name: "Joseph Abboud",
    about: "Tevise Stainless"
}
]
</script>
<template>
<div class="container 
flex flex-col items-center my-2
w-full h-auto sm:ml-2
sm:grid sm:grid-cols-2 gap-1
md:grid md:grid-cols-3 gap-2
lg:grid lg:grid-cols-4 gap-3">
<ProductCard 
:name="item.name"
:about="item.about"
:likes="item.likes" 
:price="item.price" 
v-for="(item, index) in products" :key="index" 
:image="item.image" 
class="product-style"/>

</div>
</template>
<style scoped>

/*.container {
    display: grid;
    grid-template-columns: 25% 25% 25% 25%;
    row-gap: 14px;
    column-gap: 14px;
    width: auto;
    margin-left: 30px;
}*/
.product-style {
    /*margin: 4px;*/
}

</style>