<template>
    <div class='logo'>
        <h1 class="fin">Rena.</h1>
    </div>
</template>
<script>
import { onMounted } from 'vue'
import { gsap } from 'gsap'
export default {
    setup () {
        onMounted(() => {
            gsap.from('.fin ', 2, {
                ease: 'expo',
                transform: 'translateY(200%)'
            })
        })
    }
}
</script>


<style scoped>
.logo{
    position: fixed;
    top: 20px;
    left: 40px;
    overflow: hidden;
    z-index: 10;
}
</style>