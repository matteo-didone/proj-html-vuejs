<template>
    <section id="pricing" class="pricing">
        <div class="container" data-aos="fade-up">

            <div class="section-title">
                <p>Price List</p>
                <h2><span>Our</span> Pricing</h2>
                <p>When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface .
                </p>
            </div>

            <div class="row">

                <div class="col-lg-4" data-aos="fade-up" data-aos-delay="100">
                    <div class="box white-column">
                        <h3>Designing</h3>
                        <h4> PROCESS </h4>

                        <p>$</p>
                        <h1>40</h1>
                        <p>Per Month</p>

                        <ul>
                            <li> <span>Creative</span> Design Enabled </li>
                            <li> <span>Vibrant</span> Color Usage </li>
                            <li> <span>Eye</span> Catching Design </li>
                            <li> <span>Extreme</span> Typography </li>
                            <li> <span>Exceptional</span> Design </li>
                        </ul>
                        <a href="#" class="buy-btn"><span>Order Now</span> <i class="fa-solid fa-arrow-right"></i></a>
                    </div>
                </div>

                <div class="col-lg-4" data-aos="fade-up" data-aos-delay="100">
                    <div class="box rose-column">
                        <h3>Developing</h3>
                        <h4> PRODUCT </h4>

                        <p>$</p>
                        <h1>60</h1>
                        <p>Per Month</p>

                        <ul>
                            <li> <span>Creative</span> Design Enabled </li>
                            <li> <span>Vibrant</span> Color Usage </li>
                            <li> <span>Eye</span> Catching Design </li>
                            <li> <span>Extreme</span> Typography </li>
                            <li> <span>Exceptional</span> Design </li>
                        </ul>
                        <a href="#" class="buy-btn"><span>Order Now</span> <i class="fa-solid fa-arrow-right"></i></a>
                    </div>
                </div>

                <div class="col-lg-4" data-aos="fade-up" data-aos-delay="100">
                    <div class="box white-column">
                        <h3>Supporting</h3>
                        <h4>CLIENTS</h4>

                        <p>$</p>
                        <h1>80</h1>
                        <p>Per Month</p>

                        <ul>
                            <li> <span>Creative</span> Design Enabled </li>
                            <li> <span>Vibrant</span> Color Usage </li>
                            <li> <span>Eye</span> Catching Design </li>
                            <li> <span>Extreme</span> Typography </li>
                            <li> <span>Exceptional</span> Design </li>
                        </ul>
                        <a href="#" class="buy-btn"><span>Order Now</span> <i class="fa-solid fa-arrow-right"></i></a>
                    </div>
                </div>

            </div>

        </div>
    </section>
</template>

<script>
import { store } from '../store.js'

export default {
    name: 'OurPricing',

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
.pricing {
    background: linear-gradient(to left, #040737, #020331);
}

.section-title {
    padding-top: 70px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-bottom: 50px;
}

.section-title p {
    color: #fa898e;
    text-align: center;
}

.section-title h2 {
    text-align: center;
    color: white;
    margin-bottom: 30px;
}

.section-title h2 span {
    font-weight: bold;
    color: white;
}

.section-title p:last-child {
    color: #ffffff;
    text-align: center;
    width: 670px;
    height: 50px;
}


.pricing .box {
    padding: 60px 40px;
    box-shadow: 0 3px 20px -2px rgba(20, 45, 100, 0.1);
    background: #fff;
    height: 100%;
    border-top: 4px solid #fff;
    border-radius: 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.pricing .box.rose-column {
    background-image: linear-gradient(to right, #ba286e, #ef5f69);
    height: 100%;
    color: white;
}

.pricing h3 {
    font-weight: 500;
    margin-bottom: 15px;
    font-size: 20px;
    color: black;
}

.pricing h4 {
    font-size: 48px;
    color: black;
    font-weight: 400;
    font-family: "Jost", sans-serif;
    margin-bottom: 25px;
}

.pricing h4 sup {
    font-size: 28px;
}

.pricing h4 span {
    font-size: 18px;
    display: block;
}

.pricing ul {
    list-style: none;
    padding: 0;
    margin: 0;
    text-align: center;
    margin-bottom: 30px;
}

.pricing ul li {
    padding: 10px 0 10px 0px;
    position: relative;
}


.white-column .buy-btn {
    background-image: linear-gradient(to right, #ba286e, #ef5f69);
    color: white;
    transition: background-image 0.3s;
    border-radius: 30px;
    padding: 10px 30px;
    position: relative;

    &:hover {
        background-image: linear-gradient(to left, #0799c8, #1b4a8c);
    }
}

.rose-column .buy-btn {
    background-color: white;
    color: #ef5f69;
    transition: background-image 0.3s;
    border-radius: 30px;
    padding: 10px 30px;
    position: relative;
}
</style>    