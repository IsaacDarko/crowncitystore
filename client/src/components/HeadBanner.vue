<template>
    <section class="Hero">
        <!--setting up the 3 div columns in the head-banner each with condition classes in order to render the div based on the currentClicked value-->

        <!--setting up the div1 (dawn-blue) column with 3 condition classes in order to render the div based on the currentClicked value-->
        <div v-bind:class="{'blue bg-dawn-blue': currentClicked === 0, 'expanded bg-dawn-blue': currentClicked === 1, 'retracted bg-dawn-blue': currentClicked != 1}" 
        @click="expandBox(1)">    
            <!--setting up the image hovering over the div using conditional class rendering based on the clicked state of the parent div-->  
            <img  v-bind:class="{'hoverimg-dawn': currentClicked === 0, 'hoverimg-dawn-expanded': currentClicked === 1, 'hoverimg-dawn-retracted': currentClicked != 1}"
            src="../assets/nikedawns.png" alt="bluenikes" />
            <!--setting up the background h1-text (dawn-title) using conditional class rendering based on the clicked state of the parent div-->
            <h1 v-bind:class="{'dawn-title': currentClicked === 0, 'dawn-title-expanded': currentClicked === 1, 'dawn-title-retracted': currentClicked != 1}" 
            >NEW</h1>
        </div>

        <!--setting up the div2 (noon-white) column with 3 condition classes in order to render the div based on the currentClicked value-->
        <div v-bind:class="{'white bg-storm-gray': currentClicked === 0, 'expanded bg-storm-gray': currentClicked === 2, 'retracted bg-storm-gray': currentClicked != 2}"  
        @click="expandBox(2)">
            <!--setting up the image hovering over the div using conditional class rendering based on the clicked state of the parent div-->
            <img v-bind:class="{'hoverimg-noon': currentClicked === 0, 'hoverimg-noon-expanded': currentClicked === 2, 'hoverimg-noon-retracted': currentClicked != 2}" 
            src="../assets/nikenoons.png" alt="whitenikes" />
             <!--setting up the background h1-text (noon-title) using conditional class rendering based on the clicked state of the parent div-->
            <h1 v-bind:class="{'noon-title': currentClicked === 0, 'noon-title-expanded': currentClicked === 2, 'noon-title-retracted': currentClicked != 2}"
            >BOLD</h1>
        </div>

        <!--setting up the div3 (dusk-pink) column with 3 condition classes in order to render the div based on the currentClicked value-->
        <div v-bind:class="{'pink bg-dusk-pink': currentClicked === 0, 'expanded bg-dusk-pink': currentClicked === 3, 'retracted bg-dusk-pink': currentClicked != 3}" 
        @click="expandBox(3)">
            <!--setting up the image hovering over the div using conditional class rendering based on the clicked state of the parent div-->
            <img v-bind:class="{'hoverimg-dusk': currentClicked === 0, 'hoverimg-dusk-expanded': currentClicked === 3, 'hoverimg-dusk-retracted': currentClicked != 3}" 
            src="../assets/nikedusks.png" alt="pinknikes" />
             <!--setting up the background h1-text (dusk-title) using conditional class rendering based on the clicked state of the parent div-->
            <h1 v-bind:class="{'dusk-title': currentClicked === 0, 'dusk-title-expanded': currentClicked === 3, 'dusk-title-retracted': currentClicked != 3}"
            >FAST</h1>
        </div>        
        
    </section>
</template>




<script>
    //exporting the data and methods to make it accessible to the entire component
    export default {
        //declared data variable 'currentClicked' to keep track of the div which has been clicked
        data() {
            return {
                currentClicked : 0
            };
        },
        methods: {
        //function expandBox can be called by any of the divs and accepts an integer(n) which is the number of the div which of clicked
            expandBox(n) {
                //if the div is already clicked set currentClick to 0 to return the div to its orignal state
                if(this.currentClicked === n){
                    this.currentClicked = 0
                //else set currentClick to the number associated with the clicked div, this in turn expands the div
                }else{
                    this.currentClicked = n
                }
            //if currentClicked is not n and is not 0, div will retract, since another div has been clicked and is currently expanded
            }

        }
    };

</script>




<!--applying all the required Css rules to style elements and perform the needed animations-->
<style lang="css" scoped>

.Hero{
    width: 100%;
    height: 70rem;
    display: flex;
    flex: 1;
    flex-direction: row;
}


/*this class is applied to any div to expand it when currentClicked is set to it's associated number*/
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

/*this class is applied to any div to retract it when currentClicked is not set to 0, or it's associated number*/
.retracted{
    display: flex;  
    justify-content: center;  
    align-items: center;
    flex-direction: column;
    width: 20%;
    transition: width 500ms ease-in;
    color: white;
    z-index: 2;
    overflow: hidden;
}

/*default styling for dawn div*/
.blue{
    display: flex;  
    justify-content: center;  
    align-items: center;
    flex-direction: column;
    width: 34%;
    color: white;
    z-index: 2;
}

/*default styling for noon div*/
.white{
    display: flex;  
    justify-content: center;  
    align-items: center;
    flex-direction: column;
    width: 32%;
    color: black;
    z-index: 2;
}

/*default styling for dusk div*/
.pink{
    display: flex;  
    justify-content: center;  
    align-items: center;
    flex-direction: column;
    width: 34%;
    color: white;
    z-index: 2;
}

/*styling for background h1 for the dawn div (dawn-title) when the div is in default*/
.dawn-title{
    z-index:0;
    font-size:150px;
    font-weight:900;
    font-style: italic;
    color:white;
}

/*styling for background h1 for the dawn div (dawn-title) when the div expands*/
.dawn-title-expanded{
    z-index:1;
    font-size:330px;
    font-weight:900;
    font-style: italic;
    color:white;
    transition: font-size 500ms ease-in;
    transform: scale(1);
}

/*styling for background h1 for the dawn div (dawn-title) when the div retracts*/
.dawn-title-retracted{
    z-index:-1;
    font-style: italic;
    color:white;
    font-size:150px;
    font-weight:900;
    transition: font-size 500ms ease-in;
    transform: scale(1);
}

/*styling for background h1 for the noon div (noon-title) when the div is in default*/
.noon-title{
    z-index:0;
    font-size:150px;
    font-weight:900;
    font-style: italic;
    color:black;
}

/*styling for background h1 for the noon div (noon-title) when the div expands*/
.noon-title-expanded{
    z-index:1;
    font-size:330px;
    font-weight:900;
    font-style: italic;
    color:black;
    transition: font-size 500ms ease-in;
    transform: scale(1);
}

/*styling for background h1 for the noon div (noon-title) when the div retracts*/
.noon-title-retracted{
    z-index:-1;
    font-style: italic;
    color:black;
    font-size:150px;
    font-weight:900;
    transition: font-size 500ms ease-in;
    transform: scale(1);
}

/*styling for background h1 for the dusk div (dusk-title) when the div is in default*/
.dusk-title{
    z-index:0;
    font-size:150px;
    font-weight:900;
    font-style: italic;
    color:white;
}

/*styling for background h1 for the dusk div (dusk-title) when the div expands*/
.dusk-title-expanded{
    z-index:1;
    font-size:330px;
    font-weight:900;
    font-style: italic;
    color:white;
    transition: font-size 500ms ease-in;
    transform: scale(1);
}

/*styling for background h1 for the dusk div (dusk-title) when the div retracts*/
.dusk-title-retracted{
    z-index:-1;
    font-style: italic;
    color:white;
    font-size:150px;
    font-weight:900;
    transition: font-size 500ms ease-in;
    transform: scale(1);
}


/*styling for hovering-foreground image for the dawn div (hoverimg-dawn) when the div is in default*/
.hoverimg-dawn {
   position: absolute;
   z-index: 3;
   width: 525px;
   height: 639px;
   margin: 1rem 0rem;
}

/*styling for hovering-foreground image for the dawn div (hoverimg-dawn) when the div expands*/
.hoverimg-dawn-expanded{
    position: absolute;
    z-index: 4;
    width: 525px;
    height: 639px;
    margin: 1rem 0rem;
    rotate: 30deg;
    transition: rotate 500ms ease-in;
}

/*styling for hovering-foreground image for the dawn div (hoverimg-dawn) when the div retracts*/
.hoverimg-dawn-retracted{
    position: absolute;
    z-index: 0;
    width: 525px;
    height: 639px;
    animation: rotate 30s infinite linear;
    rotate: 0deg;
    transition: rotate 500ms ease-in;
}



/*styling for hovering-foreground image for the noon div (hoverimg-noon) when the div is in default*/
.hoverimg-noon {
   position: absolute;
   z-index: 3;
   width: 519px;
   height: 1041px;
}

/*styling for hovering-foreground image for the noon div (hoverimg-noon) when the div expands*/
.hoverimg-noon-expanded{
    position: absolute;
    z-index: 4;
    width: 519px;
    height: 1041px;
    rotate: 25deg;
    transition: rotate 500ms ease-in;
}

/*styling for hovering-foreground image for the noon div (hoverimg-noon) when the div retracts*/
.hoverimg-noon-retracted{
    position: absolute;
    z-index: 0;
    width: 519px;
    height: 1041px;
    rotate: 0deg;
    transition: rotate 500ms ease-in;
}



/*styling for hovering-foreground image for the dusk div (hoverimg-dusk) when the div is in default*/
.hoverimg-dusk {
   position: absolute;
   z-index: 3;
   width: 520px;
   height: 831px;
}

/*styling for hovering-foreground image for the dusk div (hoverimg-dusk) when the div expands*/
.hoverimg-dusk-expanded{
    position: absolute;
    z-index: 4;
    width: 520px;
    height: 831px;
    rotate: 31deg;
    transition: rotate 500ms ease-in;
}

/*styling for hovering-foreground image for the dusk div (hoverimg-dusk) when the div retracts*/
.hoverimg-dusk-retracted{
    position: absolute;
    z-index: 0;
    width: 520px;
    height: 831px;
    rotate: 0deg;
    transition: rotate 500ms ease-in;
}


</style>