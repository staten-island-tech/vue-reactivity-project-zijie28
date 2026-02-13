<script setup>
import { ref } from 'vue'
const prop = defineProps({
    totals: {
        type: Array,
        required: true
    }
})
let total = ref(0)
prop.totals.forEach(item => {
    total.value = 0
    total.value += item.price
})


</script>

<template>
    <div>
        <p class="total">Total:</p>
        <p class="number" >{{ total }}</p>
    </div>
</template>