<template>
    <div class="hero-wrapper">
        <div class="left-container">
            <div class="title-container">
                <h1>Business Planning</h1>
                <h1>Digital Technology</h1>
                <h1>Modern Solutions!</h1>
            </div>

            <div class="subtitle-container">
                <p>
                    When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface .
                </p>
            </div>

            <div class="ml-auto button-container">
                <button class="btn try-it-now-button" type="submit">Try It Now</button>
                <button class="btn explore-more-button" type="submit">Explore More</button>
            </div>
        </div>

        <div class="right-container">
            <img src="../assets/images/header.png" alt="hero-image">
        </div>
    </div>
</template>


<script>
import { store } from '../store.js'

export default {
    name: 'AppHero',

    components: {

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

.hero-wrapper {
    background-color: rgba(8, 19, 74, 255);
    display: flex;
    justify-content: space-around;
    align-items: center;
    color: white;
    padding-bottom: 170px;

    .left-container {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        justify-content: center;

        .title-container {
            font-weight: bolder;
            margin-bottom: 50px;

            h1 {
                font-size: 60px;
                font-weight: bolder;
            }

            h1:first-child,
            h1:last-child {
                font-weight: bold;
            }
        }

        .subtitle-container {
            margin-bottom: 20px;

            p {
                color: #047fac;
                text-align: left;
                width: 460px;
                height: 50px;
                font-size: 16px;
                font-weight: bold;
            }
        }

        .button-container {
            display: flex;
            margin-top: 20px;

            button {
                margin-right: 10px;
                height: 40px;
                border-radius: 40px;
                padding: 0 20px;
            }
        }
    }

    .right-container {
        img {
            width: 100%;
            height: auto;
        }
    }
}

.try-it-now-button {
    width: 175px;
    height: 50px !important;
    background-image: linear-gradient(to left, #ef5f69, #ba286e);
    border: none;
    color: white;

    &:hover {
        background-image: linear-gradient(to right, #0799c8, #1b4a8c);
    }
}

.explore-more-button {
    width: 175px;
    height: 50px !important;
    background-image: linear-gradient(to left, #0799c8, #1b4a8c);
    border: none;
    color: white;

    &:hover {
        background-image: linear-gradient(to right, #ef5f69, #ba286e);
    }
}
</style>    