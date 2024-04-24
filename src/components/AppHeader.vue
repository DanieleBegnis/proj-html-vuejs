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
                    <div class="col-6 d-flex py-2">
                        <div class="mail">
                            <i class="fa-solid fa-envelope"></i>
                            info@example.com
                        </div>
                        <div class="phone px-4">
                            <i class="fa-solid fa-phone"></i>
                            +1(817)9013377
                        </div>
                    </div>
                    <div class="col-6 d-flex  justify-content-end  py-2">
                        <ul class="d-flex">
                            <li><i class="fa-brands fa-square-facebook  px-1"></i></li>
                            <li><i class="fa-brands fa-square-pinterest px-1"></i></li>
                            <li><i class="fa-brands fa-square-twitter px-1"></i></li>
                            <li><i class="fa-brands fa-linkedin px-1"></i></li>
                            <li><i class="fa-brands fa-square-instagram px-1"></i></li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
        <div class="header-bottom">
            <div class="container">
                <div class="row py-2">
                    <div class="col-6 d-flex">
                        <img src="../assets/img/logo.png" alt="">
                    </div>
                    <div class="col-6 d-flex">
                        <ul class=" d-flex align-items-center px-3">
                            <HeaderLinks v-for="link in links" :cardInfo="link"></HeaderLinks>
                        </ul>
                        <button type="button" class="btn ms-btn-primary rounded-pill my-2">Get in Touch!</button>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

.header-top {
    background-color: #7f7045;
    color: #fff;

    ul {
        padding-right: 90px;
    }

    .fa-solid {
        color: $brand-primary;
    }

    .fa-square-facebook {
        color: #343faa;
    }

    .fa-square-pinterest {
        color: #b4254a;
    }

    .fa-square-twitter {
        color: #90d6de;
    }

    .fa-linkedin {
        color: #075fcc;
    }

    .fa-square-instagram {
        color: #9c27a3;
    }
}

.ms-btn-primary {
    background-color: $brand-primary;
    color: #fff;

    &:hover {
        background-color: #173b67;
    }
}
</style>