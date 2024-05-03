<script setup>
import { ChevronDown, Minus, Plus, } from 'lucide-vue-next';
</script>
<template>
    <div class="left-side-bar border-r border-x-grey-100 bg-white hidden sm:block">
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
</template>

<style scoped>


/*.left-side-bar {
    width: 280px;
    border-right:  1px solid rgb(219, 218, 218);
    background-color: white;
}*/
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