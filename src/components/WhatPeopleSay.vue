<template>
    <div class="wrapper">

        <div class="title-container">
            <p class="testimonial">Testimonial</p>
            <h1> <span class="title-bold">What</span> People Say</h1>
            <p class="description">When, while the lovely valley teems with vapour around meand the meridian sun strikes the
                upper surface .</p>
        </div>

        <div class="row card-container justify-content-center">
            <div class="card" v-for="card in cards" :key="card.title">
                <div class="card-content">
                    <div class="img-container">
                        <img :src="card.image" class="card-img-top" :alt="card.alt" />
                    </div>
                    <div class="stars-container">
                        <i class="fa-solid fa-star" style="color: #b6256f;"></i>
                        <i class="fa-solid fa-star" style="color: #b6256f;"></i>
                        <i class="fa-solid fa-star" style="color: #b6256f;"></i>
                        <i class="fa-regular fa-star" style="color: #b6256f;"></i>
                        <i class="fa-regular fa-star" style="color: #b6256f;"></i>
                    </div>
                    <div class="background-quote">
                        "
                    </div>
                    <p class="card-text">When, while lovely valley teems with vapour around meand meridian sun strikes the
                        upper impenetrable foliage of my trees, and but a thousand.</p>
                    <h5 class="card-title">Michkel Anegl</h5>
                    <p class="role">Marketing Management</p>
                </div>
            </div>
        </div>

        <div class="logo-container">
            <div class="logo-card" v-for="logo in logoArray" :key="logo.name">
                <img :src="logo.image" :alt="logo.name">
            </div>
        </div>
    </div>
</template>

<script>
import { store } from '../store.js'

export default {
    name: 'WhatPeopleSay',

    components: {

    },

    data() {

        return {
            store,

            cards: [
                {
                    image: "https://demo.phlox.pro/corporate-2/wp-content/uploads/sites/100/2019/04/szabo-viktor-1266895-unsplash-1024x1024.png",
                    alt: "First Card Picture",
                },
                {
                    image: "https://demo.phlox.pro/corporate-2/wp-content/uploads/sites/100/2019/04/philipe-cavalcante-539505-unsplash-1024x1024.png",
                    alt: "Second Card Picture",
                },
                {
                    image: "https://demo.phlox.pro/corporate-2/wp-content/uploads/sites/100/2019/04/fabio-spinelli-695744-unsplash-1024x1024.png",
                    alt: "Third Card Picture",
                },
            ],

            logoArray: [
                {
                    image: 'https://demo.phlox.pro/corporate-2/wp-content/uploads/sites/100/2019/04/client-1-1.png',
                    name: 'Golden',
                },
                {
                    image: 'https://demo.phlox.pro/corporate-2/wp-content/uploads/sites/100/2019/04/clienty-2.png',
                    name: 'Sweety Cafeteria',
                },
                {
                    image: 'https://demo.phlox.pro/corporate-2/wp-content/uploads/sites/100/2019/04/clienty-4.png',
                    name: 'Fastlane Sportswear',
                },
                {
                    image: 'https://demo.phlox.pro/corporate-2/wp-content/uploads/sites/100/2019/04/client-5.png',
                    name: 'Mighty Furnitures',
                },
                {
                    image: 'https://demo.phlox.pro/corporate-2/wp-content/uploads/sites/100/2019/04/clienty-3.png',
                    name: 'Jack Roller',
                },
            ],
        };
    },

    methods: {

    }
}
</script>


<style lang="scss" scoped>
.logo-container {
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: center;
    margin-top: 50px;
    margin-bottom: 50px;
}

.title-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 120px;

    .testimonial {
        color: #fa858b;
    }

    h1 {
        margin: 10px 0;
        font-weight: normal;

        .title-bold {
            font-weight: bolder;
        }
    }

    .description {
        margin-bottom: 10px;
    }
}

.card-container {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 50px;
}

.card {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin: 10px;
    width: 300px;
    height: 400px;
    border: none;
}

.card-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
}

.img-container {
    width: 100px;
    height: 100px;
    border: 5px solid #b6256f;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
}

.card-text {
    margin-top: 10px;
}

.stars-container {
    margin-top: 10px;

    .fa-star {
        margin: 0 2px;
    }
}

.card-title {
    margin-top: 10px;
}

.role {
    margin-top: 5px;
}
</style>    