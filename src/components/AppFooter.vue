<script>
import FooterLinks from './FooterLinks.vue';

export default {
    name: 'AppFooter',
    components: {
        FooterLinks
    },
    data() {
        return {
            supports: [
                {
                    text: 'Contact Us',
                },
                {
                    text: 'Online Chat',
                },
                {
                    text: 'WhatsApp',
                },
                {
                    text: 'Telegram',
                },
                {
                    text: 'Snapchat',
                }
            ],
            abouts: [
                {
                    text: 'About Us',
                },
                {
                    text: 'Blog',
                },
                {
                    text: 'Career',
                },
                {
                    text: 'Job',
                },
                {
                    text: 'In press',
                }
            ],
            faqs: [
                {
                    text: 'Account',
                },
                {
                    text: 'Order',
                },
                {
                    text: 'Delivery',
                },
                {
                    text: 'Payment',
                },
                {
                    text: 'Return',
                }
            ],
        }
    }
}
</script>

<template>
    <footer>
        <div class="container">
            <div class="row justify-content-evenly py-5">
                <div class="col-2">
                    <div class="py-2 fw-bold ms-title">Get in Touch</div>
                    <p>Have a question for us? We'll answer your problems here</p>
                    <ul class="d-flex">
                        <li><i class="fa-brands fa-square-facebook  px-1"></i></li>
                        <li><i class="fa-brands fa-square-pinterest px-1"></i></li>
                        <li><i class="fa-brands fa-square-twitter px-1"></i></li>
                        <li><i class="fa-brands fa-linkedin px-1"></i></li>
                        <li><i class="fa-brands fa-square-instagram px-1"></i></li>
                    </ul>
                </div>
                <div class="col-2">
                    <div class="py-2 fw-bold ms-title">Support</div>
                    <ul>
                        <FooterLinks v-for="support in supports" :cardInfo="support"></FooterLinks>
                    </ul>
                </div>
                <div class="col-2">
                    <div class="py-2 fw-bold ms-title">About</div>
                    <ul>
                        <FooterLinks v-for="about in abouts" :cardInfo="about"></FooterLinks>
                    </ul>
                </div>
                <div class="col-2">
                    <div class="py-2 fw-bold ms-title">FAQ</div>
                    <ul>
                        <FooterLinks v-for="faq in faqs" :cardInfo="faq"></FooterLinks>
                    </ul>
                </div>
                <div class="col-2">
                    <div class="py-2 fw-bold ms-title">Contact Me</div>
                    <div class="d-flex">
                        <i class="fa-solid fa-paper-plane"></i>
                        <p>Via Campiglio, 9, 38080 Carisolo TN</p>
                    </div>
                    <div class="d-flex">
                        <i class="fa-solid fa-phone"></i>
                        <p>02 457 645 73</p>
                    </div>
                    <div class="d-flex">
                        <i class="fa-solid fa-envelope"></i>
                        <p>MaxPower@gmail.com</p>
                    </div>
                </div>
            </div>
        </div>
        <hr>
        <div class="copyright py-2" >Copyright 2024 by AltDogMilo.com</div>
    </footer>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

footer {
    background-color: #000;
    color: #b5a8a6;

    .ms-title {
        color: $brand-primary
    }
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
.copyright {
    color: #fff;
    text-align: center;
}
</style>