<script>
export default {
    name: 'Header'
}
</script>


<template>
    <header>
        <div class="top-fixed">
            <div class="topbar d-flex container">
                <div class="menu d-flex">
                    <ul>
                        <li><a href="#">Donna</a></li>
                        <li><a href="#">Uomo</a></li>
                        <li><a href="#">Bambino</a></li>
                    </ul>
                </div>
                <div class="logo d-flex"></div>
                <div class="menu-account d-flex">
                    <p><i class="fa-regular fa-user"></i></p>
                    <p><i class="fa-regular fa-heart"></i></p>
                    <p><i class="fa-solid fa-bag-shopping"></i></p>
                </div>
            </div>
        </div>
    </header>
</template>


<style lang="scss" scoped>

@use "../scss/partials/variables" as *;

header {
    margin-bottom: 60px;

    .top-fixed {
        position: fixed;
        width: 100%;
        top: 0;
        left: 0;
        background-color: $top-color;
        box-shadow: 0 4px 2px 0px $gray-color;
        z-index: 2;
    }

    .topbar {
        width: 100%;
        height: 60px;

        .menu {
            width: 20%;
            align-items: center;
            justify-content: flex-start;

            ul {
                list-style: none;

                li {
                    display: inline-block;

                    a {
                        text-decoration: none;
                        align-items: center;
                        padding-right: 5px;
                        color: $white-color;
                    }
                }
            }
        }

        .logo {
            align-items: center;
            width: 60%;
            background-image: url('/src/assets/img/boolean-logo.png');
            background-size: contain;
            background-size: 20%;
            background-repeat: no-repeat;
            background-position: center;
        }

        .menu-account {
            align-items: center;
            justify-content: flex-end;
            width: 20%;

            p {
                padding-left: 10px;

                i {
                    cursor: pointer;
                }
            }
        }
    }


}</style>