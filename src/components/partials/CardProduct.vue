<script>
export default {
    name: "CardProduct",
    props: {
        products: Object
    },
    computed: {
        description() {
            return this.products.modello.toUpperCase();
        },
        priceDiscount() {
            return `${this.products.lastPrice.toFixed(2, '0')} €`;
        },
        priceFull() {
            return `${this.products.fullPrice.toFixed(2, '0')} €`;
        }
    }

}
</script>


<template>
    <!-- Singola card -->
    <section class="card">
        <div class="img">
            <img class="first" :src="`/src/assets/img/${products.primaryImage}`" alt="">
            <img class="second" :src="`/src/assets/img/${products.secondaryImage}`" alt="">
        </div>
        <div class="heart">
            <p>&hearts;</p>
        </div>
        <p v-if="products.discount !== null" class="discount">{{ products.discount }}</p>
        <p v-if="products.sostenibilita === true" class="sustain" :class=" products.discount === null && products.sostenibilita === true ? 'sus-only' : '' ">Sostenibilità</p>
        <p class="trademark">{{ products.marca }}</p>
        <p class="description text-strong">{{ description }}</p>
        <span class="price-discount text-red">{{ priceDiscount }}</span>
        <span v-if="this.products.fullPrice !== null" class="price">{{ priceFull }}</span>
    </section>
</template>


<style lang="scss" scoped>
@use "../../scss/partials/variables" as *;

.card {
    width: 33%;
    min-width: 200px;
    display: inline-block;
    margin-top: 50px;
    position: relative;
    font-size: 12px;
    padding: 5px;

    img {
        width: 100%;
        cursor: pointer;
    }

    .img {
        .first {
            display: block;
        }

        .second {
            display: none;
        }

        &:hover .first {
            display: none;
        }

        &:hover .second {
            display: block;
        }
    }

    .heart {
        width: 40px;
        height: 40px;
        background-color: $white-color;
        color: black;
        text-align: center;
        line-height: 40px;
        font-size: 25px;
        position: absolute;
        top: 2%;
        right: 0;
        cursor: pointer;

        &:hover {
            color: $red-color;
        }
    }

    .discount {
        background-color: $red-color;
        display: inline-block;
        padding: 5px 10px;
        position: absolute;
        left: 5px;
        bottom: 15%;
        font-weight: 600;
        color: $white-color;
    }

    .trademark,
    .price,
    .price-discount {
        font-size: 10px;
        padding-top: 5px;
    }

    .sustain {
        display: inline-block;
        padding: 5px 10px;
        background-color: $green-color;
        position: absolute;
        left: 14%;
        bottom: 15%;
        font-weight: 600;
        color: $white-color;
    }

    .sus-only {
        position: absolute;
        left: 5px;
    }

    .price {
        text-decoration: line-through;
        margin-left: 10px;
    }
}
</style>