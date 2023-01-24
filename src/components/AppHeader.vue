<script>

import AppNav from './AppNav.vue';
export default {
    components: {
        AppNav,
    },
    data() {
        return {
            nav: [
                'Home',
                'About Us',
                'vehicles',
                'Dealers',
                'Packages',
                'Blog',
                'Contact',
            ]
        }
    }
}
</script>
<template>
    <header>
        <div class="cont">
            <div class="logo">
                <img src="../assets/logo-autocar11.png" alt="logo">
            </div>
            <AppNav :nav="nav" />
            <div class="header-buttons">
                <a href="#" class="button-h">
                    <img src="../assets/padlock.png" alt="#">
                    My Account
                </a>
                <a href="#" class="button-h">
                    <img src="../assets/add.png" alt="#">
                    Add Car
                </a>
                <button class="btn " type="button" data-bs-toggle="offcanvas" data-bs-target="#offcanvasExample"
                    aria-controls="offcanvasExample">
                    <i class="fa-solid fa-bars"></i>
                </button>

                <div class="offcanvas offcanvas-start" tabindex="-1" id="offcanvasExample"
                    aria-labelledby="offcanvasExampleLabel">
                    <div class="offcanvas-header">

                        <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close"></button>
                    </div>
                    <div class="offcanvas-body">
                        <!--contenuto -->
                    </div>
                </div>

                <a href="#" class="button-h">
                    <img src="../assets/headphones.png" alt="#">
                    +1(234)567 89 10
                </a>
            </div>
        </div>
    </header>

</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

header {
    width: 100%;
    // position: fixed;
}

.cont {
    display: flex;
    width: 75%;
    margin: 10px auto;
    align-items: center;
    justify-content: space-around;
}

.header-buttons {
    display: flex
}

.button-h {
    @include header-btn;
    margin-right: 5px;
    text-decoration: none;

    img {
        width: 50px;
        filter: invert(1);
        padding: 5px;
    }
}

.logo {
    img {
        width: 200px;
    }
}

.btn {
    font-size: 25px;
}
</style>