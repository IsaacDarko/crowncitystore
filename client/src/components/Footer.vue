<template>

    <div class="footer bg-storm-gray">

        <div class="footer-body">

            <div class="socials">
                <img src="" alt="">
                <p>
                    We believe brand interaction is key in 
                    commu nication. Real innovations and 
                    a positive.
                </p>
            </div>

            <div class="about">
                <h1>second col</h1>
            </div>

            <div class="company">
                <h1>third col</h1>
            </div>

            <div class="contacts">
                <h1>fourth col</h1>
            </div>
            
        </div>

        <hr class="divider">

        <div class="footer-base">

            <div>

            </div>

            <div>

            </div>

        </div>
        
    </div>

</template>

<script setup>

</script>

<style lang="css" scoped>
    .footer{
        width: 100%;
        height: 30rem;
    }

    .footer-body{
        height: 75%;
        display: flex;
        flex: 1;
        flex-direction: row;
        justify-content: flex-start;
    }

    .socials{
        width: 40%;
        display: flex;  
        justify-content: center;  
        align-items: center;
        flex-direction: column;
        padding:1rem 3rem;
    }

    .about{
        width: 20%;
        display: flex;  
        justify-content: center;  
        align-items: center;
        flex-direction: column;
        padding:1rem 2rem;
    }

    .company{
        width: 20%;
        display: flex;  
        justify-content: center;  
        align-items: center;
        flex-direction: column;
        padding:1rem 2rem;
    }

    .contacts{
        width: 20%;
        display: flex;  
        justify-content: center;  
        align-items: center;
        flex-direction: column;
        padding:1rem 2rem;
    }
    
    .divider{
        border-color: rgb(191, 189, 189);
    }

    .footer-base{

    }

</style>