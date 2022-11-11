<script>
export default {
    name: 'FooterList',
    props: {
        list: Object,
        title: String,
    }
}
</script>

<template>
    <ul class="p-0 py-2 mb-0">
        <li class="f-title">
            <h4 class="text-uppercase">{{ list.title }}</h4>
        </li>
        <li v-for="subEl in list.subElements"><a :href="subEl.link" class="sub-el">{{ subEl.text
        }}</a></li>
    </ul>
</template>