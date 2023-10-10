<script>
export default {
    name: "Footer",
    data() {
        return {
            footerMenu: [
                {
                    href: "#",
                    text: "Informazioni legali"
                },

                {
                    href: "#",
                    text: "Informativa sulla privacy"
                },

                {
                    href: "#",
                    text: "Diritto di recesso"
                },
            ],

            icons: [
                {
                    icon: 'fa-brands fa-square-twitter',
                    title: 'twitter'
                },
                {
                    icon: 'fa-brands fa-square-facebook',
                    title: 'facebook'
                },
                {
                    icon: 'fa-brands fa-square-instagram',
                    title: 'instagram'
                },
                {
                    icon: 'fa-brands fa-square-pinterest',
                    title: 'pinterest'
                },
                {
                    icon: 'fa-brands fa-youtube',
                    title: 'youtube'
                },
            ]
        }
    }
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
                        <li v-for="(item, index) in footerMenu" :key="index"><a :href="item.href">{{ item.text }}</a></li>
                    </ul>
                </div>
                <div class="social">
                    <p>Trovaci anche su</p>
                    <ul>
                        <li v-for="(icon, index) in icons" :key="index"><i :class="[icon.icon]"></i></li>
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
}
</style>