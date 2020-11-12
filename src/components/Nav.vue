<template>
<div>
    <div class="nav">
      <div class="link">
        <a href="#top" @click="about = false, contact = false, top = true" class="nav_link" :class="{active: top}">
            <p>Top</p>
            <div class="nav_link_line "></div>
        </a>
      </div>  
        <div class="link">
        <a href="#about" @click="top = false, contact = false, about = true" class="nav_link" :class="{active: about}">
            <p>About</p>
            <div class="nav_link_line "></div>
        </a>
      </div>
        <div class="link">
        <a href="#contact" @click="top = false, about = false, contact =  true" class="nav_link" :class="{active: contact}">
            <p>Contact</p>
            <div class="nav_link_line "></div>
        </a>
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
import { ref, onMounted } from 'vue'
import { gsap } from 'gsap'

export default {
  setup () {
    onMounted(() => {
      gsap.from('.line', 1, {
              width: 0,
      })
    })
    const top =  ref(true)
    const about =  ref(false)
    const contact =  ref(false)

    return{
      top,
      about,
      contact
    }
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
    width: 100%;
    position: relative;
    cursor: pointer;
    text-align: right;
    transition: all .3s;
}
a{
  color: white;
  text-decoration: none;
    transition: all .3s;

}
.link{
    margin-bottom: 35px;
    transition: all .3s;

}
.nav_link_line{
    width: 100%;
    height: 3px;
    margin-right: 10px;
    justify-self: flex-end;
    background: white;
    transition: all .3s;

}
.nav_link p{
    opacity: 0;
    font-size: 15px;
    display: none;
    transition: all .3s;

}
.nav_link.active p{
    opacity: 1;
    display: block

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