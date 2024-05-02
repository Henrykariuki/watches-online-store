<script setup>
import MyHeader from './components/MyHeader.vue'
import LeftPanel from './components/LeftPanel.vue'
import FiltersRow from './components/FiltersRow.vue'
import ProductsGrid from './components/ProductsGrid.vue'
</script>

<template>
 <body>
  <header>
  <MyHeader></MyHeader>
</header>
  <main style="display: flex; ">
    <div>
      <LeftPanel></LeftPanel>
    </div>
    <div class="w-full">
      <FiltersRow></FiltersRow>
      <ProductsGrid></ProductsGrid>
    </div>
  </main>
 </body> 
</template>

<style scoped>

</style>
