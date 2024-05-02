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
<div  class="product-card-container hover:shadow-lg duration-100  ">
    <div class="image-container">
       <div class="image-box">
        <img :src="image" alt="green watch" class="image">
       </div>
        <div class="likes">
             <p style="font-size: 12px">{{ likes }}</p><Plus size="8px"/><Heart size="12px"/>
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

.product-card-container {
    width: 100%;
    /*margin-right: 8px;*/
    background-color: white;
    margin-bottom: 18px;
    height: auto;
}
.image-box {
    width: auto;
    height: auto;
    transition: 0.15s;
}
.image-box:hover{
transform: scale(0.95);

}

.image {
    width: 100%;
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
    background-color: whitesmoke;
}
.image-container {
    position: relative;
    cursor: pointer;
}
.likes {
    position: absolute;
    top: 6px;
    right: 6px;
    display: flex;
    align-items: center;
    }
</style>