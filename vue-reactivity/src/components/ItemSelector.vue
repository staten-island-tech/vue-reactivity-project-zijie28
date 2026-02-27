<template>
    <div>
        <select name="catagory" @change="change">
            <option id="select-option" value="">All</option>
            <option id="select-option" value="Food">Food</option>
            <option id="select-option" value="Technology">Technology</option>
            <option id="select-option" value="Miscellaneous">Miscellaneous</option>
        </select>
    </div>
</template>

<script setup>
import { dict } from './ShoppingInventory';
const emit = defineEmits(['update'])
function change(event) {
    if(event.target.value === 'Food'){
        const filter = dict.filter(item => item.category === 'Food');
        emit('update', filter)
    } else if(event.target.value === 'Technology') {
        const filter = dict.filter(item => item.category === 'Technology');
        emit('update', filter)
    } else if(event.target.value === 'Miscellaneous') {
        const filter = dict.filter(item => item.category === 'Miscellaneous');
        emit('update', filter)
    } else {
        emit('update', dict)
    }
}
</script>

<style scoped>
.catagory{
  background-color: rgb(85, 126, 126);
  text-align: center;
  width: 15%;
}

#select-option{
  background-color: rgb(85, 126, 126);  
}

div{
    display: flex;
    justify-content: center;
    align-items: center;  
}
</style>