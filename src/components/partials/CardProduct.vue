<script>
export default {
    name: "CardProduct"
}
</script>


<template>

    <!-- Singola card -->
    <section class="card">
            <div class="img">
                <img class="first" src="/src/assets/img/1.webp" alt="">
                <img class="second" src="/src/assets/img/1b.webp" alt="">
            </div>
            <div class="heart">
                <p>&hearts;</p>
            </div>
            <p class="discount">-50%</p>
            <p class="sustain">Sostenibilità</p>
            <p class="trademark">Levi's</p>
            <p class="description text-strong">RELAXED FIT TEE UNISEX</p>
            <span class="price-discount text-red">14,99 <span>&euro;</span></span>
            <span class="price">29,99 <span>&euro;</span></span>
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

        #sus-only {
            position: absolute;
            left: 5px;
        }

        .price {
            text-decoration: line-through;
        }
    }

</style>