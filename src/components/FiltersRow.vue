<script setup>
import { X, ChevronDown } from 'lucide-vue-next';
</script>
<template>
  <div class="filter-container w-full h-auto lg:w-full lg:h-auto lg:flex lg:justify-between lg:items-center sm:ml-2 ">
        <div class="grid grid-cols-2 gap-1
        lg:flex ">
            <button class="filter-buttons">Handwatches<X size="12px"/></button>
            <button class="filter-buttons">$1,500 &#183; $30,500<X  size="12px"/></button>
            <button class="filter-buttons">Mens<X  size="12px"/></button>
            <button class="filter-buttons">Rolex<X  size="12px"/></button>
        </div>
        <button style="background-color: white;  
        padding: 8px 4px; display: 
        flex; text-align: center;" 
        class="w-full rounded-lg cursor-pointer my-1 lg:w-auto hover:bg-gray-300">Newest first<ChevronDown size="12px"/></button>
  </div>
</template>
<style scoped>
/*.filter-container {
    width: 1100px;
    height: 60px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}*/
 
.filter-buttons {
    background-color: white;
    border-radius: 16px;
    margin-right: 8px;
    border: 1px solid rgb(219, 218, 218);
    padding: 8px 4px;
    display: flex;
    align-items: center;
    cursor: pointer;
    transition: 0.15s;
}
.filter-buttons:hover {
    background-color: lightgrey;
}
</style>