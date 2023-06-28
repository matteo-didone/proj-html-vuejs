<template>
    <div class="top-section">
        <!-- Title Container -->
        <div class="title-container">
            <p>Portfolio</p>
            <h2><span>latest</span> work</h2>
        </div>

        <!-- Carousel Controls -->
        <div class="carousel-controls">
            <div class="carousel-control-btn-container">
                <button class="carousel-controls-btn" @click="previousSlide">
                    <i class="fa-thin fa-arrow-left"></i>
                </button>
            </div>

            <div class="carousel-control-btn-container">
                <button class="carousel-controls-btn" @click="nextSlide">
                    <i class="fa-thin fa-arrow-right"></i>
                </button>
            </div>
        </div>
    </div>

    <!-- Carousel / Slider -->
    <div class="slide-container">
        <div class="slide-content">
            <div class="card-wrapper">
                <!-- Card -->
                <div v-for="item in carouselItems" :key="item.id" class="card">
                    <div class="image-content">
                        <span class="overlay"></span>
                        <div class="card-image">
                            <img class="card-img" :src="item.image" :alt="item.title" />
                        </div>
                    </div>
                    <div class="card-content">
                        <h2 class="card-title">{{ item.title }}</h2>
                        <p class="card-description">{{ item.category }}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Pagination dots -->
    <div class="dots">
        <i v-for="(item, index) in carouselItems" :key="index"
            :class="{ 'fa-solid fa-circle': true, 'selected': activeIndex === index }"></i>
    </div>
</template>

<script>
import { store } from '../store.js';


export default {
    name: 'CarouselLatestWork',

    data() {
        return {
            store,

            carouselItems: [
                {
                    id: 1,
                    title: 'Basket of Flower on the table',
                    category: 'Branding Strategy',
                    image:
                        'https://demo.phlox.pro/corporate-2/wp-content/uploads/sites/100/2019/04/8wa60okr-1-790x576.jpg',
                },
                {
                    id: 2,
                    title: 'Purinky Products',
                    category: 'Digital Experience',
                    image:
                        'https://demo.phlox.pro/corporate-2/wp-content/uploads/sites/100/2019/04/DRY-1-790x576.jpg',
                },
                {
                    id: 3,
                    title: 'Satisfy Poster',
                    category: 'Branding Strategy',
                    image:
                        'https://demo.phlox.pro/corporate-2/wp-content/uploads/sites/100/2019/04/a247b00b-3621-470f-b4b8-b3ac46f25907-1-790x576.jpg',
                },
                {
                    id: 4,
                    title: 'Mock-Up Template',
                    category: 'Ecommerce',
                    image:
                        'https://demo.phlox.pro/corporate-2/wp-content/uploads/sites/100/2019/04/84316050-0af0-49db-a53a-241d47ddad0e-2-607x443.jpg',
                },
                {
                    id: 5,
                    title: 'Landing Page',
                    category: 'Digital Experience',
                    image:
                        'https://demo.phlox.pro/corporate-2/wp-content/uploads/sites/100/2019/04/a247b00b-3621-470f-b4b8-b3ac46f25907-1-790x576.jpg',
                },
            ],

            activeIndex: 0,

            isAutoplayActive: false,
            isAutoplayReversed: false,
            autoplayInterval: null,
        };
    },

    methods: {

        previousSlide() {
            this.activeIndex = (this.activeIndex - 1 + this.carouselItems.length) % this.carouselItems.length;
        },
        nextSlide() {
            this.activeIndex = (this.activeIndex + 1) % this.carouselItems.length;
        },

        isActive(index) {
            return index === this.activeIndex;
        },

        goToThumbnailSlide(newIndex) {
            this.activeIndex = newIndex;
        },
    },
};
</script>


<style lang="scss" scoped>
.slide-container {
    height: 600px;
    width: 100%;
    background-color: white;
    border: none;
}

.top-section {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;

    .title-container {
        margin-top: 100px;
        margin-left: 150px;

        p {
            color: #fa858b;
        }

        h2 {
            font-size: 40px;
            font-weight: normal;

            span {
                font-weight: bolder;
            }
        }
    }

    .carousel-controls {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
        margin-top: 100px;
        margin-right: 150px;

        .carousel-control-btn-container {
            display: flex;
            justify-content: center;
            align-items: center;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            border: 1px solid #fa858b;
            background-color: transparent;
        }

        .carousel-control-btn-container:first-child {
            margin-right: 30px;
        }

        .carousel-controls-btn {
            display: flex;
            justify-content: center;
            align-items: center;
            width: 100%;
            height: 100%;
            background-color: transparent;
            border: none;
            cursor: pointer;
        }

        .fa-thin {
            color: #fa858b;
            font-size: 16px;
        }
    }

}


.card-wrapper {
    border: none;
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    margin-top: 50px;

    overflow-x: scroll;

    .card {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        margin-left: 550px;
        background-color: white;
        border: none;
        
        .card-image {
            position: relative;
            width: 500px;
            height: 350px;
            border-radius: 10%;
            background: #fff;
            padding: 3px;
        }

        .card-image .card-img {
            width: 100%;
            height: 100%;
            border-radius: 8%;
            object-fit: cover;
        }

        .card-content {
            width: 500px;
            height: 150px;


            display: flex;
            justify-content: space-between;

            .card-title {
                font-size: 16px;
                font-weight: bold;
                margin: 0;
            }

            .card-description {
                color: #989898;
                margin: 0;
            }
        }

    }
}

.dots {
    display: flex;
    justify-content: center;
    margin-top: 10px;
    margin-bottom: 200px;

    i {
        color: grey;
        font-size: 12px;
        margin: 0 5px;
        cursor: pointer;
    }

    i.selected {
        color: #fa858b;
    }
}
</style>
