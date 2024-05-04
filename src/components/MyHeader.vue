<script setup>
import {Bell, ShoppingCart, User, Menu, X, AlignLeft} from 'lucide-vue-next';
import {ref} from 'vue';




const open = ref(false)
const hidden = "openLeft"
const openLeft = ref(false)

const menuOpen = () => {
    open.value = !open.value
}

const openLeftMenu = () => {
    openLeft.value = !openLeft.value
}

</script>
<template>
 <div class="">
    <div class="header-box  width-100% height-auto">
        <div class="header-container sm:block">
            <p class="header-title sm:leading-9 md:leading-9" style="font-size: 40px; margin-left: 24px; font-weight: 600">Henry Watches</p>
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
            <div class="sm:hidden" @click="menuOpen"><Menu size="38px"/></div>
        </div>
        <div class="header-container-info">
            <div class="header-info">
                <p style="font-size: 54px; font-weight: 600;">Watches</p>
                <div class="watch-count">250</div>
            </div>
        </div>
        <div class="left-side-bar-menu border w-full h-14 mb-px pt-2 pl-7" >
            <div class="md:hidden lg:hidden" @click="openLeftMenu"><AlignLeft size="38" /></div>
            <div class="left-side-bar  md:hidden lg:hidden duration-500" :class="[openLeft ? 'left-0' : 'left-[-100%]']">
                <div class="left-side-bar bg-white  sm:block">
      <div class="items">250 items</div>
            <div class="container-one">
                <div class="watches-container">
                    <p class="watches">Watches</p>
                    <div>
                      <ChevronDown Plus size="16px"  />
                    </div>
                </div>
                <div class="category">
                    <div class="remove"><Minus Plus size="16px" /></div>
                    <p class="category-text">Handwatches</p>
                </div>
                <div class="category">
                    <div class="add"><Plus Plus size="16px" /></div>
                    <p class="category-text">Briefcases</p>
                </div>
                <div class="category">
                    <div class="add"><Plus Plus size="16px" /></div>
                    <p class="category-text">Evening bags</p>
                </div>
            </div>
            <div class="container-two">
                <div class="watches-container">
                    <p class="watches">Price</p>
                    <div>
                      <ChevronDown />
                    </div>
                </div>
                <div class="graph-base">
                    <div class="red-dot"></div>
                    <div class="red-dot-two"></div>
                    <div class="graph-data">
                    <p>$1,500</p>
                    <p>$30,500</p>
                </div>
                </div>
            </div>
            <div class="container-three">
                <div class="watches-container">
                    <p class="watches">Gender</p>
                    <div>
                      <ChevronDown />
                    </div>
                </div>
                <div class="category">
                    <div class="remove"><Minus Plus size="16px"/></div>
                    <p class="category-text">Mens</p>
                </div>
                <div class="category">
                    <div class="add"><Plus Plus size="16px"/></div>
                    <p class="category-text">Womens</p>
                </div>
            </div>
            <div class="container-four">
                <div class="watches-container">
                    <p class="watches">Brands</p>
                    <div>
                      <ChevronDown />
                    </div>
                </div>
                <input type="text" placeholder="Search brands" class="search-bar hover:placeholder-gray-900 ">
                <div class="category">
                    <div class="remove"><Minus Plus size="16px"/></div>
                    <p class="category-text">Rolex</p>
                </div>
                <div class="category">
                    <div class="add"><Plus Plus size="16px" /></div>
                    <p class="category-text">Rado</p>
                </div>
            </div>
            <div class="container-five">
                <div class="watches-container">
                    <p class="watches">Condition</p>
                    <div>
                      <ChevronDown />
                    </div>
                </div>
                <div class="category">
                    <div class="remove"><Minus Plus size="16px" /></div>
                    <p class="category-text">Fair</p>
                </div>
                <div class="category">
                    <div class="add"><Plus size="16px"/></div>
                    <p class="category-text">Good</p>
                </div>
            </div>
    </div>
            </div>
        </div>
        
        <div class="right-side-bar duration-500 " :class="[open ? 'right-0' : 'left-[-100%]']">
            <div class="close-button" @click="menuOpen"><X size="20px"/></div>
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
    height: 88px;
    border-bottom: 1px solid rgb(219, 218, 218);
}
.right-side-bar {
    position: absolute;
    background-color: rgba(128, 128, 128, 0.171);
    backdrop-filter: blur(10px);
    top: 62px;
    right: 0;
    width: 100%;
    height: 400px;
    z-index: 1;
    border-radius: 2px;
    text-align: center;
}
.close-button {
    width:24px; 
    height: 24px;
    display: flex;
    justify-content: center;
    align-items: center;
    float: right;
    margin-bottom: 2px;
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
    top: 18px;
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

.left-side-bar-menu {
    position: relative;
    border-bottom: 1px solid rgb(219, 218, 218);;
}
.left-side-bar {
    position: absolute;
    width: auto;
    height: auto;
    z-index: 1;
    left: 1;
    border-radius: 0 4px 4px 0;
}


.items {
    width: 200px;
    height: 30px;
    padding-left: 30px;
    padding-top: 8px;
    font-weight: 600;
    color: rgb(105, 104, 104);
}
.watches-container {
    display: flex;
    justify-content: space-between;
    width: 200px;
    height: 60px;
    align-items: center;
    margin-left: 10px;
}
.watches {
    font-size: 16px;
    font-weight: 600;
    cursor: pointer;
}
.container-one,
.container-two,
.container-three,
.container-four {
    width: 250px;
    height: auto; 
}
.category {
    width: 200px;
    height: 40px;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    padding-left: 20px;
    transition: 0.15s;
}
.category-text {
    font-size: 13px;
    font-weight: 600;
    cursor: pointer;
}
.remove, .add {
    width: 25px;
    height: 25px;
    display: flex;
    align-items: center;
}
.category:hover {
    color: red;
}


.graph-base {
    width: 200px;
    height: 1px;
    border: 1px solid grey;
    margin: 40px auto;
    background-color: grey;
    border-radius: 3px;
    position: relative;
}
.red-dot {
    width: 10px;
    height: 10px;
    border-radius: 5px;
    background-color: red;
    position: absolute;
    top: -4px;
    right: 12px;
}
.red-dot-two {
    width: 10px;
    height: 10px;
    border-radius: 5px;
    background-color: red;
    position: absolute;
    top: -4px; 
}
.graph-data {
    width: 200px;
    height: 25px;
    display: flex; 
    justify-content: space-between;
    align-items: center;
}
.search-bar {
    padding: 10px 15px;
    outline: none;
    border: 2px solid grey;
    margin-left: 10px;
    transition: 0.15s;
}
.search-bar:hover {
    background-color: lightgray;
    color: black;
    cursor: text;
}
</style>
