<template>
    <div class="wrapper">

        <div class="title-container">
            <p>Testimonial</p>
            <h1> <span>What</span> People Say</h1>
            <p>When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface .</p>
        </div>

        <div class="card-container">
            <div class="card">

            </div>

            <div class="card">

            </div>

            <div class="card">

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
.logo-container{
    display: flex;
    flex-direction: row;
    justify-content: space-evenly;
    align-items: center;
    margin-top: 50px;
    margin-bottom: 50px;
} 
</style>    