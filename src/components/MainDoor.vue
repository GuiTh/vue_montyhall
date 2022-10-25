<template>
  <div class="door-area">
    <div class="door-f">
        <MainGift v-if="open && hasGift" />
    </div>
    <div class="door">
        <div class="number">{{number}}</div>
        <div class="knob"></div>
    </div>
  </div>
</template>

<script>
import MainGift from './MainGift';

export default {
    name:'MainDoor',
    components: {MainGift},
    props:{
        number:{},
        hasGift:{type: Boolean}
    },
    data:function(){
        return{
            open:false,
            selected: false
        }
    }
}
</script>

<style>
:root{
    --dor-border: 5px solid brown;
}
.door-area{
    position: relative;
    width: 200px;
    height: 310px;
    border-bottom: 10px solid #AAA;
    margin-bottom: 20px;
    font-size: 3rem;
    display: flex;
    justify-content: center;
}
.door-frame{
    position: absolute;
    height: 300px;
    width: 180px;
    
}
</style>