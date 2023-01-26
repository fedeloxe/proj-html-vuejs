<script>
import AppCategories from './AppCategories.vue';

export default {
    components: {
        AppCategories,
    },
    data() {
        return {
            array: {
                categories: [
                    'All Categories',
                    'Cabrio',
                    'Coupe',
                    'Hatchback',
                    'Pick Up',
                    'Sedan',
                    'SUV',
                ],

                brand: [
                    'Brand',
                    'Audi',
                    'BMW',
                    'Ford',
                    'Hyundai',
                    'Opel',
                    'Seat',
                    'Skoda',
                    'Toyota',
                ],

                fuel: [
                    'Fuel Type',
                    'Diesel',
                    'Electric',
                    'Gasoline',
                    'LPG',
                ],

                trasmission: [
                    'Trasmission',
                    'Automaitic',
                    'Manual',
                    'Semiatomatic',
                    'Touch',
                ],

                status: [
                    'Status',
                    '2nd Hand',
                    'By Owner',
                    'From The Gallery',
                    'New',
                ],


            }


        }
    }

}
</script>
<template>
    <div class="cont-search d-flex">
        <input type="text" placeholder="Keywords" class="input">
        <input type="text" placeholder="Location" class="input">
        <!-- <div class="select">
            <select @change="('select')">
                <option v-for="(item, index) in categories" :key="index" :value="item">{{ item }}</option>
            </select>
        </div> -->

        <div class="select"> <!--funzione per le categorie della ricerca-->
            <select @change="('select')" v-for="(item, index ) in array" :key="index">
                <option v-for="(item, index) in item" :key="index" :value="item">{{ item }}
                </option>
            </select>
        </div>
        <button class="btn">Search</button>
    </div>

    <AppCategories />


</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as*;
@use '../styles/partials/mixins' as*;

.cont-search {
    display: flex;
    width: 75%;
    margin: 10px auto;
    align-items: center;
    justify-content: center;
}

.btn {

    background-color: $black;
    color: $white;
    padding: 20px 50px;
}

.input {
    padding: 20px 0px;
    border: 2px solid $grey;
    border-radius: 5px;
    text-align: center;
    max-width: 150px;
    margin-right: 20px;
}

select {
    border: 2px solid $grey;
    border-radius: 5px;
    padding: 20px 10px;
    margin-right: 20px;
    text-align: center;
    width: 150px;

}
</style>