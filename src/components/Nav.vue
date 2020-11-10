<template>
<div>
    <div class="nav">
        <div class="nav_link active">
            <p>Top</p>
            <div class="nav_link_line "></div>
        </div>
        <div class="nav_link">
            <p>About</p>
            <div class="nav_link_line"></div>
        </div>
        <div class="nav_link">
            <p>Contact</p>
            <div class="nav_link_line"></div>
        </div>
    </div>
    <div class="socials">
      <div class="line"></div>
      <img src="../assets//instagram.svg" alt="">
      <img src="../assets//twitter.svg" alt="">
      <img src="../assets//linkedin.svg" alt="">
    </div>
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
.nav{
    position: fixed;
    top: 50%;
    right: 0;
    transform: translateY(-50%);
    width: 60px
}
.nav_link{
    margin-bottom: 35px;
    width: 100%;
    position: relative;
    cursor: pointer;
    text-align: right
}
.nav_link_line{
    width: 100%;
    height: 3px;
    margin-right: 10px;
    justify-self: flex-end;
    background: white;
}
.nav_link p{
    opacity: 0;
    font-size: 15px;
    display: none;
}
.nav_link.active p{
    opacity: 1;
    display: block;
   

}
.nav_link.active .nav_link_line{
    width: 0%;
}

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
@media (max-width: 478px){
    .nav{
        width: 30px
    }
    .nav_link p{
        font-size: 10px
    }
}
</style>