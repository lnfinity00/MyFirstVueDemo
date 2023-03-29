<script setup>
import { ref, reactive } from "vue";
import TabItem from "./components/TabItem.vue"
import TabList from "./components/TabList.vue"
import Tab from "./components/Tab.vue"
const current = ref(0);//0表示球员，1表示球队
const player = reactive([{
    name: "梅西",
    img: "/public/img/messi.png",
    rate: 1,
    hot: 51120
}, {
    name: "内马尔",
    img: "/public/img/neymar.png",
    rate: 2,
    hot: 41120
}, {
    name: "C罗",
    img: "/public/img/ronaldo.png",
    rate: 3,
    hot: 31120
}, {
    name: "胡炜臻",
    img: "/public/img/胡.jpg",
    rate: 4,
    hot: 250
}
])
const team = reactive([
    {
        name: "巴西",
        img: "/public/img/巴西.jpg",
        rate: 1,
        hot: 40000
    }, {
        name: "法国",
        img: "/public/img/\法国.jpg",
        rate: 2,
        hot: 30000
    }, {
        name: "荷兰",
        img: "/public/img/荷兰.jpg",
        rate: 3,
        hot: 20000
    }, {
        name: "荷兰",
        img: "/public/img/荷兰.jpg",
        rate: 3,
        hot: 20000
    }
])
</script>
<template>
    <Tab>
        <template #player>
            <TabList :player="player"></TabList>
        </template>
        <template #team>
            <TabList :player="team"></TabList>
        </template>
    </Tab>
</template>
