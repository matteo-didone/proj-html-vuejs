<template>
    <header>
        <nav class="navbar">
            <div class="container-fluid">
                <div class="left-header d-flex align-items-center">
                    <a class="navbar-brand" href="#">
                        <img src="../assets/images/white-logo-2.png" alt="white-logo" width="30" height="24"
                            class="d-inline-block align-text-top" id="logo-navbar">
                    </a>
                </div>

                <div class="right-header d-flex align-items-center">
                    <ul class="navbar-nav">
                        <li class="nav-item">
                            <a class="nav-link active home-link" aria-current="page" href="#">Home</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#">About</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#">Services</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#">Blog</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#">Contact</a>
                        </li>
                        <li class="nav-item">
                            <a class="nav-link" href="#">Portfolio</a>
                        </li>
                    </ul>

                    <div class="ml-auto">
                        <button class="btn btn-outline-light sign-in-button" type="submit">Sign in</button>
                    </div>

                </div>
            </div>
        </nav>
        
        <AppHero />

    </header>
</template>


<script>
import { store } from '../store.js'
import AppHero from './AppHero.vue'

export default {
    name: 'AppHeader',

    components: {
        AppHero
    },

    data() {

        return {
            store,
        };
    },

    methods: {

    }
}
</script>


<style lang="scss" scoped>
@import '../styles/general.scss';
@import 'bootstrap/scss/bootstrap';

.color-coral {
    color: #F9636B;
}

header .navbar {
    background-color: rgba(9, 20, 76, 255);
    height: 120px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    color: white;

    .container-fluid {
        padding-left: 20px;
        padding-top: 10px;
        width: 100%;

        .left-header {
            display: flex;
            align-items: center;
            justify-content: flex-start;
            height: 50%;

            .navbar-brand {
                margin-right: 20px;

                #logo-navbar {
                    height: fit-content;
                    width: fit-content;
                    padding-left: 130px;
                }
            }
        }

        .right-header {
            display: flex;
            align-items: center;
            justify-content: flex-end;
            padding-right: 150px;
            height: 50%;

            ul {
                display: flex;
                align-items: center;
                justify-content: flex-end;
                flex-direction: row;
                color: white;
                height: 100%;

                li {
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    padding: 0 10px;

                    font-weight: bold;

                    &:not(:last-child) {
                        margin-right: 10px;
                    }

                    a {
                        color: white;

                        &.home-link {
                            color: #F9636B;
                        }
                    }
                }
            }

            .sign-in-button {
                margin-left: 20px;
                margin-right: 20px;
                align-items: center;
                appearance: none;
                background-image: linear-gradient(to right, #0799c8, #1b4a8c);
                border: 0;
                width: 110px;
                height: 40px;
                border-radius: 20px;
                box-sizing: border-box;
                color: #fff;
                cursor: pointer;
                display: inline-flex;
                justify-content: center;
                line-height: 1;
                list-style: none;
                overflow: hidden;
                padding-left: 16px;
                padding-right: 16px;
                position: relative;
                text-align: left;
                text-decoration: none;
                transition: box-shadow .15s, transform .15s;
                user-select: none;
                -webkit-user-select: none;
                touch-action: manipulation;
                white-space: nowrap;
                will-change: box-shadow, transform;
                font-size: 18px;
                transition: background-image 0.3s ease;
            }

            .sign-in-button:hover {
                background-image: linear-gradient(to right, #ef5f69, #ba286e);

            }

            .sign-in-button:active {
                box-shadow: #3c4fe0 0 3px 7px inset;
            }
        }

        .ml-auto {
            margin-left: 20px;
        }
    }
}
</style>    