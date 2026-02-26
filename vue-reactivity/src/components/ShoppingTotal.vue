<script setup>
import { computed } from 'vue'
const prop = defineProps({
    totals: {
        type: Array,
        required: true
    }
})


const value = computed(() => {
    return prop.totals.reduce((sum , item) => sum + item.quantity * parseFloat(item.price.slice(1)), 0);
})


</script>

<template>
    <div class = "total">
        <p class="word-total">Total:</p>
        <p class="showed-total" >{{ value }}</p>
    </div>
</template>

<style scoped>
.total {
  display: flex;
  flex-direction: row;
  justify-content: flex-start;
  align-items: center;
  background-color: rgb(85, 126, 126);
  width: 100%;
  height: 10vh;
  border-radius: 20px;
  box-shadow: 5px 4px 4px;
  margin-bottom: 3.5%;
  width: 90vw;
}

.word-total {
  float: left;
  text-align: left;
  font-size: xx-large;
  background-color: rgb(85, 126, 126);
  border-radius: 10px;
  margin: 1%;
  width: 90%;
}

.showed-total {
  float: left;
  text-align: left;
  font-size: xx-large;
  background-color: rgb(85, 126, 126);
  border-radius: 10px;
  margin: 1%;
}
</style>