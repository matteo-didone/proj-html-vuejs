<template>
    <div class="title-container">
        <p>Portfolio</p>
        <h2><span>latest</span> work</h2>
    </div>

    <div class="slide-container swiper">
        <div class="slide-content">
            <div class="card-wrapper swiper-wrapper">
                <!-- Card -->
                <div v-for="item in carouselItems" :key="item.id" class="card swiper-slide">
                    <div class="image-content">
                        <span class="overlay"></span>
                        <div class="card-image">
                            <img class="card-img" :src="item.image" :alt="item.title" />
                        </div>
                    </div>
                    <div class="card-content">
                        <h2>{{ item.title }}</h2>
                        <p class="description">{{ item.category }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { store } from '../store.js'

export default {
    name: 'CarouselLatestWork',

    components: {},

    data() {
        return {
            store,

            carouselItems: [
                {
                    id: 1,
                    title: 'Basket of Flower on the table',
                    category: 'Branding Strategy',
                    image: 'https://demo.phlox.pro/corporate-2/wp-content/uploads/sites/100/2019/04/8wa60okr-1-790x576.jpg',
                },
                {
                    id: 2,
                    title: 'Purinky Products',
                    category: 'Digital Experience',
                    image: 'https://demo.phlox.pro/corporate-2/wp-content/uploads/sites/100/2019/04/DRY-1-790x576.jpg',
                },
                {
                    id: 3,
                    title: 'Satisfy Poster',
                    category: 'Branding Strategy',
                    image: 'https://demo.phlox.pro/corporate-2/wp-content/uploads/sites/100/2019/04/DRY-1-790x576.jpg',
                },
                {
                    id: 4,
                    title: 'Mock-Up Template',
                    category: 'Ecommerce',
                    image: 'https://demo.phlox.pro/corporate-2/wp-content/uploads/sites/100/2019/04/84316050-0af0-49db-a53a-241d47ddad0e-2-607x443.jpg',
                },
                {
                    id: 5,
                    title: 'Landing Page',
                    category: 'Digital Experience',
                    image: 'https://demo.phlox.pro/corporate-2/wp-content/uploads/sites/100/2019/04/a247b00b-3621-470f-b4b8-b3ac46f25907-1-790x576.jpg',
                },
            ],
        };
    },

    methods: {
        getImagePath(image) {
            return (`../assets/images/${image}`);
        },
    },
};
</script>

<style lang="scss" scoped>
.slide-container {
    height: 600px;
    width: 100%;
    max-width: 1120px;
    background-color: white;
    border: none;
}

.card-wrapper {
    border: none;
}

.card {
    border: none;
}

.image-content,
.card-content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 10px 14px;
    border: 0px solid none;
}

.card-image {
    position: relative;
    width: 150px;
    height: 150px;
    border-radius: 50%;
    background: #fff;
    padding: 3px;
}

.card-image .card-img {
    width: 100%;
    height: 100%;
    border-radius: 20%;
    object-fit: cover;
}
</style>
