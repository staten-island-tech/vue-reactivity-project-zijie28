<script setup>
import ItemCards from './components/ItemCards.vue';
import { ref } from 'vue';
import ShoppingCart from './components/ShoppingCart.vue';
import ShoppingTotal from './components/ShoppingTotal.vue';
const dict = ref([{
        "name": "Mayodenoche",
        "id-name": "Mayodenoche",
        "category": "Food",
        "image": "https://i5.walmartimages.com/asr/46535c5c-7151-4626-b969-83e772ba0d21.3bd9fed39226c0c5918d6e09bdaeb571.jpeg",
        "price": "$1000"

    },
    {
        "name": "Suspicious Mayodenoche",
        "id-name": "Suspicious-Mayodenoche",
        "category": "Food",
        "image": "https://www.tasteofhome.com/wp-content/uploads/2024/12/Korean-Corn-Dogs_EXPS_TOHVP24_277260_MR_12_03_2.jpg",
        "price": "$500"
    },
    {
        "name": "Credit Card",
        "id-name": "Credit-Card",
        "category": "Technology",
        "image": "https://pngimg.com/uploads/credit_card/credit_card_PNG71.png",
        "price": "$200"
    },
    {
        "name": "a normal ssd that won't brick",
        "id-name": "a-normal-ssd-that-won't-brick",
        "category": "Technology",
        "image": "https://encrypted-tbn3.gstatic.com/shopping?q=tbn:ANd9GcTtkczvwcLoQOMz1OLwNFjje86QLepsM0szFu8uBa5xgWYwdvw3YMqVWfq6EJjR30e5ZdVUP4wBavi6-ds2PcCtHLdA8MhQw26KvY7FxdbED3ee13bzBlMdmQ",
        "price": "$300"
    },
    {
        "name": "Galaxy Donut",
        "id-name": "Galaxy-Donut",
        "category": "Food",
        "image": "https://upload.wikimedia.org/wikipedia/commons/thumb/a/a5/Glazed-Donut.jpg/1920px-Glazed-Donut.jpg",
        "price": "$150"
    },
    {
        "name": "Virtual Shoes",
        "id-name": "Virtual-Shoes",
        "category": "Miscellaneous",
        "image": "https://academy.scene7.com/is/image/academy/20841626?$pdp-gallery-ng$",
        "price": "$1200"
    },
    {
        "name": "Cursed Banana",
        "id-name": "Cursed-Banana",
        "category": "Food",
        "image": "https://upload.wikimedia.org/wikipedia/commons/8/8a/Banana-Single.jpg",
        "price": "$80"
    },
    {
        "name": "Invisible Cloak (Probably)",
        "id-name": "Invisible-Cloak-(Probably)",
        "category": "Miscellaneous",
        "image": "https://upload.wikimedia.org/wikipedia/commons/a/a2/Chess_tile.png?20050618233941",
        "price": "$999"
    },
    {
        "name": "Bread Helmet",
        "id-name": "Bread-Helmet",
        "category": "Food",
        "image": "https://i.kym-cdn.com/photos/images/original/000/184/659/IChJ1.jpg",
        "price": "$210"
    },
    {
        "name": "Meme NFT",
        "id-name": "Meme-NFT",
        "category": "Technology",
        "image": "https://i.imgflip.com/4/4t0m5.jpg",
        "price": "$9999"
    },
    {
        "name": "Suspicious Soup",
        "id-name": "Suspicious-Soup",
        "category": "Food",
        "image": "https://media.istockphoto.com/photos/fish-soup-japanese-style-fish-soup-with-soy-sauce-picture-id505400398?k=20&m=505400398&s=612x612&w=0&h=MJFHkTLJ30FdSSXEPiR2JUXUDGiZVm_UmebV91oPEBk=",
        "price": "$45"
    },
    {
        "name": "The Bay Harbor Butcher",
        "id-name": "The-Bay-Harbor-Butcher",
        "category": "Miscellaneous",
        "image": "https://tse4.mm.bing.net/th/id/OIP.6a12uOEQUikVNM0Ol4jj2QHaEK?cb=12&rs=1&pid=ImgDetMain&o=7&rm=3",
        "price": "$275"
    },
    {
        "name": "Dogecoin Coin",
        "id-name": "Dogecoin-Coin",
        "category": "Technology",
        "image": "https://thevideoink.com/wp-content/uploads/2022/05/Dogecoin-1.jpg",
        "price": "$420"
    },
    {
        "name": "Funky Flashlight",
        "id-name": "Funky-Flashlight",
        "category": "Technology",
        "image": "https://thumbs.dreamstime.com/b/groovy-cartoon-travel-flashlight-funny-character-face-vector-comic-emoji-camping-lamp-traveler-portable-funky-emotion-347328145.jpg",
        "price": "$33"
    },
    {
        "name": "Mystery Box",
        "id-name": "Mystery-Box",
        "category": "Miscellaneous",
        "image": "https://cdn.shoplightspeed.com/shops/610593/files/2916194/mystery-box-mystery-box-7500.jpg",
        "price": "$777"
    },
    {
        "name": "Choco Katana",
        "id-name": "Choco-Katana",
        "category": "Miscellaneous",
        "image": "https://th.bing.com/th/id/R.9e5bc5c6f910c61aeaa4203fc1453155?rik=1PmCUiZGCfRzvw&riu=http%3a%2f%2f2.bp.blogspot.com%2f-JoAYS2gdgbc%2fTf9J_23fB2I%2fAAAAAAAACj4%2foHqMEqi5Dls%2fs1600%2fPocky_1_wm.jpeg&ehk=goZLkdj2G0eLOrQQffmO2rW3pJEvZr%2bMWjENn4pQa20%3d&risl=&pid=ImgRaw&r=0",
        "price": "$199"
    },
    {
        "name": "Air Fryer Drone",
        "id-name": "Air-Fryer-Drone",
        "category": "Technology",
        "image": "https://th.bing.com/th/id/OIP.BVe9-1FegAKZd9yCZGc0FQHaD3?o=7&cb=12rm=3&rs=1&pid=ImgDetMain&o=7&rm=3",
        "price": "$1450"
    },
    {
        "name": "Mini Volcano",
        "id-name": "Mini-Volcano",
        "category": "Miscellaneous",
        "image": "https://th.bing.com/th/id/R.22a84ebb179a87c5972a0602f2baa9cc?rik=CJAmo%2bPsTCqxBw&riu=http%3a%2f%2f3.bp.blogspot.com%2f-jQKtk_FK7b8%2fTV8q5uddyjI%2fAAAAAAAAAVo%2fpcC66MXURUU%2fs1600%2farenal%2bvolcano%2beruption.jpg&ehk=baZlhYP1vQFJFG0KGEMGKZNBhLLl%2bouGEBbZwDlcWZs%3d&risl=&pid=ImgRaw&r=0",
        "price": "$605"
    },
    {
        "name": "Quantum Dice",
        "id-name": "Quantum-Dice",
        "category": "Miscellaneous",
        "image": "https://cdn11.bigcommerce.com/s-70184/images/stencil/1280w/products/3914/10989/d20-dice-transparent-blue__20693.1665519675.jpg?c=2",
        "price": "$888"
    },
    {
        "name": "Time-Travel Alarm Clock",
        "id-name": "Time-Travel-Alarm-Clock",
        "category": "Technology",
        "image": "https://i5.walmartimages.com/asr/4c40c713-7ccb-4e16-81e6-a70d900170b8.0c1153c4cd79501bd330bddb5c083bac.jpeg",
        "price": "$1234"
}])

let cart = ref([])

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

</script>

<template>
  <div id="container">
    <ItemCards v-for="item in dict" :key="item.name":item="item" @purchase="initCount"></ItemCards>
  </div>
  <div id="shopping">
    <ShoppingCart v-for="item in cart" :key="item.name" :shop-item="item" @plus="add" @minus="minus"></ShoppingCart>
    <ShoppingTotal :totals="cart"></ShoppingTotal>
  </div>
</template>

<style scoped>

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
