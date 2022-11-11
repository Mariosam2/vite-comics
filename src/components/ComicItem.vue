<script>
export default {
    name: 'ComicItem',
    props: {
        img: String,
        title: String
    }
}
</script>
<template>
    <div class="col">
        <img :src="img" :alt="title">
        <h6 class="text-white text-uppercase py-2">{{ title }}</h6>
    </div>
</template>
<style lang="scss" scoped>
.col {
    img {
        width: 100%;
        aspect-ratio: 1/1;
        object-fit: cover;
        object-position: center top;
    }
}
</style>