<template>
    <div class="about">
        <h1>ABOUT.</h1>
        <p>We at Rena make sure you get the best quality and stunning clothing that will make you feel like a celeb .</p>
    </div>
</template>

<script>
//import { onMounted } from 'vue'

export default {
    setup () {
        
    }
}

</script>

<style scoped>
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
    width: 50%;
}
.about p{
    font-size: 30px;
    width: 50%;

}
@media (max-width: 1070px) {
    .about{
        flex-direction: column
    }
    .about h1,.about p{
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