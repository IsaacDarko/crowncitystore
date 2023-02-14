<template>
    <section class="Hero">

        <div v-bind:class="{'blue bg-dawn-blue': currentClicked === 0, 'expanded bg-dawn-blue': currentClicked === 1, 'retracted bg-dawn-blue': currentClicked != 1}" 
        @click="expandBox(1)">      
            <img  v-bind:class="{'hoverimg-dawn': currentClicked === 0, 'hoverimg-dawn-expanded': currentClicked === 1, 'hoverimg-dawn-retracted': currentClicked != 1}"
            src="../assets/nikedawns.png" alt="bluenikes" />
            <h1 v-bind:class="{'dawn-title': currentClicked === 0, 'dawn-title-expanded': currentClicked === 1, 'dawn-title-retracted': currentClicked != 1}" 
            >NEW</h1>
        </div>

        <div v-bind:class="{'white bg-storm-gray': currentClicked === 0, 'expanded bg-storm-gray': currentClicked === 2, 'retracted bg-storm-gray': currentClicked != 2}"  
        @click="expandBox(2)">
            <img v-bind:class="{'hoverimg-noon': currentClicked === 0, 'hoverimg-noon-expanded': currentClicked === 2, 'hoverimg-noon-retracted': currentClicked != 2}" 
            src="../assets/nikenoons.png" alt="whitenikes" />
            <h1 v-bind:class="{'noon-title': currentClicked === 0, 'noon-title-expanded': currentClicked === 2, 'noon-title-retracted': currentClicked != 2}"
            >BOLD</h1>
        </div>

        <div v-bind:class="{'pink bg-dusk-pink': currentClicked === 0, 'expanded bg-dusk-pink': currentClicked === 3, 'retracted bg-dusk-pink': currentClicked != 3}" 
        @click="expandBox(3)">
            <img v-bind:class="{'hoverimg-dusk': currentClicked === 0, 'hoverimg-dusk-expanded': currentClicked === 3, 'hoverimg-dusk-retracted': currentClicked != 3}" 
            src="../assets/nikedusks.png" alt="pinknikes" />
            <h1 v-bind:class="{'dusk-title': currentClicked === 0, 'dusk-title-expanded': currentClicked === 3, 'dusk-title-retracted': currentClicked != 3}"
            >FAST</h1>
        </div>        
        
    </section>
</template>




<script>
    
    export default {
        data() {
            return {
                currentClicked : 0
            };
        },
        methods: {
            expandBox(n) {
                if(this.currentClicked === n){
                    this.currentClicked = 0
                }else{
                    this.currentClicked = n
                }
            }

        }
    };

</script>





<style lang="css" scoped>

.Hero{
    width: 100%;
    height: 70rem;
    display: flex;
    flex: 1;
    flex-direction: row;
}

.expanded{
    display: flex;  
    justify-content: center;  
    align-items: center;
    flex-direction: column;
    width: 60%;
    transition: width 500ms ease-in;
    color: white;
    z-index: 3;
}

.retracted{
    display: flex;  
    justify-content: center;  
    align-items: center;
    flex-direction: column;
    width: 20%;
    transition: width 500ms ease-in;
    color: white;
    z-index: 2;
}

.blue{
    display: flex;  
    justify-content: center;  
    align-items: center;
    flex-direction: column;
    width: 34%;
    color: white;
    z-index: 2;
}


.white{
    display: flex;  
    justify-content: center;  
    align-items: center;
    flex-direction: column;
    width: 32%;
    color: black;
    z-index: 2;
}


.pink{
    display: flex;  
    justify-content: center;  
    align-items: center;
    flex-direction: column;
    width: 34%;
    color: white;
    z-index: 2;
}

.dawn-title{
    z-index:0;
    font-size:150px;
    font-weight:900;
    font-style: italic;
    color:white;
}

.dawn-title-expanded{
    z-index:1;
    font-size:330px;
    font-weight:900;
    font-style: italic;
    color:white;
    transition: font-size 500ms ease-in;
    transform: scale(1);
}

.dawn-title-retracted{
    z-index:-1;
    font-style: italic;
    color:white;
    font-size:150px;
    font-weight:900;
    transition: font-size 500ms ease-in;
    transform: scale(1);
}

.noon-title{
    z-index:0;
    font-size:150px;
    font-weight:900;
    font-style: italic;
    color:black;
}

.noon-title-expanded{
    z-index:1;
    font-size:330px;
    font-weight:900;
    font-style: italic;
    color:black;
    transition: font-size 500ms ease-in;
    transform: scale(1);
}

.noon-title-retracted{
    z-index:-1;
    font-style: italic;
    color:black;
    font-size:150px;
    font-weight:900;
    transition: font-size 500ms ease-in;
    transform: scale(1);
}

.dusk-title{
    z-index:0;
    font-size:150px;
    font-weight:900;
    font-style: italic;
    color:white;
}

.dusk-title-expanded{
    z-index:1;
    font-size:330px;
    font-weight:900;
    font-style: italic;
    color:white;
    transition: font-size 500ms ease-in;
    transform: scale(1);
}

.dusk-title-retracted{
    z-index:-1;
    font-style: italic;
    color:white;
    font-size:150px;
    font-weight:900;
    transition: font-size 500ms ease-in;
    transform: scale(1);
}



.hoverimg-dawn {
   position: absolute;
   z-index: 3;
   width: 525px;
   height: 639px;
   margin: 1rem 0rem;
}

.hoverimg-dawn-expanded{
    position: absolute;
    z-index: 4;
    width: 525px;
    height: 639px;
    margin: 1rem 0rem;
    rotate: 30deg;
    transition: rotate 500ms ease-in;
}

.hoverimg-dawn-retracted{
    position: absolute;
    z-index: 1;
    width: 525px;
    height: 639px;
    animation: rotate 30s infinite linear;
    rotate: 0deg;
    transition: rotate 500ms ease-in;
}


.hoverimg-noon {
   position: absolute;
   z-index: 3;
   width: 519px;
   height: 1041px;
}

.hoverimg-noon-expanded{
    position: absolute;
    z-index: 4;
    width: 519px;
    height: 1041px;
    rotate: 25deg;
    transition: rotate 500ms ease-in;
}

.hoverimg-noon-retracted{
    position: absolute;
    z-index: 1;
    width: 519px;
    height: 1041px;
    rotate: 0deg;
    transition: rotate 500ms ease-in;
}


.hoverimg-dusk {
   position: absolute;
   z-index: 3;
   width: 520px;
   height: 831px;
}

.hoverimg-dusk-expanded{
    position: absolute;
    z-index: 4;
    width: 520px;
    height: 831px;
    rotate: 31deg;
    transition: rotate 500ms ease-in;
}

.hoverimg-dusk-retracted{
    position: absolute;
    z-index: 1;
    width: 520px;
    height: 831px;
    rotate: 0deg;
    transition: rotate 500ms ease-in;
}


</style>