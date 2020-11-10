<template>
    <div class="land">
        <div class="shop_cloth">
            <h1>SHOP</h1>
            <h1>CLOTHING.</h1>
        </div>
        <div class="image">
            <div class="top"></div>
            <img src="../assets/homeimg.svg" alt="" srcset="">
            <div class="bottom"></div>
        </div>
    </div>
</template>

<script setup>

</script>

<style scoped>
.land{
    display: flex;
    align-items: center;
    height: 100vh;
    width: 90%;
    padding-left: 5%; 
}
.shop_cloth{
    display: flex;
    align-items: flex-start;
    justify-content: flex-start;
    flex-direction: column;
    width: 35%;
    font-size: 45px;
    margin-right: 100px;
}
.shop_cloth h1:nth-child(2){
    align-self: flex-end
}
.shop_cloth h1{
    font-weight: 400;
}
.image{
    width: 600px;
    justify-self: flex-start;
    height: 100%;
    position: relative;
}
.image img{
    object-fit: cover;
    width: 100%;
    position: absolute;
    height: 60%;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
.image .top{
    position: absolute;
    top: 0;
    left: 50%;
    transform: translateX(-50%);
    height: 20%;
    width: 350px;
    background: #FFFFFF;
}
.image .bottom{
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    height: 20%;
    width: 350px;
    background: #FFED49;
}
@media (max-width: 1706px){
    
    .shop_cloth h1:nth-child(2){
        align-self: flex-start;
    }
}
@media (max-width: 1526px){
    .land{
        flex-direction: column;
        align-items: center;
        justify-content: space-between;
        height: 80vh;
        padding: 0;
        margin: auto;
        margin-top: 20vh;
    }
    .shop_cloth{
        font-size: 30px;
        justify-content: center;
        align-items: center;
        width: 100%;
        margin-right: 0px;
        margin-bottom: 50px;
    }
    .image{
        width: 80%;
        height: 100%;
    }
    .image .top{
        display: none;
    }
    .image .bottom{
        display: none;
    }
    .image img{
        width: 100%;
        height: 100%;
    }
    .shop_cloth h1:nth-child(2){
        align-self: center;
    }
}
</style>