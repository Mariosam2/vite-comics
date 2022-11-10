<script>
import IconsComp from './IconsComp.vue';
export default {
    name: 'SiteMain',
    components: {
        IconsComp,
    }
}
</script>
<template>
    <main id="site_main">
        <section class="content">
            <div class="container">
                <div class="row">
                    <div class="col py-5">
                        <h2 class="text-white"> &#8594; Content goes here &#8592; </h2>
                    </div>
                </div>
            </div>
        </section>
        <icons-comp></icons-comp>
    </main>
    <!-- /#site_main -->
</template>