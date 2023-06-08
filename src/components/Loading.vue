<template>
    <div class="container">
        <div class="loader"></div>
        <div class="loader"></div>
        <div class="loader"></div>
    </div>


</template>


<style scoped>
.container{
    display: flex;
    margin-top: 1rem;
}
.loader{
    border-radius: 50%;
    background-color: gray;
    height: 1.5rem;
    width: 1.5rem;
    margin-left: .3rem;
}

.loader:nth-child(1){
    animation: load .6s ease-in-out alternate infinite;
}

.loader:nth-child(2){
    animation: load .6s ease-in-out alternate .2s infinite;
}

.loader:nth-child(3){
    animation: load .6s ease-in-out alternate .4s infinite;
}

@keyframes load {
    from{
        transform: scale(1);
    }

    to{
        transform: scale(0.2);
    }
}
</style>