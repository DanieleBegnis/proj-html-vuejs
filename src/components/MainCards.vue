<script>
export default {
    name: 'MainCards',
    props: ['cardInfo']
}
</script>

<template>
    <div class="col-2">
        <div class="card-image">
            <img :src="cardInfo.image">
        </div>
        <h5> {{ cardInfo.title }} </h5>
        <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Molestias, minima aut.</p>
        <div class="next">
            <img src="../assets/img/right.png" alt="">
        </div>
    </div>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

.col-2 {
    background-color: $brand-primary;
    color: #fff;
}
</style>