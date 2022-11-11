<script>
import IconsComp from './IconsComp.vue';
import Jumbotron from './Jumbotron.vue';
import Comic from './Comic.vue';
import data from '../assets/data/data.js';
export default {
    name: 'SiteMain',
    components: {
        IconsComp, Jumbotron, Comic
    },
    data() {
        return {
            comics: data,
        }
    }
}
</script>
<template>
    <main id="site_main">
        <jumbotron>
        </jumbotron>
        <section class="content">
            <div class="container">
                <div class="row row-cols-1 row-cols-md-3 row-cols-xl-6 g-3">
                    <comic v-for="comic in comics" :img="comic.thumb" :title="comic.series">
                    </comic>
                </div>
                <div class="callToAction text-center">
                    <a href="#" class="btn btn-primary rounded-0 text-uppercase p-2 fw-bold">Load More</a>
                </div>

            </div>
        </section>
        <icons-comp></icons-comp>
    </main>
    <!-- /#site_main -->
</template>