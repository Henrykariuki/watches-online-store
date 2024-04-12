<script setup>
import { X, ChevronDown } from 'lucide-vue-next';
</script>
<template>
  <div class="filter-container">
        <div style="display: flex; margin-left: 16px;">
            <button class="filter-buttons">Handwatches<X size="12px"/></button>
            <button class="filter-buttons">$1,500 &#183; $30,500<X  size="12px"/></button>
            <button class="filter-buttons">Mens<X  size="12px"/></button>
            <button class="filter-buttons">Rolex<X  size="12px"/></button>
        </div>
        <button style=" border: none; background-color: white;  padding: 8px 4px; display: flex; text-align: center; margin-right: 8px;">Newest first<ChevronDown size="12px"/></button>
  </div>
</template>
<style scoped>
* {
  margin: 0;
  padding: 0;
  font-family: Arial, Helvetica, sans-serif;
  box-sizing: border-box;
}
.filter-container {
    width: 1050px;
    height: 60px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.filter-buttons {
    background-color: white;
    border-radius: 16px;
    margin-right: 8px;
    border: 1px solid rgb(219, 218, 218);
    padding: 8px 4px;
    display: flex;
    align-items: center;
}
</style>