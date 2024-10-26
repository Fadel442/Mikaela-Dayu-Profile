<template>
    <div class="container">
        <div class="leftM">
            <h1>Mikaela Dayu</h1>
            <h4>MC - COSPLAYER - MODEL</h4>
        </div>
        <div class="rightM">
            <img src="/gambar/dayu.png" alt="">
        </div>
    </div>
</template>

<style scoped>
@media (max-width: 400px) {
    .container {
        display: flex;
        flex-direction: column;
        /* margin: 50px 50px; */
        align-items: center;
        text-align: center;
        justify-content: center;
    }
    .leftM h1{
        font-size: 35px;
        font-weight: bold;
        padding-bottom: 10px;
    }
    .leftM h4 {
        font-size: 15px;
        font-weight: lighter;
    }
    .rightM {
        align-items: center;
        justify-content: center;
        margin: 50px 0;
    }
    .rightM img {
        width: 300px;
        height: 320px;
        background-color: #FFCDEA;
        border-radius: 50px;
    }
}
</style>