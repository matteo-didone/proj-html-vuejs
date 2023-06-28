<template>
    <div class="wrapper">
        <div class="left-section">
            <h1>We Offer Awesome Services</h1>
            <p>When, while lovely valley teems with vapour around meand meridian sun strikes the upper surface</p>
        </div>

        <div class="right-section">
            <div class="searchbar">
                <input type="text" placeholder="Enter Your Email Address">
                <button>Subscribe</button>
            </div>
        </div>
    </div>
</template>

<script>
import { store } from '../store.js'

export default {
    name: 'ServicesOffered',

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
.wrapper {
    background-image: linear-gradient(to right, #ba286e, #ef5f69);
    border-radius: 40px;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 1600px;
    height: 250px;
    margin: 0 auto;

    z-index: 1;
    position: relative;
    top: 100px;
}

.left-section {
    flex: 1;
    color: white;
    padding: 20px;
}

.right-section {
    flex: 1;
}

h1,
p {
    color: white;
    text-align: left;
    margin: 0;
}

.searchbar {
    width: 540px;
    height: 65px;
    border-radius: 35px;
    background-color: white;
    display: flex;
    align-items: center;
    padding: 0 10px;
}

.searchbar input[type="text"] {
    flex: 1;
    border: none;
    outline: none;
}

.searchbar button {
    width: 175px;
    height: 50px;
    border: none;
    border-radius: 25px;
    background-image: linear-gradient(to right, #0799c8, #1b4a8c);
    color: white;
}

.searchbar button:hover {
    background-image: linear-gradient(to left, #ef5f69, #ba286e);
}
</style>