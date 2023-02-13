<template>

    <section class="tail-shop">

        <div class="shop-banner">

            <h1 class="banner-title">
                styles to fall <br> in love with
            </h1> 

            <p class="banner-text">Find something better than roses</p>

            <button class="shop-button">
                Shop
            </button>

        </div>

    </section>

</template>


<script setup>

</script>

<style lang="css" scoped>  
    .tail-shop{
        width: 100%;
        height: 35rem;
        display: flex;  
        flex-direction: row;
    }


    div.shop-banner {
        width: 100%;
        height: 90%;
        background: url('../assets/rect.png');
        background-repeat: no-repeat;
        background-size: 1535px 611px;
        padding: 5rem;
        color: white;
    }

    h1{
        font-size: 80px;
        font-weight: 1000;
        text-transform: capitalize;
        margin-bottom: 2rem;
        line-height: 5rem;
    }

    .shop-button{
        width: 8rem;
        height: 4rem;
        border-radius: 2rem;
        background-color: white;
        color: black;
        font-size: 18px;
        font-weight: bold;
        margin-top: 1rem;
    }

</style>