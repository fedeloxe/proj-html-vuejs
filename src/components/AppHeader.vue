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
        <div class="container">
            <div class="logo">
                <img src="../assets/logo-autocar11.png" alt="logo">
            </div>
            <AppNav :nav="nav" />
            <div class="header-buttons">
            </div>

        </div>

    </header>

</template>


<style lang="scss" scoped>
header {
    width: 100%;
}

.container {
    display: flex;
    width: 80%;
    margin: 0 auto;
}
</style>