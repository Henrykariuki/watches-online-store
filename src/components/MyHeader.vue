<script setup>
</script>
<template>
 <div class="header-container"><p class="logo">COCS</p>
    <div class="header-buttons">
        <div class="button">Auctions</div>
        <div class="button">Buy now</div>
        <div class="button">Hot deals</div>
        <div class="button"> New arrivals</div>
        <div class="button">Sell items</div>
        <div class="header-icon"><box-icon name='search'></box-icon></div>
    </div>
    <div>
        <div class="header-icons-container">
            <div class="header-icon"><box-icon type='solid' name='cart'></box-icon></div>
            <div class="header-icon"><box-icon type='solid' name='bell'></box-icon></div>
            <div class="header-icon"><box-icon type='solid' name='user'></box-icon></div>
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

    width: 100%;
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
</style>
