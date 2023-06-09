<template>
    <nav class="navbar" v-if="open">
        <button @click="open = !open" class="icon-open"><MenuIcon class="icon-nav-open" /></button>
        <div class="navlink-container">
            <div class="navbar-link">Link1</div>
            <div class="navbar-link">Link2</div>
            <div class="navbar-link">Link3</div>
        </div>
    </nav>
    <button v-else @click="open = !open" class="icon-close"><MenuIcon class="icon-nav-close" /></button>

</template>

<script setup lang='ts'>
import {ref} from 'vue'
import MenuIcon from 'icons/Menu.vue';

let open:boolean = ref(false)

const onClick = () =>{
    open = !open
    console.log(open)
}
</script>

<style scoped>
.material-design-icon.icon-nav-open{
    display: block;
    transform: scale(1.2);
}
.icon-open{
    border: none;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    background-color: black;
    width:3rem;
    height: 3rem;

    
}



.material-design-icon.icon-nav-close{
    display: block;
    transform: scale(1.2);
}

.icon-close{
    border: none;
    width:3rem;
    height: 3rem;
    background-color: white;
}


.navbar{
    width: 10vw;
    height: 100vh;
    background-color: black;

}

.navlink-container{
    display: flex;
    flex-direction: column;
    align-items: center;
}

.navbar-link{
    color:white;
    padding: 5rem 0;

}


</style>