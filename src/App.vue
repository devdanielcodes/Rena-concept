<template>
  <div class="main">
    <v-logo />
    <v-land />
    <v-about />
    <v-contact />
    <v-soc />
  </div>
</template>

<script setup>
import Logo from '@/components/Logo.vue'
import Landing from '@/components/Landing.vue'
import About from '@/components/About.vue'
import Contact from '@/components/Contact.vue'
import Socials from '@/components/socials.vue'


  export default{
    components: {
      'v-logo': Logo ,
      'v-land': Landing ,
      'v-about': About ,
      'v-contact': Contact,
      'v-soc': Socials,

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
body{
  background: black;
  color: white;
}

</style>
