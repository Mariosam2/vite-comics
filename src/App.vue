<script>
import SiteHeader from './components/SiteHeader.vue';
import SiteMain from './components/SiteMain.vue';
import IconSection from './components/IconSection.vue';
import SiteFooter from './components/SiteFooter.vue';

export default {
  name: 'App',
  components: {
    SiteHeader,
    SiteMain,
    IconSection,
    SiteFooter,
  }
}
</script>

<template>
  <site-header></site-header>
</template>