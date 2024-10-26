<template>
    <div class="container">
        <div class="leftM">
            <div class="content">
                <h1>Juara 3</h1>
                <h1>Cung-Nduk Pasar Turi 2024</h1>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce condimentum nibh sed eros condimentum
                    convallis. Aenean interdum tristique quam, eu varius sapien placerat nec. Fusce ac tortor semper
                    erat condimentum tempus eu ut tellus. Cras viverra, magna in feugiat venenatis, quam justo convallis
                    sem, non rutrum augue eros ac ante. Phasellus tempor massa non urna facilisis congue. Morbi euismod
                    sapien diam, quis feugiat nunc condimentum nec. Curabitur volutpat vulputate consectetur.
                    Pellentesque iaculis.</p>
                <router-link to="">
                    <button class="porto-btn">My Portofolio</button>
                </router-link>
            </div>
        </div>
        <div class="rightM">
            <img src="" alt="">
        </div>
    </div>
</template>

<style scoped>
.container {
    display: flex;
    justify-content: center;
    text-align: center;
    align-items: center;
    margin: 0 50px;
}
.porto-btn {
    width: 150px;
    height: 30px;
    margin: 30px 0;
    border-radius: 100px;
    background-color: #FB9AD1;
    color: white;
    border-style: none;
}

@media (max-width: 400px) {
    .container {
        flex-direction: column;
        margin: 0 20px;
    }

    .leftM {
        padding: 0;
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
        font-size: 10px;
        margin: 20px 0;
    }
}

/* 480 */
@media (max-width: 480px) {
    .container {
        flex-direction: column;
        margin: 0 20px;
    }

    .leftM {
        padding: 0;
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
        font-size: 15px;
        margin: 20px 0;
    }
    .porto-btn {
        width: 200px;
    }
}
</style>