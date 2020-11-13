<template>
  <div class="main">
    <img src="./assets/bg.svg" alt="" class="bg">
    <v-logo class="logo" />
    <v-land id="top" />
    <v-about id="about" />
    <v-contact id="contact"/>
    <v-nav />
    <div class="cursor"></div>
  </div>
</template>

<script>
import { onMounted } from 'vue'
import { gsap } from 'gsap'

import Logo from './components/Logo.vue'
import Landing from './components/Landing.vue'
import About from './components/About.vue'
import Contact from './components/Contact.vue'
import Nav from './components/Nav.vue'




  export default{
    components: {
      'v-logo': Logo ,
      'v-land': Landing ,
      'v-about': About ,
      'v-contact': Contact,
      'v-nav': Nav

    },
    setup(){
      onMounted(() => {
          gsap.from('.bg', 1, {
                transform: 'translateX(-100%)',
                ease: 'expo'
            })

            let cursor = document.querySelector('.cursor')

            document.addEventListener('mousemove', (e) => {
              cursor.style.top = e.clientY + 'px'
              cursor.style.left = e.clientX + 'px'
            })

            let img = document.querySelector('.mainImg')

            img.addEventListener('mouseenter', () => {
              cursor.style.transform = 'scale(1.5)'
            })
            img.addEventListener('mouseleave', () => {
              cursor.style.transform = 'scale(1)'
            })

        })
    }
  }
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@200;300;400;500;600&display=swap');
*, html{
  font-family: 'montserrat', sans-serif;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}
html{
  scroll-behavior: smooth;
  cursor: none;
}
body{
  background: black;
  color: white;
  /*   */
}
::-webkit-scrollbar{
  width: 0;
}
.bg{
  position: fixed;
  top: 0;
  left: 0%;
  z-index: -1;
}
.cursor{
  position: fixed;
  width: 50px;
  height: 50px;
  border-radius: 1000px;
  background: white;
  mix-blend-mode: difference;
  transform: translate(-50%, -50%);
  pointer-events: none;
  transition: all .1s;
  transform-origin: 100% 100%;
}
</style>
