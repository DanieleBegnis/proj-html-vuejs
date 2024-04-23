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
                        <p>About Us</p>
                    </div>
                    <h3>Welcome DogMilo Pets</h3>
                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nesciunt consectetur id, accusantium quod deserunt delectus, quisquam, dolore atque dolorem porro nemo? Ad ut distinctio repellat illum vel animi incidunt! Aut.</p>
                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Nesciunt consectetur id, accusantium quod deserunt delectus, quisquam, dolore atque dolorem porro nemo? Ad ut distinctio repellat illum vel animi incidunt! Aut.</p>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

.about {
    .col-5 {
        img {
            height: 80%;
        }
    }
}
</style>