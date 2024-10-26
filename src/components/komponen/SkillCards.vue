<template>
    <div class="container">
        <div class="card" v-for="(item, card) in cards" :key="card">
            <img :src="item.image" alt="" class="card-image">
            <h2>{{ item.title }}</h2>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            cards: [
                {
                    image: '/logos/ic_mc.png',
                    title: 'Public Speaking',
                },
                {
                    image: '/logos/ic_model.png',
                    title: 'Modelling',
                },
                {
                    image: '/logos/ic_dance.png',
                    title: 'Dancing',
                },
                {
                    image: '/logos/ic_arts.png',
                    title: 'Martial Arts',
                },
                {
                    image: '/logos/id_act.png',
                    title: 'Acting',
                },
            ]
        }
    },
}
</script>

<style scoped>
.container {
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    flex-wrap: wrap;
}

.card {
    width: 250px;
    height: 200px;
    /* Adjust height as needed */
    background: white;
    margin: 0 30px 30px;
    /* Add margin to bottom for spacing */
    padding: 20px;
    border-radius: 10px;
    border-style: solid;
    border-color: #FB9AD1;
    box-shadow: 0 0 10px rgba(248, 79, 231, 0.5);
    overflow: hidden;
    transition: box-shadow 0.3s ease-in-out;
    position: relative;
    /* Added for pseudo-element */
}

.card-image {
    width: 100px;
    height: auto;
    border-radius: 10px;
    margin: 10px 0 0 0;
    /* Space between image and text */
}
h2 {
    color: #FB9AD1;
    text-align: center;
    margin: 0 10px;
}

@media (max-width: 400px) {
    .container {
        align-items: center;
    }

    .card {
        width: 85px;
        height: 70px;
        margin: 10px 20px;
        padding: 0;
    }

    .card-image {
        width: 25px;
        height: 25px;
        margin: 10px 0 0 0;
    }

    h2 {
        font-weight: bold;
        font-size: 8px;
        text-align: center;
        margin-right: 10px;
        /* display: none; */
    }
}

/* 480 */
@media (max-width: 480px) {
    .container {
        align-items: center;
    }

    .card {
        width: 85px;
        height: 80px;
        margin: 10px 20px;
        padding: 0;
    }

    .card-image {
        width: 25px;
        height: 25px;
        margin: 15px 0 0 0;
    }

    h2 {
        font-weight: bold;
        font-size: 8px;
        text-align: center;
        margin-right: 10px;
        /* display: none; */
    }
}
</style>