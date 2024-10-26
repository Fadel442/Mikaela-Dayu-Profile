<template>
    <div class="container">
        <div class="leftM">
        
            <img src="" alt="">
        </div>
        <div class="rightM">
            <div class="content">
                <h1>About Me</h1>
                <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce condimentum nibh sed eros condimentum
                    convallis. Aenean interdum tristique quam, eu varius sapien placerat nec. Fusce ac tortor semper
                    erat condimentum tempus eu ut tellus. Cras viverra, magna in feugiat venenatis, quam justo convallis
                    sem, non rutrum augue eros ac ante. Phasellus tempor massa non urna facilisis congue. Morbi euismod
                    sapien diam, quis feugiat nunc condimentum nec. Curabitur volutpat vulputate consectetur.
                    Pellentesque iaculis.</p>
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
        font-size: 15px;
    }
}
</style>