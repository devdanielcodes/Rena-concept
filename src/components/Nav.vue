<template>
    <div class="nav">
        <div class="nav_link active">
            <p>Top</p>
            <div class="nav_link_line"></div>
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
    right: -1%;
    transform: translateY(-50%);
}
.nav_link{
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 10px;
    cursor: pointer;
}
.nav_link_line{
    width: 50px;
    height: 3px;
    margin-right: 10px;
    background: white;
}
.nav_link p{
    opacity: 0;
}
.nav_link.active p{
    opacity: 1;
}
.nav_link.active .nav_link_line{
    width: 25px;
}
</style>