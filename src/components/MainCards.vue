<script>
export default {
    name: 'MainCards',
    props: ['cardInfo']
}
</script>

<template>
    <div class="col-2 my-2 rounded-pill d-flex">
        <div class="card-image">
            <img :src="cardInfo.image">
        </div>
        <h5> {{ cardInfo.title }} </h5>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Molestias, minima aut.</p>
        <div class="next rounded-circle">
            <img src="../assets/img/right.png" alt="">
        </div>
    </div>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

.col-2 {
    background-color: $brand-primary;
    color: #fff;
    text-align: center;
    flex-direction: column;

    &:hover {
        background-color: $brand-secondary;
    }

    .card-image {
        height: 70px;

        img {
            height: 100%;
        }
    }

    .next {
        background-color: #ffcc01;
        width: 50px;
        height: 50px;

        img {
            height: 100%;
        }
    }
}
</style>