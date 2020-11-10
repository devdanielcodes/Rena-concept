<template>
  <div class="main">
    <v-nav />
    <v-land />
    <v-about />
    <v-contact />
  </div>
</template>

<script setup>
import Nav from '@/components/Nav.vue'
import Landing from '@/components/Landing.vue'
import About from '@/components/About.vue'
import Contact from '@/components/Contact.vue'

  export default{
    components: {
      'v-nav': Nav ,
      'v-land': Landing ,
      'v-about': About ,
      'v-contact': Contact 

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
