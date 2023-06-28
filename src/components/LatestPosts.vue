<template>
    <div class="row">
        <div class="col-md-12 title-container">
            <span class="blog">Blog</span>
            <h1>
                <span class="title-bold">Latest</span> Posts
            </h1>
            <span class="description">
                When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface.
            </span>
        </div>
    </div>

    <div class="all-cards-container">
        <div class="right-card">
            <div class="big-card">
                <div class="text-container">
                    <p>April 21, 2019 • by Paul</p>
                    <h2>Amazon gets CCI nod to acquire 49% stake in</h2>
                    <p>When, while the lovely valley teems with vapour around meand the meridian sun s...</p>
                </div>

                <div class="button-container">
                    <button class="btn">Read More</button>
                </div>
            </div>
        </div>

        <div class="left-card">
            <div class="smaller-card">
                <div class="text-container">
                    <p>April 21, 2019 • by Paul</p>
                    <h2>Clearing Corporations get SEBI nod to invest in overnight funds</h2>
                    <p>When, while the lovely valley teems with vapour around meand the meridian sun s...</p>
                </div>

                <div class="button-container">
                    <button class="btn">Read More</button>
                </div>
            </div>

            <div class="smaller-card">
                <div class="text-container">
                    <p>April 21, 2019 • by Paul</p>
                    <h2>Shabnam Dhillion, wife of RSSB chief Gurinder Dhillon, passes away in London</h2>
                    <p>When, while the lovely valley teems with vapour around meand the meridian sun s...</p>
                </div>

                <div class="button-container">
                    <button class="btn">Read More</button>
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.title-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 120px;

    .blog {
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

.all-cards-container {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
}

.right-card {
    flex: 2;

    .big-card {
        background-image: url('../assets/images/headway-537308-unsplash-1380x703.jpg');
        padding: 50px 50px 50px 50px;
    }
}

.left-card {
    display: flex;
    flex-direction: column;
    flex: 1;

    .smaller-card {
        background-image: linear-gradient(to top, #142b67, #020230);
    }
}

.text-container {
    text-align: center;
    color: white;
}
</style>