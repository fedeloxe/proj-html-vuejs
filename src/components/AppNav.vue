<script>

export default {
    props: {
        nav: Object
    }

}
</script>
<template>
    <div class="nav-bar">
        <ul>
            <li v-for="(item, index) in nav" :key="index">
                <a href="">{{ item }}</a>
            </li>
        </ul>

    </div>

</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as*;

ul {
    list-style-type: none;
    display: flex;

    li {
        padding: 10px;
        margin-top: 10px;
    }
}

a {
    color: $black;
    text-decoration: none;
    font-size: large;
    font-size: 17px;
    font-weight: 700;
}
</style>