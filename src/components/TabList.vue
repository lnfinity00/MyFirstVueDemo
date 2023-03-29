<script setup>
import TabItem from './TabItem.vue';
const props=defineProps(["player"]);
</script>

<template>
<div class="tab-list">
                <!-- <TabItem :item=player[0] ></TabItem>
                <TabItem :item=player[1] ></TabItem>
                <TabItem :item=player[2] ></TabItem> -->
                <TabItem v-for="player in player" :item="player"></TabItem>   
            </div>

</template>


<style scoped>
.tab-list{
margin: 20px;
}
 </style>