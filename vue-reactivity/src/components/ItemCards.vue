<script>
</script>

<template>
    <div class="item_container">
        <img src={{ item.image }}>
        <p class="item-description">{{ item.description }}</p>
        <p class="price">{{ item.price }}</p>
        <button @submit.prevent="purchase()" class="purchase">Purchase</button>
    </div>
</template>

<script setup>
function purchase(){

}

defineProps({
    item: {
        type: Object,
        required: true
    }
})
</script>