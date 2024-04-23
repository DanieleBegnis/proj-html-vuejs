<script>
export default {
    name: 'HeaderLinks',
    props: ['cardInfo']
}
</script>

<template>
    <li class="d-flex align-items-center px-3">
        <a href="#">{{ cardInfo.text }}</a>
    </li>
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