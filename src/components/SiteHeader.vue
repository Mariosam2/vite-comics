<script>
export default {
    name: 'SiteHeader',
    data() {
        return {
            links: [
                {
                    link: '#',
                    text: 'characters',
                },
                {
                    link: '#',
                    text: 'comics',
                },
                {
                    link: '#',
                    text: 'movies',
                },
                {
                    link: '#',
                    text: 'tv',
                },
                {
                    link: '#',
                    text: 'games',
                },
                {
                    link: '#',
                    text: 'collectibles',
                },
                {
                    link: '#',
                    text: 'videos',
                },
                {
                    link: '#',
                    text: 'fans',
                },
                {
                    link: '#',
                    text: 'news',
                },
                {
                    link: '#',
                    text: 'shop',
                },

            ]
        }
    }
}
</script>
<template>
    <header id="site_header">
        <nav class="navbar navbar-expand-lg py-0">
            <div class="container">
                <a class="navbar-brand p-0" href="#"><img id="logo" src="../assets/img/dc-logo.png" alt="logo"></a>
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
                    data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent"
                    aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarSupportedContent">
                    <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
                        <li class="nav-item" v-for="link in links">
                            <a class="nav-link ms_nav-item text-uppercase" :href="link.link">{{ link.text }}</a>
                        </li>


                    </ul>
                </div>
            </div>
        </nav>

    </header>
    <!-- /#site_header -->
</template>