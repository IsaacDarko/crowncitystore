<template>
    <div class="mid-bottom">
        <h1 class="title">Popular Right Now</h1>

        <div class="categories">
            <div>
                <img class="cat-imgs" src="../assets/hoodieguy.jpg" alt="mens_nike_fleece">
                <p class="label">Men's Nike Fleece</p>
            </div>

            <div>
                <img class="cat-imgs" src="../assets/hoodiegirl.jpg" alt="womens_nike_fleece">
                <p class="label">Women's Nike Fleece</p>
            </div>

            <div>
                <img class="cat-imgs" src="../assets/hoodiekid.jpg" alt="kids_nike_fleece">
                <p class="label">Kid's Nike Fleece</p>
            </div>
        </div>

    </div>

</template>

<script setup>

</script>

<style lang="css" scoped>
    .mid-bottom{
        display: flex;
        flex: 1;
        flex-direction: column;
        padding: 2rem 5rem;
        margin: 5rem 0rem;
    }

    .title{
        padding: 2rem 1rem;
        font-size: 40px;
        font-weight: light;
    }

    .categories{
        display: flex;
        flex: 1;
        flex-direction: row;

    }

    .cat-imgs{
        padding: 0rem 1rem;
    }

    .label{
        padding: 1rem;
        font-size: 20px;
        font-weight: lighter;
    }

</style>