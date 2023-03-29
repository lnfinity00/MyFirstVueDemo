<script setup>
import { ref } from "vue";
const current = ref(0);//0表示球员，1表示球队
</script>
<template>
    <!-- 外部容器 -->
    <div class="tab-wrapper">
        <div class="tab-header">
            <div @click="current = 0" class="tab-button" v-bind:class="{ active: current === 0 }">热门球员</div>
            <div @click="current = 1" class="tab-button" v-bind:class="{ active: current === 1 }">热门球队</div>
        </div>
        <div class="main">
            <div v-show="current === 0">
                <!-- <TabList :player="player"></TabList> -->
                <slot name="player"></slot>
            </div>
            <div v-show="current === 1">
                <!-- <TabList :player="team"></TabList> -->
                <slot name="team"></slot>
            </div>
        </div>
    </div>
</template>
<style scoped>
.tab-wrapper {
    width: 800px;
    box-sizing: border-box;
    padding: 20px;
    background-color: rgb(45, 83, 211);
}
.tab-header {
    display: flex;
    border-radius: 10px;
    overflow: hidden;
}
.tab-button {
    font-size: 30px;
    flex: auto;
    background-color: #fff;
    padding: 10px 0;
    text-align: center;
    cursor: pointer;
    transition: 0.30s;
}
.tab-button:not(.active):hover {
    color: rgb(187, 2, 52);
}
.active {
    background-color: rgb(187, 2, 52);
    color: #fff;
}
</style>