<script>
import Hero from './Hero.vue';
export default {
    name: 'AppMain',
    components: {
        Hero
    },
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
                        <div>About Us</div>
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
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

.about {
    background-image: url('src/assets/img/dog-logo.png');
    background-repeat: no-repeat;
    background-size: 10%;
    background-position: right;
    background-position-y: 40px;

    .col-5 {
        img {
            height: 80%;
            vertical-align: middle;
        }
    }
}
</style>