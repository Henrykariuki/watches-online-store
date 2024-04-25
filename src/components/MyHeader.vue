<script setup>
import {Bell, ShoppingCart, User } from 'lucide-vue-next';
</script>
<template>
 <div class="header-box">
    <div class="header-box">
        <div class="header-container">
            <p class="header-title" style="font-size: 40px; margin-left: 24px; font-weight: 600">Henry Watches</p>
            <div class="header-buttons">
                <div class="button">Auctions</div>
                <div class="button"> Buy now</div>
                <div class="button">Hot deals</div>
                <div class="button">New arrivals</div>
                <div class="button">Sell item</div>
            </div>
            <div class="header-icons-container">
                <div class="header-icons"><Bell /></div>
                <div class="header-icons"><ShoppingCart /></div>
                <div class="header-icons"><User /></div>
            </div>
        </div>
        <div class="header-container-info">
            <div class="header-info">
                <p style="font-size: 54px; font-weight: 600;">Watches</p>
                <div class="watch-count">250</div>
            </div>
        </div>
    </div>
 </div>      
</template>
<style scoped>
.header-box {
    width: 100%;
    height: auto;
}
.header-container {
    width: 100%;
    height: 84px;
    border: 1px solid rgb(219, 218, 218);;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: white;
}
.header-container-info {
    position: relative;
    width: 100%;
    height: 116px;
    border-bottom: 1px solid rgb(219, 218, 218);;
}
.button {
    padding: 10px;
    font-weight: 600;
    margin-right: 10px;
    transition: 0.15s;
    border-radius: 4px;
}
.header-buttons {
    width: auto;
    height: 60px;
    display: flex;
    align-items: center;
    cursor: pointer;
}
.button:hover, .header-icons:hover{
    background-color: lightgrey;
}
.header-icons-container {
    width: auto;
    height: 50px;
    display: flex;
    align-items: center;
    width: 220px;
    justify-content: space-between;
    margin-right: 20px;
}
.header-icons {
    width: 40px;
    height:40px;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 20px;
    cursor: pointer;
    transition: 0.15s;
}
.header-info {
    position: absolute;
    width: 236px;
    height: 58px;
    position: relative;
    left: 24px;
    top: 36px;
}
.watch-count {
    position: absolute;
    width: 36px;
    height: 18px;
    top: 0;
    right: -28px;
    font-weight: 600;
    color: rgb(202, 4, 4);
}
@media (max-width: 300px) {
    .header-container {
        width: 100%;
        height: 84px;
    }
    .header-buttons {
        display: none;
    }
    .header-icons {
        display: none;
    }
    
}
</style>
