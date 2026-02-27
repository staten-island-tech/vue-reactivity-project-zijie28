<script setup>
import ItemCards from './components/ItemCards.vue';
import { ref } from 'vue';
import ShoppingCart from './components/ShoppingCart.vue';
import ShoppingTotal from './components/ShoppingTotal.vue';
import { dict } from './components/ShoppingInventory';
import ItemSelector from './components/ItemSelector.vue';

let cart = ref([])
let Vardict = ref(dict)

function initCount(name, price){
    const checker = cart.value.filter((item) => item.name === name)
    if (checker.length === 0) {
    const dict = { name: name, price: price, quantity: 1 };
    cart.value.push(dict);
    } else {
        add(name);
    }
}

function add(name) {
    const index = cart.value.findIndex(item => item.name === name)
    cart.value[index].quantity++;
}

function minus(name) {
    const index = cart.value.findIndex(item => item.name === name);
    cart.value[index].quantity--;
    if (cart.value[index].quantity === 0) {
        cart.value.splice(index, 1);
    }
}

function updateDict(Object) {
    Vardict.value = Object;
    console.log(Vardict)
}
</script>

<template>
    <ItemSelector @update="updateDict"></ItemSelector>
  <div id="container">
    <ItemCards v-for="item in Vardict" :key="item.name":item="item" @purchase="initCount"></ItemCards>
  </div>
  <div id="shopping">
    <ShoppingCart v-for="item in cart" :key="item.name" :shop-item="item" @plus="add" @minus="minus"></ShoppingCart>
    <ShoppingTotal :totals="cart"></ShoppingTotal>
  </div>
</template>

<style scoped>

html {
  font-size: 10px;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Montserrat';
  background-color: rgb(53, 60, 66);
}
#container {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-around;
  width: 90vw;
  column-gap: 1vh;
  row-gap: 4vh;
  padding-top: 1%;
  margin-left: 4.5%;
  margin-bottom: 3.5%;
}

#shopping {
  display: flex;
  flex-direction: column;
  width: 90vw;
  gap: 2vh;
  margin-left: 4.5%;
  margin-bottom: 3.5%;
}
</style>
