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

        <div class="row card-container">
            <!-- Card 1 -->
            <div class="col">
                <div class="card">
                    <img src="../assets/images/Group-247.png" class="card-img-top" alt="First Card Picture" />
                    <div class="card-body">
                        <h5 class="card-title">Data Analysis</h5>
                        <p class="card-text">
                            When, while the lovely valley teems with vapour around meand the
                            meridian sun strikes the upper
                        </p>
                    </div>
                </div>
            </div>
            <!-- Card 2 -->
            <div class="col">
                <div class="card">
                    <img src="../assets/images/Group-567.png" class="card-img-top" alt="Second Card Picture" />
                    <div class="card-body">
                        <h5 class="card-title">SEO Optimization</h5>
                        <p class="card-text">
                            When, while the lovely valley teems with vapour around meand the
                            meridian sun strikes the upper
                        </p>
                    </div>
                </div>
            </div>
            <!-- Card 3 -->
            <div class="col">
                <div class="card">
                    <img src="../assets/images/Group-538.png" class="card-img-top" alt="Third Card Picture" />
                    <div class="card-body">
                        <h5 class="card-title">Security Data</h5>
                        <p class="card-text">
                            When, while the lovely valley teems with vapour around meand the
                            meridian sun strikes the upper
                        </p>
                    </div>
                </div>
            </div>
            <!-- Card 4 -->
            <div class="col">
                <div class="card">
                    <img src="../assets/images/Group-566.png" class="card-img-top" alt="Fourth Card Picture" />
                    <div class="card-body">
                        <h5 class="card-title">Branding Strategy</h5>
                        <p class="card-text">
                            When, while the lovely valley teems with vapour around meand the
                            meridian sun strikes the upper
                        </p>
                    </div>
                </div>
            </div>
        </div>

        <div class="row">
            <div class="button-container">
                <button class="btn view-all-services-button" type="submit">
                    View All Services
                </button>
            </div>
        </div>
    </div>
</template>
  
<style lang="scss" scoped>
.wrapper {
    text-align: center;

    .title-container {
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-bottom: 20px;

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
        justify-content: center;
        align-items: center;
        margin-bottom: 20px;

        .card {
            width: 200px;
            text-align: center;
            border: none;

            img.card-img-top {
                width: 200px;
                height: 200px;
            }

            .card-title {
                font-weight: bold;
            }

            .card-text {
                text-align: center;
            }

            &:hover {
                box-shadow: 0px 3px 6px rgba(0, 0, 0, 0.16);
            }
        }
    }

    .view-all-services-button {
        background-image: linear-gradient(to right, #ba286e, #ef5f69);
        color: white;
        transition: background-image 0.3s;

        &:hover {
            background-image: linear-gradient(to left, #0799c8, #1b4a8c);
        }
    }
}
</style>