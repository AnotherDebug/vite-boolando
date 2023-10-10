<script>
export default {
    name: "Footer"
}
</script>


<template>
    <footer>

        <!-- Info footer -->
        <div class="row d-flex">
            <div class="info d-flex">
                <div class="property">
                    <p class="text-strong">Boolando s.r.l.</p>
                    <ul>
                        <li><a href="#">Informazioni legali</a></li>
                        <li><a href="#">Informativa sulla privacy</a></li>
                        <li><a href="#">Diritto di recesso</a></li>
                    </ul>
                </div>
                <div class="social">
                    <p>Trovaci anche su</p>
                    <ul>
                        <li><i class="fa-brands fa-square-twitter"></i></li>
                        <li><i class="fa-brands fa-square-facebook"></i></li>
                        <li><i class="fa-brands fa-square-instagram"></i></li>
                        <li><i class="fa-brands fa-square-pinterest"></i></li>
                        <li><i class="fa-brands fa-youtube"></i></li>
                    </ul>
                </div>
            </div>
        </div>
        <!-- /Info footer -->

    </footer>
</template>


<style lang="scss" scoped>

@use "../scss/partials/variables" as *;

footer {
    color: $white-color;
    background-color: $black-color;

    .row {
        width: 100%;
        height: 80px;
        /* background-color: #000; */
        justify-content: center;
        align-items: flex-end;

        .info {
            width: 1200px;
            height: 80px;
            align-items: center;
            justify-content: space-between;

            .property {
                height: 40px;
                justify-content: center;
                align-items: center;

                ul {
                    list-style: none;

                    li {
                        display: inline-block;

                        a {
                            text-decoration: none;
                            color: $white-color;
                            padding-right: 10px;
                            font-size: 10px;
                        }
                    }
                }
            }

            .social {
                height: 40px;
                justify-content: center;
                align-items: center;

                p {
                    font-size: 10px;
                    text-align: center;
                }

                ul {
                    list-style: none;

                    li {
                        display: inline-block;
                        padding-top: 5px;
                        padding-left: 5px;

                        i {
                            cursor: pointer;
                        }
                    }
                }
            }
        }
    }
}</style>