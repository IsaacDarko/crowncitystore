<template>
    <section class="Hero">

        <div class="blue bg-dawn-blue">
            <img src="" alt="">
            <h1 class="text-9xl italic font-black">NEW</h1>

        </div>

        <div class="white bg-glossy-white">
            <img src="" alt="">
            <h1 class="text-9xl italic font-black">BOLD</h1>
        </div>

        <div class="pink bg-dusk-pink">
            <img src="" alt="">
            <h1 class="text-9xl italic font-black">FAST</h1>
        </div>        
        
    </section>
</template>

<script setup>

</script>

<style lang="css" scoped>

.Hero{
    width: 100%;
    height: 50rem;
    display: flex;
    flex: 1;
    flex-direction: row;
}

.blue{
    display: flex;  
    justify-content: center;  
    align-items: center;
    flex-direction: column;
    width: 34%;
    color: white;
}

.white{
    display: flex;  
    justify-content: center;  
    align-items: center;
    flex-direction: column;
    width: 32%;
}

.pink{
    display: flex;  
    justify-content: center;  
    align-items: center;
    flex-direction: column;
    width: 34%;
    color: white;
}

</style>