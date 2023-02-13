<template>

    <section class="midsection">
        
        <div class="texts">
            <h1 class="title">Fresh Air</h1>

            <p>With its heritage track look and innovative Air design, the Air Max SC brings iconic comfort to your everyday style</p>
        </div>

        <div class="buttons">

            <button class="shop-gender">Shop Men's</button>
            <button class="shop-gender">Shop Women's</button>

        </div>

    </section>
</template>

<script setup>

</script>

<style lang="css" scoped>
    .midsection{
        display: flex;  
        justify-content: center;  
        align-items: center;
        flex-direction: column;
        margin-bottom: 5rem;
    }

    .texts{
        display: flex;  
        justify-content: center;  
        align-items: center;
        flex-direction: column;
        padding: 2rem;
        margin: 1rem;
        width: 37%;
    }

    .title{
        font-size: 60px;
        font-weight: 900;
        text-transform: capitalize;
    }

    p{
        font-size: 20px;
        font-weight: lighter;
        text-align: justify;
    }

    .buttons{

    }


    .shop-gender{
        width: 9rem;
        height: 4rem;
        border-radius: 2rem;
        background-color: black;
        color: white;
        font-weight: bold;
        margin: 0rem 1rem;
    }


</style>