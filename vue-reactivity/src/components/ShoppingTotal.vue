<script setup>
import { computed, ref } from 'vue'
const prop = defineProps({
    totals: {
        type: Array,
        required: true
    }
})
let total2 = ref(0)

const value = computed(() => {
    total2.value = 0
    const total = prop.totals.forEach((item) => {
        const item_total = item.value * item.quantity
        total2.value += item_total
    })
    return total
})


</script>

<template>
    <div>
        <p class="total">Total:</p>
        <p class="number" >{{ total2 }}</p>
    </div>
</template>