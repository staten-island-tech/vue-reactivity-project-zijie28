

<template>
    <div class="item_container">
        <img src={{ item.image }}>
        <p class="item-name">{{ item.name }}</p>
        <p class="price">{{ item.price }}</p>
        <button @submit.prevent="purchase()" id={{ item.id-name }}>Purchase</button>
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