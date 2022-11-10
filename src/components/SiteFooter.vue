<script>
export default {
    name: 'SiteFooter',
    data() {
        return {
            items: [
                {
                    lists:
                        [
                            {
                                title: 'dc comics',
                                subElements: [
                                    {
                                        text: 'Characters',
                                        link: '#'
                                    },
                                    {
                                        text: 'Comics',
                                        link: '#'
                                    },
                                    {
                                        text: 'Movies',
                                        link: '#'
                                    },
                                    {
                                        text: 'TV',
                                        link: '#'
                                    },
                                    {
                                        text: 'Games',
                                        link: '#'
                                    },
                                    {
                                        text: 'Videos',
                                        link: '#'
                                    },
                                    {
                                        text: 'News',
                                        link: '#'
                                    },
                                ]
                            },
                            {
                                title: 'shop',
                                subElements: [
                                    {
                                        text: 'Shop DC',

                                        link: '#'
                                    },
                                    {
                                        text: 'Shop DC Collectibles',

                                        link: '#'
                                    },

                                ]
                            },

                        ]


                },

                {
                    lists: [
                        {
                            title: 'dc ',
                            subElements: [
                                {
                                    text: 'Terms Of Use',
                                    link: '#'
                                },
                                {
                                    text: 'Privacy policy (New)',
                                    link: '#'
                                },
                                {
                                    text: 'Ad Choices',
                                    link: '#'
                                },
                                {
                                    text: 'Advertising',
                                    link: '#'
                                },
                                {
                                    text: 'Jobs',
                                    link: '#'
                                },
                                {
                                    text: 'Subscriptions',
                                    link: '#'
                                },
                                {
                                    text: 'Talent Workshop',
                                    link: '#'
                                },
                                {
                                    text: 'CPSC Certificates',
                                    link: '#'
                                },
                                {
                                    text: 'Ratings',
                                    link: '#'
                                },
                                {
                                    text: 'Shop Help',
                                    link: '#'
                                },
                                {
                                    text: 'Contact Us',
                                    link: '#'
                                },
                            ]
                        }
                    ]

                },
                {
                    lists: [
                        {
                            title: 'sites',
                            subElements: [
                                {
                                    text: 'DC',
                                    link: '#'
                                },
                                {
                                    text: 'MAD Magazine',
                                    link: '#'
                                },
                                {
                                    text: 'DC Kids',
                                    link: '#'
                                },
                                {
                                    text: 'DC Universe',
                                    link: '#'
                                },
                                {
                                    text: 'DC Power Visa',
                                    link: '#'
                                },

                            ]
                        }
                    ]

                },

            ],
            socials: [
                {
                    img: 'footer-facebook.png',
                    link: '#'
                },
                {
                    img: 'footer-twitter.png',
                    link: '#'
                },
                {
                    img: 'footer-youtube.png',
                    link: '#'
                },
                {
                    img: 'footer-pinterest.png',
                    link: '#'
                },
                {
                    img: 'footer-periscope.png',
                    link: '#'
                },
            ],
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
    <footer id="site_footer">
        <div class="footer-top">
            <div class="container">
                <div class="row">
                    <div class="col-12 col-lg-5 d-flex flex-wrap justify-content-between py-5">
                        <div class="item" v-for="item in items">
                            <ul class="p-0 py-2 mb-0" v-for="list in item.lists">
                                <li class="f-title">
                                    <h4 class="text-uppercase">{{ list.title }}</h4>
                                </li>
                                <li v-for="subEl in list.subElements"><a href="subEl.link" class="sub-el">{{ subEl.text
                                }}</a></li>
                            </ul>
                        </div>

                    </div>
                    <div class="col-7 d-none d-lg-block dc-logo"></div>
                </div>
            </div>

        </div>
        <div class="footer-bottom py-5">
            <div class="container">
                <div class="row">
                    <div class="col-12 d-flex justify-content-between flex-wrap">
                        <a href="" class="btn ms_btn rounded-0 text-uppercase mb-3">Sign up Now!</a>
                        <div class="socials">
                            <h5 class="me-4 text-uppercase">Follow Us</h5>
                            <a :href="social.link" v-for="social in socials" class="px-2"><img
                                    :src="getImageUrl(social.img)" alt="" /></a>

                        </div>
                    </div>
                </div>
            </div>

        </div>
    </footer>
    <!-- /#site_footer -->
</template>