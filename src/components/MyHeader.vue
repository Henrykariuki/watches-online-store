<script setup>
import {Bell, ShoppingCart, User, Menu, X } from 'lucide-vue-next';
 function showSidebar() {
    const sidebar = document.querySelector('.right-side-bar')
    sidebar.style.display = 'block'
 } 

 function hideSidebar() {
    const sidebar = document.querySelector('.right-side-bar')
    sidebar.style.display = 'none'
 }
</script>
<template>
 <div class="bg-yellow-100">
    <div class="header-box  width-100% height-auto">
        <div class="header-container sm:block">
            <p class="header-title" style="font-size: 40px; margin-left: 24px; font-weight: 600">Henry Watches</p>
            <div class="hidden sm:flex sm:items-center sm:cursor-pointer">
                <div class="button">Auctions</div>
                <div class="button"> Buy now</div>
                <div class="button">Hot deals</div>
                <div class="button">New arrivals</div>
                <div class="button">Sell item</div>
            </div>
            <div class="header-icons-container hidden sm:flex w-auto h-auto justify-between mr-5 px-4">
                <div class="header-icons">
                    <Bell />
                    <div class="tooltip">Notification</div>
                </div>
                <div class="header-icons">
                    <ShoppingCart />
                    <div class="tooltip">Shopping Cart</div>
                </div>
                <div class="header-icons">
                    <User />
                    <div class="tooltip">User Profile</div>
                </div>
                
            </div>
            <div onclick=showSidebar() class="sm:hidden"><Menu size="38px"/></div>
        </div>
        <div class="header-container-info">
            <div class="header-info">
                <p style="font-size: 54px; font-weight: 600;">Watches</p>
                <div class="watch-count">250</div>
            </div>
        </div>
        <div class="right-side-bar">
            <div onclick=hideSidebar() class="close-button"><X /></div>
            <div class="button">Auctions</div>
            <div class="button"> Buy now</div>
            <div class="button">Hot deals</div>
            <div class="button">New arrivals</div>
            <div class="button">Sell item</div>
        </div>
    </div>
 </div>      
</template>
<style scoped>

.header-container {
    width: 100%;
    height: 84px;
    border: 1px solid rgb(219, 218, 218);;
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: white;
    position: relative;
}
.header-container-info {
    position: relative;
    width: 100%;
    height: 116px;
    border-bottom: 1px solid rgb(219, 218, 218);;
}
.right-side-bar {
    position: absolute;
    border: 1px solid black;
    background-color: rgba(128, 128, 128, 0.171);
    backdrop-filter: blur(10px);
    top: 84px;
    right: 0;
    width: 180px;
    height: 400px;
    z-index: 1;
    border-radius: 2px;
    display: none;
}
.close-button {
    border: 1px solid black; 
    width:24px; 
    height: 24px;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-left: 152px;
}
.button {
    padding: 10px;
    font-weight: 600;
    margin-right: 10px;
    transition: 0.15s;
    border-radius: 4px;
}

.button:hover, .header-icons:hover{
    background-color: lightgrey;
}
.header-icons-container {
   position: relative;
}
.tooltip {
    position: absolute;
    border: 1px solid black;
    padding: 4px;
    background-color: rgb(20, 20, 20);
    color: white;
    bottom: -40px;
    border-radius: 6px;
    opacity: 0;
    transition: 0.15s;
    text-wrap: nowrap;
}

.header-icons:hover .tooltip {
    opacity: 1;
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

</style>
