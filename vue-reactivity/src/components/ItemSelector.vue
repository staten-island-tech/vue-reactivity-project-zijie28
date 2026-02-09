<template>
    <div>
        <select name="catagory" @change="change()">
            <option id="select-option" value="">All</option>
            <option id="select-option" value="Food">Food</option>
            <option id="select-option" value="Technology">Technology</option>
            <option id="select-option" value="Miscellaneous">Miscellaneous</option>
        </select>
    </div>
</template>

<script setup>
function change(){
    this.value
}
</script>