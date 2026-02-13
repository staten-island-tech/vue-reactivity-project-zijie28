<template>
    <div class="shopping-item">
        <p class="cart-description">{{ shopItem.name }}</p>
        <p class="cost">{{ shopItem.price }}</p>
        <button @click="$emit('minus', shopItem.name)">-</button>
        <p class="quantity">{{ shopItem.quantity }}</p>
        <button @click="$emit('plus', shopItem.name)">+</button>
    </div>
</template>

<script setup>
defineProps({
    shopItem: {
        type: Object,
        required: true
    },
})
</script>

<style scoped>
.shopping-item {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  background-color: rgb(85, 126, 126);
  width: 100%;
  height: 10vh;
  border-radius: 20px;
  box-shadow: 5px 4px 4px;
}

.cart-description {
  float: left;
  text-align: left;
  font-size: xx-large;
  background-color: rgb(85, 126, 126);
  border-radius: 10px;
  margin: 1%;
  width: 20%;
}
.cost {
  width: 50%;
  font-size: xx-large;
  background-color: rgb(85, 126, 126);
  margin: 1%;
}
button {
    width: 10%;
    height: 40%;
    background-color: rgb(85, 126, 126);
    font-size: xx-large;
}

.quantity {
  font-size: xx-large;
  background-color: rgb(85, 126, 126);
  padding: 10px;
}
</style>