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
                <button class="carousel-controls-btn" @click="getPrevious">
                    <i class="fa-thin fa-arrow-left"></i>
                </button>
            </div>

            <div class="carousel-control-btn-container">
                <button class="carousel-controls-btn" @click="getNext">
                    <i class="fa-thin fa-arrow-right"></i>
                </button>
            </div>
        </div>

    </div>

    <!-- Carousel / Slider -->
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

    <!-- Pagination dots -->
    <div class="dots"></div>
</template>
  
<script>
import { store } from '../store.js';
import { register } from 'swiper/element/bundle';

register();

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

    mounted() {
        const carouselElement = document.querySelector('#app');

        this.startAutoplay();

        carouselElement.addEventListener('mouseenter', this.pauseAutoplay);
        carouselElement.addEventListener('mouseleave', this.resumeAutoplay);
    },

    beforeUnmount() {
        const carouselElement = document.querySelector('#app');

        carouselElement.removeEventListener('mouseenter', this.pauseAutoplay);
        carouselElement.removeEventListener('mouseleave', this.resumeAutoplay);
    },

    methods: {
        getPrevious() {
            if (this.activeIndex === 0) {
                this.activeIndex = this.carouselItems.length - 1;
            } else {
                this.activeIndex--;
            }
        },

        getNext() {
            if (this.activeIndex === this.carouselItems.length - 1) {
                this.activeIndex = 0;
            } else {
                this.activeIndex++;
            }
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
    max-width: 1120px;
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

        .carousel-control-btn-container:first-child{
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
