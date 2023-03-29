
<script setup>
import {ref,reactive} from "vue"
import Photo from "./photo.vue";
import Hotbar from "./hotbar.vue";
const props = defineProps(["item"])
</script>

<template>
 <div class="tab-item">
                  <Photo :src=props.item.img :rate=props.item.rate></Photo>
                 <div class="desc">
                <span class="name">{{props.item.name}}</span>
            <Hotbar :hot=props.item.hot :maxhot=70000></Hotbar>
                    </div>
                </div>
            
</template>
<style scoped>
.tab-item{
display: flex;
margin-bottom: 20px;
}

.desc{
font-size: 30px;
color: #fff;
display: flex;
flex-flow: column;
justify-content: space-evenly;
/* background-color: #bfc; */
flex: auto;
margin-left: 30px;
}
 
</style>