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
    <section>
        <div class="container">
            <div class="row">
                <div class="col-5">
                    <img src="" alt="">
                </div>
                <div class="col-7"></div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

</style>