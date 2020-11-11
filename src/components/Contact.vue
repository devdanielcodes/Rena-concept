<template>
    <div class="contact">
        <div class="con">
            <h1>Contact.</h1>
            <form>
                <label class="label" for="">Name</label>
                <input type="text">
                <label class="label" for="">Email</label>
                <input type="mail">
                <label class="label" for="">Msg</label>
                <input type="text">
                <button>Send</button>
            </form>
        </div>
        <div class="em">
            <img src="../assets/cont.png" alt="" class="contimg">
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
            .from('.contimg', 2, {
                y: '100%',
                ease: 'expo',
                scrollTrigger:{
                    trigger: '.contact',
                    toggleActions: 'restart',   
                    start: 'top center'
                } 
            })
        })


    }
}

</script>

<style scoped>

.contact{
    height: 100vh;
    width: 90%;
    margin: auto;
    position: relative;
}
.contact h1{
    font-size: 100px;
    padding: 50px 0;
    font-weight: 400;
}
form{
    width: 400px;
    position: absolute;
    top: 50%;
    left: 10%;
    transform: translateY(-50%);
}
form input{
    width: 100%;
    margin-bottom: 5vh;
    border: none;
    height: 30px;
    border-bottom: 2px solid white;
    background: none;
    color: white;
    outline: none;
}
button{
    border: none;
    padding: 20px;
    font-size: 20px;
    border-bottom: 2px solid white;
    background: none;
    color: white;
    outline: none;
}
.em{
    overflow: hidden;
    position: absolute;
    top: 50%;
    right: 10%;
    width: 500px;
    height: 40vh;
    transform: translateY(-50%);
}
.contimg{
    width: 100%;
    height: 100%;
    object-fit: cover;
}
@media (max-width: 1400px){
    .em{
        width: 300px
    }  
}
@media (max-width: 960px){
    .em{
        display: none
    }
}
@media (max-width: 490px){  
    .contact h1{
        font-size: 60px;
    }
    form{
        width: 80%;
    }
}
</style>