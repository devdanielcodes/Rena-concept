<template>
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
</template>

<script setup>

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
    margin-bottom: 15px;
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
@media (max-width: 478px){
    .nav{
        width: 30px
    }
    .nav_link p{
        font-size: 10px
    }
}
</style>