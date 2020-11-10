<template>
<div class="socials">
      <div class="line"></div>
      <img src="../assets//instagram.svg" alt="">
      <img src="../assets//twitter.svg" alt="">
      <img src="../assets//linkedin.svg" alt="">
    </div>
</template>

<script>
import { onMounted } from 'vue'
import { gsap } from 'gsap'

export default {
  setup () {
    onMounted(() => {
      gsap.from('.line', 1, {
              width: 0,
      })
    })
  }
}

</script>

<style scoped>
.socials{
  display: flex;
  align-items: center;
  position: fixed;
  bottom: 40px;
  left: 0;
  width: 150px;
  justify-content: space-between
}
.socials .line{
  width: 60px;
  height: 3px;
  margin-right: 10px;
  background: white;
}
.socials img{
  margin-right: 10px;;
  cursor: pointer;
}
</style>