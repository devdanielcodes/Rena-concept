<template>
    <div class="contact">
        <div class="con">
            <h1>Contact.</h1>
            <form>
                <label for="">Name</label>
                <input type="text">
                <label for="">Email</label>
                <input type="mail">
                <label for="">Msg</label>
                <input type="text">
                <button>Send</button>
            </form>
        </div>
        <img src="../assets/cont.png" alt="" class="cont">
    </div>
</template>

<script>

</script>

<style scoped>
.contact{
    height: 100vh;
    width: 90%;
    margin: auto;
    position: relative
}
.contact h1{
    font-size: 100px;
    font-weight: 400;
}
.con{
    position: absolute;
    top: 50%;
    left: 0;
    transform: translateY(-60%);
    width: 100%;
}
form{
    width: 400px;
}
form input{
    width: 100%;
    margin-bottom: 5vh;
    border: none;
    height: 30px;
    border-bottom: 2px solid white;
    background: none;
    color: white;
    outline: none;
}
button{
    border: none;
    padding: 20px;
    font-size: 20px;
    border-bottom: 2px solid white;
    background: none;
    color: white;
    outline: none;
}
.cont{
    position: absolute;
    top: 50%;
    right: 10%;
    width: 500px;
    transform: translateY(-50%);
}
@media (max-width: 1400px){
    .cont{
        width: 300px
    }  
}
@media (max-width: 960px){
    .cont{
        display: none
    }
}
@media (max-width: 490px){  
    .contact h1{
        font-size: 60px;
    }
    form{
        width: 80%;
    }
}
</style>