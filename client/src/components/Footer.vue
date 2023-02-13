<template>

    <div class="footer bg-storm-gray">

        <div class="footer-body">

            <div class="socials">
                <img class="footer-logo" src="../assets/svgs/talogo.png" alt="travel-agent-logo">
                <p class="vision">
                    We believe brand interaction is key in 
                    communication. Real innovations and 
                    a positive.
                </p>
                <div class="social-icons">
                    <a href="#"><img class="ico" src="../assets/svgs/twitter.png" alt="twitter"></a>
                    <a href="#"><img class="ico" src="../assets/svgs/insta.png" alt="instagram"></a>
                    <a href="#"><img class="ico" src="../assets/svgs/youtube.png" alt="youtube"></a>
                </div>
            </div>

            <div class="about">
                <h1 class="title">About Us</h1>
                <ul>
                    <li><a href="#">Features</a></li>
                    <li><a href="#">FAQ's</a></li>
                    <li><a href="#">News</a></li>
                    <li><a href="#">Pricing</a></li>
                </ul>
            </div>

            <div class="company">
                <h1 class="title">Company</h1>
                <ul>
                    <li><a href="#">Core Values</a></li>
                    <li><a href="#">Partner w/ us</a></li>
                    <li><a href="#">Blog</a></li>
                    <li><a href="#">Contact</a></li>
                </ul>
            </div>

            <div class="contact-form">
                <h1 class="title">Get In Touch</h1>
                    <input type="text" placeholder="Your email here..." class="form-input"/>
                    <button class="form-button" @click="submitForm">Get Access</button>
            </div>

        </div>

        <hr class="divider">

        <div class="footer-base">

            <div class="copyright">
                <h1>Travel Agent © 2023. All Rights Reserved</h1>
            </div>

            <div class="privacy">
                <ul class="last-menu">
                    <li><a href="#">Terms of Service</a></li>
                    <li><a href="#">Privacy Policy</a></li>
                </ul>

            </div>

        </div>
        
    </div>

</template>



<script setup>
    function submitForm() {
        console.log('message submitted')
    }

</script>



<style lang="css" scoped>
    .footer{
        width: 100%;
        height: 30rem;
        padding: 0rem 3rem;
    }

    .footer-body{
        height: 75%;
        display: flex;
        flex: 1;
        flex-direction: row;
        justify-content: flex-start;
        color: #858585;
    }

    .socials{
        width: 40%;
        display: flex;  
        justify-content: center;  
        flex-direction: column;
        padding: 5rem 2rem;
    }

    .footer-logo{
        width: 115px;
        height: 46px;
        margin: 1rem 0rem;
    }

    .vision{
        width: 65%;
        font-size: 17px;
        margin: 1rem 0rem;
    }

    .social-icons{
        display: flex;
        flex: 1;
        flex-direction: row;
        margin: 1rem 0rem;
    }

    .ico{
        width: 26px;
        height: 22px;
        margin: 0rem 0.3rem;
    }

    .title{
        font-size: 20px;
        font-weight: light;
        padding: 1rem;
        color: black;
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

    .contact-form{
        width: 20%;
        display: flex;  
        flex-direction: column;
        padding:4rem 2rem;
    }

    li {
        margin: 1rem 0rem;
    }

    .form-input{
        -webkit-user-select: none; /* WebKit browsers */
        -moz-user-select: none; /* Mozilla browsers */
        -ms-user-select: none; /* Internet Explorer */
        user-select: none; /* Standard syntax */
        width: 100%;
        height: 3rem;
        background-color: #d5d5d5;
        padding: 1rem;
        margin: 1rem 0rem;
    }

    .form-button{
        width: 100%;
        height: 3rem;
        background-color: black;
        font-size: 15px;
        font-weight: light;
        color: white;
    }
    
    .divider{
        border-color: rgb(191, 189, 189);
    }

    .footer-base{
        width: 100%;
        height: 75%;
        display: flex;
        flex: 1;
        flex-direction: row;
        justify-content: flex-start;
        color: #858585;
    }

    .copyright {
        width: 70%;
        padding: 2rem 3rem;
    }

    .last-menu {
        display: flex;
        flex: 1;
        flex-direction: row;
        justify-content: flex-start;    
        padding: 2rem ;    
    }

    li {
        margin-left: 2rem;
    }

</style>