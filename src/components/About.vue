<template>
    <div class="about">
        <div class="em">
            <h1>ABOUT.</h1>
        </div>
        <div class="em">
            <p>We at Rena make sure you get the best quality and stunning clothing that will make you feel like a celeb.</p>
        </div>   
    </div>
</template>

<script>
import { gsap } from 'gsap'
import { ScrollTrigger } from "gsap/dist/ScrollTrigger.min.js"
import { onMounted } from 'vue'


export default {
    setup () {
        

        onMounted(() => {
            gsap.registerPlugin(ScrollTrigger)


            gsap
            .from('.about h1, .about p', 1, {
                opacity: 0,
                y: '200%',
                ease: 'expo',
                scrollTrigger:{
                    trigger: '.about',
                    toggleActions: 'restart',   
                    start: 'top center',
                } 
            })
        })


    }
}

</script>

<style scoped>
.em{
    overflow: hidden;
    width: 50%;

}
.about{
    height: 100vh;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-evenly;
    align-items: center;
    width: 90%; 
    margin: auto;
}
.about h1{
    font-size: 100px;
    font-weight: 400;
}
.about p{
    font-size: 30px;

}
@media (max-width: 1070px) {
    .about{
        flex-direction: column
    }
    .about .em,.about p{
        width: 90%;
    }
}
@media (max-width: 490px) {
    .about h1{
        font-size: 60px
    }
    .about p{
        font-size: 24px
    }
}
</style>