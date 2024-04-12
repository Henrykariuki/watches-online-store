<script setup>
import ProductCard from './ProductCard.vue'
</script>
<template>
<div class="container">
<ProductCard class="product-style"></ProductCard>

</div>
</template>
<style scoped>
.container {
    display: flex;
    width: 100%;
}
.product-style {
    margin: 4px;
}
</style>