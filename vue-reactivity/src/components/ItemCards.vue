<template>
    <div class="item">
        <img :src="item.image">
        <p class="item-name">{{ item.name }}</p>
        <p class="price">{{ item.price }}</p>
        <button :id="item['id-name']" @click="$emit('purchase', item.name, item.price)">Purchase</button>
    </div>
</template>

<script setup>

defineProps({
    item: {
        type: Object,
        required: true
    }
})
</script>

<style scoped>

html {
  font-size: 10px;
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Montserrat';
  background-color: rgb(53, 60, 66);
}
.item {
  display: flex;
  flex-direction: column;
  background-color: rgb(85, 126, 126);
  width: 20%;
  height: 45vh;
  border-radius: 20px;
  box-shadow: 5px 4px 4px;
}

img {
  height: 60%;
  width: auto;
  margin: 3%;
  border-radius: 5%;

}

.price {
  display: flex;
  justify-content: center;
  font-size: small;
  background-color: rgb(85, 126, 126);
  border-radius: 500px;
  margin: 3%;
}

.item-name {
  display: flex;
  justify-content: center;
  font-size: xx-large;
  background-color: rgb(85, 126, 126);
  border-radius: 10px;
  margin: 1%;
}

button {
  display: flex;
  justify-content: center;
  font-size: small;
  background-color: rgb(85, 126, 126);
  border-radius: 500px;
  border: 2px solid rgb(25, 42, 42);
  margin: 3%;
  box-shadow: none;
}
button:hover {
  background-color: rgb(107, 158, 158);
}

</style>

