<script>
import Hero from './Hero.vue';
import MainCards from './MainCards.vue';
import CommentCards from './CommentCards.vue';
export default {
    name: 'AppMain',
    components: {
        Hero,
        MainCards,
        CommentCards
    },
    data() {
        return {
            cards: [
                {
                    image: 'src/assets/img/d-1.png',
                    title: 'Pet Sitting'
                },
                {
                    image: 'src/assets/img/d-2.png',
                    title: 'Puppy Sitting'
                },
                {
                    image: 'src/assets/img/d-3.png',
                    title: 'Dog Walking'
                },
                {
                    image: 'src/assets/img/d-4.png',
                    title: 'Night Care'
                },
                {
                    image: 'src/assets/img/d-5.png',
                    title: 'nail Trimming'
                }
            ],
            comments: [
                {
                    image: 'src/assets/img/t1.png',
                    title: 'Great Place',
                    name: 'Tobias May'
                },
                {
                    image: 'src/assets/img/t1.png',
                    title: 'Great Place',
                    name: 'Tobias May'
                }
            ]
        }
    }
}
</script>

<template>
    <main>
        <Hero></Hero>
        <!-- about section -->
        <section class="about">
            <div class="container">
                <div class="row">
                    <div class="col-5">
                        <img class="py-5" src="../assets/img/about.png" alt="">
                    </div>
                    <div class="col-7">
                        <div class="d-flex py-5">
                            <img src="../assets/img/dog-icon.png" alt="">
                            <div class="subtitle">About Us</div>
                        </div>
                        <h3>Welcome DogMilo Pets</h3>
                        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nesciunt consectetur id,
                            accusantium
                            quod deserunt delectus, quisquam, dolore atque dolorem porro nemo? Ad ut distinctio repellat
                            illum vel animi incidunt! Aut.</p>
                        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nesciunt consectetur id,
                            accusantium
                            quod deserunt delectus, quisquam, dolore atque dolorem porro nemo? Ad ut distinctio repellat
                            illum vel animi incidunt! Aut.</p>
                    </div>
                </div>
            </div>
        </section>
        <!-- services section -->
        <section class="services">
            <div class="container">
                <div class="row">
                    <div class="col-12 d-flex justify-content-center">
                        <p class="my-4 ms-color-secondary">Service</p>
                    </div>
                </div>
                <div class="row">
                    <div class="col-12 d-flex justify-content-center">
                        <h3>DogMilo Pet Care Services <br>
                            For Your Best Friends.</h3>
                    </div>
                </div>
                <div class="row justify-content-evenly">
                    <MainCards v-for="card in cards" :cardInfo="card"></MainCards>
                </div>
            </div>
        </section>
        <!-- choose section -->
        <section class="choose d-flex">
            <img src="../assets/img/why.png" alt="">
            <div class="container">
                <div class="row justify-content-end">
                    <div class="d-flex">
                        <img src="../assets/img/dog-icon.png" alt="">
                        <p class="ms-color-secondary">choose Us</p>
                    </div>
                    <h3>Why Choose US?</h3>
                    <div class="d-flex paragraph">
                        <img src="../assets/img/w-3.png" alt="">
                        <div>
                            <h5>Safety first</h5>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores incidunt nisi
                                exercitationem nostrum reiciendis praesentium quam officia</p>
                        </div>
                    </div>
                    <div class="d-flex paragraph w-75">
                        <img src="../assets/img/w-2.png" alt="">
                        <div>
                            <h5>Play Yards</h5>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores incidunt nisi
                                exercitationem nostrum reiciendis praesentium quam officia</p>
                        </div>
                    </div>
                    <div class="d-flex paragraph w-50">
                        <img src="../assets/img/w-1.png" alt="">
                        <div>
                            <h5>Monitor your Pets</h5>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores incidunt nisi
                                exercitationem nostrum reiciendis praesentium quam officia</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <!-- review section -->
        <section>
            <div class="container">
                <div class="row my-5">
                    <div class="col-4">
                        <div class="d-flex">
                            <div class="card-image">
                                <img src="../assets/img/dog-icon.png" alt="">
                            </div>
                            <p class="ms-color-secondary">Review & Rating</p>
                        </div>
                        <h4>Over 8000 Customers With 5-Stars reviews</h4>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Enim mollitia animi, dolor modi
                            placeat
                            perferendis quibusdam deleniti eveniet nobis quis ipsa fuga! Amet distinctio voluptas minima
                            labore officia? Maxime, sunt.</p>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                        <i class="fa-solid fa-star"></i>
                    </div>
                    <CommentCards v-for="comment in comments" :cardInfo="comment"></CommentCards>
                </div>
                <!-- next/ previous buttons -->
                <div class="review-buttons d-flex justify-content-end">
                    <div class="comment-button">
                        <img src="../assets/img/left-arrow.png" alt="">
                    </div>
                    <div class="comment-button">
                        <img src="../assets/img/next.png" alt="">
                    </div>
                </div>
            </div>
        </section>
        <!-- newsletter section -->
        <section class="newsletter-section">
            <div class="newsletter d-flex justify-content-between">
                <!-- input mail -->
                <div class="news-image">
                    <!-- <img src="../assets/img/news.png" alt=""> -->
                </div>
                <div>
                    <h3>Subscribe to our Newsletter</h3>
                    <input type="text">
                </div>

            </div>
        </section>
    </main>

</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

.about {
    background-image: url('src/assets/img/dog-logo.png');
    background-repeat: no-repeat;
    background-size: 10%;
    background-position: right;
    background-position-y: 40px;
    max-height: 600px;

    .col-5 {
        img {
            height: 80%;
            vertical-align: middle;
        }
    }

    .subtitle {
        color: $brand-secondary;
    }
}

.services {
    background-color: #f5f5f5;
    background-image: url('src/assets/img/dog-left.png');
    background-image: url('src/assets/img/dog-logo.png');
    background-repeat: no-repeat;
    background-size: 10%;
    background-position: right;


}

.ms-color-secondary {
    color: $brand-secondary;
}

.paragraph {

    height: 150px;

}

.fa-star {
    color: #fed404;
}

.col-4 {
    .card-image {
        width: 40px;
    }
}
.review-buttons {
    padding-bottom: 200px;
}

.comment-button {
    background-color: $brand-primary;
    width: 40px;
    height: 40px;
    margin-left: 18px;

    &:hover {
        background-color: $brand-secondary;
    }

    img {
        width: 100%;
        padding: 4px;
    }
}

.newsletter-section {
    position: relative;
}

.newsletter {
    background-color: $brand-primary;
    width: 45%;
    height: 200px;
    border-radius: 20px;
    position: absolute;
    left: 50%;
    bottom: -100px;
    transform: translate(-50%);
    color: #fff;
    .news-image {
        width: 50%;
        image {
            width: 100%;
        }
    }
}
</style>