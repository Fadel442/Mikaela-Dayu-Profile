<template>
    <div class="container">
        <div class="leftM">

            <img src="" alt="">
        </div>
        <div class="rightM">
            <div class="content">
                <h1>About Me</h1>
                <p>
                    I’m Mikaela Dayu, I have passion and dedicated to my work as a model, MC, and cosplayer
                    performer. Modeling is my primary focus, where I collaborate with talented photographers and
                    designers to create captivating visuals that explore a range of aesthetics and emotions. It’s an art
                    form that challenges me creatively, and I love the versatility it brings to my career. Alongside
                    modeling, I work as an MC, bringing energy, professionalism, and a welcoming atmosphere to every
                    event I host, from formal gatherings to interactive product launches. Engaging with diverse
                    audiences and making each event memorable is something I genuinely enjoy. Additionally, I am an
                    experienced cosplayer, where I immerse myself in bringing beloved characters to life with detailed
                    costumes and performances. Balancing these roles has allowed me to grow as a versatile performer,
                    blending creativity with a deep commitment to making each project special and impactful.</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
.container {
    display: flex;
    margin: 50px 0;
}

.rightM {
    width: 100%;
}

/* 400 */
@media (max-width: 400px) {
    .container {
        margin: 0 20px;
    }

    .rightM {
        padding: 0;
        /* text-align: center; */
    }

    .content {
        text-align: center;
        margin: 25px 20px;
    }

    .content h1 {
        font-size: 20px;
        font-weight: bold;
    }

    .content p {
        margin: 20px 0;
        font-size: 10px;
    }
}

/* 480 */
@media (max-width: 480px) {
    .container {
        margin: 0 20px;
    }

    .rightM {
        padding: 0;
        /* text-align: center; */
    }

    .content {
        text-align: center;
        margin: 25px 20px;
    }

    .content h1 {
        font-size: 25px;
        font-weight: bold;
    }

    .content p {
        margin: 20px 0;
        font-size: 10px;
    }
}
</style>