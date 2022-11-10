<script>
export default {
    name: 'IconsComp',
    data() {
        return {
            icons: [
                {
                    desc: 'digital comics',
                    img: 'buy-comics-digital-comics.png',
                    link: '#'
                },
                {
                    desc: 'dc merchandise',
                    img: 'buy-comics-merchandise.png',
                    link: '#'
                },
                {
                    desc: 'subscription',
                    img: 'buy-comics-subscriptions.png',
                    link: '#'
                },
                {
                    desc: 'comic shop locator',
                    img: 'buy-comics-shop-locator.png',
                    link: '#'
                },
                {
                    desc: 'dc power visa',
                    img: 'buy-dc-power-visa.svg',
                    link: '#'
                },
            ]
        }

    },
    methods: {
        getImageUrl(name) {
            return new URL(`../assets/img/${name}`, import.meta.url).href
        }
    }
}
</script>
<template>
    <section class="ms_icons">
        <div class="container ">
            <div class="row p-4">
                <div class="col-12 d-flex">
                    <div class="ms_icon d-flex align-items-center flex-grow-1 py-4" v-for="icon in icons">
                        <img :src="getImageUrl(icon.img)" :alt="icon.desc">
                        <a :href="icon.link" class="ms_description text-uppercase p-3 text-white">{{ icon.desc }}</a>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>