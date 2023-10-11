<script>
import CardProduct from './partials/CardProduct.vue';
import products from '../data/products';
export default {
    name: "Main",
    components: {
        CardProduct
    },
    data() {
        return {
            products
        }
    }
}
</script>


<template>
    <main>
        <div class="container">

            <CardProduct v-for="product in products" :key="product.id" :products="product" />

        </div>
    </main>
</template>


<style lang="scss">

main {
    padding-bottom: 50px;
}
</style>