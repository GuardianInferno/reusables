<template>
    <div class="container">
        <div class="box"></div>
        <div @click="active = !active" :class="[active ? 'box2-open' : 'box2']" >click me</div>
    </div>
</template>

<script setup lang="ts">
import {ref, computed } from 'vue'


let active: boolean = ref(false)




</script>

<style scoped>

.container{
    background: #f0f0f0;
    height: 20rem;
    display: flex;
    justify-content: center;
    align-items: center;
}


.box2{
    border-radius: 20px;
    margin: 1rem;
    width: 60px;
    height: 60px;
    background: #f0f0f0;
    box-shadow: 0 0 0 #cccccc,
                0 0 0 #ffffff,
                10px 10px 10px #cccccc inset,
                -10px -10px 10px #ffffff inset;
}

.box2-open{
    border-radius: 20px;
    margin: 1rem;
    width: 60px;
    height: 60px;
    background: #f0f0f0;
    box-shadow: 0 0 0 #cccccc,
                0 0 0 #ffffff,
                10px 10px 10px #cccccc inset,
                -10px -10px 10px #ffffff inset;
    animation: animate 4s cubic-bezier(0.16, 1, 0.3, 1) 1s alternate;
    animation-fill-mode: forwards;  

}


.box{
    border-radius: 20px;
    margin: 1rem;
    width: 60px;
    height: 60px;
    background: #f0f0f0;
    box-shadow: 0 0 0 #cccccc,
                0 0 0 #ffffff,
                10px 10px 10px #cccccc inset,
                -10px -10px 10px #ffffff inset;
    animation: animate 4s cubic-bezier(0.16, 1, 0.3, 1) 1s infinite alternate;
}

@keyframes animate {
    0%{
        width: 60px;
        height: 60px;
        background: #f0f0f0;
        box-shadow: 0 0 0 #cccccc,
                    0 0 0 #ffffff,
                    10px 10px 10px #cccccc inset,
                    -10px -10px 10px #ffffff inset;
    }

    25%{
        width: 60px;
        height: 60px;
        background: #f8f8f8;
        box-shadow: 10px 10px 10px #cccccc,
                    10px 10px 10px #ffffff
                    0 0 0 #cccccc inset,
                    0 0 0 #ffffff inset;

    }

    50%{
        width: 60px;
        height: 240px;
        background: #f8f8f8;
        box-shadow:  10px 10px 10px #cccccc,
                     10px 10px 10px #ffffff,
                     0 0 0 #cccccc inset,
                     0 0 0 #ffffff inset;
    }

    75%{
        widows: 270;
        height: 240px;
        background:#fafafa;
        box-shadow: 20px 20px 20px #cccccc,
                    5px 5px 5px #ffffff,
                    0 0 0 #cccccc inset,
                    0 0 0 #ffffff inset;
    }

    100%{
        width: 480px;
        height: 240px;
        background: #fafafa;
        box-shadow:  40px 40px 40px #cccccc,
                     0 0 0 #ffffff,
                     0 0 0 #cccccc inset,
                     2px 2px 2px #ffffff inset;

    }
    
}


</style>