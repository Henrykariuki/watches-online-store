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
<div class="container">
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
.container {
    display: grid;
    grid-template-columns: 25% 25% 25% 25%;
    row-gap: 14px;
    column-gap: 14px;
    width: auto;
    margin-left: 30px;
}
.product-style {
    margin: 4px;
}
@media (min-width: 1200px) {
    .container {
        display: grid;
        grid-template-columns: 24% 24% 24% 24%;
        width: auto;
    }   
}

@media (min-width: 700px) and (max-width: 1200px) {
    .container {
        display: grid;
        grid-template-columns: 25% 25% 25%;
        width: auto;
    }
}

@media (max-width: 900px) {
    .container {
        display: grid;
        grid-template-columns: 25% 25%;
        width: auto;
    }
}
@media (max-width: 400px) {
    .container {
        display: grid;
        grid-template-columns: 20% 20%;
        width: auto;
        row-gap: 6px;
        column-gap: 6px;
    }
}
</style>