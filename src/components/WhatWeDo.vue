<template>
    <div class="container-fluid wrapper">
        <div class="row">
            <div class="col-md-12 title-container">
                <span class="our-services">Our Services</span>
                <h1>
                    <span class="title-bold">What</span> We Do
                </h1>
                <span class="description">
                    When, while the lovely valley teems with vapour around meand the
                </span>
            </div>
        </div>

        <div class="row card-container justify-content-center">
            <!-- Card 1 -->
            <div class="card">
                <div class="card-content">
                    <div class="img-container">
                        <img src="../assets/images/Group-247.png" class="card-img-top" alt="First Card Picture" />
                    </div>
                    <h5 class="card-title">Data Analysis</h5>
                    <p class="card-text">
                        When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper
                    </p>
                    <div class="arrow-container">
                        <i class="fa-light fa-arrow-right" style="color: #ffffff;"></i>
                    </div>
                </div>
            </div>
            <!-- Card 2 -->
            <div class="card">
                <div class="card-content">
                    <div class="img-container">
                        <img src="../assets/images/Group-567.png" class="card-img-top" alt="Second Card Picture" />
                    </div>
                    <h5 class="card-title">SEO Optimization</h5>
                    <p class="card-text">
                        When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper
                    </p>
                    <div class="arrow-container">
                        <i class="fa-light fa-arrow-right" style="color: #ffffff;"></i>
                    </div>
                </div>
            </div>
            <!-- Card 3 -->
            <div class="card">
                <div class="card-content">
                    <div class="img-container">
                        <img src="../assets/images/Group-538.png" class="card-img-top" alt="Third Card Picture" />
                    </div>
                    <h5 class="card-title">Security Data</h5>
                    <p class="card-text">
                        When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper
                    </p>
                    <div class="arrow-container">
                        <i class="fa-light fa-arrow-right" style="color: #ffffff;"></i>
                    </div>
                </div>
            </div>
            <!-- Card 4 -->
            <div class="card">
                <div class="card-content">
                    <div class="img-container">
                        <img src="../assets/images/Group-566.png" class="card-img-top" alt="Fourth Card Picture" />
                    </div>
                    <h5 class="card-title">Branding Strategy</h5>
                    <p class="card-text">
                        When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper
                    </p>
                    <div class="arrow-container">
                        <i class="fa-light fa-arrow-right" style="color: #ffffff;"></i>
                    </div>
                </div>
            </div>
        </div>

        <div class="row">
            <div class="col">
                <div class="button-container">
                    <button class="btn view-all-services-button" type="submit">
                        View All Services
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.wrapper {
    text-align: center;
    padding-top: 70px;
    padding-bottom: 150px;

    .title-container {
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-bottom: 120px;

        .our-services {
            color: #fa858b;
        }

        h1 {
            margin: 10px 0;

            .title-bold {
                font-weight: bold;
            }
        }

        .description {
            margin-bottom: 10px;
        }
    }

    .card-container {
        display: flex;
        align-items: center;
        margin-bottom: 120px;

        .card {
            width: 238px;
            height: 400px;
            margin: 0 80px;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: rgb(68, 68, 68);
            font-size: 16px;
            font-style: normal;
            line-height: 24px;
            padding: 24px;
            box-sizing: border-box;
            hyphens: manual;
            position: relative;
            text-rendering: optimizelegibility;
            transition-property: all;
            transition-duration: 0.3s;
            transition-timing-function: ease-in;
            background-color: white;
            border: none;

            margin-bottom: 18px;

            .img-container {
                background-color: #fff;
                transform: translateY(-60px);
                box-shadow: 0px 4px 8px rgba(0, 0, 0, 0);
                display: flex;
                align-items: center;
                justify-content: center;
            }

            img.card-img-top {
                width: 150px;
                height: 150px;
                border-radius: 15px;
                background-color: white;
                margin: auto;
                transition: all 0.3s;
            }

            &:hover {

                .img-container {
                    background-color: #fff;
                    width: 250px;
                    height: 250px;
                    border-radius: 20%;
                    transform: translateY(-60px);
                    box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.16);
                    display: flex;
                    align-items: center;
                    justify-content: center;
                }

                img.card-img-top {
                    width: 130px;
                    height: 130px;
                }

                .card-content {
                    background-image: linear-gradient(to bottom, rgba(5, 6, 95, 0.8), rgba(1, 2, 48, 255));
                    border-radius: 40px;
                    padding-top: 0px;
                    padding-left: 100px;
                    padding-right: 100px;
                    padding-bottom: 40px;
                    color: white;
                    position: relative;
                    z-index: 1;
                    transform: translateY(-20px);
                    position: relative;

                    .arrow-container {
                        position: absolute;
                        cursor: pointer;
                        bottom: 0px;
                        left: 50%;
                        top: 95%;
                        transform: translateX(-50%);
                        width: 40px;
                        height: 40px;
                        background-color: #dc476d;
                        border-radius: 50%;
                        display: flex;
                        align-items: center;
                        justify-content: center;
                        transition: opacity 0.3s;
                        opacity: 0;
                    }

                    &:hover .arrow-container {
                        opacity: 1;
                    }
                }

                &:hover::before::after {
                    content: '';
                    width: 0;
                    height: 0;
                    border-left: 10px solid transparent;
                    border-right: 10px solid transparent;
                    border-top: 10px solid white;
                }
            }

            .card-title {
                font-weight: bold;
                margin-top: 12px;
                font-size: 30px;
                margin-bottom: 20px;
            }

            .card-text {
                text-align: center;
                width: 235px;
            }
        }
    }

    .view-all-services-button {
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
}

.button-container {
    margin-top: 90px;
}
</style>
