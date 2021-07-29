<template>
    <v-app>
        <v-app-bar app dense>
            <v-app-bar-title>AngelD</v-app-bar-title>
        </v-app-bar>

        <v-main>
            <v-container fluid>
                <router-view />
            </v-container>
        </v-main>

        <v-footer app>
            <v-container fluid></v-container>
        </v-footer>
    </v-app>
</template>

<script>
export default {
    name: "App",

    data: () => ({
        //
    }),
};
</script>
