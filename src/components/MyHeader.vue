<script setup>
import {Bell, ShoppingCart, User } from 'lucide-vue-next';
</script>
<template>
  <div class="header-box">    
        <div class="header-container"><p class="logo">Henry Watches</p>
            <div class="header-buttons">
                <div class="button">Auctions</div>
                <div class="button">Buy now</div>
                <div class="button">Hot deals</div>
                <div class="button"> New arrivals</div>
                <div class="button">Sell items</div>
                <div class="header-icon">
                <box-icon name='search'></box-icon></div>
            </div>
            <div>
                <div class="header-icons-container">
                    <div class="header-icon">
                    <ShoppingCart color="black"/>
                    </div>
                    <div class="header-icon">
                    <Bell/>
                    </div>
                    <div class="header-icon">
                    <User/>
                    </div>
                </div>
            </div>
        </div>   
      <div class="header-title-container">
        <div  class="watch">
            Watches
            <div class="watch-numbers">250</div>
        </div>
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
.header-box {
    z-index: 100;
    width: auto;
    height: auto;
}

.logo {
  font-size: 40px;
  font-weight: 600;
  cursor: pointer;
}

.header-container {
  display: flex;
  justify-content: space-around;
  border-top: 1px solid rgb(219, 218, 218);
  border-bottom: 1px solid rgb(219, 218, 218);
  height: 90px;
  align-items: center;
}

.header-buttons {
  display: flex;
  width: 600px;
  height: 70px;
  justify-content: space-between;
  align-items: center;
}

.button {
  width: 100px;
  height: 40px;
  display: flex;
  align-items: center;
  font-weight: bold;
  cursor: pointer;
}

.header-icons-container {
  width: 200px;
  height: 70px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.header-icon {
  width: 40px;
  height: 40px;
  display: flex;
  align-items: center;
  cursor: pointer;
}
.header-title-container {
    width: 100%;
    height: 98px;
    border-bottom:  1px solid rgb(219, 218, 218);
}
.watch {
    font-size: 65px;
    font-weight: 600;
    margin: 38px 0 0  42px;
    position: relative;
    width: 280px;
    height: 70px;
}
.watch-numbers {
   position: absolute;
   padding: 12px; 
   font-size: 18px;
   top: -8px;
   right: -25px;
   color: rgb(221, 22, 22);
}
</style>
