<template>

    <div class="navbar">

            <div class='navbar-logo'>
                <img class="site-logo" src="../assets/svgs/sitelogo.png" alt='logo' />
            </div>

            <ul class='navbar-menu'>
                <li class="navbar-links"> <a href="#">New&Featured</a> </li>
                <li class="navbar-links"> <a href="#">Men</a> </li>
                <li class="navbar-links"> <a href="#">Women</a> </li>
                <li class="navbar-links"> <a href="#">Kids</a> </li>
                <li class="navbar-links"> <a href="#">Sale</a> </li>
            </ul>

            <div class='navbar-icons'> 
                <img class="icons" src="../assets/svgs/heart.png" alt="favourite">
                <img class="icons" src="../assets/svgs/cart.png" alt="cart">
            </div>
        
    </div>

</template>




<script setup>

</script>




<style lang="css" scoped>
    .navbar {
        background-color: rgba(0,0,0,0);
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 60px;
        padding: 4rem 8rem;
        color: #000;
        position: absolute;
        z-index: 5;
    }

    .site-logo{
        width: 80px;
        height: 29px;
    }

    .navbar-menu {  
        width: 40%;
        display: flex;
        flex: 1;
        flex-direction: row;
        justify-content: flex-start;
        align-items: center;
        margin: 0 5rem;
        padding: 0rem 16rem;
    }

    .navbar-icons{
        display: flex;
        flex: 1;
        flex-direction: row;
        justify-content: flex-end;
        width: 30%;
    }

    .icons{
        width: 20px;
        height: 20px;
       margin: 0rem 1rem;
    }

    li {
        display: flex;
        flex-direction: row;
        list-style: none;
        margin: 0 1rem;
        cursor: pointer;
    }
    

</style>