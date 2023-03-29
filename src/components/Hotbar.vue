<script setup>
import {computed} from "vue"
const props=defineProps(["hot","maxhot"]);
const width=computed(()=>{
        return (props.hot/props.maxhot) *100+"%";

})
// console.log(width);

</script>


<template>
 <div class="hot-bar">
                            <div class="inner">{{ props.hot }}热度</div>
                        </div>



</template>


<style scoped>
.hot-bar{
border-radius: 20px;
background-color:rgb(3,37,103) ;
text-indent: 0.5em;
overflow:hidden;
}
.inner{
    width: v-bind(width);
border-radius: 20px;
background-color:rgb(187,3,52);
background-image: linear-gradient(90deg,rgb(187,3,52)50%,rgb(66,2,12));
white-space: nowrap;
}


</style>