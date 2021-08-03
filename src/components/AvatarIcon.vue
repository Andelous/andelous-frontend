<template>
    <v-avatar
        v-bind:color="avatarColor"
        v-bind:size="avatarSize"
        class="elevation-4"
    >
        <v-icon v-bind:color="iconColor" v-bind:size="iconSize">
            {{ icon }}
        </v-icon>
    </v-avatar>
</template>

<script>
export default {
    name: "AvatarIcon",

    props: ["icon", "avatar-size", "icon-size", "avatar-color", "icon-color"],

    computed: {},

    data: () => ({}),
};
</script>
