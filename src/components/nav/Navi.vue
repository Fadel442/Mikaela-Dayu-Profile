<template>
    <nav>
        <div class="container">
            <div>
                <img src="/logos/ic_md.png" alt="" class="ic_md">
            </div>
            <div class="cont1" v-if="!isMobile">
                <RouterLink to="/">
                    <img src="" alt="">
                </RouterLink>
                <RouterLink to="/">
                    <img src="" alt="">
                </RouterLink>
                <RouterLink to="/">
                    <img src="" alt="">
                </RouterLink>
            </div>
            <button class="menu-icon" v-if="isMobile" @click="toggleMenu">
                <img src="/logos/ic_menu.png" alt="">
            </button>
        </div>
        <div class="dropdown-menu" v-if="isMobile && isMenu">
            <RouterLink :to="{ name: 'homeP'}" class="color-menu">Home</RouterLink>
            <div class="dropdown-portofolio" @click="togglePortfolio">
                Portofolio
                <div class="portfolio-menu" v-if="isPortfolioMenu">
                    <RouterLink to="/" class="color-menu">MC</RouterLink>
                    <RouterLink to="/" class="color-menu">Model</RouterLink>
                    <RouterLink to="/" class="color-menu">Others</RouterLink>
                </div>
            </div>
            <RouterLink to="/" class="color-menu">Contact Me!</RouterLink>
        </div>
    </nav>
    <RouterView />
</template>

<script>
export default {
    data() {
        return {
            isMenu: false,
            isMobile: false,
            isPortfolioMenu: false,
        }
    },
    methods: {
        toggleMenu() {
            this.isMenu = !this.isMenu;
            if (!this.menu) {
                this.isPortfolioMenu = false;
            }
        },
        togglePortfolio() {
            this.isPortfolioMenu = !this.isPortfolioMenu;
        },
        checkScreenSize() {
            this.isMobile = window.innerWidth <= 480;
        },
    },
    mounted() {
        this.checkScreenSize();
        window.addEventListener('resize', this.checkScreenSize);
    },
    beforeDestroy() {
        window.removeEventListener('resize', this.checkScreenSize);
    },

}
</script>

<style scoped>
.container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

@media (max-width: 480px) {
    .container {
        /* display: flex; */
        padding: 20px 30px 0 30px;
        justify-content: space-between;
        align-items: center;
    }
    nav {
        height: 80px;
        width: 100%;
    }

    .cont1 {
        display: none;
    }

    .ic_md {
        width: 50px;
        height: 50px;
    }

    .menu-icon {
        width: 30;
        height: 30;
        cursor: pointer;
        border: none;
        background: none;
    }

    img {
        width: 30px;
        height: 30px;
    }

    .dropdown-menu {
        position: absolute;
        top: auto;
        width: 100%;
        height: auto;
        /* adjust based on your layout */
        background-color: #FB9AD1;
        color: white;
        padding: 10px;
        border-radius: 5px;
        display: flex;
        flex-direction: column;
        text-align: center;
        gap: 10px;
    }
    .dropdown-menu .color-menu {
        color: white;
    }

    .dropdown-portfolio {
        cursor: pointer;
    }

    .portfolio-menu {
        display: flex;
        flex-direction: column;
        gap: 5px;
        padding-top: 10px;
    }
}
</style>