<script>
import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide, Navigation, Pagination } from 'vue3-carousel';


export default {
    components: {
        Carousel,
        Slide,
        Pagination,
        Navigation,
    },
    data() {
        return {
            config: {
                autoplay: 2000,
                // wrapAround: true,
                // loop: true,
                pauseAutoplayOnHover: true,
            },
            images: [
                {
                    gambar: '/gambar/nduk1.jpg',
                },
                {
                    gambar: '/gambar/nduk2.jpg',
                },
                {
                    gambar: '/gambar/nduk3.jpg',
                },
            ],
            isMobile: true,
            currentSlide: 0,
        }
    },
    watch: {
        currentSlide(newIndex) {
            // Periksa jika mencapai akhir dari slide
            if (newIndex === this.images.length) {
                this.currentSlide = 0; // Kembali ke slide pertama
            }
        }
    },
    methods: {
        startAutoplay() {
            setInterval(() => {
                this.currentSlide++;
            }, this.config.autoplay);
        },
    },
    checkScreenSize() {
        this.isMobile = window.innerWidth <= 480;
    },
    mounted() {
        this.startAutoplay();
        this.checkScreenSize();
        window.addEventListener('resize', this.checkScreenSize);
    }, beforeDestroy() {
        window.removeEventListener('resize', this.checkScreenSize);
    },
}
</script>

<template>
    <div class="container">
        <div class="isMobile" v-if="isMobile">
            <Carousel v-bind="config" :modelValue="currentSlide">
                <Slide v-for="(item, image) in images" :key="image">
                    <img :src="item.gambar" alt="">
                </Slide>
                <template #addons>
                    <Navigation />
                    <Pagination />
                </template>
            </Carousel>
        </div>
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
        <div class="rightM" v-if="!isMobile">
            <Carousel v-bind="config" :modelValue="currentSlide">
                <Slide v-for="(item, image) in images" :key="image">
                    <img :src="item.gambar" alt="">
                </Slide>
                <!-- <template #addons>
                    <Navigation />
                    <Pagination />
                </template> -->
            </Carousel>
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

.rightM {
    max-width: 100%;
    overflow: hidden;
    /* Sembunyikan overflow */
}
.isMobile {
    max-width: 100%;
    overflow: hidden;
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
        font-size: 20px;
        font-weight: bold;
    }

    .content p {
        display: none;
    }

    img {
        width: 150px;
        height: 200px;
    }
    .isMobile {
        margin: 20px 0 0 0;
        /* overflow: hidden; */
    }
}
</style>