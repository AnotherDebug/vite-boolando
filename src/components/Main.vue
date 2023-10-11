<script>
import CardProduct from './partials/CardProduct.vue';
export default {
    name: "Main",
    components: {
        CardProduct
    }
}
</script>


<template>
    <main>
        <div class="container">

            <CardProduct />
            <CardProduct />
            <CardProduct />
            <CardProduct />
            <CardProduct />
            <CardProduct />

        </div>
    </main>
</template>


<style lang="scss">

main {
    padding-bottom: 50px;
}
</style>