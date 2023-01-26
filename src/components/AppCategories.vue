<script>
export default {
    data() {
        return {
            categoryCar: [
                {
                    img: '/cabrio.jpg',
                    label: 'Cabrio',
                    listing: '3',
                },
                {
                    img: '/coupe.jpg',
                    label: 'Coupe',
                    listing: '0',
                },
                {
                    img: '/hatchback.jpg',
                    label: 'Hatcback',
                    listing: '2',
                },
                {
                    img: '/pickup.jpg',
                    label: 'Pick Up',
                    listing: '0',
                },
                {
                    img: '/sedan.jpg',
                    label: 'Sedan',
                    listing: '3',
                },
                {
                    img: '/suv.jpg',
                    label: 'SUV',
                    listing: '4',
                }
            ]
        }
    },

}
</script>
<template>

    <a href="" class="car-cont">
        <div v-for="(item, index) in categoryCar" :key="index" class="car">
            <img :src="item.img" alt="">
            <h5>{{ item.label }}</h5>
            <p>{{ item.listing }} Listings</p>

        </div>

    </a>




</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

.car-cont {
    display: flex;
    justify-content: center;
    text-decoration: none;
    color: $black;

    .car {
        display: flex;
        flex-direction: column;
        text-align: center;
        padding: 20px;
        box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
        width: 240px;
    }
}
</style>