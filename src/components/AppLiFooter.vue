<script>
export default {
    props: {
        link: Object,
    }

}
</script>
<template>
    <div class="link-foot">
        <ul>
            <li v-for="(item, index) in link" :key="index">
                <a href="">{{ item }}</a>
            </li>
        </ul>
    </div>

</template>


<style>

</style>