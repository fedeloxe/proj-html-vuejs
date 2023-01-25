<script>
export default {
    props: {
        footerLink: Object,
    }

}
</script>
<template>
    <div class="link-cont">
        <div class="link-foot" v-for="(item, index ) in footerLink" :key="index">
            <h4>{{ item.title }}</h4>
            <ul>
                <li v-html="item" v-for="(item, index) in item.content" :key="index" style="padding-left:1em">

                </li>
            </ul>
        </div>

    </div>

</template>


<style lang="scss">
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

.link-cont {
    display: flex;
    color: $white;

    .link-foot {
        padding: 0 20px;

        ul {
            list-style-type: "\25AC";
            ;
        }

        li {
            padding: 10px 0;

            a {
                text-decoration: none;
                color: $white;
            }
        }
    }
}
</style>