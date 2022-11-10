<script>
export default {
    name: 'IconsComp',
    data() {
        return {
            icons: [
                {
                    desc: 'digital comics',
                    img: 'buy-comics-digital-comics.png',
                },
                {
                    desc: 'digital comics',
                    img: 'buy-comics-digital-comics.png',
                },
                {
                    desc: 'digital comics',
                    img: 'buy-comics-digital-comics.png',
                },
                {
                    desc: 'digital comics',
                    img: 'buy-comics-digital-comics.png',
                },
                {
                    desc: 'digital comics',
                    img: 'buy-comics-digital-comics.png',
                },
            ]
        }

    },
    methods: {
        getImageUrl(name) {
            return new URL(`./dir/${name}.png`, import.meta.url).href
        }
    }
}
</script>
<template>
    <section class="ms_icons">
        <div class="container">
            <div class="row">
                <div class="col-12 d-flex justify-content-center">
                    <div class="ms_icon d-flex align-items-center p-5" v-for="icon in icons">
                        <img :src="getImageUrl(icon.img)" :alt="icon.desc">
                        <span class="ms_description text-uppercase p-3 text-white">{{ icon.desc }}</span>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>