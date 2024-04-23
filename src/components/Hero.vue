<script>
export default {
    name: 'Hero'
}
</script>

<template>
    <section class="hero">
        <div class="container">
            <div class="row">
                <div class="col-3">
                    <h1>Welcome to DogMilo pets</h1>
                    <p>Lorem ipsum dolor sit amet cons.sit amet conssit amet cons</p>
                    <div class="d-flex">
                        <button type="button" class="btn ms-btn-primary rounded-pill">Get in Touch!</button>
                        <i class="fa-brands fa-telegram"></i>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>


<style scoped lang="scss">
@use '../style/partials/variables' as *;

.hero {
    background-image: url('src/assets/img/b.png');
    background-size: cover;
    background-position: center;
    height: 400px;
    color: #fff;
}
.ms-btn-primary {
    background-color: $brand-primary;
    color: #fff;
    &:hover {
            background-color: #173b67;
        }
}
.fa-telegram {
    color: #72cff8;
    font-size: 40px;
    padding-left: 12px;
}
.col-3 {
    padding-top: 80px;
}
</style>