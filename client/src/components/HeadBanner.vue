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
    color: white;
    z-index: 3;
    animation-delay: 1s;
    animation-duration: 3s;
    animation-fill-mode: forwards;
}

@keyframes expanded {
   
    from { 
            left: 0% 
        }
    to { 
            left:  26%
        }
}

.retracted{
    display: flex;  
    justify-content: center;  
    align-items: center;
    flex-direction: column;
    width: 20%;
    color: white;
    z-index: 1;
    animation: slide 10s ease-in-out linear infinite;
    animation-delay: 1s;
    animation-duration: 15s;
    animation-fill-mode: forwards;
}

@keyframes retracted {
  from {
    transform: translateX(60%);
  }
  to {
    transform: translateX(34%);
  }
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
}

.dawn-title-retracted{
    z-index:-2;
    font-style: italic;
    color:white;
    font-size:150px;
    font-weight:900;
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
}

.noon-title-retracted{
    z-index:-2;
    font-style: italic;
    color:black;
    font-size:150px;
    font-weight:900;
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
}

.dusk-title-retracted{
    z-index:-2;
    font-style: italic;
    color:white;
    font-size:150px;
    font-weight:900;
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
    animation: rotation 30s infinite linear;
    transition-timing-function: ease-in-out;
    rotate: 30deg;
}

@keyframes hoverimg-dawn-expanded {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(90deg);
  }
}

.hoverimg-dawn-retracted{
    position: absolute;
    z-index: 2;
    width: 525px;
    height: 639px;
    animation: rotate 30s infinite linear;
    transition-timing-function: ease-in-out;
}

@keyframes hoverimg-dawn-retracted {
  from {
    transform: rotate(90deg);
  }
  to {
    transform: rotate(0deg);
  }
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
    animation: rotation 30s infinite linear;
    transition-timing-function: ease-in-out;
    rotate: 30deg;
}

@keyframes hoverimg-noon-expanded {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(90deg);
  }
}

.hoverimg-noon-retracted{
    position: absolute;
    z-index: 2;
    width: 519px;
    height: 1041px;
    animation: rotation 30s infinite linear;
    transition-timing-function: ease-in-out;
   
}

@keyframes hoverimg-noon-retracted {
  from {
    transform: rotate(120deg);
  }
  to {
    transform: rotate(0deg);
  }
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
    animation: rotate 30s infinite linear;
    transition-timing-function: ease-in-out;
    rotate: 31deg;
}

@keyframes hoverimg-dusk-expanded {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(30deg);
  }
}

.hoverimg-dusk-retracted{
    position: absolute;
    z-index: 2;
    width: 520px;
    height: 831px;
    animation: rotate 30s infinite linear;
    transition-timing-function: ease-in-out;
}

@keyframes hoverimg-dusk-retracted {
  from {
    transform: rotate(30deg);
  }
  to {
    transform: rotate(-60deg);
  }
}


</style>