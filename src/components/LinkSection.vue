<template>
    <div>
        <h5 class="grey--text mb-1">{{ title }}</h5>
        <flex-link
            v-for="link in links"
            v-bind:key="link.text"
            v-bind:text="link.text"
            v-bind:href="link.href"
            v-bind:target="link.target"
            v-bind:icon="link.icon"
            v-bind:icon-color="link['icon-color']"
        />
    </div>
</template>

<script>
import FlexLink from "./FlexLink.vue";

export default {
    name: "LinkSection",

    components: {
        "flex-link": FlexLink,
    },

    props: ["title", "links"],

    data: () => ({}),
};
</script>
