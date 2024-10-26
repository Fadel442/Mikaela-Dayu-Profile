<template>
    <div class="container">
        <div class="blok1">

        </div>
        <div>
            <h1>
                {{ section }}
            </h1>
        </div>
        <div class="blok2">

        </div>
    </div>
</template>

<script>
export default {
    props: ['section'],
}
</script>

<style scoped>
.container {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 50px;
}

.blok1, .blok2 {
    height: 5px;
    width: 100%;
    margin: 0 50px;
    border-radius: 100px;
    background-color: #FB9AD1;
}

h1 {
    text-align: center;
    font-size: 20px;
    font-weight: bold;
}

@media (max-width: 400px) {
    .container {
        margin-bottom: 15px;
    }

    .blok1, .blok2 {
        height: 3px;
        margin: 0 30px;
    }

    h1 {
        font-size: 15px;
    }
}
</style>