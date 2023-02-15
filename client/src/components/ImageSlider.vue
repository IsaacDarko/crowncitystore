<template>
    <!--mark-up for image slider imported in the mid-top section -->
    <section class="slider">

        <div class="nav">
            <h2 class="title" >Popular Right Now</h2><!--Title of section-->
            <!--slider controls buttons, previous and next buttons with a buffer image in between-->
            <button class="prev" @click="prevImageSet"><img src="../assets/svgs/bkwrdbtn.png" alt="previous" style="height: 25px; width: 25px;"></button>
            <img src="../assets/svgs/buffer.png" alt="button-buffer" style="height: 25px; width: 25px;">
            <button class="next" @click="nextImageSet"><img src="../assets/svgs/fwrdbtn.png" alt="next" style="height: 25px; width: 25px;"></button>
        </div>
        <!--Slider container-->
        <div class="slide">
            <div class="slider-container" >
                <img v-for="(image, index) in visibleImages"  :key="index" :src="image" :class="index === 0 ? 'slide-left' : 'slide-right'" />
            </div>
        </div>
        
        
        
    </section>

</template>




<script>
//importing all the required images for the slider assigned to variables
    import slide1 from '../assets/rect2.jpg';
    import slide2 from '../assets/rect3.jpg';
    import slide3 from '../assets/rect4.jpg';
    import slide4 from '../assets/rect5.jpg';
    import slide5 from '../assets/rect6.jpg';
    import slide6 from '../assets/rect7.jpg';
    
    //exporting all data and functions in the script to make the availbale to the entire component
    export default {
        data() {
        return {
            currentIndex: 0,
            images: [
                slide1,
                slide2,
                slide3,
                slide4,
                slide5,
                slide6
            ],
            imagesPerSet: 3
        };
        },
        //calculating the limit of the number of visible images in a set
        computed: {
        visibleImages() {
            return this.images.slice(this.currentIndex, this.currentIndex + this.imagesPerSet);
        }
        },
        //setting up my slider control functions
        methods: {
        //prevImageSet is called when the previous button is clicked
        prevImageSet() {
            if (this.currentIndex === 0) {
            this.currentIndex = this.images.length - this.imagesPerSet;
            } else {
            this.currentIndex = Math.max(0, this.currentIndex - this.imagesPerSet);
            }
        },
        //nextImageSet is called when the next button is clicked
        nextImageSet() {
            if (this.currentIndex + this.imagesPerSet >= this.images.length) {
            this.currentIndex = 0;
            } else {
            this.currentIndex += this.imagesPerSet;
            }
        }
        }
    };
</script>



<!--Applying Css styles-->
<style lang="css" scoped>
    .slider{
        display: flex;
        flex-direction: column;
    }

    .nav{
        display: flex;
        flex: 1;
        flex-direction: row;
        align-items: flex-end;
    }

    .title{
        width: 70%;
        padding: 0rem 5rem;
        font-size: 30px;
        font-weight:lighter;
    }

    .prev{
       display: flex; 
       align-content: flex-end;
    }

    .next{
        display: flex;
        align-content: flex-start;
    } 

    .slide{
        width: inherit;
        height: inherit;
        display: flex;
        flex: 1;
        flex-direction: row;
    }

    .slider-container {
        display: flex;
        flex: 1;
        flex-direction: row;
        width: inherit;
        height: inherit;
        overflow: hidden;
    }

    .slide-left {
        animation: slide 10s ease-in-out linear infinite;
        transition: slide 500ms ease-in-out;
    }

    @keyframes slide-left {
        0% {
            transform: translateX(100%);
            
        }
        50% {
            transform: translateX(50%);
        }
        100% {
            transform: translateX(0%);
        }
    }

    .slide-right {
        animation: slide 10s ease-in-out linear infinite;
        transition: slide 1500ms ease-in-out;
    }

    @keyframes slide-right {
        0% {
            transform: translateX(-100%);
        }
        50% {
            transform: translateX(-50%);
        }
        100% {
            transform: translateX(0%);
        }
    }

    img {
        padding: 0.5rem;
        margin: 0.5rem;
        width: 30rem;
        height: 30rem;
    }

</style>
