<script>
import HeaderLinks from './HeaderLinks.vue';

export default {
    name: 'AppHeader',
    components: {
        HeaderLinks
    },
    data() {
        return {
            links: [
                {
                    text: 'Home',
                    active: false
                },
                {
                    text: 'About',
                    active: false
                },
                {
                    text: 'Services',
                    active: false
                },
                {
                    text: 'Training',
                    active: false
                },
                {
                    text: 'Blogs',
                    active: false
                }
            ]
        }
    }
}
</script>

<template>
    <header>
        <div class="header-top">
            <div class="container">
                <div class="row">
                    <div class="col-6 d-flex">
                        info
                    </div>
                    <div class="col-6 d-flex">
                        social media links
                    </div>
                </div>
            </div>
        </div>
        <div class="header-bottom">
            <div class="container">
                <div class="row">
                    <div class="col-6 d-flex">
                        <img src="..src/assets/img/logo.png" alt="">
                    </div>
                    <div class="col-6 d-flex align-items-center py-3">
                        <HeaderLinks  v-for="link in links" :cardInfo="link"></HeaderLinks>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

.header-top {
    background-color: $brand-primary;
}

</style>