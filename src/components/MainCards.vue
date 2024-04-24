<script>
export default {
    name: 'MainCards',
    props: ['cardInfo']
}
</script>

<template>
    <div class="col-2 my-2 rounded-pill d-flex">
        <div class="card-image my-3">
            <img :src="cardInfo.image">
        </div>
        <h5> {{ cardInfo.title }} </h5>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Molestias, minima aut.</p>
        <div class="d-flex justify-content-center">
            <div class="next rounded-circle my-3">
                <img src="../assets/img/right.png" alt="">
            </div>
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
        display: flex;
        justify-content: center;

        img {
            height: 100%;
        }
    }

    .next {
        background-color: #ffcc01;
        width: 50px;
        height: 50px;
        position: relative;

        img {
            height: 50%;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            transform: translate(-50%, -50%);
        }
    }
}
</style>