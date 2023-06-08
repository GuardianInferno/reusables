<template>
    <nav class="navbar" v-if="open">
        <button @click="open = !open"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><title>dots-horizontal-circle</title><path d="M12,2A10,10 0 0,1 22,12A10,10 0 0,1 12,22A10,10 0 0,1 2,12A10,10 0 0,1 12,2M12,10.5A1.5,1.5 0 0,0 10.5,12A1.5,1.5 0 0,0 12,13.5A1.5,1.5 0 0,0 13.5,12A1.5,1.5 0 0,0 12,10.5M6.5,10.5A1.5,1.5 0 0,0 5,12A1.5,1.5 0 0,0 6.5,13.5A1.5,1.5 0 0,0 8,12A1.5,1.5 0 0,0 6.5,10.5M17.5,10.5A1.5,1.5 0 0,0 16,12A1.5,1.5 0 0,0 17.5,13.5A1.5,1.5 0 0,0 19,12A1.5,1.5 0 0,0 17.5,10.5Z" /></svg></button>
        <div class="navlink-container">
            <div class="navbar-link">Link1</div>
            <div class="navbar-link">Link2</div>
            <div class="navbar-link">Link3</div>
        </div>
    </nav>
    <button v-else @click="open = !open">test</button>

</template>

<script setup lang='ts'>
import {ref} from 'vue'
import MenuIcon from 'vue-material-design-icons/Menu.vue';

let open = ref(false)

const onClick = () =>{
    open = !open
    console.log(open)
}
</script>

<style scoped>

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