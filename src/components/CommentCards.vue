<script>
export default {
    name: 'CommentCards',
    props: ['cardInfo']
}
</script>

<template>
    <div class="col-4 py-2">
        <div>
            <i class="fa-solid fa-star"></i>
            <i class="fa-solid fa-star"></i>
            <i class="fa-solid fa-star"></i>
            <i class="fa-solid fa-star"></i>
            <i class="fa-solid fa-star"></i>
        </div>
        <div class="py-2 fw-bold">{{ cardInfo.title }}</div>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Enim mollitia animi, dolor modi placeat
            perferendis quibusdam deleniti eveniet nobis quis ipsa fuga! Amet distinctio voluptas minima
            labore officia? Maxime, sunt.</p>
        <div class="user d-flex">
            <div class="card-image">
                <img :src="cardInfo.image">
            </div>
            <div class="user-info px-3">
                <div class="py-2 fw-bold">{{ cardInfo.name }}</div>
                <p>UI/UX Designer</p>
            </div>
        </div>

    </div>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

.col-4 {
    background-color: #f4f4f4;


    .card-image {
        height: 70px;
        border-radius: 50%;
        overflow: hidden;

        img {
            height: 100%;
        }
    }

    .fa-star {
        color: #fed404;
    }
}
</style>