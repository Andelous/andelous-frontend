<template>
    <a
        v-bind:target="computedTarget"
        style="text-decoration: none;"
        class="d-flex justify-start align-center mb-1"
        v-bind:href="href"
    >
        <v-icon v-bind:color="iconColor">{{ icon }}</v-icon>
        &nbsp;{{ text }}&nbsp;
        <v-icon x-small color="blue darken-2" v-if="computedTarget == '_blank'">
            mdi-open-in-new
        </v-icon>
    </a>
</template>

<script>
export default {
    props: ["text", "href", "target", "icon", "icon-color"],

    computed: {
        computedTarget: function() {
            return this.target ? this.target : "_self";
        },
    },
};
</script>
