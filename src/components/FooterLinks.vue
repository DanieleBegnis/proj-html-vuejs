<script>
export default {
    name: 'FooterLinks',
    props: ['cardInfo']
}
</script>

<template>
    <li  class="py-1">
        <a href="#">{{ cardInfo.text }}</a>
    </li>
</template>

<style scoped lang="scss">
@use '../style/partials/variables' as *;

ul {
    a {
        color: #b5a8a6;

        &:hover {
            color: $brand-primary;
        }
    }
}
</style>