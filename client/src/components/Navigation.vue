<template>

    <div class="navbar">

            <div class='navbar-logo'>
                <img src={images.logoclear} alt='logo' />
            </div>

            <ul class='navbar-menu'>
                <li class="navbar-links"> <a href="#">New&Featured</a> </li>
                <li class="navbar-links"> <a href="#">Men</a> </li>
                <li class="navbar-links"> <a href="#">Women</a> </li>
                <li class="navbar-links"> <a href="#">Kids</a> </li>
                <li class="navbar-links"> <a href="#">Sale</a> </li>
            </ul>

            <div class='navbar-icons'> 
                <h4>hearticon</h4>
                <h4>carticon</h4>
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
        z-index: 2;
    }

    .navbar-menu {  
        width: 50%;
        display: flex;
        flex: 1;
        flex-direction: row;
        justify-content: flex-start;
        align-items: center;
        margin: 0 23rem;
    }

    li {
        display: flex;
        flex-direction: row;
        list-style: none;
        margin: 0 1rem;
        cursor: pointer;
    }
    

</style>