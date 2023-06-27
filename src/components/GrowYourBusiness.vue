<template>
    <div class="grow-your-business-wrapper">

        <div class="left-container">
            <img src="../assets/images/men-data.png" alt="men-data-image">
        </div>

        <div class="right-container">
            <div class="title-container">
                <p>Start Your Project</p>
                <h1>Grow Your Business</h1>
                <h2>With Our Strategy</h2>
            </div>

            <div class="subtitle-container">
                <p>
                    When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface
                    .of the impenetrable foliage of my trees, and but a few stray gleams steal into the inner sanctuary,
                </p>
            </div>

            <div class="ml-auto button-container">
                <button class="btn try-it-now-button" type="submit">Try It Now</button>
                <button class="btn explore-more-button" type="submit">Explore More</button>
            </div>
        </div>
    </div>
</template>


<script>
import { store } from '../store.js'

export default {
    name: 'GrowYourBusiness',

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

.grow-your-business-wrapper {
    background-color: rgba(8, 19, 74, 255);
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    color: white;
    padding-bottom: 170px;

    .left-container {
        display: flex;
        justify-content: center;
        align-items: center;
        margin-top: 150px;

        img {
            width: 80%;
            height: auto;
        }
    }

    .right-container {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        justify-content: center;

        margin-top: 40px;

        .title-container {
            font-weight: bolder;
            margin-bottom: 50px;

            p {
                font-size: 16px;
                margin-bottom: 25px;
                font-weight: normal;
            }

            h1 {
                font-size: 60px;
                font-weight: bolder;
            }

            h2 {
                font-size: 50px;
            }
        }

        div.subtitle-container {
            width: 500px !important;
            margin-bottom: 10px;


            p {
                color: #047fac;
                text-align: left;
                height: auto;
                font-size: 16px;
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