<script>
export default {
    name: 'HeaderLinks',
    props: ['cardInfo']
}
</script>

<template>
    <ul>
        <li class="d-flex align-items-center" >
            <a class="px-6" href="#">{{ cardInfo.text }}</a>
        </li>
    </ul>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

ul {
    a {
        color: #444444;

        &:hover {
            color: $brand-primary;
        }
    }
}
</style>