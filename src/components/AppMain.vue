<script>
import Hero from './Hero.vue';
import MainCards from './MainCards.vue';
export default {
    name: 'AppMain',
    components: {
        Hero,
        MainCards
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
            ]
        }
    }
}
</script>

<template>
    <Hero></Hero>
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
                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nesciunt consectetur id, accusantium
                        quod deserunt delectus, quisquam, dolore atque dolorem porro nemo? Ad ut distinctio repellat
                        illum vel animi incidunt! Aut.</p>
                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nesciunt consectetur id, accusantium
                        quod deserunt delectus, quisquam, dolore atque dolorem porro nemo? Ad ut distinctio repellat
                        illum vel animi incidunt! Aut.</p>
                </div>
            </div>
        </div>
    </section>
    <section class="services">
        <div class="container">
            <div class="row">
                <div class="col-12 d-flex justify-content-center">
                    <p class="my-4">Service</p>
                </div>
            </div>
            <div class="row">
                <div class="col-12 d-flex justify-content-center">
                    <h3>DogMilo Pet Care Services <br>
                    For Your Best Friends.</h3>
                </div>
            </div>
            <div class="row justify-content-center">
                <MainCards v-for="card in cards" :cardInfo="card"></MainCards>
            </div>
        </div>
    </section>
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
    p {
        color: $brand-secondary;
    }
}
</style>