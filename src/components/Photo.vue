<script setup>
import { computed } from 'vue';
const props=defineProps(["src","rate"]);
const color=computed(()=>{
        if(props.rate==1){
        return "rgb(254,45,70)";
        }else if(props.rate==2){
        return "rgb(245,102,1)"
        }else{
        return "rgb(247,169,1)"
        
        }

})
</script>
<template>
<div class="photo">
                        <img :src=props.src> 
                      <span>{{ props.rate }}</span>
                    </div>  
</template>


<style scoped>
.photo{
    position:relative;
width: 150px;
background-color: #fff;
border-radius: 10px;
overflow: hidden;
}
.photo img{
width: 100%;
vertical-align: middle;

}
.photo span{
position: absolute;
top: 0;
left: 0;
width: 50px;
height: 50px;
background-color:v-bind(color);
font-size: 20px;
font: bold;
color: #fff;
display: flex;
justify-content: center;
align-items: center;
border-bottom-right-radius: 20px ;
}

</style>