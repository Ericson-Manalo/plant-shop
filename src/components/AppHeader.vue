<template lang="">
    <header>

            <!--UPPER HEADER-->
        <div class="upper-header">
            <!-- <img class="header-logo" src="https://logos-world.net/wp-content/uploads/2020/12/Nespresso-Logo-700x394.png" alt="Logo Of Nespresso"> -->
            LOGO
            <div class="upper-items">
                <div>
                    <a href="">
                        <i class="fa-solid fa-magnifying-glass pe-2"></i>
                        <span class="d-none d-md-inline d-lg-inline">CERCA</span>
                    </a>
                </div>
                <div>
                    <a href="">
                        <i class="fa-solid fa-cart-shopping pe-2"></i>
                        <span class="d-none d-md-inline d-lg-inline">CARRELLO</span>
                    </a>
                    
                </div>
                <div>
                    <a href="">
                        <i class="fa-regular fa-circle-user pe-2"></i>
                        <span class="d-none d-md-inline d-lg-inline">ACCEDI</span>
                    </a>
                </div>

            </div>
        </div>

        <!--LOWER HEADER-->
        <nav class="lower-header navbar navbar-expand-lg navbar-light ">
            <div class="container-fluid">
                <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarTogglerDemo01" aria-controls="navbarTogglerDemo01" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarTogglerDemo02">
                    <ul class="navbar-nav mr-auto mt-2 mt-lg-0">
                        <li class="nav-item" v-for="link in links">
                            <a class="nav-item">
                            <router-link :to="{name: link.route}">
                                {{link.name}}
                            </router-link>
                        </a>
                        </li>
                    </ul>
                </div>
            </div>

        </nav>

    </header>
</template>

<script>
export default {
    data() {
        return {
            links: [
                {
                    route: 'offerte',
                    name: 'Offerte'
                },
                {
                    route: 'piante_esterno',
                    name: 'Piante da esterno'
                },
                {
                    route: 'piante_interno',
                    name: 'Piante da interno'
                },
                {
                    route: 'vasi',
                    name: 'Vasi e arredo'
                },
                {
                    route: 'promozioni',
                    name: 'Promozioni'
                },
                {
                    route: 'assistenza',
                    name: 'Assistenza'
                },
                {
                    route: 'dove',
                    name: 'Dove siamo'
                },

            ]
        }
    },
}
</script>

<style scoped lang="scss">
@use '../styles/general.scss' as*;


    header{
        height: 160px;
        background-color: white;
        // color: black;

        .upper-header{
            display: flex;
            justify-content: space-between;
            max-width: 996px;
            // background-color: red;
            margin: 0 auto;

            img.header-logo{
                height: 80px
            }

            div.upper-items{
                display: flex;
                height: 80px;
                align-items: center;

                div{
                    margin-right: 2rem;

                    a{
                        color: #2f2f2f;
                    }
                }

            }
        }

        .lower-header{
            height: 80px;
            background-color: #2f2f2f;
            // width: 996px;
            color: white;
            margin: 0 auto;
            text-align: center;

            ul{
                display: flex;
                align-items: center;
                height: 100%;
                justify-content: space-evenly;
                padding-right: 2rem;
                width: 100%;
                color: white !important; 


                li{
                    list-style-type: none;

                    a{
                        color: white;

                        &:hover{
                            border-bottom: 2px solid #22684f;
                        }
                    }
                }
            }
        }

    }
</style>