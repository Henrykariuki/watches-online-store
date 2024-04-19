<script setup>

import { Heart } from 'lucide-vue-next';
import { Plus } from 'lucide-vue-next';

const props = defineProps({
    image: {
        type: String,
        required: true
    },
    price: {
        type: Number,
        required: true
    },
    likes: {
        type: Number,
        required: true
    },
    name: {
        type: String,
        required: true
    },
    about: {
        type: String,
        required: true
    }
    

})


</script>
<template>
<div class="product-card-container">
    <div class="image-container">
        <img :src="image" alt="green watch" class="image">
        <div class="likes">
             <p style="font-size: 12px">{{ likes }}<Plus size="8px"/></p>
            <Heart size="12px"/>
        </div>
    </div>
    <div class="watch-info-container">
        <P class="watch-name">{{ name }}</P>
        <p class="about-watch">{{ about }}</p>
        <p class="watch-price">{{ price }}</p>
    </div>
</div>
</template>
<style scoped>
* {
  margin: 0;
  padding: 0;
  font-family: Arial, Helvetica, sans-serif;
  box-sizing: border-box;
}
.product-card-container {
    width: auto;
    margin-right: 8px;
    background-color: white;
}
.image {
    /*width: 250px;*/
    height: 250px;
    object-fit: cover;
}
.watch-name, .watch-price {
    font-weight: 600;
}
.about-watch {
    color: rgb(87, 87, 87);
    margin-top: 4px;
    margin-bottom: 4px;
    font-size: 12px;
}
.watch-info-container {
    padding-top: 8px;
}
.image-container {
    position: relative;
}
.likes {
    position: absolute;
    top: 6px;
    right: 6px;
    display: flex;
    align-items: center;
}
</style>